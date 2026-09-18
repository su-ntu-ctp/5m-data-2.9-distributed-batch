# Pre-class brief

![Unit 2.9](./assets/unit-2-9-distributed-batch-processing.png)

### Where are we?

FreshCart gets acquired by a larger retail group. Suddenly you're not processing 50 million rows — you're processing 5 billion rows of combined transaction data across 12 countries. A single machine, even with Polars, can't handle this. You need to distribute the work across a cluster of machines.

### Why this matters

Apache Spark is the industry standard for large-scale batch data processing. Most data engineering job descriptions list it as a requirement. More importantly, the distributed computing concepts you learn here — lazy evaluation across a cluster, partitioned processing, shuffle operations — form the mental model for understanding any distributed data system.

### Key concepts

**Spark Architecture** — Spark builds a DAG (directed acyclic graph) of transformations and only executes when an "action" (like `.show()` or `.count()`) is called. This is the same concept from Polars (**Lesson 2.8**) but now distributed across multiple machines.

**Spark DataFrames and SQL** — Spark's DataFrame API mirrors pandas-like operations (`.select()`, `.filter()`, `.groupBy()`) but executes across a cluster. The ability to register a DataFrame as a SQL temp view means data engineers and analysts can collaborate in the same framework.

**The Big Data Ecosystem Evolution** — Hadoop → MapReduce → Spark. Understanding *why* Spark exists (it keeps data in memory between steps, unlike MapReduce's disk-heavy approach) gives you historical context for the tools you'll encounter in job interviews and legacy systems.

📄 [View lesson 2.9 interactive page](https://su-ntu-ctp.github.io/5m-data-2.9-distributed-batch/)
