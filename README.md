### irq-preemption-test-for-EV3OSEK

The content of example/IrqPreemtionTest has to be moved to the example folder in EV3OSEK.

The Programm can then be executed by using make and flashing to sd. 

For further instructions refere to the EV3OSEK Repo.



# Results in EV3OSEK with old cpu_support.S and execeptionhandler.S:
'''
Task 2(0, 0, 0) start at 1.

Task 2(0, 1, 0) end at 2005.

Task 3(0, 1, 0) start at 2007.

Task 3(0, 1, 1) end at 4002.

Task 1(0, 1, 1) start at 5001.

Task 1(1, 1, 1) end at 6995.

Task 2(1, 1, 1) start at 8001.

Task 2(1, 2, 1) end at 9995.

Task 1(1, 2, 1) start at 10001.

Task 1(2, 2, 1) end at 11995.

Task 3(2, 2, 1) start at 11998.

Task 3(2, 2, 2) end at 13992.

Task 1(2, 2, 2) start at 15001.

Task 1(3, 2, 2) end at 16995.

Task 2(3, 2, 2) start at 16998.

Task 2(3, 3, 2) end at 18992.

Task 1(3, 3, 2) start at 20001.

Task 1(4, 3, 2) end at 21995.

Task 3(4, 3, 2) start at 21998.

Task 3(4, 3, 3) end at 23992.

Task 2(4, 3, 3) start at 24001.

Task 1(4, 4, 3) start at 25001.

Task 1(5, 4, 3) end at 26995.
'''


Here goes something wrong, cause the OS hangs after 27s and no other Task gets loaded.

## Results in EV3OSEK with patched cpu_support.S and exceptionhandler.S:
'''
Task 2(0, 0, 0) start at 1.

Task 2(0, 1, 0) end at 2004.

Task 3(0, 1, 0) start at 2007.

Task 3(0, 1, 1) end at 4001.

Task 1(0, 1, 1) start at 5001.

Task 1(1, 1, 1) end at 6994.

Task 2(1, 1, 1) start at 8001.

Task 2(1, 2, 1) end at 9994.

Task 1(1, 2, 1) start at 10001.

Task 1(2, 2, 1) end at 11995.

Task 3(2, 2, 1) start at 11997.

Task 3(2, 2, 2) end at 13991.

Task 1(2, 2, 2) start at 15001.

Task 1(3, 2, 2) end at 16995.

Task 2(3, 2, 2) start at 16997.

Task 2(3, 3, 2) end at 18991.

Task 1(3, 3, 2) start at 20001.

Task 1(4, 3, 2) end at 21995.

Task 3(4, 3, 2) start at 21997.

Task 3(4, 3, 3) end at 23991.

Task 2(4, 3, 3) start at 24001.

Task 1(4, 4, 3) start at 25001.

Task 1(5, 4, 3) end at 26995.

Task 2(5, 4, 3) end at 27991.

Task 1(5, 4, 3) start at 30001.

...
'''

For more output see OutputAfter10Min.txt File.
