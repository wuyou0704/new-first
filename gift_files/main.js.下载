(function(){'use strict';var merrywrap=document.getElementById('merrywrap'),box=merrywrap.querySelector('.giftbox'),step=1,stepTimes=[1000,1000,2000,2000];function init(){box.addEventListener('click',runAnimation);}
function runAnimation(){if(step===1){box.removeEventListener('click',runAnimation);}
incStep(step);if(step===4){letitsnow();return;}
if(step===3){setGridDelays();}
setTimeout(function(){runAnimation();},stepTimes[step-1]);++step;}
function incStep(step){classie.remove(merrywrap,'step-'+Number(step-1));classie.add(merrywrap,'step-'+step);}
function setGridDelays(){[].slice.call(merrywrap.querySelectorAll('.row')).forEach(function(row,i){var itemsrow=[].slice.call(row.querySelectorAll('span')),itemsrowCount=itemsrow.length,factor=(itemsrowCount-1)*0.01,delays=[itemsrowCount-1];for(var k=0;k<itemsrowCount;++k)
delays[k]=k*0.01+((itemsrowCount-1-i)*factor);shuffle(itemsrow);itemsrow.forEach(function(item,j){var delay=delays[j];item.style.webkitTransition='-webkit-transform 0.4s ease-out '+delay+'s, opacity 0.4s '+delay+'s';item.style.transition='transform 0.4s ease-out '+delay+'s, opacity 0.4s '+delay+'s';});})}
function letitsnow(){var canvas=document.getElementById("snowfall");canvas.width=window.innerWidth;canvas.height=window.innerHeight;var emitter=Object.create(rectangleEmitter);emitter.setCanvas(canvas);emitter.setBlastZone(0,-10,canvas.width,1);emitter.particle=snow;emitter.runAhead(0);emitter.start(60);}
function shuffle(array){var currentIndex=array.length,temporaryValue,randomIndex;while(0!==currentIndex){randomIndex=Math.floor(Math.random()*currentIndex);currentIndex-=1;temporaryValue=array[currentIndex];array[currentIndex]=array[randomIndex];array[randomIndex]=temporaryValue;}
return array;}
init();})();