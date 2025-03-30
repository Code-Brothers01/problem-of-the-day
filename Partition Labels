class Solution {
public:
    vector<int> partitionLabels(string s) {
        vector<int>lastOccurences(26,0);
        for(int i = 0;i < s.size();i++){
            lastOccurences[s[i] - 'a'] = i;
        }
        int partitionEnd = 0;int partitionStart = 0;
        vector<int>result;
        for(int i = 0;i < s.size();i++){
            partitionEnd = max(partitionEnd,lastOccurences[s[i] - 'a']);
            if(i == partitionEnd){
                result.push_back(i - partitionStart + 1);
                partitionStart = i + 1;
            }
        }
        return result;
    }
};
