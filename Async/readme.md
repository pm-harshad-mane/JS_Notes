Refer: 
- https://github.com/jawache/async-javascript-workshop
- https://v8.dev/
-- V8 is synchronous
-- Chrome, Node, Electron is a container which embeds V8 and extends it
-- Node, Chrome, Electron may have async execution
- https://electronjs.org/ 
-- a V8 based tool to build cross platform desktop apps with JavaScript, HTML, and CSS
-- used by Slack, VSCode, GitHib, Skype

https://node.green/ mentions which features are available in each Node version

NVM allows you to use multiple versions of Node on same machine

"Node Exec" VSCode extension alllows you to execute any selected snippet to execute by pressing F8
"Live Server" VSCode extension opens a local server and opens a selected (html)file in browser
"Pretier" VS Code extension, pretifies the code, run command format, formats JS, .md, html

Command + Shift P opens a command pallet in VSCode


Sync Vs Async
- Sync is easier to read and predict
- Async difficult to read and predict
- Async is better for performance

Threads
- Threads are just like processes with shared memory
- shared memory means race conditions
- you need locks to handle race conditions
- locks: dead-locks, live-locks
- when a thread blocks another thread takes over
- writing performant multi-threaded code is hard

Even Driven programming
- Node abstracts all IO operations into events that are handled on an implicit eventloop
- Your JS code is single threaded
- Node does use threads
- One main thread
- Asynchronicity is provided by events
- Uses events to sync state
- Code doesn't block means there is always something that is running
- Node makes it easy to write performant code


Async Patterns
- Callbacks
  - old
  - widely used 
  - examples
    - setTimeout 
    - setInterval
    - setImmediate
    - process.nextTick
  - always pass error as a first argument in Node
  - Callback hell
    - nested callbacks
    - Promises solve callback hells
  - Try-catch does not work with async code
- Promises
  - not so old
  - widely used
- Async/Await
  - very new
- Generators
  - old
  - not much used

