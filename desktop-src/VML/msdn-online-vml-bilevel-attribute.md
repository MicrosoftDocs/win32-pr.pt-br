---
title: Atributo biníveis da VML
description: Atributo biníveis da VML
ms.assetid: 5b87e928-6f0a-4b00-833a-3c2add2d5677
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6831b84f77777cfa21a5bd5c80cb59e447c5a5ce1da78875cc9bd5ff07548690
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118602866"
---
# <a name="vml-bilevel-attribute"></a>Atributo biníveis da VML

este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). para obter informações, recomendações e orientações sobre a versão atual do Windows Internet explorer, consulte [internet explorer developer Center](https://msdn.microsoft.com/ie/).

 

Determina se uma imagem será exibida em preto e branco. Leitura/gravação. **VgTriState**.

**Aplica-se a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintaxe de marca**

<v: *Element* bilevement = " *expression* " >

**Sintaxe do script**

*elemento* . bilevel = "*expressão*"

*expressão* = de *elemento*. binível

**Comentários**

Se **for true**, a imagem será exibida usando duas cores (preto e branco). O padrão é **False**. Isso cria um efeito semelhante à Posterização.

*Atributo padrão da VML*

**Exemplo**

A imagem será exibida somente em preto e branco.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata bilevel="True" src="kids.jpg"/>
   </v:shape>
```



 

 