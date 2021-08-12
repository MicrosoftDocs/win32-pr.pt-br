---
title: Atributo Title (Forma)(VML)
description: Atributo Title (Forma)(VML)
ms.assetid: 08680706-5274-46d4-9199-4fdbf32f884b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55ec2a16df6740bca64357dae039f4222de956300604198b2d199977970c526d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118596504"
---
# <a name="title-attribute-shapevml"></a>Atributo Title (Forma)(VML)

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Define o texto exibido quando o ponteiro do mouse se move sobre a forma. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *element* title=" *expressão* ">

**Sintaxe do script**

*element* .title="*expression*"

*expressão* = *elemento*.title

**Comentários**

O **atributo Title** é semelhante ao atributo Html **Title** padrão. O comportamento de um título é semelhante a um Microsoft Windows ToolTip.

**Atributo padrão VML**

**Exemplo**

O título da forma é "Exibição de Dica de Ferramenta" e será exibido quando o ponteiro do mouse se mover sobre a forma.


```HTML
   <v:rect id=myrect fillcolor="red" title="ToolTip display"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



[Exemplo de atributo title](/previous-versions/bb264097(v=vs.85)). (Requer o Microsoft Internet Explorer 5 ou superior.)

 

 