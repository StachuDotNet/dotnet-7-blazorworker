Dark uses wasm'd F# in its Editor.
Our usage of the wasm happens in a WebWorker.
The official `blazor.webassembly.js` that's usually used to load/run Blazor'd stuff doesn't work out of the box for WebWorkers (due to `document` not existing, etc.)
So Dark had to 'fork' that file until it worked for us, but it was kind of hacky.
We're trying to upgrade to .net 7, but our blazorworker is failing somewhere.
This repo is my investigation in creating a new blazorworker for .net 7
