Random()
=========
The code:
---------
.. code::java 
      public Random(long seed) {
        if (getClass() == Random.class)
            this.seed = new AtomicLong(initialScramble(seed));
        else {
            // subclass might have overriden setSeed
            this.seed = new AtomicLong();
            setSeed(seed);
        }
    }
 --------
When you setup a Random random object thingy, you put the seed in the () of the Random() class you set the random variable to. It can make its own seed too if you don't put one in.
