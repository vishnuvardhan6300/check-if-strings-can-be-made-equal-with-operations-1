# check-if-strings-can-be-made-equal-with-operations-1
leetcode problem No:2839

import java.util.*;

class Solution {
    public boolean canBeEqual(String s1, String s2) {
        char[] even1 = {s1.charAt(0), s1.charAt(2)};
        char[] odd1  = {s1.charAt(1), s1.charAt(3)};
        
        char[] even2 = {s2.charAt(0), s2.charAt(2)};
        char[] odd2  = {s2.charAt(1), s2.charAt(3)};
        
        Arrays.sort(even1);
        Arrays.sort(odd1);
        Arrays.sort(even2);
        Arrays.sort(odd2);
        
        return Arrays.equals(even1, even2) && Arrays.equals(odd1, odd2);
    }
}