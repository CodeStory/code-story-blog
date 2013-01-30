---
layout: post
title: L'échoppe de monade sur Scalaskel en Java
lang: français
badge: binary
category: post
---

Voici un exemple de solution au challenge Scalaskel. Codé en java 8. Enfin une des versions beta de java 8, sachant que l'Api collection est toujours très instable.

{% highlight java %}
import java.util.ArrayList;
import java.util.List;

import static java.util.streams.Streams.repeat;

public class ScalaskelJava8 {
  public static final int FOO = 1;
  public static final int BAR = 7;
  public static final int QIX = 11;
  public static final int BAZ = 21;

  public List<List<Integer>> combinations(int cents) {
    Combinations combinations = new Combinations();
    combinations.add(0, 0, 0, cents, BAZ);
    return combinations.list;
  }

  static class Combinations {
    final List<List<Integer>> list = new ArrayList<>();

    void add(int baz, int qix, int bar, int foo, int canUse) {
      if ((canUse >= BAZ) && (foo >= BAZ)) add(baz + 1, qix,     bar,     foo - BAZ, BAZ);
      if ((canUse >= QIX) && (foo >= QIX)) add(baz    , qix + 1, bar,     foo - QIX, QIX);
      if ((canUse >= BAR) && (foo >= BAR)) add(baz    , qix,     bar + 1, foo - BAR, BAR);

      list.add(repeat(baz, BAZ)
        .concat(repeat(qix, QIX))
        .concat(repeat(bar, BAR))
        .concat(repeat(foo, FOO))
        .into(new ArrayList<>()));
    }
  }
}{% endhighlight %}

Notez que cette solution compacte, n'est pas la plus rapide, en partie à cause de la récursion, en partie aussi parceque l'on avance dans la récursion cent par cent.

Et vous, vous avez du code à partager ?