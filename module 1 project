#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
#include <unordered_map>
using namespace std;


int main() {
   int N,T;
    cin>>N;
    unordered_map<int,int>idbalances;
     for(int i=0;i<N;i++)
    {
        int userID,balance;
        cin>>userID>>balance;
        idbalances[userID]=balance;
    }
    cin>>T;
    while(T--){
        int from_userID,to_userID,amount;
        cin>>from_userID>>to_userID>>amount;
    if (idbalances[from_userID]>=amount)
    {
        idbalances[from_userID]-=amount;
        idbalances[to_userID]+=amount;
        cout<<"Success"<<'\n';
        }
        else
        {
            cout<<"Failure"<<'\n';
        }
    }   
vector<pair<int, int>> final;
    for (auto p:idbalances)
        {
        final.push_back({p.first,p.second});
            }
    sort(final.begin(), final.end(), [](const std::pair<int, int>& a, const std::pair<int, int>& b) {
if (a.second==b.second)
    {
    return a.first < b.first;
    }
        return a.second < b.second;
});
cout<<endl;
for(const auto&p:final)
    {
    cout<<p.first<<" "<<p.second<<'\n';
     }
}
