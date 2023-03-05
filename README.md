# top-k
  public:
    vector<int> topK(vector<int>& nums, int k) {
        // Code here
       map<int,int>mp;
       for(int i=0;i<nums.size();i++)
       {
           mp[nums[i]]++;
       }
       vector<pair<int,int>>vect;
       for( auto i:mp)
       {
           vect.push_back(make_pair(i.second,i.first));
           
       }
       sort(vect.begin(),vect.end());
       reverse(vect.begin(),vect.end());
        int i=0;
       vector<int>v;
      while(i<k)
      {
       v.push_back(vect[i].second);
       i++;
      }
       return v;
    
    }
    
   
};
