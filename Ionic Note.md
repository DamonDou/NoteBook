1. Ionic 在多个Page之前进行切跳转时，消失的Page不会被销毁掉。Ionic会缓存这些Page,这样做的目的是为了在不同页面之间进行跳转时，能够流畅切换。

2. [routerLink]指令。在页面上通过这个指令在不同路由之间跳转。

3. 在代码中通过router对象进行跳转

  import { Component } from '@angular/core';
  import { Router } from '@angular/router';

  @Component({
    ...
  })
  export class LoginComponent {

    constructor(private router: Router){}

    navigate(){
      this.router.navigate(['/detail'])
    }
  }

4. 如果需要在代码中更新页面中的内容，需要使用DomController
  
    import { DomController } from '@ionic/angular';
    constructor(private domCtrl: DomController) {

    }
