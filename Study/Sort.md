## STL sort
* default값은 오름차순

### 배열일 경우
```c++
int a[100];
// sort(배열의 포인터, 배열의 포인터 + 배열의 크기)
sort(a, a+100)
```

### vector일 경우
```c++
vector<int> a(100);
// sort(iterator의 begin(), iterator의 end())
sort(a.begin(), a.end());

sort(a.begin(), a.end(), greater<int>());   // 내림차순
sort(a.begin(), a.end(), less<int>());      // 오름차순 (default);
```

### 비교함수 이용
```c++
bool cmp(const pair<ll,ll> &a, const pair<ll,ll> &b) {
    if(a.second == b.second) {
        return a.first < b.first;
    }
    return a.second < b.second;
}
```

### 중복 제거
```c++
vector<int> a(100);
sort(a.begin(), b.begin());
a.erase(unique(a.begin(), a.end()), a.end());
```
```c++
unordered_set<int> s(nums.begin(), nums.end());
```

### pair
```c++
pair<int, int> p;
make_pair(1, 1);
```

### 최댓값, 최솟값
```c++
int nmin = *min_element(v.begin(), v.end());
int nmax = *max_element(v.begin(), v.end());
```