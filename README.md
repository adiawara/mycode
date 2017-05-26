# mycode
print '                 That program has been elaborated by Aboubacar Diawara '
print '                                        this is a guess number game '
print '         The user will enter his or her guess until the correct number is guessed '
print '                The number of guesses might be limited , in this case up to  6'
print '    The program will keep asking the user to guess until the correct number is guessed. '
print '                     Then the program will print how many guess was required '
print '  try/except, we use them to avoid the program to bubble up exception errors to the user '
print '                         just to handle the possible errors coming from users '
print '                           so, a chance is given to the user to fixe his errors '
print
print

import random

attempts = 0

username = raw_input('               Hello, what is your name?  ')
while username==None or len(username)==0 or username=="" :
                username=raw_input("You entered nothing. Please enter your name: \n")
                len(username)>0
number = random.randint(1,20)
print'Well, ' , username, ', I am thinking of a number between 1 and 20.'

while attempts < 6:
    try:
        guess = raw_input('Take a guess:  ')
        guess = int(guess)
    except:
        print ' Bad entry, please enter an integer number ' , exit()
    if (guess < 0 or guess > 20):
        print ' Bad entry, please choose between 1 amd 20 ' , exit()
    attempts = attempts + 1
    def comparater(number , guess):
        if number < guess :
            return -1  # and print 'Your guess is too low'
        if number > guess :
            return 1  # and print 'Your guess is too high'
        if number == guess :
            return 0  # and print 'Your guess matches'
        

    result = comparater(number , guess)
    print result
    if result == 0: break

if guess == number:
     print('Good job, ', username , '! You guessed my number in ',  attempts , ' guesses!')

if guess != number:
     print('Nope. The number I was thinking of was ' , number)
    

