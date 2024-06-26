# unit-6-java-answer

72.1.1

package q911391;
import java.util.*;

public class SimpleArrayListDemo {
    public static void main(String[] args) {
        List<String> namesList = new ArrayList<String>();
        namesList.add("Hyderabad");
        namesList.add("Bangalore"); // Corrected spelling
        namesList.add("Chennai");
        
        for (String name : namesList) { // Corrected the syntax for iterating over the list
            System.out.println(name.substring(0, 3));
            // Print the String up to 3 characters using substring method
        }
    }
}




package q11367;

import java.util.*;

public class ArrayListDemo {

    public static void main(String[] args) {
        List aList = new ArrayList();

        System.out.println("aList.size() = " + aList.size());
        System.out.println("aList = " + aList);

        aList.add("First Entry");
        aList.add("Second Entry");

        System.out.println("aList.size() = " + aList.size());
        System.out.println("aList = " + aList);

        List bList = new ArrayList(aList);
        System.out.println("bList.size() = " + bList.size());
        System.out.println("bList = " + bList);

        List<String> cList = new ArrayList<>(20);
        System.out.println("cList.size() = " + cList.size());
        System.out.println("cList = " + cList);
    }
}





package q35988;

import java.util.*;

public class ArrayListIterationDemo {

    public static void main(String[] args) {

        List namesList = new ArrayList();

        for (String argument : args) {
            if (argument.length() >= 9 && Character.isUpperCase(argument.charAt(8))) {
                namesList.add(argument);
            }
        }

        for (String name : namesList) {
            System.out.println(name);
        }

        for (int i = 0; i < namesList.size(); i++) {
            System.out.println("Name at index " + i + " is: " + namesList.get(i));
        }
    }
}


73.1.3


package q11955;

import java.util.*;

public class ArrayListIterationDemo {

    public static void main(String[] args) {

        List<String> namesList = new ArrayList<String>();

        for (String x : args) {
            if (Character.isUpperCase(x.charAt(0))) {
                namesList.add(x);
            }
        }

        for (Object name : namesList) {
            System.out.println(name); // print elements in the namesList
        }
    }
}




73.1.4

package q23673;

import java.util.ArrayList;

public class ArrayListIterationDemo {

    public static void main(String[] args) {
        ArrayList<String> arr = new ArrayList<>();

        for (String arg : args) {
            arr.add(arg);
        }

        for (int i = 0; i < arr.size(); i++) {
            System.out.println("Name at index " + i + " is: " + arr.get(i));
        }
    }
}

73.1.5

package q23676;

import java.util.ArrayList;

public class ArrayListIterationDemo {

    public static void main(String[] args) {
        ArrayList<String> arr = new ArrayList<>();

        for (String x : args) {
            arr.add(x);
        }


            System.out.println("Name at index 2 is: " + arr.get(2));

        }    
}


73.1.6

package q24085;

import java.util.ArrayList;
import java.util.List;

public class ArrayListIterationDemo {

    public static void main(String[] args) {
        List<String> namesList = new ArrayList<>();

        for (String arg : args) {
            namesList.add(arg);
        }

        System.out.println(namesList);
        System.out.println("Size of the list is: " + namesList.size());
    }
}

73.1.7

package q35985;

import java.util.*;

public class ArrayListMethodsDemo {

    public static void main(String[] args) {

        List alist = new ArrayList(args.length);

        for (String argument : args) {
            alist.add(argument);
        }

        System.out.println("aList = " + alist);
        System.out.println("aList.size() = " + alist.size());
        System.out.println("removedElement = " + alist.get(3));
        alist.remove(3);
        System.out.println("aList = " + alist);
        alist.set(0, "Steve Jobs");
        System.out.println("alist = " + alist);
        alist.add(0, "Bill Gates");
        System.out.println("alist = " + alist);
    }
}


74.1.1

package q36170;

import java.util.*;

public class TreeSetDemo {

    public static void main(String[] args) {

        Set<String> namesSet = new TreeSet<>();

        Scanner scanner = new Scanner(System.in);

        String str1 = scanner.nextLine();
        namesSet.add(str1);

        String str2 = scanner.nextLine();
        namesSet.add(str2);

        namesSet.add("Budha");

        System.out.println("namesSet = " + namesSet);

        namesSet.add("Budha");

        System.out.println("namesSet = " + namesSet);

        namesSet.remove(str2);

        System.out.println("namesSet = " + namesSet);

        scanner.close();
    }
}

74.1.2

package q37263;

import java.util.*;

public class TreeSetDemo {

    public static void main(String[] args) {

        Set<String> namesSet = new TreeSet<>();

        Scanner scanner = new Scanner(System.in);

        String str;

        for (int i = 0; i < 3; i++) {
            str = scanner.nextLine();
            namesSet.add(str);
        }

        System.out.println("namesSet = " + namesSet);

        str = scanner.nextLine();
        namesSet.add(str);

        System.out.println("namesSet = " + namesSet);

        for (int i = 0; i < 2; i++) {
            str = scanner.nextLine();
            namesSet.remove(str);
        }

        System.out.println("namesSet = " + namesSet);

        scanner.close();
    }
}

75.1.1

package q37264;

import java.util.*;

public class HashMapDemo {

    public static void main(String[] args) {

        Scanner scanner = new Scanner(System.in);

        HashMap<String, String> aMap = new HashMap<>();

        System.out.println("aMap.size() = " + aMap.size());
        System.out.println("aMap = " + aMap);

        String key1, value1;
        key1 = scanner.nextLine();
        value1 = scanner.nextLine();

        String key2, value2;
        key2 = scanner.nextLine();
        value2 = scanner.nextLine();

        String key3, value3;
        key3 = scanner.nextLine();
        value3 = scanner.nextLine();

        String key4, value4;
        key4 = scanner.nextLine();
        value4 = scanner.nextLine();

        aMap.put(key1, value1);
        aMap.put(key2, value2);
        aMap.put(key3, value3);
        aMap.put(key4, value4);

        System.out.println("aMap.size() = " + aMap.size());
        System.out.println("aMap = " + aMap);

        HashMap<String, String> bMap = new HashMap<>(aMap);

        System.out.println("bMap.size() = " + bMap.size());
        System.out.println("bMap = " + bMap);

        HashMap<String, String> cMap = new HashMap<>(20);

        System.out.println("cMap.size() = " + cMap.size());
        System.out.println("cMap = " + cMap);

        scanner.close();
    }
}

75.1.2

package q37267;

import java.util.*;

public class HashMapPutMethodDemo {

    public static void main(String[] args) {

        Map<String, String> namesMap = new HashMap<>();

        Scanner input = new Scanner(System.in);

        // read two strings representing key1 and value1
        String key1, value1;
        key1 = input.nextLine();
        value1 = input.nextLine();
        namesMap.put(key1, value1);

        // read two strings representing key2 and value2
        String key2, value2;
        key2 = input.nextLine();
        value2 = input.nextLine();
        namesMap.put(key2, value2);

        // read two strings representing key3 and value3
        String key3, value3;
        key3 = input.nextLine();
        value3 = input.nextLine();
        namesMap.put(key3, value3);

        // print namesMap
        System.out.println("namesMap = " + namesMap);

        input.close(); // Closing the Scanner object to prevent resource leak
    }
}

75.1.3


package q37268;

import java.util.*;

public class HashMapGetMethodDemo {

    public static void main(String[] args) {

        Map<String, String> namesMap = new HashMap<>();

        Scanner input = new Scanner(System.in);

        namesMap.put("Sun", "Sunday");
        namesMap.put("Mon", "Monday");
        namesMap.put("Tue", "Tuesday");
        namesMap.put("Thu", "Thursday");

        System.out.println("namesMap " + namesMap);

        System.out.println("Enter key to get value: ");
        String key = input.nextLine();

        String result = namesMap.get(key);

        System.out.println("Value mapped to Tue is: " + result);

        input.close();
    }
}

75.1.4

package q37266;

import java.util.*;

public class HashMapMethodsDemo {

    public static void main(String[] args) {

        Map<String, String> namesMap = new HashMap<>();

        Scanner input = new Scanner(System.in);

        String key1, value1;
        key1 = input.nextLine();
        value1 = input.nextLine();
        namesMap.put(key1, value1);

        String key2, value2;
        key2 = input.nextLine();
        value2 = input.nextLine();
        namesMap.put(key2, value2);

        String key3, value3;
        key3 = input.nextLine();
        value3 = input.nextLine();
        namesMap.put(key3, value3);

        System.out.println("namesMap = " + namesMap);

        System.out.println("Value mapped to " + key2 + " is: " + namesMap.get(key2));

        System.out.println("Enter value to change for " + key2 + ": ");
        String x = input.nextLine();
        namesMap.put(key2, x);

        System.out.println("namesMap = " + namesMap);

        System.out.println("New value mapped to " + key2 + " is: " + namesMap.get(key2));

        System.out.println("namesMap.size() = " + namesMap.size());

        input.close(); 
    }
}


75.1.5



package q37269;

import java.util.*;

public class CharcountDemo {

    public static void main(String[] args) {

        HashMap<Character, Integer> namesMap = new HashMap<>();

        Scanner scanner = new Scanner(System.in);

        String str = scanner.nextLine();

        for (int i = 0; i < str.length(); i++) {
            char c = str.charAt(i);
            if (namesMap.containsKey(c)) {
                namesMap.put(c, namesMap.get(c) + 1);
            } else {
                namesMap.put(c, 1);
            }
        }

        System.out.println(namesMap);

        scanner.close();
    }
}


75.1.6

package q36018;

import java.util.*;

public class HashMapIterationDemo {

    public static void main(String[] args) {

        Map<String, String> namesMap = new HashMap<>();

        for (String argument : args) {
            String shortName = argument.substring(0, 3);
            namesMap.put(shortName, argument);
        }

        Set<String> shortNameset = new HashSet<>(namesMap.keySet());

        for (String key : shortNameset) {
            System.out.println(key + " : " + namesMap.get(key));
        }
    }
}


75.1.7


import java.util.*;

public class HashMapIterationDemo {

    public static void main(String[] args) {

        Map<String, String> namesMap = new HashMap<>();

        for (String str : args) {
            String key = str.substring(0, 2);
            namesMap.put(key, str);
        }

        Set<String> shortNamesSet = new HashSet<>(namesMap.keySet());

        for (String key : shortNamesSet) {
            System.out.println(key + " " + namesMap.get(key));
        }
    }
}


75.1.8

package q36021;

import java.util.*;

public class HashMapIterationDemo {

    public static void main(String[] args) {

        HashMap<String, String> namesMap = new HashMap<>();

        for (String str : args) {
            String key = str.substring(0, 3);
            namesMap.put(key, str);
        }

        Set<Map.Entry<String, String>> entrySet = namesMap.entrySet();

        for (Map.Entry<String, String> entry : entrySet) {
            String key = entry.getKey();
            String value = entry.getValue();
            System.out.println(key + " : " + value);
        }
    }
}



75.1.9


package q24086;

import java.util.*;

public class HashMapIterationDemo {

    public static void main(String[] args) {

        Map<String, String> namesMap = new HashMap<>();

        Set<String> shortNamesSet = namesMap.keySet();

        for (String str : args) {
            String key = str.substring(0, 2);
            namesMap.put(key, str);
        }

        System.out.println(namesMap);
    }
}


76.1.1


package q37270;

import java.util.*;

public class ArrayDequeDemo {

    public static void main(String[] args) {

        ArrayDeque<String> arrayDeque = new ArrayDeque<>();

        Scanner input = new Scanner(System.in);

        String str1 = input.nextLine();
        String str2 = input.nextLine();
        String str3 = input.nextLine();

        arrayDeque.offer(str1);
        arrayDeque.offer(str2);
        arrayDeque.offer(str3);

        System.out.println("After all offer calls: " + arrayDeque);

        System.out.println("Poll returns: " + arrayDeque.poll());

        System.out.println("After calling poll: " + arrayDeque);

        String str4 = input.nextLine();
        String str5 = input.nextLine();

        arrayDeque.push(str4);
        arrayDeque.push(str5);

        System.out.println("After all push calls: " + arrayDeque);

        System.out.println("Pop returns: " + arrayDeque.pop());

        System.out.println("After calling pop: " + arrayDeque);

        String str6 = input.nextLine();
        String str7 = input.nextLine();

        arrayDeque.offerFirst(str6);
        arrayDeque.offerLast(str7);

        System.out.println("ArrayDeque after offerFirst and offerLast calls: " + arrayDeque);

        input.close();
    }
}


76.1.2

package q37271;

import java.util.*;

public class ArrayDequeDemo {

    public static void main(String[] args) {

        ArrayDeque<String> arrayDeque = new ArrayDeque<>();

        Scanner scanner = new Scanner(System.in);

        String str1 = scanner.nextLine();
        String str2 = scanner.nextLine();
        String str3 = scanner.nextLine();

        arrayDeque.offer(str1);
        arrayDeque.offer(str3);
        arrayDeque.offer(str2);

        System.out.println("after all offers calls : " + arrayDeque);

        scanner.close();
}
}

76.1.3


package q37272;

import java.util.*;

public class ArrayDequeDemo {

    public static void main(String[] args) {

        ArrayDeque<String> arrayDeque = new ArrayDeque<>();

        Scanner scanner = new Scanner(System.in);

        String str1 = scanner.nextLine();
        String str2 = scanner.nextLine();
        String str3 = scanner.nextLine();

        arrayDeque.offer(str1);
        arrayDeque.offer(str3);
        arrayDeque.offer(str2);

        System.out.println("After all offers calls : " + arrayDeque);

        System.out.println("Poll returns : " + arrayDeque.poll());

        System.out.println("After calling poll : " + arrayDeque);

        System.out.println("Peek returns : " + arrayDeque.peek());

        System.out.println("After calling peek : " + arrayDeque);

        scanner.close();
    }
}


77.1.1

package q35981;

import java.util.*;

public class GenericListDemo {

    public static void main(String[] args) {

        ArrayList<Integer> numbersList = new ArrayList<>();

        numbersList.add(72);
        numbersList.add(78);
        numbersList.add(81);

        int total = 0;

        for (int number : numbersList) {
            total += number;
        }

        System.out.println("total = " + total);
    }
}



79.1.1

package q11394;

public class CustomGenericClassExample {

    public static void main(String[] args) {

        A<String> al = new A<>("Ganga");
        System.out.println("al.getValue() = " + al.getValue());

        A<Boolean> a2 = new A<>(true);
        System.out.println("a2.getValue() = " + a2.getValue());
    }
}

class A<T> {
    private T t;

    public A(T t) {
        this.t = t;
    }

    public T getValue() {
        return t;
    }

    public void setValue(T t) {
        this.t = t;
    }
}


80.1.1

package q11395;

import java.util.*;

public class BoundedTypeExample {

public static void main(String[] args) {

List<String> namesList = new ArrayList();

// add "Ganga" to the List.

// add "Krishna" to the List.

namesList.add("Ganga");

namesList.add("Krishna");

Set<String> namesSet = new LinkedHashSet<>();

// add "Ganga" to the List.

// add "Narmada" to the List.

namesSet.add("Ganga");

namesSet.add("Narmada");

System.out.println("largerCollection" largerCollection(namesList.

namesSet));

}

public static <T extends Collection> T largerCollection(T collection1, T

collection2){

//Define a generic method that takes two collections using the generic type parameter <T extends Collection>

return (collection1.size() > collection2.size())? collection1: collection2;
 }

}


81.1.1


package q11396;

import java.util.*;

public class WildCardTypesDemo {

    public static void main(String[] args) {

        List<? extends Number> upperList = Arrays.asList(2, 3, 4); // Hint: change here

        List<? super Number> lowerList = new ArrayList<>(); // Hint: change here

        List<Integer> noBoundsList = new ArrayList<>();

        upperBoundedMethod(upperList);

        lowerBoundedMethod(lowerList);

        noBoundedMethod(noBoundsList);
    }

    public static void upperBoundedMethod(List<? extends Number> list) { // change here

        System.out.println("In upperBoundedMethod");

        for (Number number : list) {
            System.out.println(number);
        }
    }

    public static void lowerBoundedMethod(List<? super Integer> list) { // change here

        System.out.println("In LowerBoundedMethod");

        list.add(2);
        list.add(3);
        list.add(4);

        System.out.println("list: " + list);
    }

    public static void noBoundedMethod(List<Integer> list) {

        System.out.println("In noBoundedMethod");

        list.add(8);
        list.add(7);

        System.out.println("list: " + list);
    }
}


















