# bloomfilter
Pure python implementation of Bloom Filter. It comes in two flavors as BitBloomFilter and IntBloomFilter.

BitBloomFilter uses single bit for storing hashes. IntBloomFilter can store virtually unlimited hashes per each entry in BloomFilter, and it is more appropriate for adding and removing entries from bloom filter.

Neither, BitBloomFilter nor IntBloomFilter dynamically resize.

# Example
```python
from bloomfilter import BitBloomFilter
bf = BitBloomFilter()
bf.add(1)
print(bf.has(1)) # True
print(bf.remove(1))
print(bf.has(1)) # False
```

# Testing
```bash
$ python -m unittest -v test_bloomfilter
```
