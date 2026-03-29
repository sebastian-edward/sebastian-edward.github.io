---
layout: post
title: LSM-tree vs B-tree
---

### LSM-tree
LSM(log-structured and merge)-tree is an efficient database engine which is suitable for high write situation. When user write data, it's stored in memory at first. This can be very efficient and
these data can be sorted in a short time. The data structure used in memory is often called memtable. After the data reach some threshhold, these data will be appended to disk. The process act like
we appending data to log file. These data is appended at the end of one segment sequencially. Sence we don't need to maintain any fixed structure like B-tree, this process could be finished very
quickly. These segment is called SSTable.
LSM-tree will do another thing to make it more wonderful. It will finish the compaction and merge process at the background. This process will use several recently used segment and merge them like the merge sort algorithm. At the same time, LSM-tree will delete the duplicated record and keep the most recently appended value of each key. That will make the segment smaller. This process can also avoid page segmentation.
When deleting data, LSM-tree will not delete the key value pair directly. It will append a mark record to segment. Then while merging the data, the values whose key is marked will be deleted.
But if we want to read, LSM-tree can be hard to perform. It need to scan the segments to find the right data. That would generate many I/Os.
