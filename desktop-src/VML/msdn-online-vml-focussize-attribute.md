---
title: Atributo FocusSize de VML
description: Atributo FocusSize de VML
ms.assetid: 6ca5af2c-3064-423f-a7bb-202f23bf95da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8149973932e9601be2caa0306eefcec08951b238
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008341"
---
# <a name="vml-focussize-attribute"></a>Atributo FocusSize de VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

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



 

 