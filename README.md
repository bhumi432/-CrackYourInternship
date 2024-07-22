# -CrackYourInternship
solving DSA questions 45 days challenge
question 1
class Solution {
public:
    int findDuplicate(vector<int>& nums) {
        unordered_map<int,int>mp;
        for(int i=0;i<nums.size();i++){
            mp[nums[i]]++;
        }
        for(auto j:mp){
            if(j.second>1){
                return j.first;
            }
        }
        return -1;
    }
};
