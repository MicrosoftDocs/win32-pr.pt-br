---
title: Atributo ID (TextBox)(VML)
description: Atributo ID (TextBox)(VML)
ms.assetid: b9eb75cc-4d0a-4e83-a897-e35995ae7c53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 453a3a7e88c847cf63a1362d43cb6acaf21a548b141b71ffd2724c779f8eebac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099286"
---
# <a name="id-attribute-textboxvml"></a>Atributo ID (TextBox)(VML)

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Um nome que fornece um identificador exclusivo para uma caixa de texto. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[TextBox](msdn-online-vml-textbox-element.md)

**Sintaxe de marca**

<v: *element* id=" *expressão* ">

**Sintaxe do script**

*element* .id="*expression*"

*expressão* = *elemento*.id

**Comentários**

Use **a ID** para se referir a uma caixa de texto específica. Depois de criar uma caixa de texto e dar a ela uma ID, você poderá usar o nome da ID quando quiser manipular a caixa de texto.

*Atributo padrão VML*

**Exemplo**

A forma tem uma ID de caixa de texto chamada "mytextbox".


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:10pt;left:10pt;width:50pt;height:50pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:textbox id="mytextbox">
   VML
   </v:textbox/>
   </v:shape>
```



 

 