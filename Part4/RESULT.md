
            


We do not get the expecting i=0 for any of the programs. The reason could be that there is a mutex lock. This happens when two threads try to access the same memory simultanously. The mechanism makes only one of them access it, while the other is left out. This makes the behavior unpredictable. 
