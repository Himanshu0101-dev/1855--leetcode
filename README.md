# 1855--leetcode
Maximum Distance Between a Pair of Values




class Solution:
    def maxDistance(self, nums1, nums2):
        i, j = 0, 0
        maxDist = 0
        n, m = len(nums1), len(nums2)
        
        while i < n and j < m:
            if nums1[i] <= nums2[j]:
                maxDist = max(maxDist, j - i)
                j += 1
            else:
                i += 1
        
        return maxDist
