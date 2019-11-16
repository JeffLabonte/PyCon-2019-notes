# Fantastic anti-patterns and where to fin them:  Pinpointing performance bottlenecks

Notes:

Tool: Flame Graphs ( Sampling perfomance )

Solution to bottlenecks:

1. profiling

2. flame graphs

Profiler:

* Program that analyses another program at runtim and reports useful data
  
  * instrumentation
    
    * changes the target program with various hooks so it reports data
    
    * very accurate data points
    
    * costly
    
    * can affect the behaviour
    
    * e.g `coverage`
  
  * Sampling
    
    * statistical so approximate
    
    * not coslty ( can run in prod!)
      
      * some CPu/cache overhead
    
    * no code changes, inspect a running program
    
    * e.g `py-spy`

`flame-graph` ( More of a profiler )

* Vertical: stack trace depth

* horizontal axus: time spend proportional to parent ( No Order)

* "Gaps" between vertical levels

What to look for:

1. Find big overhead ( Gaps )

2. High horizontal portion

3. recurring function calls

Anti-patern: Costly eager string formatting:

- logging that has a lot of arguments

- formatter

Anti-patter: Repeated file system reads:

1. File system reads are expensive

2. Real life equivalent ( `ensure_keyboard`)

( Read of files should be  using`@lru_cache`)

`lru_cache` in the `functools`

```python
@functoors.lr_cache(maxsize=128, tped=False)
Decorator to wrap a function with a memorizing callable that save up to 128 calls ( Reduce IO intesive overhead)
```

It can deal with C-Extension as well
