# Seq.iter2<'T1,'T2> Function (F#)

Applies the given function to two collections simultaneously. If one sequence is shorter than the other then the remaining elements of the longer sequence are ignored.

**Namespace/Module Path:** Microsoft.FSharp.Collections.Seq

**Assembly:** FSharp.Core (in FSharp.Core.dll)


## CAPS_SYNTAX_MD

```
// Signature:
Seq.iter2 : ('T1 -> 'T2 -> unit) -> seq<'T1> -> seq<'T2> -> unit

// Usage:
Seq.iter2 action source1 source2
```

#### CAPS_PARAMETERS_MD
*action*
Type: **'T1 -&gt; 'T2 -&gt;**[unit](http://msdn.microsoft.com/en-us/library/00b837c2-6c8a-483a-87d3-0479c64037a7)


A function to apply to each pair of elements from the input sequences.


*source1*
Type: [seq](http://msdn.microsoft.com/en-us/library/2f0c87c6-8a0d-4d33-92a6-10d1d037ce75)**&lt;'T1&gt;**


The first input sequence.


*source2*
Type: [seq](http://msdn.microsoft.com/en-us/library/2f0c87c6-8a0d-4d33-92a6-10d1d037ce75)**&lt;'T2&gt;**


The second input sequence.



**exceptions tag is not supported!!!!**

## CAPS_REMARKS_MD
This function is named **Iterate2** in compiled assemblies. If you are accessing the function from a .NET language other than F#, or through reflection, use this name.

**The following code shows how to use Seq.iter2 and compares its behavior to related functions.**
```

    let seq1 = [1; 2; 3]
    let seq2 = [4; 5; 6]
    Seq.iter (fun x -> printfn "Seq.iter: element is %d" x) seq1
    Seq.iteri(fun i x -> printfn "Seq.iteri: element %d is %d" i x) seq1
    Seq.iter2 (fun x y -> printfn "Seq.iter2: elements are %d %d" x y) seq1 seq2
```

**Output**
**Seq.iter: element is 1**
**Seq.iter: element is 2**
**Seq.iter: element is 3**
**Seq.iteri: element 0 is 1**
**Seq.iteri: element 1 is 2**
**Seq.iteri: element 2 is 3**
**Seq.iter2: elements are 1 4**
**Seq.iter2: elements are 2 5**
**Seq.iter2: elements are 3 6**
## Platforms
Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2


## Version Information
**F# Core Library Versions**

Supported in: 2.0, 4.0, Portable




## See Also
[Collections.Seq Module &#40;F&#35;&#41;](Collections.Seq+Module+%28F%23%29.md)

[Microsoft.FSharp.Collections Namespace &#40;F&#35;&#41;](Microsoft.FSharp.Collections+Namespace+%28F%23%29.md)
