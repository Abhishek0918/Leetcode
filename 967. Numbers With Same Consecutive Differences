C++





class Solution {
public:

    void solve(int depth, int num, int N, int K, vector<int> &ans) {
        if (depth == 0) {
            ans.push_back(num);
            return;
        }

        if (depth == N) {
            for (int i = 1; i <= 9; i++)
                solve(depth - 1, i, N, K, ans);
            if (N == 1)
                solve(depth - 1, 0, N, K, ans);
        }

        else {
            int last = num % 10;

            if (last + K <= 9)
                solve(depth - 1, num * 10 + last + K, N, K, ans);

            if (K != 0 && last - K >= 0)
                solve(depth - 1, num * 10 + last - K, N, K, ans);
        }

    }

    vector<int> numsSameConsecDiff(int N, int K) {
        vector<int> ans;
        solve(N, 0, N, K, ans);

        return ans;
    }
};
