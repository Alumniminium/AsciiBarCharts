## ASCII BAR CHARTS!

This is a simple library for generating ASCII bar charts. It's code is unreadable, unmaintainable, makes other programmers cry and is most likely buggy af. It's also very slow. But it works I think.

It's not very flexible. It can only print positive 64bit integers. But it's a start - and looking at the codebase, it's also the end.

![Charts Screenshot](/preview.webp?raw=true "Charts Example")

### Usage for the brave

```cs
internal class Program
{
    private static void Main(string[] args)
    {
        var data = new Dictionary<string, long>
        {
            {"one", 1},
            {"two", 2},
            {"three", 3},
            {"four", 4},
            {"five", 5},
            {"six", 6},
            {"seven", 7},
            {"eight", 8},
            {"nine", 9},
            {"ten", 10},
            {"eleven", 11},
            {"twelve", 12},
            {"thirteen", 13},
            {"fourteen", 14},
            {"fifteen", 15},
            {"sixteen", 16},
            {"seventeen", 17},
            {"eighteen", 18},
            {"nineteen", 19},
            {"twenty", 20},
            {"nice", 69}
        };

        var graph = new asciigraph.AsciiBarGraph(data);
        Console.WriteLine("Vertical");
        var lines = graph.DrawVertical(25);
        foreach (var line in lines)
            Console.WriteLine(line);   
        Console.WriteLine("Horizontal - Compact");
        lines = graph.DrawHorizontal(78);
        foreach (var line in lines)
            Console.WriteLine(line);
        Console.WriteLine("Horizontal");
        lines = graph.DrawHorizontal(78,false);
        foreach (var line in lines)
            Console.WriteLine(line);    
    }
}
```

*Built for the [atlas server statistics page.](https://github.com/Alumniminium/atlas)*

