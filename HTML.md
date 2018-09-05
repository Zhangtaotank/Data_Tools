# HTML
## 1. Basic Syntaxes
### Structure
     - h1/h2(head), title(title), body(body), p(paragraph)
### List
     - ol(ordered list), ur(unordered list), li(list)
### Style
     - Div(Division)
     - Span()
## 2. Html Attributes
### Image Tag
     - <image scr="" alt=""> (src:Source) (alt: to show something else if the source file can not be accessed)
### Hyper-Link
      - <a href="Link Addresses"> Text </a> (Click the Text then get to the linked address)
### Forms
      - <form action="/action_page.php" method="get">
          First name: <input type="text" name="fname"><br>
          Last name: <input type="text" name="lname"><br>
          <input type="Text" value="Submit"> (Type: the table's type, for example, if "Text", it's text, if "Password", it will be hidden)
        </form>
### Submitting the form information, two main methods
       -Label: label for="id", input ID = "id"
       -action
### Linking radio buttons
        - <h3>Do you already own a dog?</h3>
          <label for="yes">Yes</label>
          <input type="radio" id="yes" name="dog_choice" value="yes">
          
          <label for="no">No:</label>
          <input type="radio" id="no" name= "dog_choice" value="no">
          
          "If you select one radio button, the other will be automatically deselected, because the two bottons have 
          the same type and share the same name 'dog_choice'. "
### Drop-down menus
         - <p>How clean is your house (Rated 1-3 with 3 being cleanest))</p>
          <select name="stars">
            <option value="Great">3</option>
            <option value="Okay">2</option>
            <option value="Bad">1</option>
          </select>
### Text area inputs
          - <p>Any other comments?</p>
          <textarea name="name" rows="8" cols="80"></textarea>
          <input type="submit" name="" value="Submit Feedback">
