# Main topics

## Basic Control flow and Linq (intro to lambdas)

```csharp
if(this.IsSuperBasic())
{
  // Skip talking about it...
}
else
{
  // There is something a little weird with c# boolean operations?
  string boom = null;

  // && and || are "short-circuit" operators so
  if(boom != null && boom.Length > 1)
  {
    // The second statement is never evaluated and so the Null is ok
  }

  // & and | are eager operators so
  if(boom != null & boom.Length > 1)
  {
    // This would throw a NullReferenceException even though the first statement is false
  }

  // You can also make assignments in if statements
  bool? result;
  if((result = this.SomePossiblyNullOperation()).HasValue && result.Value)
  {
    // This is done a lot in JS so it probably means it's a bad idea...
  }
}

// c# has 4 types of loops; while, do...while, for, and foreach
// You can use do...while loops to sneak a goto through code review
do
{
  if(this.DoSomeWork() == false)
  {
    break; // aka GOTO the end of the loop and skip the rest of the code
  }

  this.DoSomeMoreWork();
} while(false)

// You should probably never use a for loop in c#, it _is_ 2018...
// There is one big gotcha with foreach loops to be aware of
foreach(var thisItem in allTheItems())
{
  // This will throw an exception because you can't modify the collectiong when enumerating over it
  allTheItems.Remove(thisItem);
  // It's usually more subtle than this though...
}

// The last thing to bring up are some of the more "esoteric" c# operators


```

## Lambdas and Anonymous Methods
## Event Handlers using Lambdas
## Parallel.For and ForEach using Lambdas (this is terrifying)
## Thread Pool and Cancellation Tokens
## Async Await and Cancellation tokens(?)
## Locking and Race Conditions
## Concurrent Collections
## Exceptions using linq and control flow for aggregate and base types
