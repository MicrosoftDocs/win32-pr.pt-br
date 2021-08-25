---
title: Atributo de ID (Fill) (VML)
description: Atributo de ID (Fill) (VML)
ms.assetid: 56865772-51bd-4729-8e56-6b00e3c6bed0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22f317cef4d588444f5c01770dafd5b56af0d2bca48ee228ff789a11b46348bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007866"
---
# <a name="id-attribute-fillvml"></a>Atributo de ID (Fill) (VML)

este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). para obter informações, recomendações e orientações sobre a versão atual do Windows Internet explorer, consulte [internet explorer developer Center](https://msdn.microsoft.com/ie/).

 

Um nome que fornece um identificador exclusivo para um preenchimento. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Preencher](msdn-online-vml-fill-element.md)

**Sintaxe de marca**

<v: *Element* ID = " *expression* " >

**Sintaxe do script**

*Element* . ID = "*expressão*"

*expressão* = de *elemento*. ID

**Comentários**

Use **ID** para se referir a um preenchimento específico. Depois de criar um preenchimento e fornecer a ele uma ID, você poderá usar o nome da ID quando desejar manipular o preenchimento.

*Atributo padrão da VML*

**Exemplo**

A forma tem uma ID de preenchimento chamada "myfill".


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill id="myfill"/>
   </v:shape>
```



 

 