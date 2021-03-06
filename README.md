### Prompt:

"Let's consider a long, quiet country road with houses scattered very sparsely along it. (We can picture the road as a long line segment, with an eastern endpoint and a western endpoint.) Further, let's suppose that despite the bucolic setting, the residents of allthese houses arre avid cell phone users. You want to place cell phone base stations at certain points along the road, so that every house is within four miles of one of the base stations. Give an efficent algorithm that achieves this goal, using as few base stations as possible."

### Solution:

The takeaway from the prompt is that there's a straight road from A to B so I can simplify it to making sure there is a mark within 4 units of every point. With that in mind the easiest efficient approach would be taking the first point and placing a mark four units away from it and then ignoring points for the next 4 units after that, then simply repeating the process until all points have been accounted for. This runs at O(n) making it an efficient solution, note that this only works on lists of floats going from least to greatest in the form of a text file, as the assignment was open-ended I decided to go for ideal data inputs, though it does have checks for cases where either a file isn't entered or a file doesn't exist. If it was designed to be part of a larger product it could be modified to take in an input and produce an output but as it's standalone I opted to use a simple GUI for usability.

### Language:

- [Python 3](https://www.python.org/downloads/)

### Libraries:

- [Tkinter](https://docs.python.org/3/library/tkinter.html)
- [os](https://docs.python.org/3/library/os.html)
- [sys](https://docs.python.org/3/library/sys.html)

### User Manual:

On opening the application the user will be prompted to input a file name, note that files should be in the same folder as the application. The user should then click the "enter" button. Upon entering the name of a valid file an output will appear below stating the locations of the needed base stations in miles along the road as well as the total number of stations needed. A file must contain nothing but numbers and have them be separated by new lines in order for the application to function properly. If no file is entered or a file does not exist a pop-up error message will appear. The program can be used multiple times without having to exit and re-open it.

## Example File:

    Group1.txt
    
## Example File Contents:

    4.3
    12
    17
    15
    18
    20
    25
