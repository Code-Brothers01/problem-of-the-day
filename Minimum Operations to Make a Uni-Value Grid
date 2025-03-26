class Solution {
public:
    int minOperations(vector<vector<int>>& grid, int x) {
        int result = 0;
        vector<int>arr;
        for(int row = 0;row < grid.size();row++){
            for(int col = 0;col < grid[0].size();col++){
                arr.push_back(grid[row][col]);
            }
        }
        int len = arr.size();
        nth_element(arr.begin(),arr.begin() + len/2,arr.end());
        int median = arr[len/2];
        for(int num : arr){
            if(num % x != median % x) return -1;
            result += abs(median - num)/x;
        }
        return result;
    }
};
