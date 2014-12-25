## Neural Networks in the Browser

__Note__: This has been broken by the current version of LambdaNet, but will be fixed when cabal install/update of LambdaNet is available.

### First Time Setup

Install [leiningen](http://leiningen.org).
  1. Download the [lein script](https://raw.githubusercontent.com/technomancy/leiningen/stable/bin/lein)
  2. Place it on your $PATH where your shell can find it (eg. `~/bin`)
  3. Set it to be executable (`chmod a+x ~/bin/lein`)
  4. Run it (`./lein`) and it will download the self-install package

### Build and run frontend
```
cd frontend
lein cljsbuild once
lein ring server
```
The front end will then be running on port 3000.

### Routes
```
/create
```
Takes a vector of layer config objects and a weight initialization function key and returns a vector of weight matrices.

```
/train
```
Takes a vector of weight matrices, a list of training inputs, and a list of expected outputs. Returns a trained vector of weight matrices.

```
/evaluate
```
Takes a vector of weight matrices and input data and returns the result of running the input data through the network represented by the vector of weight matrices.
