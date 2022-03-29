# ros2-useful-scripts

## Supported Feature

- [x] rosbag2 compression
- [ ] rosbag2_record.sh
- [ ] ros2_check_topic_values.sh

## scripts/rosbag2_compress.sh

Compress rosbag2 and put together for uploads

- Command
  - Be careful for last / in directory path.

```
./scripts/rosbag2_compress.sh {thread} {directory path}
# example
# ./scripts/rosbag2_compress.sh 12 ~/Downloads/rosbag/

```


- input

```
.
├── rosbag
│  ├── rosbag2_2022_01_09-13_49_29
│  │  ├── metadata.yaml
│  │  └── rosbag2_2022_01_09-13_49_29_0.db3
│  ├── rosbag2_2022_02_05-00_54_33
│  │  ├── metadata.yaml
│  │  └── rosbag2_2022_02_05-00_54_33_0.db3
```

- output

```

├── rosbag
│  ├── rosbag2_2022_01_09-13_49_29
│  │  ├── metadata.yaml
│  │  └── rosbag2_2022_01_09-13_49_29_0.db3
│  ├── rosbag2_2022_02_05-00_54_33
│  │  ├── metadata.yaml
│  │  └── rosbag2_2022_02_05-00_54_33_0.db3
│  └── zst
│     ├── rosbag2_2022_01_09-13_49_29_0.db3.zst
│     └── rosbag2_2022_02_05-00_54_33_0.db3.zst
```

