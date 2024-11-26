## Frontend Masters - Web Accesibility Course

On this file you can find all the notes that i added and what i learned
from each session and from the exercises.

1) Module 1: Screen Readers. 

 On the first module of the course, i learned about the different screen readers that we can find, some of them are
cheap and there are others that can be quite expensive.
 If we work with screen readers we can end up finding some screen readers bug, and this can be due to the version of the
screen reader of the structure of our HTML. To avoid this, we must ensure that our web page is using semantic HTML.
 This will help a lot users to use our page and this can have a big impact if we ensure that a user with some disability
can navigate and interact without problems in our page.


2) Module 2: Accesible HTML (Semantic HTML)
Semantic HTML is super helpful when using screen readers and Accesibility.

 There are some HTML tags that dont add any functionality to a Screen reader. This tags are more helpful for things like
SEO, an example of this are: aside, footer, header.
 And tags like input, button, textarea, provide a lot of functionality to screen readers.
  To ensure that we have a good Semantic HTML, we can follow WebAIM's recommendations. 

 In Semantic HTML and Accesible HTML. An Anti-Pattern would be to add the "img" tag, without an alt attribute to describe the image, or
adding an input with type "button" instead of using the button tag, and so on.


3) Module 3: Aria Labels:
 Aria labels are super helpul when interacting with a screen reader. Disabled users who use them they will get two outputs from a
screen reader: Audio and Text.
 If we dont follow semantic HTML and add tags that dont are not semantic. The screen reader will give the user an incorrect output and this
can cause problems to the user. So, to avoid this problem we can use the the atrribute "role" to specify the role of a given tag.
 Plus, we can complement this with adding an aria-label to properly add either a label, a description, mark if an element is required,
if it's an autocomplete, etc. Additionally, if we have elements that constantly update, we can use aria-live to let the user know about
this updates and be aware of any new change.


4) Module 4: Focus Management
 Focus management is another important feature to cover and address when adding accesibility to an application.
 There will be scenarios where users will only navigate using keyboards in this case, pressing tab or shit + tab, to navigate through. To
properly handle this kind of navigation we can use tab-index.
  Depending on the value of the tab-index we will have different behaviours:
    - If we add `-1` or any negative value, the element wont be reachable through keyboard navigation.
    - If we add `0` means that the element should be focusable and reachable thorugh keyboard navigation.
    - If we add `any` positive value, it means that the element should be focusable and reachable through sequential keyboard navigation.
      its order is defined by the value of the attribute.

 Also, when thinking about users go navigate with keyboards or using another method, its a nice practice to add a hidden button called "Skip to content". This button will remain hidden and when the user starts navigating it will appear and if a user clicks on it, it will
 send the user to the content of the page that's important, making navigation more easy for them.