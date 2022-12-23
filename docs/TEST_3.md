# Intro 
This test is designed to be completed at your leisure – there is no time limit, but we hope  that it won't take more than about 2 hours of your time. If you find that you're unable to  complete it in about 2 hours, that's ok. Just let us know in a note how far you got, and give us some thoughts about what is missing – we won't hold it against you! The goal here is to evaluate HOW you write code, not how fast.

Thanks and good luck! 

## Specifications
We would like you to write a single page web app without any backend.  

1. Page always adjusts to a size of a browser window (fully filling it up - width and  height - with minimal width fixed to 400px and minimal height fixed to 300px) 
2. Page is split to a 'top toolbar' (where 'options' are displayed) and 'content' (rest of  the page) 
3. The 'top toolbar' is at least 50px high and is split into 4 equal parts called 'option  placeholders' (boxes - side by side - whole boxes clickable)  

**Wireframe:**

```
 +-------+-------+-------+-------+ 
 | All   | Opt1* | Opt2  | Opt3  | 
 +=======+===----+-------+-------| 
 | | 
 | | 
 | Currently selected: | 
 | > Opt 1, Opt 3 < | 
 | | 
 | | 
 +-------------------------------+ 
````

The 4 'option placeholders' for options on top of a page behave as follows: 

1. 'All' option is a virtual option, is always there and is selected by default 
2. 'All' option is exclusive to other options but other options are not exclusive to  themselves and behave like 'toggle options' (if one is selected it can be unselected  and vice versa) 
3. Always at least one option must be selected (either 'All' or any combination of other  options - e.g. Opt2 or Opt1+Opt3 or Opt1+Opt2+Opt3 etc) 
4. Selecting any of other options shall automatically deselect 'All' option 
5. Selecting 'All' option shall automatically (if not selected currently) deselect all other  options 
6. Current selection state (if option is selected) is represented by making the option  text bold and underlined and this selection state is updated immediately after the  option is clicked (so user gets immediate feedback of what options are selected - 
waiting only for a delayed update of the 'contents' part of the page) 
7. Whenever options selection state is changed the 'content' of a page gets updated  with the current state of the selection (update of 'content' is delayed - till after the  progress bar finishes its run, with the progress bar being played during the delay,  but the 'option placeholders' /buttons/ state is updated immediately after the  selection was done) 
8. The 'content' is updated NOT IMMEDIATELY - but with a delay of 3 seconds - in  which time a progress bar is run from left to right (effectively it means that during  the run of the progress bar the selected options can be freely changed - with each  change resetting the progress bar). 
9. Whenever options state is changed by user during the running of the progress bar,  current run of a progress bar is reset and starts countdown again (for the updated  options selection, only if it actually changed) - this shall allow the user to e.g. quickly jump from 'All' selection to 'Opt1+Opt2' selection (user clicks 'Opt1' then on 'Opt2'  /before progress bar started for 'Opt1' click finishes/ - both options are selected now and progress bar is relaunched - finally content is updated with 'Opt1+Opt2') 
10. The progress bar (the "=" character on the example layout above) runs just below  the 'option placeholders'. For an example, go to youtube.com and see the 'red  progress bar' at the top of a page, which is running from left to right whenever any  video/link is chosen. 

## Non Functional Requirements 

1. Don't create your own "template engine" 
2. Please don't use these libraries or frameworks (jquery, bootstrap, angular) • Usage of bundlers, CSS preprocessors and task runners is encouraged 
