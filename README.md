# Py2Enum
Реализация Enum-а для python 2 с возможностью применения побитовых флагов. 

Example: 

    myEnum = Enum('First','dfdf','rt')
    val = myEnum( myEnum.First + myEnum.rt )
    if val == 'First':
        print val.__sum__()

Добавлены условия сочетания флагов (см. файл Example):

In Optional you can specify the condition for compatible flags of your enum. In example I have specified on incompatible flags for first and second bits if first bit is 0 and second if not 0. This feature is rarely needed, but can be very useful.

So. In example for e(2) its give out the error, becaurse 2 = 1 0. For e(3) it works, becaurse 3 = 1 1. But it is just example! You can specify any condition  for flag bits which you need or work without its

You can also apply lambda expression for the condition. Same as in method check in example.py only shorter:

    e = Enum('first','dfdf','rt').Optional(lambda a: a & 3 != 2) 

Or for man readable:

    e = Enum('first','dfdf','rt')

    e.Optional(lambda val: val & (e.first + e.dfdf) != (not e.first) + e.dfdf)
    
And check its:
    
    e(3) # works
    
    e(2) # error
