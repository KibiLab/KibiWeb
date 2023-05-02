<script>
// Function to move element in array
function arrayMove(arr, fromIndex, toIndex) {
  var element = arr[fromIndex];
  arr.splice(fromIndex, 1);
  arr.splice(toIndex, 0, element);
}

// Convert string to array
let str = '["a", "b", "c"]';
let newArr = JSON.parse(str);
console.log("New Array is: ", newArr);
console.log(newArr[0]);

let page = [
  {
    "type":"div",
    "include":"abc ksjd fkj kfj kdf",
    "contain":"s1_1 s1_2 s1_3",
    "px":"px-10",
    "py":"py-10",
  },
  {
    "type":"img",
    "include":"abc ksjd fkj kfj kdf",
    "contain":"s1_1 s1_2 s1_3",
    "px":"px-10",
    "py":"py-10",
  }
]

var strobj = JSON.stringify(page);
var unstrobj = JSON.parse(strobj);

</script>
<div class="px-10 py-10">  
  <h1 class="text-3xl py-8 px-8 font-bold">Hello World!</h1>
  <p>{page[0].type}</p>
  <p>{page[0].include}</p>
  <p>{page[0].contain}</p>
  <p>{page[0].px}</p>
  <p>{page[0].py}</p>
</div>
<div class="px-10 py-10">  
  <h1 class="text-3xl py-8 px-8 font-bold">JSON.stringify</h1>
  <p>{strobj}</p>  
</div>
<div class="px-10 py-10">  
  <h1 class="text-3xl py-8 px-8 font-bold">JSON.parse</h1>
  <p>{unstrobj[1].type}</p>
  <p>{unstrobj[1].include}</p>
  <p>{unstrobj[1].contain}</p>
  <p>{unstrobj[1].px}</p>
  <p>{unstrobj[1].py}</p> 
</div>
