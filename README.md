# cod__12.03.2024
#include <iostream> 
#include <fstream> 
#include <string>   
#include <vector> 
#include <cstdlib>
#include <cmath>
#include <algorithm>
#include <iterator>
#include <list>
#include<random>
using namespace std;


void show(list<int>& _lst) 
{
    for (auto i : _lst)
    {
        cout << i << ' ';
    }
    cout << endl;
    //вывод 4 элемента списка
    auto lst_front = _lst.begin();
    advance(lst_front, 3);
    cout << *lst_front << '\n';
    //вывод предпоследнего элемента
    advance(lst_front, 99);
    cout << *lst_front << '\n';
    ///////////////////////////////

}


int main() {
    setlocale(LC_ALL, "ru");
    list<int> lst{};
    
    for(int i = 0; i < 101; i++)
    {
        int tmp_num = rand() % 200;
        lst.push_front(tmp_num);
    }
    lst.push_front(203);
    lst.push_front(202);
    lst.push_front(201);
    
    
    show(lst);

    
    return 0;
}
