# Gradually automate a manual procedure

The problem with a manual procedure is that you have to repeat the same steps over and over again without making a single mistake. You go through manual procedures all the time: you need to set up a SSH account on a server, do a couple of actions after each commit or work with a tool that you haven't used for months.

We can gradually replace a manual procedure with a do-nothing script. You write a do-nothing script with all the steps you need to take to get to a well-defined result. The do-nothing script consists of a separate method for each step and each method only prints the description of each step.

```python
def wait_for_enter():
  raw_input("Press Enter to continue...")

def doThis():
  print("Do this.")
  wait_for_enter()

def doThat():
  print("Do that.")
  wait_for_enter()

main():
  doThis()
  doThat()

if __name__ == "__main__":
  main()
  print("Finished.")
```

The do-nothing script will start with only printing the description of each step, but gradually you replace each method with the code to automate each step.

This has the following advantages:
  * You don't have to automate everything at once. Writing a quick and low-cost script is a good starting point to understand what needs to be automated in the first place.
  * You can use it over and over again and get the same result. A do-nothing script reduces errors by not letting you skip a step or doing them out of order. This becomes even more relevant if there are any contextual changes, like making decision branches, handling upcoming errors or using if-then rules.
  * A do-nothing script can be shared with others which in the very least helps them understand what steps they need to take to get to a well-defined result.

**source**: [Do-nothing scripting: the key to gradual automation](https://blog.danslimmon.com/2019/07/15/do-nothing-scripting-the-key-to-gradual-automation/)
