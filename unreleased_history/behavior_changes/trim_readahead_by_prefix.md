*  Trim readahead_size during scans so data blocks containing keys that are not in the same prefix as the seek key in `Seek()` are not prefetched when `ReadOptions::auto_readahead_size=true` (default value) and `ReadOptions::prefix_same_as_start = true`