#include <bits/stdc++.h>
using namespace std;
#define Yalla_Benna ios_base::sync_with_stdio(0),cin.tie(0),cout.tie(0);
#define el cout << '\n'
#define int long long
#define ull unsigned long long
#define yes cout << "YES"
#define no cout << "NO"
#define print cout <<
#define Bye_Mn8er_Salam return 0;
#define test while(TC--)
#define loop1(n) for(int i=1;i<=n;i++)
#define loop0(n) for(int i=0;i<n;i++)
#define pq priority_queue
#define all(ar) ar.begin(),ar.end()
#define Wlk_Rooooo7 return
                                // tic-tac-toe game
signed main() {
    again:
    // 0 empty , 1 --> x , 2 --> o 
    int grid[100][100];

    int n;
    cout<<"Enter grid dimension: ";
    cin>>n;
    
    int rs[100], cs[100], dr[100], dc[100];

    int verify = 0;

    // Add row n position 
    for(int r = 0; r < n; ++r)
        rs[verify] = r, cs[verify] = 0, dr[verify] = 0, dc[verify++] = 1;
    
    // Add column n position
    for(int c = 0; c < n; ++c)
        rs[verify] = 0, cs[verify] = c, dr[verify] = 1, dc[verify++] = 0;
    
    // Add diagonal position
    rs[verify] = 0, cs[verify] = 0, dr[verify] = 1, dc[verify++] = 1;
    
    // Add anti-diagonal position
    rs[verify] = 0, cs[verify] = n - 1, dr[verify] = 1, dc[verify++] = -1;
    
    int turn = 0;
    int steps = 0;

    while(true){
        if(steps == n*n){
            cout<<"Tie\n";
            break;
        }
        char symbol = 'x';
        if(turn == 1)
            symbol = 'o';
        cout<<"Player "<<symbol<<" turn. Enter empty location (r, c): ";
        int r, c;
        cin>>r>>c;

        r--, c--;
        if(r < 0 || r >= n || c < 0 || c >= n || grid[r][c] != 0){
            cout<<"Invalid input. Try again\n";
			continue;
        }
        grid[r][c] = turn + 1;
        
        // print the grid 
        for(int r = 0; r < n; ++r){
            for(int c = 0; c < n; ++c){
                char ch = '.';
                if(grid[r][c] == 1)
                    ch = 'x';
                if(grid[r][c] == 2)
                    ch='o';
                    
                cout<<ch<< " ";
            }   
            el; 
        }

        // check win status
        for(int check = 0; check < verify; ++check){
            int r = rs[check], c = cs[check], rd = dr[check], cd = dc[check];
            int count = 0, first = grid[r][c];

            if (first == 0)
				continue;

            for(int step = 0; step < n; ++step, r += rd, c += cd)
                count += grid[r][c] == first;
                
            if (count == n) {
				cout<<"Player "<< symbol<<" won\n";
				goto if_want;
			}
        }
        turn = !turn; // 0 be 1 , 1 be 0
        steps++;
    }
    if_want:
    char is_want;
    cout<<"You want to play again ? (y/n) ";
    cin>>is_want;

    if(is_want == 'y')
        goto again;

    Bye_Mn8er_Salam;
}
                                        // By AbdEl-Rahman Hamouda.
