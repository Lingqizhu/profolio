const textInput= document.getElementById("textInput");

const encodeBtn = document.getElementById("encodeBtn");
const decodeBtn = document.getElementById("decodeBtn");
const textOutput = document.getElementById("textOutput");
let inputs = [textInput]


//encodebtn.addEventListener("click",encodeText)
//decodebtn.addEventListener("click",decodeText);

//turn all characters to uppercase
inputs.forEach(input=>{
    input.oninput = () =>{
        input.value = input.value.toUpperCase()
    }
})

function encodeText(){
    let textInput= document.getElementById("textInput").value;
    let keyInput = parseInt(document.getElementById("userKey").value);
    let newStr="";

    for(let i=0;i<textInput.length;i++){
        let ascii_num = textInput[i].charCodeAt();
        let sum = ascii_num + keyInput%27;
        if(sum>90){
            sum = sum - 26;
        }else{
            sum = sum;
        }
       newStr += String.fromCharCode(sum);
    }
    document.getElementById('textOutput').innerHTML = newStr;
    //return newStr;
}
 encodeBtn.addEventListener('click',encodeText)
 decodeBtn.addEventListener('click',decodeText)

 function decodeText(){
    let textInput= document.getElementById("textInput").value;
    let keyInput = parseInt(document.getElementById("userKey").value);
    let newStr="";

    for(let i=0;i<textInput.length;i++){
        let ascii_num = textInput[i].charCodeAt();
        let sum = ascii_num - keyInput%27;
        if(sum<65){
            sum = sum + 26;
        }else{
            sum = sum;
        }
       newStr += String.fromCharCode(sum);
    }
    document.getElementById('textOutput').innerHTML = newStr;
 }
/*function encodeText(text,key){
    var lowerCaseStr = text.toString().toLowerCase();
    var alphabet = "abcdefghijklmnopqrstuvwxyz".split("");
    var newStr = "";
    for(let i=0; i<lowerCaseStr.length;i++){
        var currentLetter = lowerCaseStr[i];
        if(currentLetter === " "){
            newStr = currentLetter;
            continue;
        }
        var currentIndex = alphabet.indexOf(currentLetter);
        var newIndex = currentIndex + key;
        newStr += alphabet[newIndex];
    }
      return newStr;
      result.innerHTML = "newStr";
}
function decodeText(){
    console.log(text);
}
*/
