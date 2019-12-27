---
layout: default
date: 2019-12-27
title: Dataframe Storage Mini-Benchmark
---

Quick benchmark on how to read/write/store your Pandas dataframe if you don't want to read from CSV all the time. Conclusion:

1. If file size matters, use Parquet
2. If read speed matters, use Feather
3. If both matter, use HDF5/Static
4. Write speeds don't differ much, except HDF5/PyTables and CSV
5. Avoid CSV

If you want to load only some columns, use Parquet or Feather. The way Pandas uses HDF5 cannot deal with this.

Figures:

![File Size Comparison](https://cheleb.net/public/images/bench_file_size.png)

![Read Speed Comparison](https://cheleb.net/public/images/bench_read_speed.png)

![Write Speed Comparison](https://cheleb.net/public/images/bench_write_speed.png)

Code:

- [Jupyter/IPython Notebooks](https://cheleb.net/ipython/bench/)
