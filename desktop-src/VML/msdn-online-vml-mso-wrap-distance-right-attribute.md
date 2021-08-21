---
title: Atributo VML MSO-Wrap-Distance-Right
description: Atributo VML MSO-Wrap-Distance-Right
ms.assetid: 2f0ec7a3-036e-4f45-a330-f8ddccb75791
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e7984c44325e62f3192725a52f2730b3ebcfc1daa78524855f8416fb840472d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118124316"
---
# <a name="vml-mso-wrap-distance-right-attribute"></a>Atributo VML MSO-Wrap-Distance-Right

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Define a distância do lado direito da forma para o texto que a envolve. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *element* style="mso-wrap-distance-right: *expressão* ">

**Comentários**

Observe que esse atributo é diferente do atributo **Margem** CSS. **A** margem altera a origem da forma para incluir as áreas de margem, mas a distância de quebra Microsoft Office não altera a origem da forma.

*Microsoft Office Atributo Extensions*

**Exemplo**

A forma tem uma distância de wrap direita de 10 pontos.


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-right:10pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



 

 