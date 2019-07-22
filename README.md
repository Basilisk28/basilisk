# basilisk
board={'11':' ','12':' ','13':' ',
       '21':' ','22':' ','23':' ',
       '31':' ','32':' ','33':' '}
def game():
    print(board['11']+'|'+board['12']+'|'+board['13'])
    print('-+-+-')
    print(board['21']+'|'+board['22']+'|'+board['23'])
    print('-+-+-')
    print(board['31']+'|'+board['32']+'|'+board['33'])
game()
n=0
while n<9:
    if n%2==0:
        print('this is your turn X')
        move=input()
        board[move]='X'
        print(game())
    else:
        print('this is your move O')
        move=input()
        board[move]='O'
        print(game())
    n+=1
    if n>4:           
        if (board['11']==board['12']==board['13'] or board['11']==board['21']==board['31'] or board['11']==board['22']==board['33']) and board['11']!=' ': 
            print('The player '+board['11']+' has won')
            break
        elif (board['12']==board['22']==board['32'] or board['31']==board['32']==board['33']) and board['32']!=' ' :
            print('The player '+board['32']+' has won')
            break
        elif  (board['13']==board['23']==board['33'] or board['21']==board['22']==board['23']) and board['23']!=' ':
            print('The player '+board['23']+' has won')
            break


