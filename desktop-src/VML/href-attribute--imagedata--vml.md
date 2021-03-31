---
title: Atributo HRef (ImageData) (VML)
description: Atributo HRef (ImageData) (VML)
ms.assetid: vs|vml|~\shape\image\image_href.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4ea1c5a5eb4c37773d012c1ff888aa372cb7717
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641132"
---
# <a name="href-attribute-imagedatavml"></a>Atributo HRef (ImageData) (VML)

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define uma URL para uma imagem. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintaxe de marca**

<v: *Element* o:href = " *expressão* " >

**Sintaxe do script**

*Element* . href = "*expressão*"

*expressão* = de *Element*. href

**Comentários**

Quando a forma é clicada, o navegador carregará a URL. O atributo **href** é semelhante ao atributo HTML **href** padrão de âncoras.

Usar esse atributo facilita a criação de imagens buttonswith em uma página da Web.

Esse atributo será usado por Microsoft Office somente se uma imagem tiver sido vinculada e inserida. O Microsoft Word tem uma interface do usuário para inserir imagens dessa maneira.

*Atributo de extensões de Microsoft Office*

**Exemplo**

Quando a imagem for clicada, o navegador carregará o home page da Microsoft Corporation.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata o:href="https://www.microsoft.com" src="kids.jpg"/>
   </v:shape>
```



 

 