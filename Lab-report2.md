```
import java.io.IOException;
import java.net.URI;
import java.io.*;
import java.util.*;

class Handler implements URLHandler {
    // The one bit of state on the server: a number that will be manipulated by
    // various requests.
    int num = 0;
    ArrayList<String> listw = new ArrayList<String>();
    ArrayList<String> endlist = new ArrayList<String>();

    public String handleRequest(URI url) {
        String[] parameters = url.getQuery().split("=");
        if (url.getPath().contains("/add")) {
            listw.add(parameters[1]);
            System.out.println(listw.size());
        } 
        if (url.getPath().contains("/search")){
            for(int i = 0; i < listw.size(); i++){
                String word = listw.get(i);
                if(word.contains(parameters[1])){
                    endlist.add(word);
                }
            }
            String str = String.join(",", endlist);
		    System.out.println(str);
            return str;
        }
        return parameters[1];
    }
}

class SearchEngine2 {
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        int port = Integer.parseInt(args[0]);

        Server.start(port, new Handler());
    }
}
```

Above is my code for a Simple Search Engine which will remember the all the searches with "/add". Once they search with "search=..." then it will look through the array of search history and take all the searches containing the term ... and return it. 
Example: "search=wit" ... is wit. 



![image](https://github.com/JamieWei21/cse15l-lab-reports/blob/main/Example3-%20Lab2.PNG)



![image](https://github.com/JamieWei21/cse15l-lab-reports/blob/main/Example1-%20Lab2.PNG)





![image](https://github.com/JamieWei21/cse15l-lab-reports/blob/main/Example4-%20Lab2.PNG)
