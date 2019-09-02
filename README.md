# RadioButtonJs
Check radio button with js
Here are 3 radio button with value as 1, 2 and 3.
  <label><input type="radio" name="test_radio" value="1" /> Test 1</label>
  <label><input type="radio" name="test_radio" value="2" /> Test 2</label>
    <label><input type="radio" name="test_radio" value="3" /> Test 3</label>

And one text box used to show the value of selected radio button.
  <input type="text" name="result" readonly>

We are getting radio button objects via the form object.
  var form = document.getElementById('testForm');
    var radio = form.elements['test_radio'];
  
You can directly get that object as follows.
  radio = document.getElementsByName('test_radio');

Now by using for-loop  we will get value of clicked radio button.
for (var i=0, len=radio.length; i<len; i++) {
  
  Calling function "my_script" on click of each radio button elements by using javascript "onclick" event on object radio.
  radio[i].onclick = my_script;
  
  Alternativly you can also use addEventListener method for that.
  //radio[i].addEventListener("click", my_script);
  
  And at last you have to define function what to do, in our example, we are putting the value of radio object in the result object.
  function my_script(){
    result.value = this.value;
  }
}
