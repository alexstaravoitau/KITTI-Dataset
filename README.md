# KITTI Dataset Exploration

## Dependencies

Apart from the common dependencies like `numpy` and `matplotlib` notebook requires [`pykitti`](https://github.com/utiasSTARS/pykitti). You can install `pykitti` via pip using:

```
pip install pykitti
```

## Project structure

| File                   | Description                                                                                      |
| ---------------------- | ------------------------------------------------------------------------------------------------ |
| `kitti-dataset.ipynb`  | Jupyter Notebook with dataset visualisation routines and output.                                 |
| `parseTrackletXML.py`  | Methods for parsing tracklets (e.g. dataset labels), originally created by Christian Herdtweck.  |
| `utilities.py`         | Convenient logging routines.                                                                     |

## Dataset

I have used one of the raw datasets available on [KITTI website](http://www.cvlibs.net/datasets/kitti/raw_data.php). See the first one in the list: [2011_09_26_drive_0001 (0.4 GB)](http://kitti.is.tue.mpg.de/kitti/raw_data/2011_09_26_drive_0001/2011_09_26_drive_0001_sync.zip).

* **Length**: 114 frames (00:11 minutes)
* **Image resolution**: `1392 x 512` pixels
* **Labels**: 12 Cars, 0 Vans, 0 Trucks, 0 Pedestrians, 0 Sitters, 2 Cyclists, 1 Trams, 0 Misc

I mainly focused on point cloud data and plotting labeled tracklets for visualisation. Cars are marked in **blue**, trams in **red** and cyclists in **green**.

<p align="center">
  <img src="pcl_data.gif" alt="Point cloud data with labels"/>
</p>

For a more in-depth exploration and implementation details [see notebook](kitti-dataset.ipynb).
