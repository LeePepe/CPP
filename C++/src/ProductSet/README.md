### 1. ProductSet

* In mathematics, a Cartesian product is a mathematical operation which returns a set (or product set or simply product) from multiple sets. That is, for sets A and B, the Cartesian product A × B is the set of all ordered pairs (a, b) where a ∈ A and b ∈ B. Products can be specified using set-builder notation, e.g.
* In my file, I define it as a class. That's wrong. But I didn't find a great way to show a simple set from two sets.
* It just has two privte properties Set A and Set B.


    Remember Cartesian product is a **operation**.

### 2. Relation

* Relation is subset of ProductSet.
* Of cource, Relation is a operation.
* Fortunately, We can use a boolean matrix to represent a relation.
* But generally we do not discusse normal relation.

#### Operations on relation
-1 is inverse and ~ is complement.

* Suppose that R and S are relations from A to B.
    1. If R ⊆ S, then R-1 ⊆ S-1.
    2. If R ⊆ S, then ~R ⊆ ~S.
    3. (R ∩ S)-1 = R-1 ∩ S-1 and (R ∪ S)-1 = R-1 ∪ S-1.
    4. ~(R ∩ S) = ~R ∩ ~S and ~(R ∪ S) = ~R ∪ ~S.
* Let R and S be relations on a set A.
    1. If R is reflexive, so is R-1.
    2. If R and S are reflxive, then so are R ∩ S and R ∪ S.
    3. R is reflexive if and only if ~R is irreflexive.
* Let R be a relation on a set A. Then
    1. R is symmetric if and only if R = R-1.
    2. R is antisymmetric if and only if R ∩ R-1 ⊆ △.
    3. R is asymmetric if and only if R ∩ R-1 = ∅.
* Let R and S be relations on A.
    1. If R is symmetric, so are R-1 and ~R.
    2. If R adn S are symmetric, so are R ∩ S and R ∪ S.
* Let R and S be relations on A.
    1. (R ∩ S)2 ⊆ R2 ∩ S2.
    2. If R and S are transitive, so is R ∩ S.
    3. If R and S are equivalence relations, so is R ∩ S.

#### Closures

#### Composition

It is complex to program on general relation. So I do that in BinaryRelation.


### 3. BinaryRelation

    If A is a finite set and R is a relation on A.

* I use BinaryRelation to represent binary relation.
* That is, matrix will be a square matrix. And there are many properties or operations to program.

    1. Indegree adn Outdegree:

        input a number which in set.

        just count number from row or column way. then you can get in-degree and out-degree.

        if X not in set, then return -1.

    2. Path of length:

        Input a N. And calculate path. We can use a new Relation(BinaryRelation) to represent it.

    3. Properties of Relations:

        We can identify properties of a relation by its matrix as follows.

        > Reflexive:

            ∀ (a, a) ∈ R

            The matrix of a reflexive relation must have all 1's on its main diagonal.

        > Irreflexive:
    
            ∀ (a, a) ∉ R

            The matrix of a irreflexive relation must have all 0's on its main diagonal.

        > Symmetric:

            (a, b) ∈ R → (b, a) ∈ R

            The matrix of a symmetric relation when m[ij] = 1 and m[ji] = 1.
            Or MR = MᵀR.

        > Asymmetric:

            (a, b) ∈ R → (b, a) ∉ R

            The matrix of an asymmetric relation when m[ij] = 1 and m[ji] = 0.

        > Antisymmetric:

            (a, b) ∈ R ∧ (b, a) ∈ R → a = b

            The matrix of an antisymmetric relation when i ≠ j and m[ij] = 0 or m[ji] = 0.

        > Tranistive:

            (a, b) ∈ R ∧ (b, c) ∈ R → (a, c) ∈ R

            The matrix of an transitive relation when m[ik] = 1 and m[kj] = 1 and m[ij] = 1.

    4. Equivalence Relations
        
        A relation R on a set A is called an **equivalence relation** if it is reflexive, symmetric and transitive.

    5. Composition
        
        M(S∘R) = M(R) ⊙ M(S)

    6. Closures
    
        we need to find is the smallest relation R1 on A that contains R and possesses the property we desire. If a relation R1 is exist, call it the **closure** of R.

        > Reflexive closure

            R1 = R ∪ △, which △is the diagonal relation.

        > Symmetric closure

            R ∪ R-1 is the symmetric closure of R.

        > Transitive closure and Warshall's Algorithm

            The transitive closure of R is just the **connectivity relation** R∞ 

            