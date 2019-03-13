function Joined(User){
  SendAsServerMessageWithText(`${User} Joined`)
}

function Left(User){
  SendAsServerMessageWithText(`${User} left`)
}  

var latestName = "";
const CLIENT_ID = 'vFVulQrD7EARnQhi';

const drone = new ScaleDrone(CLIENT_ID, {
  data: { // Will be sent out as clientData via events
    name: getRandomName(),
    color: GetColorType(),
    isAdmin: getAdmin(),
  },
});





let members = ["Server", ""]; 
let Admins = ["TableFlipGod1492", "Aiden814", "DoctorStrange52", "password"];


drone.on('open', error => {
  if (error) {
    return console.error(error);
  }
  console.log('Successfully connected to Scaledrone');

  const room = drone.subscribe('observable-room');
  room.on('open', error => {
    if (error) {
      return console.error(error);
    }
    console.log('Successfully joined room');
  });



  

  room.on('members', m => {
    members = m;
    updateMembersDOM();
  });

  room.on('member_join', member => {
    if(member === Admins["0"] || member === Admins["2"]){
      SendAsServerMessageWithText("Admin Has Joined");
    }
    members.push(member);
    Joined(latestName)
    updateMembersDOM();
  });

  room.on('member_leave', ({id}) => {
    const index = members.findIndex(member => member.id === id);
    members.splice(index, 1);
    Left(member);
    updateMembersDOM();
  });

  room.on('data', (text, member) => {
    if (member !== "[Admin]TableFlipGod") {
      addMessageToListDOM(text, member);
      console.log("DEBUG 4, Sent As User")
    }else if(latestName === "[Admin]TableFlipGod"){
      ShowButton();
      addServerMessage(text);
      console.log("DEBUG 4, Sent As Server")
    }
  });
});

drone.on('close', event => {
  console.log('Connection was closed', event);
});

drone.on('error', error => {
  console.error(error);
});





function ShowButton() {
  var divsToHide = document.getElementsByClassName("admin"); //divsToHide is an array
  for(var i = 0; i < divsToHide.length; i++){
    //divsToHide[i].style.visibility = "hidden"; // or
    divsToHide[i].style.display = "block"; // depending on what you're doing
  }
}

function HideButton2() {
  var divsToHide = document.getElementsByClassName("admin"); //divsToHide is an array
  for(var i = 0; i < divsToHide.length; i++){
    divsToHide[i].style.visibility = "hidden"; // or
    divsToHide[i].style.display = "none"; // depending on what you're doing
  }
}



function getRandomName() {
  let Admins = ["TableFlipGod1492", "Aiden814", "DoctorStrange52", "password"];
  var name = prompt("What is your name?")
  if(name == null || name == ''){
    var NAAMEEEE = "Guest" + Math.floor(Math.random() * 9999);
    return NAAMEEEE;
  }
  if(name == Admins["0"]){
    var NAAME = name.substring(0, name.length-4)
    var password = prompt("Enter password");
      if(password === Admins["1"]) {
        //isAdmin == true;
        latestName == "[Admin]" + `${NAAME}`;
        console.log("Table is admin");
        console.log(latestName.toString())
        return `[Admin]${NAAME}`
      }
  }
  if(name == Admins["2"]){
    var password = prompt("Enter password");
    if(password == Admins["3"]){
      isAdmin == true;
      latestName == `[Admin]${name}`;
      ShowButton();
      console.log("admin")
      return `[Admin]${name}`
    }
    if(name.startsWith("[Admin]")){
      console.log("ERRRO")
    }
  }
  else {
    HideButton2();
    latestName = name;
    console.log("Not admin")
    return name;
  }
}



function GetColorType() {
  if(latestName === "[Admin]TableFlipGod"){
    console.log("DEBUG 2, User Type = Admin")
    return "#FF0000"
  }
  else{
    console.log("DEBUG 2, User Type = NonAdmin")
    console.log(latestName)
    return "#000000"
  }
}

function ChangeColor(){
  return "#FF0000"
}


//------------- DOM STUFF

const DOM = {
  membersCount: document.querySelector('.members-count'),
  membersList: document.querySelector('.members-list'),
  messages: document.querySelector('.messages'),
  input: document.querySelector('.message-form__input'),
  form: document.querySelector('.message-form'),
};

DOM.form.addEventListener('submit', sendMessage);

function sendMessage() {
  const value = DOM.input.value;
  if (value === '') {
    return;
  }
  DOM.input.value = '';
  drone.publish({
    room: 'observable-room',
    message: value,
  });
}

function createMemberElement(member) {
  if(latestName === "[Admin]TableFlipGod" || "[Admin]DoctorStrange52"){
    CreateAdmin(member);
    console.log("True")
    //isAdmin == true;
  }
  else{
    console.log("error")
    console.log(latestName)
    const { name, color } = member.clientData;
    const el = document.createElement('div');
    el.appendChild(document.createTextNode(name));
    el.className = 'member';
    el.style.color = color;
    return el;
  }
}

function CreateAdmin(member) {
  const { name, color, isAdmin } = member.clientData;
  const el = document.createElement('div');
  el.appendChild(document.createTextNode(name));
  el.className = 'Admins';
  console.log(members["0"]);
  console.log("Debug 1")
  console.log(latestName);
  console.log(isAdmin);
  return el;
}

function getAdmin(){
  if(latestName === "[Admin]TableFlipGod") {
    console.log("DEBUG 5, Admin Check True")
    return true;
  }
  else{
    console.log("DEBUG 5, Admin Check False")
    console.log(latestName)
    return false;
  }
}



function createServerElement() {
  const el = document.createElement('div');
  el.appendChild(document.createTextNode("Server:"));
  el.className = 'Server';
  el.setAttribute("class", "Server")
  console.log("Sending");
  return el;
}


function updateMembersDOM() {
  DOM.membersCount.innerText = `${members.length} users in room:`;
  DOM.membersList.innerHTML = '';
  members.forEach(member => DOM.membersList.appendChild(createMemberElement()));
}

function createMessageElement(text, member) {
  const el = document.createElement('div');
  el.appendChild(createMemberElement(member));
  el.appendChild(document.createTextNode(text));
  el.className = 'message';
  el.setAttribute("id", "admin2");
  console.log("DEBUG 3, Sent as Server")
  return el;
}



function ServerSidedMessage(text) {
  const el = document.createElement('div');
  el.appendChild(createServerElement());
  el.appendChild(document.createTextNode(text));
  el.className = 'ServerMessage';
  return el;
}

function addMessageToListDOM(text, member) {
  const el = DOM.messages;
  const wasTop = el.scrollTop === el.scrollHeight - el.clientHeight;
  el.appendChild(createMessageElement(text, member));
  if (wasTop) {
    el.scrollTop = el.scrollHeight - el.clientHeight;
  }
}

function addServerMessage(text) {
  const el = DOM.messages;
  const wasTop = el.scrollTop === el.scrollHeight - el.clientHeight;
  el.appendChild(ServerSidedMessage(text));
  if (wasTop) {
    el.scrollTop = el.scrollHeight - el.clientHeight;
  }
}


function SendAsServerMessage(){
  if(latestName === "[Admin]TableFlipGod"){
    const text = DOM.input.value;
    addServerMessage(text);
  }
  else if(latestName !== "[Admin]TableFlipGod"){
    console.log("Cant Send Not admin");
    console.log("Name " + latestName);
    HideButton2();
  }
}

function SendAsServerMessageWithText(text){
  addServerMessage(text);
}

