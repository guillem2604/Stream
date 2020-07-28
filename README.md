# Stream
##### Lista a un Mapa. Collectors.toMap(function key, function value)
```
import java.util.Map;
import java.util.stream.Collectors;
import java.util.stream.Stream;

public class Test {
    public static void main(String[] args) {

        Stream<String> stream = Stream.of( new String[]{ "1" , "2" , "3"  } );
        Map<Integer, Integer> map1 = stream
                .map(line -> line.trim())
                .map(Integer::valueOf)
                .collect(Collectors.toMap(key -> key, value -> value + 1));

        System.out.println(map1);
    }

}
```

```

Map<Integer, Integer> map1 = Files.lines(Paths.get(inputFile))
                .map(line -> line.trim())
                .map(Integer::valueOf)
                .collect(Collectors.toMap(x -> x, x -> 1))
                
```

Imprimir lista de mapas:
```
List<HashMap<String, Object>> list = new ArrayList<HashMap<String, Object>>();

    for (Map element : list) {
        Set<Map.Entry<String, Object>> entrySet = element.entrySet();
        for (Map.Entry<String, Object> mapEntry : entrySet) {
            System.out.println("Key is : " + mapEntry.getKey());
            System.out.println("Value is : " + mapEntry.getValue());
        }
    }
```



https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet
