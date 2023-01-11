# Delete-Columns-to-Make-Sorted
Delete Columns to Make Sorted

class Solution {
    public int minDeletionSize(String[] strs) {
        int rsize = strs.length;
        int csize = strs[0].length();
        if(rsize == 1){
            return 0;
        }

        int ans = 0;
        for(int i=0; i<csize; i++){
            for(int j=1; j<rsize; j++){
                if(strs[j].charAt(i) < strs[j-1].charAt(i)){
                    ans++;
                    break;
                }
            }
        }

        return ans;
    }
}

