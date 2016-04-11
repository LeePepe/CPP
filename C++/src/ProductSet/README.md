### 1. ProductSet
    1) In mathematics, a Cartesian product is a mathematical operation which returns a set (or product set or simply product) from multiple sets. That is, for sets A and B, the Cartesian product A × B is the set of all ordered pairs (a, b) where a ∈ A and b ∈ B. Products can be specified using set-builder notation, e.g.
    2) In my file, I define it as a class. That's wrong. But I didn't find a great way to show a simple set from two sets.
    3) It just has two privte properties Set A and Set B.

    4) Remember Cartesian product is a operation.

### 2. Relation
    1) Relation is subset of ProductSet.
    2) Of cource, Relation is a operation.
    3) Fortunately, We can use a boolean matrix to represent a relation.
    4) But generally we do not discusse normal relation.

### 3. Digraph
    1) If A is a finite set and R is a relation on A.
    2) I use digraph to represent 1).
    2) That is, matrix will be a square matrix. And there are many properties or operations to program.
    3) Indegree adn Outdegree:
        just count number from row or column way. then you can get in-degree and out-degree
    4) Path of length:
        Input a N. And calculate path. We can use a new Relation(Digraph) to represent it.
    5)Properties of Relations.
        We can identify properties of a relation by its matrix as follows.
        (1) Reflexive:
            ∀ (a, a) ∈ R
            The matrix of a reflexive relation must have all 1's on its main diagonal.
        (2) Irreflexive:
            ∀ (a, a) ∉ R
            The matrix of a irreflexive relation must have all 0's on its main diagonal.
        (3) Symmetric:
            (a, b) ∈ R → (b, a) ∈ R
            The matrix of a symmetric relation when m[ij] = 1 and m[ji] = 1.
            Or MR = MᵀR.
        (4) Asymmetric:
            (a, b) ∈ R → (b, a) ∉ R
            The matrix of an asymmetric relation when m[ij] = 1 and m[ji] = 0.
        (5) Antisymmetric:
            (a, b) ∈ R ∧ (b, a) ∈ R → a = b
            The matrix of an antisymmetric relation when i ≠ j and m[ij] = 0 or m[ji] = 0.

