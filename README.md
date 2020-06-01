"# LeetCodeJuneChallenge" 
"# LeetCodeJuneChallenge" 
"# Day1 june challenge" 

/**
 * Definition for a binary tree node.
 * struct TreeNode {
 *     int val;
 *     TreeNode *left;
 *     TreeNode *right;
 *     TreeNode() : val(0), left(nullptr), right(nullptr) {}
 *     TreeNode(int x) : val(x), left(nullptr), right(nullptr) {}
 *     TreeNode(int x, TreeNode *left, TreeNode *right) : val(x), left(left), right(right) {}
 * };
 */
class Solution {
public:
    TreeNode* invertTree(TreeNode* root) {
        if(!root)
    {
        return NULL;
    }
    
    TreeNode* temp=new TreeNode(0);
    TreeNode* x=invertTree(root->left);
    TreeNode* y=invertTree(root->right);
    
    temp=root->left;
    root->left=root->right;
    root->right=temp;
    return root;
        
    }
};
