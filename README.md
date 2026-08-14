# I-ITFU

This article provides executables of software and datasets used in our research for Mining Incremental Temporal Fuzzy High Utility Patterns with Indexed List.

The executables include the software of I-ITFU, ITFUM, DTFU*, ILTFU-Miner*, and TFUN* and the datasets of Chess, Mushroom, Retail, Chainstore, and T10I4D200K—T10I4D1000K.

All executables were compiled to run on 64-bit architectures.

Please refer to the following guide:

1. Note that the name of the executable for each algorithm is as follows:

| Original Name   | I-ITFU | ITFUM | DTFU* | ILTFU-Miner* | TFUN* |
| --------------- | ------ | ----- | ----- | ------------ | ----- |
| Executable Name | I-ITFU | ITFUM | DTFU  | ILTFU-Miner  | TFUN  |

2. The parameters of the executables are as follows:

 for I-ITFU, ITFUM, DTFU, ILTFU-Miner
```bash
[0]          [1]            [2]                 [3]                     [4]                      [5]                           [6]
[Executable] [Threshold(%)] [Utility Data Path] [Transaction Data Path] [Original Data Ratio(%)] [Total Number of Stream Data] [Out File Path]

```

 for TFUN
```bash
[0]          [1]            [2]                   [3]                 [4]                     [5]                      [6]                           [7]
[Executable] [Threshold(%)] [Uncertain Data Path] [Utility Data Path] [Transaction Data Path] [Original Data Ratio(%)] [Total Number of Stream Data] [Out File Path]

```

3. Next, the file name and the parameters of each dataset are as follows:

| Dataset     | Number of Transactions | Number of Items | \|T\|.avg |
| ----------- | ---------------------- | --------------- | --------- |
| Chess       | 3,196                  | 75              | 37        |
| Mushroom    | 8,124                  | 120             | 23        |
| Retail      | 88,162                 | 16,469          | 10.3      |
| Chainstore  | 1,112,949              | 46,086          | 7.2       |
| T10I4DxK    | 200,000-1,000,000      | 1,000           | 10        |

4. For example
```bash
I-ITFU 0.5 ..\Data\utilMushroom.txt ..\Data\mushroom.txt 80 4 out\out.txt
```
will run I-ITFU on mushroom, with the threshold set at 0.5%
```bash
TFUN 0.5 "..\Data\mushroom(unc).txt" ..\Data\utilMushroom.txt ..\Data\mushroom.txt 80 4 out\out.txt
```
will run I-ITFU on mushroom, with the threshold set at 0.5%

5. The output directory "/out" is required for writing result patterns for all algorithms.