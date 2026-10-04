# -SUM-OF-TWO-NUMBES
nums = {2, 7, 11, 15} and target = 9, the output is [0, 1], because 2 + 7 = 9.
/**
 * Note: The returned array must be malloced, assume caller calls free().
 */
int* twoSum(int* nums, int numsSize, int target, int* returnSize) {
    int*result=(int*)malloc(2*sizeof(int));
    *returnSize=2;

    for(int i=0;i<numsSize;i++){
        for(int j=i+1;j<numsSize;j++){
            if(nums[i]+nums[j]== target){
                result[0]=i;
                result[1]=j;
                return result;
            }
        }
    }
  return result;  
}
