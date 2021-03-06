<script>
MathJax.Hub.Queue(["Typeset",MathJax.Hub]);
</script>
$$ 
\newcommand{\d}{\mathrm{d}}
\newcommand{\bff}{\boldsymbol{f}}
\newcommand{\bfg}{\boldsymbol{g}}
\newcommand{\bfp}{\boldsymbol{p}}
\newcommand{\bfq}{\boldsymbol{q}}
\newcommand{\bfx}{\boldsymbol{x}}
\newcommand{\bfu}{\boldsymbol{u}}
\newcommand{\bfv}{\boldsymbol{v}}
\newcommand{\bfA}{\boldsymbol{A}}
\newcommand{\bfB}{\boldsymbol{B}}
\newcommand{\bfC}{\boldsymbol{C}}
\newcommand{\bfM}{\boldsymbol{M}}
\newcommand{\bfJ}{\boldsymbol{J}}
\newcommand{\bfR}{\boldsymbol{R}}
\newcommand{\bfT}{\boldsymbol{T}}
\newcommand{\bfomega}{\boldsymbol{\omega}}
\newcommand{\bftau}{\boldsymbol{\tau}}
$$

# Euclidean Algorithm

Computer science is (almost by definition) a science about computers -- a device first conceptualized in the 1800's. Computers have become so revolutionary, that it is difficult to think of our lives today without them. That said, *algorithms* are much older and have existed in the world for millenia. Incredibly, a few of the algorithms created before the Common Era (AD) are still in use today. One such algorithm was first described in Euclid's *Elements* (~ 300 BC) and has come to be known as the *Euclidean Algorithm*. 

The algorithm is a simple way to find the *greatest common divisor* (GCD) of two numbers, which is useful for a number of different applications (like reducing fractions). The first method (envisioned by Euclid) uses simple subtraction:

{% method %}
{% sample lang="c" %}
[import:18-33, unindent:"true", lang="c_cpp"](code/c/euclidean_example.c)
{% sample lang="cs" %}
[import:6-17, unindent:"true", lang="csharp"](code/cs/EuclideanAlgorithmMdAdditional.cs)
{% sample lang="clj" %}
[import:1-7, unindent:"true", lang="clojure"](code/clojure/euclidean_example.clj)
{% sample lang="cpp" %}
[import:21-35, unindent:"true", lang="c_cpp"](code/c++/euclidean_example.cpp)
{% sample lang="js" %}
[import:1-11, unindent:"true", lang="julia"](code/pseudo/euclidean.pseudo)
{% sample lang="py2" %}
[import:1-11, unindent:"true", lang="julia"](code/pseudo/euclidean.pseudo)
{% sample lang="haskell" %}
[import:1-11, unindent:"true", lang="julia"](code/pseudo/euclidean.pseudo)
{% sample lang="rs" %}
[import:1-11, unindent:"true", lang="julia"](code/pseudo/euclidean.pseudo)
{% sample lang="ml" %}
[import:1-11, unindent:"true", lang="julia"](code/pseudo/euclidean.pseudo)
{% sample lang="java" %}
[import:1-11, unindent:"true", lang="julia"](code/pseudo/euclidean.pseudo)
{% endmethod %}

Here, we simply line the two numbers up every step and subtract the lower value from the higher one every timestep. Once the two values are equal, we call that value the greatest common divisor. A graph of `a` and `b` as they change every step would look something like this:

![Subtraction-based Euclidean algorithm](res/subtraction.png)

Modern implementations, though, often use the modulus operator (%) like so

{% method %}
{% sample lang="c" %}
[import:4-16, unindent:"true", lang="c_cpp"](code/c/euclidean_example.c)
{% sample lang="cs" %}
[import:19-29, unindent:"true", lang="csharp"](code/cs/EuclideanAlgorithmMdAdditional.cs)
{% sample lang="clj" %}
[import:8-12, unindent:"true", lang="clojure"](code/clojure/euclidean_example.clj)
{% sample lang="cpp" %}
[import:7-18, unindent:"true", lang="c_cpp"](code/c++/euclidean_example.cpp)
{% sample lang="js" %}
[import:13-21, unindent:"true", lang="julia"](code/pseudo/euclidean.pseudo)
{% sample lang="py2" %}
[import:13-21, unindent:"true", lang="julia"](code/pseudo/euclidean.pseudo)
{% sample lang="haskell" %}
[import:13-21, unindent:"true", lang="julia"](code/pseudo/euclidean.pseudo)
{% sample lang="rs" %}
[import:13-21, unindent:"true", lang="julia"](code/pseudo/euclidean.pseudo)
{% sample lang="ml" %}
[import:13-21, unindent:"true", lang="julia"](code/pseudo/euclidean.pseudo)
{% sample lang="java" %}
[import:13-21, unindent:"true", lang="julia"](code/pseudo/euclidean.pseudo)
{% endmethod %}

Here, we set `b` to be the remainder of `a%b` and `a` to be whatever `b` was last timestep. Because of how the modulus operator works, this will provide the same information as the subtraction-based implementation, but when we show `a` and `b` as they change with time, we can see that it might take many fewer steps:

![Modulus-based Euclidean algorithm](res/modulus.png)

The Euclidean Algorithm is truly fundamental to many other algorithms throughout the history of computer science and will definitely be used again later. At least to me, it's amazing how such an ancient algorithm can still have modern use and appeal. That said, there are still other algorithms out there that can find the greatest common divisor of two numbers that are arguably better in certain cases than the Euclidean algorithm, but the fact that we are discussing Euclid two millenia after his death shows how timeless and universal mathematics truly is. I think that's pretty cool.

# Example Code

{% method %}
{% sample lang="c" %}
### C
[import, unindent:"true", lang="c_cpp"](code/c/euclidean_example.c)
{% sample lang="cs" %}
### C# #
[import, unindent:"true", lang="csharp"](code/cs/EuclideanAlgorithmMdAdditional.cs)
{% sample lang="clj" %}
### Clojure
[import, unindent:"true", lang="clojure"](code/clojure/euclidean_example.clj)
{% sample lang="cpp" %}
### Cpp 
[import, unindent:"true", lang="c_cpp"](code/c++/euclidean_example.cpp)
{% sample lang="js" %}
### JavaScript
[import, unindent:"true", lang="javascript"](code/javascript/euclidean_example.js)
{% sample lang="py2" %}
### Python
[import, unindent:"true", lang="python"](code/python2/euclidean_example.py)
{% sample lang="haskell" %}
### Haskell
[import, unindent:"true", lang="haskell"](code/haskell/euclidean_example.hs)
{% sample lang="rs" %}
### Rust
[import, unindent:"true", lang="rust"](code/rust/euclidean_example.rs)
{% sample lang="ml" %}
### Ocaml
[import, unindent:"true", lang="ocaml"](code/ocaml/euclidean_example.ml)
{% sample lang="java" %}
### Java
[import, unindent:"true", lang="java"](code/java/euclidean_example.jar)
{% endmethod %}
