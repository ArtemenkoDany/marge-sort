#include <iostream>
#include <vector>
using namespace std;

vector<float> vec;
vector<float> aux;

void merge(int first, int mid, int last)
{
    for(int l = first, r = mid, i = first; i <= last; i++)
    {
        if (r > last)
             aux.at(i) = vec.at(l++);
        else if (l == mid)
            aux.at(i) = vec.at(r++);
            else
            {
        if (vec.at(l) >= vec.at(r))
            aux.at(i) = vec.at(r++);
        else
            aux.at(i) = vec.at(l++);
            }
    }
    for(int x = first; x<= last; x++)
    {
        vec.at(x) = aux.at(x);
    }
}

void merge_sort(int first, int last){  //рекурсивная функция
    if (first == last)
        return;
    
    int mid = (first+last)/2+1;
    merge_sort(first, mid-1);
    merge_sort(mid, last);
    merge(first, mid, last);
}


int main()
{
    int z;
    cin >> z;
    
    for(int x = 0; x < z; x++)
    {
        int t;
        cin >> t;
        vec.push_back(t);
    }
    aux.resize(vec.size());
    merge_sort(0, z-1);
   
    cout << endl;
    for(int x = 0; x < z; x++)
    {
    cout << vec.at(x) << " ";
    }
    cout << endl;
    return 0;
}



void funk()
{
    for(int i=1; i <= vec.size(); i*=2)
        for(int k(0); k < vec.size()-i; k+=i*2)
            merge(k, k+i, k+i*2>vec.size()-2 ? vec.size()-1 :k+i*2);
}
