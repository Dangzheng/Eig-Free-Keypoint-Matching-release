# This is the part of the code about keypoint matching.
Unfortunately we lost the original dumped dataset, and only keep the way to generate the dataset. And for the reason that the old code is hard to trace, we reproduce the code according to the paper in the new version of tensorflow (1.12.0) recently. So the result inevitably be different with the result reported in the paper. Some of them are higher, some of them are lower. But very close to the paper.

# usage

`--data_tr`, `--data_va` and `--data_te` control the dataset for training, validation and testing.

We trained the model on the dataset `brown_bm_3_05`, if you want to test on the dataset `herzjesu`, just run the following line

```
python main.py --run_mode="test" --data_te="herzjesu"
```

dumping dataset uses 

```
python dump_data.py --data_tr=`brown_bm_3_05` --data_te=`brown_bm_3_05` --data_te=`brown_bm_3_05`
```

using my trained model to test the dataset `herzjesu`

```
python main.py --log_dir="mytrain" --data_te=`herzjesu`
```

If you encounter any path problem, I believe you guys could fix them.