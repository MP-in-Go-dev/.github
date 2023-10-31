<h3 align="center"> MatProGo-dev</h3>

## 📝 Table of Contents
- [📝 Table of Contents](#-table-of-contents)
- [How to Use MatProGo](#how-to-use-matprogo-)
- [The Mathematical Programming Universe](#the-mathematical-programming-universe-)

This organization is focused on centralizing some of the tools used to 
perform Mathematical Programming in the [Go](https://go.dev/) (Golang) language. It aims to 
create a universal interface for defining optimization problems (like [YALMIP](https://github.com/yalmip/YALMIP)) and 
to share simple wrappers that solve those optimization problems with arbitrary solvers (e.g., Gurobi).

## How to Use MatProGo <a name="how-to-use"></a>

The steps for making use of MatProGo's work should be as follows:
1. For your Go project, get the MatProInterface.go module.
2. Define your optimization problem using the symbolic math tools in this library (i.e., create the expressions, constraints and objective and attach them to a model).
3. For your desired problem type, get the appropriate MatProInterface wrapper (e.g. Gurobi.go) module.
4. Use the wrapper to solve the model created in Step 2.

## The Mathematical Programming Universe <a name="mp-universe"></a>

So far, we've noticed the following options available to Go users that are interested in solving Mathematical Programming problems:
- [Mosek.go](https://github.com/MOSEK/Mosek.go)
- [Gurobi.go](https://github.com/MatProGo-dev/Gurobi.go) (From this repository)
- [gonum](https://github.com/gonum/gonum)
- [osqp.go](https://github.com/jerensl/osqp.go)

Each solver is typically designed for a specific class of problem (e.g., a Quadratic Program). We describe the capabilities of each library with the following table:

| Problem Type                          |  Solvers  |
|:-------------------------------------:|:---------:|
| Linear Programs (LPs)                 | Gurobi, Gonum, Mosek, OSQP |
| Mixed Integer Linear Programs (MILPs) | Gurobi, Mosek |
| Quadratic Programs (QPs)              | Gurobi, OSQP, Mosek |
| Second-Order Cone Programs (SOCPs)    | Mosek |

