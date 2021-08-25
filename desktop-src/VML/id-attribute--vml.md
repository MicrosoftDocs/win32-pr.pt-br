---
title: Atributo ID (VML)
description: Atributo ID (VML)
ms.assetid: 39575a1c-f8ea-43e0-9ad5-540e9d803748
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc0ba0addd2d6af8a8b38af4085c79123d3178a3299269468abd73fff1951d9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007850"
---
# <a name="id-attribute-vml"></a>Atributo ID (VML)

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Fornece um identificador exclusivo para um elemento. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

Todos os elementos VML.

**Sintaxe de marca**

<v: *elementname* id=" *idname* ">

**Sintaxe do script**

*elementname* .id =" *idname* "

*expressão* = *elementname*.id

**Comentários**

Use **a ID** para se referir a um elemento específico. Depois de criar uma forma e dar a ela uma ID, você poderá usar o nome da ID quando quiser manipular o elemento.

**A ID** é necessária para usar o [elemento ShapeType.](msdn-online-vml-shapetype-element.md)

Quando o VML é gerado por Microsoft Office, se um nome de modelo de objeto for atribuído à forma, a **ID** será definida como esse nome. Se o nome do modelo de objeto não estiver definido, o nome será gerado usando o *Spid* (ID de forma interna) mais um prefixo (S para forma, M para forma mestra, T para shapetype).

*Atributo Padrão VML*.

**Exemplo**

Para alterar os atributos de uma forma, primeiro você deve dar uma ID à forma; por exemplo, "myrect".


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

 

 