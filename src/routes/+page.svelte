<script>
let page = [
  {"s1":{
    "type":"div",
    "include":"abc ksjd fkj kfj kdf",
    "contain":"s1_1 s1_2 s1_3",
    "px":"px-10",
    "py":"py-10",
  }},
  {"s2":{
    "type":"img",
    "include":"abc ksjd fkj kfj kdf",
    "contain":"s1_1 s1_2 s1_3",
    "px":"px-10",
    "py":"py-10",
  }}
]

console.log(page[0]);
console.log(page[0].s1);
if(page[1].s2){
  console.log(page[1].s2.type);
}
</script>
<div class="px-10 py-10">  
  <h1 class="text-3xl py-8 px-8 font-bold">Hello World!</h1>
  <p>{page[0].s1.type}</p>
  <p>{page[0].s1.include}</p>
  <p>{page[0].s1.contain}</p>
  <p>{page[0].s1.px}</p>
  <p>{page[0].s1.py}</p>
</div>
