This is an IUPRED2A result parser capable of parsing result files containing results for multiple sequence (as generated when providing IUPRED2A with a multi fasta file).



Showing the title and a array with the IUPRED scores, where index i will correspond to index i in the ammino acid sequence, for the first sequence:
```python3
>>> from iupred_parser import IUPREDParser
>>>
>>> for iupred_seq in IUPREDParser("iupred_result_file.result"):
...     print(iupred_seq.title)
...     print(iupred_seq.iupred_score)
...     break
...
ELMI001083|Q16821|seqslice=10-117|elmslice=50-57
[0.3053, 0.3286, 0.384, 0.3983, 0.3249, 0.2503, 0.3053, 0.346, 0.391, 0.433, 0.391, 0.4051, 0.3117, 0.3117, 0.3356, 0.4507, 0.4119, 0.3807, 0.4725, 0.4507, 0.4766, 0.5456, 0.5419, 0.5098, 0.5296, 0.6089, 0.7331, 0.6948, 0.6661, 0.6661, 0.6576, 0.6375, 0.5342, 0.5854, 0.5807, 0.5493, 0.5807, 0.712, 0.712, 0.6806, 0.6661, 0.6089, 0.6043, 0.5456, 0.5493, 0.4256, 0.4149, 0.4149, 0.4149, 0.3149, 0.3019, 0.1852, 0.2609, 0.268, 0.2817, 0.2609, 0.2002, 0.1583, 0.1852, 0.1092, 0.1137, 0.069, 0.038, 0.0463, 0.0424, 0.0543, 0.0985, 0.0985, 0.087, 0.0929, 0.1731, 0.0909, 0.1791, 0.1184, 0.1759, 0.2292, 0.2503, 0.2364, 0.1583, 0.1323, 0.2258, 0.2328, 0.3356, 0.3599, 0.2884, 0.2918, 0.2364, 0.2783, 0.2328, 0.1476, 0.1554, 0.1028, 0.2094, 0.1914, 0.2503, 0.2224, 0.2436, 0.2034, 0.247, 0.3392, 0.3286, 0.2988, 0.2364, 0.1731, 0.2503, 0.2988, 0.384]
```

Showing all the data availible for the first sequence:
```python3
>>> for iupred_seq in IUPREDParser("iupred_result_file.result"):
...     print(iupred_seq)
...     break
...
IUPREDSeq(title='ELMI001083|Q16821|seqslice=10-117|elmslice=50-57', pos=[1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, 29, 30, 31, 32, 33, 34, 35, 36, 37, 38, 39, 40, 41, 42, 43, 44, 45, 46, 47, 48, 49, 50, 51, 52, 53, 54, 55, 56, 57, 58, 59, 60, 61, 62, 63, 64, 65, 66, 67, 68, 69, 70, 71, 72, 73, 74, 75, 76, 77, 78, 79, 80, 81, 82, 83, 84, 85, 86, 87, 88, 89, 90, 91, 92, 93, 94, 95, 96, 97, 98, 99, 100, 101, 102, 103, 104, 105, 106, 107], amino_acid=['S', 'K', 'D', 'N', 'F', 'L', 'E', 'V', 'P', 'N', 'L', 'S', 'D', 'S', 'L', 'C', 'E', 'D', 'E', 'E', 'V', 'T', 'F', 'Q', 'P', 'G', 'F', 'S', 'P', 'Q', 'P', 'S', 'R', 'R', 'G', 'S', 'D', 'S', 'S', 'E', 'D', 'I', 'Y', 'L', 'D', 'T', 'P', 'S', 'S', 'G', 'T', 'R', 'R', 'V', 'S', 'F', 'A', 'D', 'S', 'F', 'G', 'F', 'N', 'L', 'V', 'S', 'V', 'K', 'E', 'F', 'D', 'C', 'W', 'E', 'L', 'P', 'S', 'A', 'S', 'T', 'T', 'F', 'D', 'L', 'G', 'T', 'D', 'I', 'F', 'H', 'T', 'E', 'E', 'Y', 'V', 'L', 'A', 'P', 'L', 'F', 'D', 'L', 'P', 'S', 'S', 'K', 'E'], iupred_score=[0.3053, 0.3286, 0.384, 0.3983, 0.3249, 0.2503, 0.3053, 0.346, 0.391, 0.433, 0.391, 0.4051, 0.3117, 0.3117, 0.3356, 0.4507, 0.4119, 0.3807, 0.4725, 0.4507, 0.4766, 0.5456, 0.5419, 0.5098, 0.5296, 0.6089, 0.7331, 0.6948, 0.6661, 0.6661, 0.6576, 0.6375, 0.5342, 0.5854, 0.5807, 0.5493, 0.5807, 0.712, 0.712, 0.6806, 0.6661, 0.6089, 0.6043, 0.5456, 0.5493, 0.4256, 0.4149, 0.4149, 0.4149, 0.3149, 0.3019, 0.1852, 0.2609, 0.268, 0.2817, 0.2609, 0.2002, 0.1583, 0.1852, 0.1092, 0.1137, 0.069, 0.038, 0.0463, 0.0424, 0.0543, 0.0985, 0.0985, 0.087, 0.0929, 0.1731, 0.0909, 0.1791, 0.1184, 0.1759, 0.2292, 0.2503, 0.2364, 0.1583, 0.1323, 0.2258, 0.2328, 0.3356, 0.3599, 0.2884, 0.2918, 0.2364, 0.2783, 0.2328, 0.1476, 0.1554, 0.1028, 0.2094, 0.1914, 0.2503, 0.2224, 0.2436, 0.2034, 0.247, 0.3392, 0.3286, 0.2988, 0.2364, 0.1731, 0.2503, 0.2988, 0.384], anchor_score=[0.4674, 0.477, 0.483, 0.4901, 0.4994, 0.5046, 0.5097, 0.5213, 0.5291, 0.5342, 0.5426, 0.5412, 0.5414, 0.5356, 0.532, 0.5167, 0.5071, 0.5013, 0.4956, 0.4904, 0.4859, 0.4758, 0.4702, 0.461, 0.4537, 0.4462, 0.4412, 0.4354, 0.4314, 0.4292, 0.429, 0.4298, 0.4325, 0.4314, 0.4285, 0.427, 0.4277, 0.4283, 0.4304, 0.4332, 0.4281, 0.4228, 0.4205, 0.4203, 0.425, 0.431, 0.4315, 0.4248, 0.4184, 0.4122, 0.4048, 0.3985, 0.395, 0.399, 0.4039, 0.4127, 0.42, 0.4232, 0.4273, 0.4326, 0.4281, 0.4231, 0.4198, 0.4153, 0.4175, 0.4211, 0.4256, 0.4307, 0.4283, 0.4288, 0.4294, 0.4196, 0.4084, 0.3964, 0.3798, 0.3604, 0.3428, 0.3303, 0.3198, 0.3067, 0.2972, 0.2943, 0.2966, 0.2967, 0.295, 0.2934, 0.2964, 0.3019, 0.3014, 0.2991, 0.3019, 0.3062, 0.3077, 0.3036, 0.3014, 0.2954, 0.2923, 0.2887, 0.2834, 0.277, 0.2725, 0.2612, 0.2568, 0.2502, 0.2476, 0.243, 0.243])
```