### irq-preemption-test-for-EV3OSEK

The content of example/IrqPreemtionTest has to be moved to the example folder in EV3OSEK.

The Programm can then be executed by using make and flashing to sd. 

For further instructions refere to the EV3OSEK Repo.



# Results in EV3OSEK with old cpu_support.S and execeptionhandler.S:
'''
Task 2(0, 0, 0) start at 1.

Task 2(0, 2, 0) end at 2005.

Task 3(0, 2, 0) start at 2007.

Task 1(0, 2, 2) start at 4001.

Task 1(2, 2, 2) end at 5995.
'''


Here goes something wrong, cause the OS hangs after 6s and no other Task gets loaded.

## Results in EV3OSEK with patched cpu_support.S and exceptionhandler.S:
'''
Task 2(0, 0, 0) start at 1.

Task 2(0, 2, 0) end at 2004.

Task 3(0, 2, 0) start at 2006.

Task 1(0, 2, 2) start at 4001.

Task 1(2, 2, 2) end at 6090.

Task 3(2, 2, 2) end at 6189.

Task 1(2, 2, 2) start at 8001.

Task 1(4, 2, 2) end at 10090.

Task 2(4, 2, 2) start at 10093.

Task 1(4, 4, 2) start at 12001.

Task 1(6, 4, 2) end at 14090.

Task 2(6, 4, 2) end at 14180.

Task 3(6, 4, 2) start at 14183.

Task 1(6, 4, 4) start at 16001.

Task 1(8, 4, 4) end at 18090.

Task 2(8, 4, 4) start at 18093.

Task 1(8, 6, 4) start at 20001.

Task 1(10, 6, 4) end at 22090.

Task 2(10, 6, 4) end at 22180.

Task 3(10, 6, 4) end at 22455.

Task 1(10, 6, 4) start at 24001.

Task 1(12, 6, 4) end at 26091.

Task 2(12, 6, 4) start at 26093.

Task 1(12, 8, 4) start at 28001.

Task 1(14, 8, 4) end at 30091.

Task 2(14, 8, 4) end at 30180.

Task 3(14, 8, 4) start at 30183.

Task 1(14, 8, 6) start at 32001.

Task 1(16, 8, 6) end at 34091.

Task 2(16, 8, 6) start at 34093.

Task 1(16, 10, 6) start at 36001.

Task 1(18, 10, 6) end at 38091.

Task 2(18, 10, 6) end at 38180.

Task 3(18, 10, 6) end at 38456.

Task 1(18, 10, 6) start at 40001.

Task 1(20, 10, 6) end at 42091.

Task 2(20, 10, 6) start at 42094.

Task 1(20, 12, 6) start at 44001.

Task 1(22, 12, 6) end at 46091.

Task 2(22, 12, 6) end at 46181.

Task 3(22, 12, 6) start at 46184.

Task 1(22, 12, 8) start at 48001.

Task 1(24, 12, 8) end at 50091.

Task 2(24, 12, 8) start at 50094.

Task 1(24, 14, 8) start at 52001.

Task 1(26, 14, 8) end at 54091.

Task 2(26, 14, 8) end at 54181.

Task 3(26, 14, 8) end at 54457.

Task 1(26, 14, 8) start at 56001.

Task 1(28, 14, 8) end at 58091.

Task 2(28, 14, 8) start at 58094.

Task 1(28, 16, 8) start at 60001.

Task 1(30, 16, 8) end at 62091.

Task 2(30, 16, 8) end at 62181.
'''

