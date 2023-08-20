# Example Nextflow query profiles pipeline

This pipeline is an example for querying cg/wgMLST profiles.

If you have Nextflow and Docker installed, you can test it out with:

```bash
nextflow run https://github.com/apetkau/nf-core-queryprofiles -profile docker,test -r dev --outdir results
```

Or, if you wish to use your own data:

```bash
nextflow run https://github.com/apetkau/nf-core-queryprofiles -r dev -profile docker --match_threshold 10 --reference_profile reference_profiles.tsv --query_profile query_profiles.tsv --outdir results --input 'https://raw.githubusercontent.com/nf-core/test-datasets/viralrecon/samplesheet/samplesheet_test_illumina_amplicon.csv'
```

Note, that the parameter of `--input` is not used right now now, but is only there until this is fixed to be used to pass the actual input data using this parameter.

Output for profile distances will be in `results/profile/results`.
