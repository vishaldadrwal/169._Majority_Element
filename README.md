# 169._Majority_Element
# Given an array nums of size n, return the majority element.  The majority element is the element that appears more than ⌊n / 2⌋ times. You may assume that the majority element always exists in the array.
# The brute force approach.
# Time Complexity: O(n²) - nested loops
# Space Complexity: O(1) - no extra space used
class Solution {
public:
    int majorityElement(vector<int>& nums) {
        int n=nums.size();
        for(int i=0;i<n;i++){
            int count=0;
            for(int j=0;j<n;j++){
                if(nums[i]==nums[j]){
                    count++;
                    }
                }
            if(count>(n/2)){
                return nums[i];
            }
        }
        return -1;
    }
};
