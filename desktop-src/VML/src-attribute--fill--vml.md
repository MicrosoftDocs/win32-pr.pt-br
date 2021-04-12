---
title: Atributo src (Fill) (VML)
description: Atributo src (Fill) (VML)
ms.assetid: 88ad9413-1863-41e2-855b-2bf155ce23cc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fddfcc6bb0ba7b4b026287c1efbbd8a20e09c37a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454085"
---
# <a name="src-attribute-fillvml"></a>Atributo src (Fill) (VML)

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define a imagem a ser carregada para um preenchimento. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Preencher](msdn-online-vml-fill-element.md)

**Sintaxe de marca**

<v: *Element* src = " *expressão* " >

**Sintaxe do script**

*Element* . src = "*expressão * * *"**

*expressão* = de *elemento*. src

**Comentários**

URL para uma imagem a ser carregada para preenchimentos de imagem e padrão. Esse atributo sempre deve estar presente e apontar para dados de imagem válidos para que uma imagem apareça. Se esse atributo aparecer sozinho (ou seja, sem **href** ou atributo de **título** ), a imagem será vinculada.

*Atributo padrão da VML*

**Exemplo**

É exibida uma imagem ao lado com o arquivo myimage.gif como uma fonte.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="tile" src="myimage.gif"/>
   </v:shape>
```



 

 