# Py2Enum
Реализация Enum-а для python 2 с возможностью применения побитовых флагов. 

Example: 

    myEnum = Enum('First','dfdf','rt')
    val = myEnum( myEnum.First + myEnum.rt )
    if val == 'First':
        print val.__sum__()

Добавлены условия сочетания флагов:

In Optional you can specify thr condition for compatible flags of your enum. In example I have specified on incompatible flags for first and second bits if first bit is 0 and second if not 0. This feature is rarely needed, but can be very useful.

So. For e(2) its give out the error, becarse 2 = 1 0. For e(3) it works, becaurse 3 = 1 1. But it is just example! You can specify any condition  for flag bits which you need or work without its

