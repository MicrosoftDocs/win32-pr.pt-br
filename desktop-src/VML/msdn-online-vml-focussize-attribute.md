---
title: Atributo FocusSize de VML
description: Atributo FocusSize de VML
ms.assetid: 6ca5af2c-3064-423f-a7bb-202f23bf95da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 322bea9f9d78ff76cd631cc36149939bb5b3db5f87dc9c80e9f2a5100f031c1e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099256"
---
# <a name="vml-focussize-attribute"></a>Atributo FocusSize de VML

este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). para obter informações, recomendações e orientações sobre a versão atual do Windows Internet explorer, consulte [internet explorer developer Center](https://msdn.microsoft.com/ie/).

 

Define o tamanho do foco para preenchimentos radiais. Leitura/gravação. **VgVector2D**.

**Aplica-se a**

[Preencher](msdn-online-vml-fill-element.md)

**Sintaxe de marca**

<v: *Element* focussize = " *expressão* " >

**Sintaxe do script**

*Element* . focussize = "*expressão*"

*expressão* = de *elemento*. focussize

**Comentários**

Os valores são frações de largura e altura da forma. A primeira é uma porcentagem do preenchimento para a borda direita da forma e a segunda é uma porcentagem do preenchimento até a parte inferior da forma. O valor padrão é 0,0. Um valor de **FocusSize** de 100%, 100% e um **FocusPosition** de 0, 0 faria com que Color2 dominasse completamente o Blend. Valores pequenos de cerca de 10%, 10% são recomendados para mesclagens balanceadas.

*Atributo padrão da VML*

**Exemplo**

O preenchimento radial criará uma mistura começando no centro como azul e ficando vermelha em todas as quatro bordas. O centro do Blend é definido por **FocusPosition** e o tamanho da cor de início interna é determinado por **FocusSize**.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l1,200, 200,200, 200,1 x e">
   <v:fill type="gradientradial" color="red" color2="blue"
   focusposition=".5,.5" focussize=".1,.1"/>
   </v:shape>
```



 

 