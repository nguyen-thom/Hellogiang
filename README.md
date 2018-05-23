# Hellogiang
MaHoa
public class BT {
	private static String encode(String origin ,int k) {
	    char[] toEncode = origin.toCharArray();
	    for (int i = 0; i < toEncode.length; i++) {
	        if (Character.isLetter(toEncode[i])) {
	        	int index=i-k;
	        	if(index<0) {
	        		index=toEncode[i]+25;
	        	}
	        	if(index>26) {
	        		index=toEncode[i]-26;
	        	}
	        	toEncode[i] -= k;
//	        	toEncode[i] = (char) ((toEncode[i]- 3 - (int)'A') % 26 + (int)'a');
	        }
	    }
	    origin= String.valueOf(toEncode);
	    return origin ;
	}
	public static void main(String[] args) {
		String s="123WKRQJWLQB";
		System.out.println(encode(s,3));
		String str="124abcxyz";
		int K=2;
		String res=encode(str, K);
		System.out.println(res);
	}
