# PupperBot
const botconfig = require("./botconfig.json");
const Discord = require("discord.js");

const bot = new Discord.Client({disableEveryone: true})

bot.on("ready", async () =>{
  console.log('${bot.user.username} is online!');

  bot.user.setActivity ("Woof!");
});

const prefix = "*";

bot.on ("message",(message) => {

  if (message.author.bot) return;

  msg = message.content.toLowerCase();

  if (msg.startsWith ("hello woof")){
    message.reply ("U'x'U, Woof!");
  }

  if (msg.startsWith ("woof")){
    message.channel.send ("woof woof!");
  }

  if (message.content.startsWith ("🐶")){
    message.reply (":dog:");
  }

  if (message.content.startsWith ("👀")){
    message.channel.send (":eyes:");
  }

  if (msg.startsWith ("louis")){
    message.channel.send ("Is a good boi.",{files:["./Louis.png"]})
  }

  if (msg.startsWith ("jstris")){
    message.channel.send ({files:["./jstris.gif"]})
  }

  if (msg.startsWith ("pupper")){
    message.channel.send ({files:["./Puppers/p5.png"]});
  }

  if (msg.startsWith ("cri")){
    message.channel.send ({files:["./cri.gif"]})
  }

  if (msg.startsWith ("doge")){
    message.channel.send ({files:["./doge.png"]})
  }

  if (msg.startsWith ("happy birthday")){
    message.channel.send ({files:["./Puppies/hb.png"]})
  }

  dog1 = "./Puppies/bo-obama.png";
  dog2 = "./Puppies/coco.png";
  dog3 = "./Puppies/corgis.png";
  dog4 = "./Puppies/doug-the-pug.png";
  dog5 = "./Puppies/frida-rescue-search-dog.png";
  dog6 = "./Puppies/Laika.png";
  dog7 = "./Puppies/lassie.png";
  dog8 = "./Puppies/millie-bush.png";
  dog9 = "./Puppies/queen-corgis.png";
  dog10 = "./Puppies/sam-the-painting-dog.png";
  dog11 = "./Puppies/spot-fetcher-bush.png";
  dog12 = "./Puppies/sunny-obama.png";
  dog13 = "./Puppies/tillman-skate-boarding-bulldog.png";
  dog14 = "./Puppies/uggie-the-artist.png";
  dog15 = "./Puppies/aww1.png";
  dog16 = "./Puppies/aww2.png";
  dog17 = "./Puppies/aww3.png";
  dog18 = "./Puppies/aww4.png";
  dog19 = "./Puppies/aww5.png";
  dog20 = "./Puppies/aww6.png";
  dog21 = "./Puppies/aww7.png";
  dog22 = "./Puppies/aww8.png";

  if (msg.startsWith ("puppy")){
    number = 21;
    var random = Math.floor (Math.random()*(number - 1 + 1))+1;
    switch (random) {
      case 1: message.channel.send ({files:[dog1]}); break;
      case 2: message.channel.send ({files:[dog2]}); break;
      case 3: message.channel.send ({files:[dog3]}); break;
      case 4: message.channel.send ({files:[dog4]}); break;
      case 5: message.channel.send ({files:[dog5]}); break;
      case 6: message.channel.send ({files:[dog6]}); break;
      case 7: message.channel.send ({files:[dog7]}); break;
      case 8: message.channel.send ({files:[dog8]}); break;
      case 9: message.channel.send ({files:[dog9]}); break;
      case 10: message.channel.send ({files:[dog10]}); break;
      case 11: message.channel.send ({files:[dog11]}); break;
      case 12: message.channel.send ({files:[dog12]}); break;
      case 13: message.channel.send ({files:[dog13]}); break;
      case 14: message.channel.send ({files:[dog14]}); break;
      case 15: message.channel.send ({files:[dog15]}); break;
      case 16: message.channel.send ({files:[dog16]}); break;
      case 17: message.channel.send ({files:[dog17]}); break;
      case 18: message.channel.send ({files:[dog18]}); break;
      case 19: message.channel.send ({files:[dog19]}); break;
      case 20: message.channel.send ({files:[dog20]}); break;
      case 21: message.channel.send ({files:[dog21]}); break;
      case 22: message.channel.send ({files:[dog22]}); break;
    }
  }

});
bot.login(botconfig.token);
