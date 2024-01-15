# Bitwise-XOR-of-subarrays

def xor_of_subarrays(n, arr):
    result = 0

    for i in range(n):
        prefix_xor = 0
        for j in range(i, n):
            prefix_xor ^= arr[j]
            result ^= prefix_xor

    return result

# Input reading
n = int(input())
arr = list(map(int, input().split()))

# Output
output = xor_of_subarrays(n, arr)
print(output)
