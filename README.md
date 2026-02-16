# String-remove-Occurence
import java.util.*;

public class RemoveARecursion {

    static String removeA(String s){
        if(s.length() == 0)
            return "";

        char ch = s.charAt(0);

        if(ch == 'a')
            return removeA(s.substring(1));
        else
            return ch + removeA(s.substring(1));
    }

    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        String s = sc.nextLine();
        System.out.println(removeA(s));
    }
}
