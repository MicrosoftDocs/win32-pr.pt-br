---
title: Atributo src (ImageData) (VML)
description: Atributo src (ImageData) (VML)
ms.assetid: ef6b57d9-dca7-4f6e-8fd1-e846e4d09fb7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca630606ba476356a046b0079da4c0593f76473
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007611"
---
# <a name="src-attribute-imagedatavml"></a>Atributo src (ImageData) (VML)

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define uma origem para a imagem. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintaxe de marca**

<v: *Element* src = " *expressão* " >

**Sintaxe do script**

*Element* . src = "*expressão*"

*expressão* = de *elemento*. src

**Comentários**

Esse atributo sempre deve ser usado com o elemento [ImageData](msdn-online-vml-imagedata-element.md) e apontar para dados de imagem válidos para uma imagem a ser exibida. Se esse atributo aparecer sem [href](https://www.bing.com/search?q=HRef) ou [title](title-attribute--imagedata--vml.md), a imagem será vinculada.

*Atributo padrão da VML*

**Exemplo**

A origem da imagem é um arquivo chamado "kids.jpg".


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata src="kids.jpg"/>
   </v:shape>
```



 

 