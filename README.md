# buddy-allocator

This is a simple buddy system allocation scheme.
All of the metadata about the memory chunk (e.g., its size and whether it's currently being used) is stored at the beginning of that block of memory.
You can initialize it by calling `create_buddy_table()` and passing in the desired power of two.
For example, passing in 16 will create a buddy system of 2^16 = 65,536 bytes.
If it returns `NULL` then the buddy system was unable to allocate enough memory.
