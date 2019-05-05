from .utils import *

def check(arg):
    if arg & 1 == 0 and (arg>>1) & 1 == 1:
        check.notis = 'Error. Incompatible flags'
        return False
    else: return True

def main():
    e = Enum('first','dfdf','rt').Optional(check)
    print e[1]
    print e.first+e.rt
    print e
    el = e(2)
    print el
    print el()
    if el == 'rt':
        print 'ok'

    print ''

    for i in e:
        print i

    print ''

    Enum('second')[1]

    print e['first']
    print e.first





if __name__ == '__main__':
    main()
