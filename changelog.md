# CHANGELOG.md

## odw-2021 (unreleased)

Features:

  - Updated verison of [igwn-py37](https://computing.docs.ligo.org/conda/environments/igwn-py37/) integrated in `environment.yml`. This is the dependency file of mybinder.org -> [Francesco](https://github.com/gw-odw/odw-2021/blob/master/environment.yml)
  - Updated verison of [igwn-py37](https://computing.docs.ligo.org/conda/environments/igwn-py37/) integrated in `igwn-py37-osx.yaml` -> [Francesco](https://github.com/gw-odw/odw-2021/blob/master/igwn-py37-osx.yaml)
  - tested new packages versions in `Google co-labs` -> [Nunzio](https://colab.research.google.com/)
  - updated `setup.md` 2021 -> [Nunzio](https://github.com/gw-odw/odw-2021/blob/setup_b/setup.md)
  - `mybinder.org` running properly with updated environment-> [Francesco](https://mybinder.org/v2/gh/gw-odw/odw-2021/master)
    - This should be the preferred method (besides direct installation) because it builds a container with the correct conda environment;
    - It is limited to 100 simultaneous participants to the same github repo: I have contacted the developers for an extension to the quota limit;
  - [igwn-py37](https://computing.docs.ligo.org/conda/environments/igwn-py37/) conda environment configured on both Linux and macOS (virtual machine) ->[Francesco](https://conda.io/projects/conda/en/latest/user-guide/install/)
    - For LVC participants: this environment is already available in other IGWN computing center.
  
Fix:

  - warn on tutorial [2.2](https://colab.research.google.com/github/gw-odw/odw-2020/blob/master/Day_2/Tuto_2.2_Matched_Filtering_In_action.ipynb) and [2.3](https://colab.research.google.com/github/gw-odw/odw-2020/blob/master/Day_2/Tuto_2.3_Signal_consistency_and_significance.ipynb) 2020 -> in `pycbc.psd.investigate_spectrum_truncation`, `max_filter_len` must be an integer 
  - warn -> import `bilby` [2.5](https://colab.research.google.com/github/gw-odw/odw-2020/blob/master/Day_2/Tuto_2.5_Parameter_estimation_for_compact_object_mergers.ipynb) 2020
