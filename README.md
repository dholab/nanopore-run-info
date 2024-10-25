# Oxford Nanopore Run Information

Before you set off your Oxford Nanopore sequencing run, make sure to pass along the following information to your friendly neighborhood bioinformatician:

- **Experiment ID**: An identifier or number for this run.
- **Instrument name**: Most instruments have an IP address as well as a name or alias, either of which can be used to access them remotely.
- **IP Address**: The address on the building network where raw data from the run will be stored.
- **Data File Path**: The absolute file path, starting from the root (`/`), where raw signal data will be placed by the instrument.
- **Barcode Kit**: The Nanopore kit used to barcode fragments from each sample prior to multiplexing. These kits' names generally look something like "SQK-NBD114-24" or "SQK-RBK114-24".
- **Flow Cell Chemistry**: While not required for basecalling, the flow cell version used can help set expectations for run QC. The chemistry will look something like "R10.4.1".
- **Number of Barcodes Used**: Also not necessary for basecalling, but still helpful for tracking how many barcodes should have non-negligible numbers of reads.

Additionally, you might also want to pass on a sample sheet in the format:

```csv
barcode,sample_id
1,sample_1
2,sample_2
```

This information can be used during basecalling or demultiplexing to give a more useful name to the output files.

For you convenience, and Excel sheet with a Run Metadata sheet and a Samplesheet sheet is included in this repo.
