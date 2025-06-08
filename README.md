# kbc
import random

lifeline = ["50-50", "audience poll"]
audience = random.choice(("A", "B", "C", "D"))
bank = 0


def question1():
    # lifeline=["50-50",'audience poll']
    wronganswer = ("(B)mumbai", "(C)agra", "(D)gujrat")
    question = "what is the capital of india"
    option = ["(A)new delhi", "(B)mumbai", "(C)agra", "(D)gujrat"]
    correctanswer = ["new delhi", "a"]
    bank = 0
    fifty = ("(A) new delhi", random.choice(wronganswer))
    audience = random.choice(("A", "B", "C", "D"))
    print(question)
    print(option)
    ans1 = input().lower()
    if ans1 in correctanswer:
        print("correct answer")
        bank += 1000
        return
    elif ans1 == "life line":
        print("which life line do you want to take")
        a = input()
        if a == "50-50" or a == "50 50":
            print(fifty)
            lifeline.remove("50-50")
            print("what do you now want to take")
            ans_1 = input()
            if ans_1 in correctanswer:
                print("correct answer")
                bank += 1000
                print("now you have", lifeline, "left")
                return
            else:
                print("wrong answer")
                print("you got", bank)
                exit()
        elif a == "audience poll":
            lifeline.remove("audience poll")
            print(audience, "got maximum votes")
            print("now what is your answer")
            ans1audience = input()
            if ans1audience in correctanswer:
                print("correct answer")
                bank += 1000
                print("now you have", lifeline, "left")
                return
            else:
                print("wrong answer")
                print("you got", bank)
                exit()
        else:
            print('wrong answer')
            exit()
    else:
        print("wrong answer")
        exit()
round1 = question1()
print(round1)


def question2():
    questio2 = "Who was the first Indian woman to win an Olympic medal?"
    bank = 1000
    option2 = """(A) Mary Kom
(B) P.V. Sindhu
(C) Karnam Malleswari
(D) Saina Nehwal"""
    wrongoption2 = """(A) Mary Kom,
(B) P.V. Sindhu,(D) Saina Nehwal"""
    correctoption2 = ["karnam Malleswari", "c"]
    fifty2 = ("(C) Karnam Malleswari ", random.choice(wrongoption2))

    print(questio2)
    print(option2)
    ans2 = input().lower()
    if ans2 in correctoption2:
        print("correct answer")
        bank += 2000

    elif ans2 == "life line":
        print("which life line do you want to take")
        b = input()
        if b == "50-50" or b == "50 50":
            if "50-50" in lifeline:
                print(fifty2)
                lifeline.remove("50-50")
                print("what do you now want to take")
                ans_2 = input().lower()
                if ans_2 in correctoption2:
                    print("correct answer")
                    bank += 2000
                    print("now you have", lifeline, "left")
                else:
                    print("wrong answer")
                    print("you got", bank)
                    exit()

            else:
                print("you dont have life line")
                print("dont fool me as a reward you loose this game")
                exit()
        if b == "audience poll":
            if "audience poll" in lifeline:

                lifeline.remove("audience poll")
                print(audience, "got maximum votes")
                print("now what is your answer")
                ans_2 = input().lower()
                if ans_2 in correctoption2:
                    print("corret answer")
                    bank += 2000
                    print("now you have", lifeline, "left")

                else:
                    print("wrong answer")
                    print("you got", bank)
                    exit()
            else:
                print("you dont have life line")
                print("dont fool me as a reward you loose this game")
                exit()
        else:
            print("wrong answer")
            print("you got",bank)
            exit()
    else:
        print("wrong answer")
        exit()


round2 = question2()
print(round2)
def question3():
    question3="Which of these books is not written by an Indian author?"
    bank=3000
    option3="""A. The Guide
    B. The White Tiger
    C. To Kill a Mockingbird
    D. Train to Pakistan"""
    wrongoption3="a) the guide",
    "B) the white Tiger",
    "D) train yo Pakistan"
    correctoption3=["c" ,"to kill a mochingbird"]
    fifty3=(random.choice(wrongoption3),correctoption3)
    print(question3)
    print(option3)
    ans3=input().lower()
    if ans3 in correctoption3:
        print("correct answer")
        bank+=3000
    elif ans3=="life line":
        print("which life line do you want to take")
        c = input()
        if c == "50-50" or c == "50 50":
            if "50-50" in lifeline:
                print(fifty3)
                lifeline.remove("50-50")
                print("what do you now want to take")
                ans_3 = input().lower()
                if ans_3 in correctoption3:
                    print("correct answer")
                    bank += 3000
                    print("now you have", lifeline, "left")
                else:
                    print("wrong answer")
                    print("you got", bank)
                    exit()
            else:
                print("you dont have life line")
                print("dont fool me as a reward you loose this game")
                exit()
        elif c == "audience poll":
            if "audience poll" in lifeline:
                lifeline.remove("audience poll")
                print(audience, "got maximum votes")
                print("now what is your answer")
                ans_3 = input().lower()
                if ans_3 in correctoption3:
                    print("corret answer")
                    bank += 3000
                    print("now you have", lifeline, "left")
                else:
                    print("wrong answer")
                    print("you got", bank)
                    exit()
            else:
                print("you dont have life line")
                print("dont fool me as a reward you loose this game")
                exit()
        else:
            print("wrong annwer")
            print("you got",bank)        
    else:
        print("wrong answer")
        print("you got",bank)
        exit()
round3=question3()
print(round3)

def question4():
    question4="which mughal emperor bulit the red fort in delhi"
    option4="""A)akbar
    B)babur
    C)shah jhan
    D)aurangzeb"""
    bank=6000
    wrongoption4="A)akbar","B)babur","D)aurangzeb"
    correctoption4=["c","shah jhan"]
    fifty4=(random.choice(wrongoption4),correctoption4)
    print(question4)
    print(option4)
    ans4=input().lower()
    if ans4 in correctoption4:
        print("correct answer")
        bank+=5000
        
    elif ans4=="life line":
        print("which life ine do you want to take ")
        d=input()
        if d=="50-50"or d=="50 50":
            if "50-50" in lifeline:
                print(fifty4)
                lifeline.remove("50-50")
                print("what do you now want to take")
                ans_4=input().lower()
                if ans_4 in correctoption4:
                    print("correct answer")
                    bank+=5000
                    print("now you have",lifeline,"left")
                    return
                else:
                    print("wrong answer")
                    print("you got",bank)
                    
                    return
            else:
                print("you dont have life line")
                print("dont fool me as areward you oose the game")
                
                return
        elif d=="audience poll":
            if "audience poll"in lifeline:
                lifeline.remove("audience poll")
                print(audience,"got maximum votes")
                print("now what is your answer")
                ans_4=input().lower()
                if ans_4 in correctoption4:
                    print("correct answer")
                    bank+=5000
                    print("now you have", lifeline, "left")
                    
                else:
                    print("wrong answer")
                    print("you got",bank)
                    return
        else:
            print("wrong answer")
            print("you get",bank)     
                
    else: 
        print("wrong answer")
        print("you got",bank)  
round4=question4()
print(round4)
          
