## Iodide, Pyodide and the future of Python on the Web



William Lachance - Mozilla



Notes:



**Jupyter notebook for data science..... MUST**



Jupyter limitation:

1. Passing file around

2. Am I making presentation or doing computation

3. Hidden depency on state of local machine

4. Shareing even a read-only copy is hard

nvviewer ( share notebook.... old way  to share)



**Glitch**

Makes web application easier to see and share ( aka collaborate on Jupyter)

[glitch website](https://glitch.com/)



## [iodide](https://alpha.iodide.io/)



Client side execution:

- Just run in your browser
  
  - no setup required

- Presentation mode
  
  - Allow you to concentrate on your content

- Easy to share, discover and remix notesbooks

- Data is first class citizen
  
  - Data stored on Ionide, right there!
  
  - Helps for 

- iomd
  
  - help enable more stuff in the MD



Specs:

- Stores content of notebook, not computational kernels

- built using stadard tools: PostgresSQL, Django

- Can be deployed everywhere



Problem:

- Computational kernel is on client, so JS works geat

- but data science ecosystem on JS is extremely immature



## Python on the browser



`asm.js`is a precursor to web assembly ([ assembly JS](http://asmjs.org/spec/latest/) )



***WebAssembly***:



* Run programs in C/C++ or Rust in the browser
  
  * Like a game UT@130FPS



We **CAN** use WA ( WebAssembly ) for Python



<u>***Loading data:***</u>

*Data in JS/web Land -> HiWire -> Python*

HiWire:

1. Heap buffer from JS to Python
   
   1. Can be slow if it runs often



In general, it is relatively fast ... but in some cases ...  it can be slow





What won't work:

- Raw network sockets

- subporcesses

- Raw filesystem access



What will work someday:

- threads

- async

- SIMD

- GPGPU
