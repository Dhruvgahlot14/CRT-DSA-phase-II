class Solution {
public:
    vector<vector<int>> zigzagLevelOrder(TreeNode* root) {
        vector<vector<int>>ans;
        if(root==NULL)
        {
            return ans;
        }
        queue<TreeNode*>q;
        q.push(root);
        int f=0;
        while(!q.empty())
        {
            vector<int>v;
            int n=q.size();
            while(n--)
            {
                TreeNode*front=q.front();
                q.pop();
                v.push_back(front->val);
                if(front->left)
                {
                    q.push(front->left);
                }
                if(front->right)
                {
                    q.push(front->right);
                }
            }
            if(f==0)
            {
                ans.push_back(v);
                f=1;
            }
            else
            {
                reverse(v.begin(),v.end());
                ans.push_back(v);
                f=0;
            }
        }
        return ans;
    }
};
