### irq-preemption-test-for-EV3OSEK

The content of example/IrqPreemtionTest has to be moved to the example folder in EV3OSEK.

The Programm can then be executed by using make and flashing to sd. 

For further instructions refere to the EV3OSEK Repo.



# Results in EV3OSEK with old cpu_support.S and execeptionhandler.S:
'''
Task 2(0, 0, 0) start at 1.

Task 2(0, 2, 0) end at 2005.

Task 3(0, 2, 0) start at 2007.

Task 3(0, 2, 2) end at 4002.

Task 1(0, 2, 2) start at 5001.

Task 1(2, 2, 2) end at 6995.

Task 2(2, 2, 2) start at 8001.

Task 2(2, 4, 2) end at 9995.

Task 1(2, 4, 2) start at 10001.

Task 1(4, 4, 2) end at 11995.

Task 3(4, 4, 2) start at 11998.

Task 3(4, 4, 4) end at 13992.

Task 1(4, 4, 4) start at 15001.

Task 1(6, 4, 4) end at 16995.

Task 2(6, 4, 4) start at 16998.

Task 2(6, 6, 4) end at 18992.

Task 1(6, 6, 4) start at 20001.

Task 1(8, 6, 4) end at 21995.

Task 3(8, 6, 4) start at 21998.

Task 3(8, 6, 6) end at 23992.

Task 2(8, 6, 6) start at 24001.

Task 1(8, 8, 6) start at 25001.

Task 1(10, 8, 6) end at 26995.


'''


Here goes something wrong, cause the OS hangs after 27s and no other Task gets loaded.

## Results in EV3OSEK with patched cpu_support.S and exceptionhandler.S:
'''
Task 2(0, 0, 0) start at 1.

Task 2(0, 2, 0) end at 2004.

Task 3(0, 2, 0) start at 2006.

Task 3(0, 2, 2) end at 4096.

Task 1(0, 2, 2) start at 5001.

Task 1(2, 2, 2) end at 7090.

Task 2(2, 2, 2) start at 8001.

Task 2(2, 4, 2) end at 9994.

Task 1(2, 4, 2) start at 10001.

Task 1(4, 4, 2) end at 12090.

Task 3(4, 4, 2) start at 12093.

Task 3(4, 4, 4) end at 14183.

Task 1(4, 4, 4) start at 15001.

Task 1(6, 4, 4) end at 17090.

Task 2(6, 4, 4) start at 17093.

Task 2(6, 6, 4) end at 19087.

Task 1(6, 6, 4) start at 20001.

Task 1(8, 6, 4) end at 22090.

Task 3(8, 6, 4) start at 22093.

Task 2(8, 6, 6) start at 24001.

Task 1(8, 8, 6) start at 25001.

Task 1(10, 8, 6) end at 27090.

Task 2(10, 8, 6) end at 28087.

Task 3(10, 8, 6) end at 28273.

Task 1(10, 8, 6) start at 30001.
...
'''
For more output see OutputAfter10Min.txt File.
For more output see OutputAfter10Min.txt File.
