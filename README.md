# Comparing-Pandas-and-Spark-Pipelines-for-Large-Scale-Data-Discretization
This project compares the performance of Pandas vs Spark for building data preprocessing pipelines to discretize features in a large-scale dataset.

## Dataset
Simulated input data of 1 million rows with 10 continuous features is created to represent a large-scale dataset typical of real-world use cases.

## Pipelines
Two pipelines are implemented - one using Pandas and the other using Spark:

**Pandas Pipeline:** Runs sequentially on a single machine. Features are discretized one-by-one using KBinsDiscretizer.

**Spark Pipeline:** Leverages Spark's distributed processing by running discretization in parallel on a Spark DataFrame.

## Metrics
Time taken and memory usage are logged for each pipeline to quantify performance differences at scale.

## Results
The results show that Spark significantly outperforms Pandas in both time and memory usage due to its ability to parallelize processing across a cluster.

## Usage
Clone this repo and run Pipeline 1 & 2.ipynb on a multi-core machine with Spark installed. Adjust core counts/cluster size to see scaling.

## Conclusion
This project demonstrates how Spark can be leveraged for data preprocessing on large scales where Pandas may not suffice. With further profiling, it can provide useful guidelines on choosing the right framework based on use case requirements.
