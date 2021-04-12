---
title: Atributo de ID (VML)
description: Atributo de ID (VML)
ms.assetid: 39575a1c-f8ea-43e0-9ad5-540e9d803748
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20a3925166a735b7813efd4cb9bc68f50bb8fa52
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454155"
---
# <a name="id-attribute-vml"></a>Atributo de ID (VML)

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Fornece um identificador exclusivo para um elemento. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

Todos os elementos de VML.

**Sintaxe de marca**

<v: *ElementName* ID = " *idname* " >

**Sintaxe do script**

*ElementName* . ID = " *idname* "

*expressão* = de *ElementName*. ID

**Comentários**

Use **ID** para se referir a um elemento específico. Depois de criar uma forma e dada a ela uma ID, você pode usar o nome da ID quando desejar manipular o elemento.

A **ID** é necessária para usar o elemento [ShapeType](msdn-online-vml-shapetype-element.md) .

Quando a VML é gerada por Microsoft Office, se um nome de modelo de objeto for atribuído à forma, a **ID** será definida com esse nome. Se o nome do modelo de objeto não estiver definido, o nome será gerado usando o *SPID* (ID de forma interna) mais um prefixo (S para Shape, M para Shape mestre, T para ShapeType).

*Atributo padrão da VML*.

**Exemplo**

Para alterar os atributos de uma forma, você deve primeiro dar uma ID à forma; por exemplo, "myRect".


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```




```HTML
   myrect.style.width = 80
   myrect.style.height = 80
   myrect.fillColor = "green"
```



[Exemplo de atributo de ID](/previous-versions/office/developer/speech-technologies/ms872141(v=msdn.10)#example). (Requer o Microsoft Internet Explorer 5 ou superior.)

 

 