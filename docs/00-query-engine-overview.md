# How Should a Query Engine Be Designed?

> Status: research outline

This chapter builds a technology-independent mental model of a modern analytical query engine before mapping the concepts to DataFusion.

## Questions

- What responsibilities belong to a query engine?
- What is the end-to-end lifecycle of a query?
- Why are planning, optimization, execution, and runtime concerns separated?
- Where are the important control-flow and data-flow boundaries?
- What design tensions appear before implementation choices are made?

## Initial mental model

```text
SQL / API
   ↓
Parsing & Binding
   ↓
Logical Representation
   ↓
Logical Optimization
   ↓
Physical Planning
   ↓
Physical Optimization
   ↓
Execution
   ↓
Runtime: Scheduling / Memory / I/O / Parallelism
```

## Next

Develop this model from first principles, then map each responsibility to DataFusion.
