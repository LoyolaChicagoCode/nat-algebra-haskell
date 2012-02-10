This example, based on chapter three of Richard Bird's Introduction to
Functional Programming using Haskell (2nd ed.) and section two of Erik
Meijer's banana paper, is intended to convey several key ideas:

- Definition of natural numbers as a very simple sublinear recursive
  algebraic data type. Think of Nat as structurally equivalent to List
  but without places to put items.

- Separation of concerns between traversal and processing: algebras
  over algebraic data types allow you to express common patterns of
  recursion as higher-order functions. The algebra for Nat is
  fashioned closely after the algebra of the linear List type.

- Transformation laws that help you refactor programs in provably
  meaning-preserving ways.

- Type classes: how to make your own types more usable by making them
  instances of certain type classes.

- HUnit, including ways to reuse test cases through parameterization.

To load the example and run the tests:

	$ ghci
	GHCi, version 7.0.3: http://www.haskell.org/ghc/  :? for help
	...
	Prelude> :load nat.hs
	[1 of 1] Compiling Main             ( nat.hs, interpreted )
	Ok, modules loaded: Main.
	*Main> runTestTT testsNatAll
	Loading package HUnit-1.2.4.2 ... linking ... done.
	Cases: 77  Tried: 77  Errors: 0  Failures: 0
	Counts {cases = 77, tried = 77, errors = 0, failures = 0}

You can also run individual tests or play around with the various
functions.