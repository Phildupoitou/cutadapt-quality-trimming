# cutadapt-quality-trimming
I would like to use cutadapt v1.9 to trim a .fastq files for sequence quality:
my command:
cutadapt -q 20 -o test_R1.fastq.clean test_R1.fastq
reply:
This is cutadapt 1.9.dev1 with Python 2.6.6
Command line parameters: -q 20 -o test_R1.fastq.clean test_R1.fastq
Trimming 0 adapters with at most 10.0% errors in single-end mode ...
Traceback (most recent call last):
  File "/usr/local/bioinfo/cutadapt/1.9/bin/cutadapt", line 10, in <module>
    cutadapt.main()
  File "/usr/local/bioinfo/cutadapt/1.9/cutadapt/scripts/cutadapt.py", line 832, in main
    stats = process_single_reads(reader, modifiers, writers)
  File "/usr/local/bioinfo/cutadapt/1.9/cutadapt/scripts/cutadapt.py", line 253, in process_single_reads
    read = modifier(read)
  File "/usr/local/bioinfo/cutadapt/1.9/cutadapt/modifiers.py", line 110, in __call__
    start, stop = quality_trim_index(read.qualities, self.cutoff_front, self.cutoff_back, self.base)
TypeError: quality_trim_index() takes at most 3 arguments (4 given)

What should I do??
Thank you
