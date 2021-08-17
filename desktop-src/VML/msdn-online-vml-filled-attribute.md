---
title: Atributo preenchido por VML
description: Atributo preenchido por VML
ms.assetid: c5a71a8d-5310-4e58-9153-c5cc64b0a5e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7053263f989dbbef163e04ca19e28afa882d20347b103c97cf2db3be4b8d25b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118346600"
---
# <a name="vml-filled-attribute"></a>Atributo preenchido por VML

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Determina se o caminho fechado será preenchido. Leitura/gravação. **VgTriState.**

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *elemento* filled=" *expressão* ">

**Sintaxe do script**

*expressão* element .filled=""

*expressão* = *elemento*.filled

**Comentários**

O valor é duplicado do **atributo On** do [elemento](msdn-online-vml-fill-element.md) Fill.

*Atributo padrão VML*

**Exemplo**

O caminho de forma é preenchido.


```HTML
   <v:shape id="rect01" filled="True"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[Exemplo de atributo preenchido.](/previous-versions/bb229669(v=vs.85)) (Requer o Microsoft Internet Explorer 5 ou superior.)

 

 