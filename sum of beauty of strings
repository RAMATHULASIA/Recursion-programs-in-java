class Solution {
    public int beautySum(String s) {
        int result = 0;
        // Iterate over all possible starting points of substrings
        for (int i = 0; i < s.length(); i++) {
            int[] freq = new int[26]; // Frequency map for 'a' to 'z'
            int maxFreq = 0;          // Track max frequency in the current substring
            // Expand the substring by moving the end pointer
            for (int j = i; j < s.length(); j++) {
                int charIndex = s.charAt(j) - 'a';
                freq[charIndex]++;
                // Update max frequency
                maxFreq = Math.max(maxFreq, freq[charIndex]);
                // Find the min frequency in the current substring
                int minFreq = Integer.MAX_VALUE;
                for (int k = 0; k < 26; k++) {
                    if (freq[k] > 0) {
                        minFreq = Math.min(minFreq, freq[k]);
                    }
                }
                // Add the beauty of the current substring
                result += (maxFreq - minFreq);
            }
        }
        return result;
    }
}
