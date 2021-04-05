---
title: Atributo de ID (caminho) (VML)
description: Atributo de ID (caminho) (VML)
ms.assetid: f0f3a526-d0e1-46f8-a85c-b99d27c3fdeb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfbd5d8d9acdcafaf015354dc4c99f3703034e89
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084556"
---
# <a name="id-attribute-pathvml"></a>Atributo de ID (caminho) (VML)

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Um nome que fornece um identificador exclusivo para um caminho. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Caminho](msdn-online-vml-path-element.md)

**Sintaxe de marca**

<v: *Element* ID = " *expression* " >

**Sintaxe do script**

*Element* . ID = "*expressão*"

*expressão* = de *elemento*. ID

**Comentários**

Use **ID** para se referir a um caminho específico. Depois de criar um caminho e fornecer a ele uma ID, você poderá usar o nome da ID quando desejar manipular o caminho.

*Atributo padrão da VML*

**Exemplo**

A forma tem uma ID de caminho chamada "MYPATH".


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id= "myPath" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



 

 