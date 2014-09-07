Lisp
========================================

Garbage Collection 在 1959 年的時候由 John McCarthy 為了解決 Lisp 的問題而提出

Tracing garbage collectors
========================================

trace 過所有能到達的 objects，到不了的就是可以回收了

衍生出來的作法有很多種

Mark and Sweep
------------------------------

Naive Mark and Sweep
~~~~~~~~~~~~~~~~~~~~

Tri-color marking
~~~~~~~~~~~~~~~~~~~~

Bitmap marking
~~~~~~~~~~~~~~~~~~~~

Lazy sweeping
~~~~~~~~~~~~~~~~~~~~

Mark and Compact
------------------------------

Copying
------------------------------

Reference counting
========================================

紀錄 reference 到 object 的數目，當 reference 變成 0 時就可以回收了

Cycles
------------------------------

幾個 object 互相 reference，形成一個 cycle，造成 reference 數不會變成 0，
一種解決方法是用 cycle detect 的 algorithm，另一種是對於會產生 cycle 的 backpointer 使用 weak reference，
weak reference 不會增加 reference 數目的計算
