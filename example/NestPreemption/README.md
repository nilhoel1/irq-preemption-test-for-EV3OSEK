
Three tasks are deployed. The example will demonstrate if the system has the support of nested preemption or not.
However, it shouldn't have this feature in the current design.

## Results in EV3OSEK with old cpu_support.S and execeptionhandler.S:
'''
Task 1(0) start at 1.

Task 1(2) end at 2001.

Task 2(0) start at 2003.

Task 2(2) end at 3993.

Task 3(0) start at 3996.

Task 3(2) end at 5986.

Task 3(2) start at 7001.

Task 2(2) start at 8001.

Task 1(2) start at 9001.

Task 1(4) end at 10991.

Task 2(6) end at 12982.

Task 3(6) end at 14972.

Task 2(6) start at 16001.

Task 2(8) end at 17991.

Task 1(4) start at 18001.

Task 1(6) end at 19991.

Task 3(6) start at 21001.

Task 3(8) end at 22991.

Task 2(8) start at 24001.

Task 2(10) end at 25991.

Task 1(6) start at 27001.

Task 1(8) end at 28991.

Task 3(8) start at 28993.

Task 3(10) end at 30984.

...
'''
## Results in EV3OSEK with patched cpu_support.S and exceptionhandler.S:
'''
Task 1(0) start at 1.

Task 1(2) end at 2005.

Task 2(0) start at 2007.

Task 2(2) end at 4001.

Task 3(0) start at 4003.

Task 3(2) end at 5998.

Task 3(2) start at 7001.

Task 2(2) start at 8001.

Task 1(2) start at 9001.

Task 1(4) end at 10995.

Task 2(4) end at 11992.

Task 3(4) end at 12988.

Task 3(4) start at 14001.

Task 3(6) end at 15995.

Task 2(4) start at 16001.

Task 2(6) end at 17995.

Task 1(4) start at 18001.

Task 1(6) end at 19995.

Task 3(6) start at 21001.

Task 3(8) end at 22995.

Task 2(6) start at 24001.

Task 2(8) end at 25995.

Task 1(6) start at 27001.

Task 1(8) end at 28995.

Task 3(8) start at 28997.

Task 3(10) end at 30992.

...

'''

