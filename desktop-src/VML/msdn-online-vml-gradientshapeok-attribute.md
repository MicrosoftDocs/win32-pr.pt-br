---
title: Atributo GradientShapeOK de VML
description: Atributo GradientShapeOK de VML
ms.assetid: c26ac4cb-f7f0-4666-b32f-d9fcaf9044a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d1b7c215fbe0b98c11f7e4d33301e81798bd37f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366618"
---
# <a name="vml-gradientshapeok-attribute"></a>Atributo GradientShapeOK de VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina se um caminho de gradiente será composto de caminhos concêntricos repetidos. Leitura/gravação. **VgTriState**.

**Aplica-se a**

[Caminho](msdn-online-vml-path-element.md)

**Sintaxe de marca**

<v: *Element* gradientshapeok = " *expressão* " >

**Sintaxe do script**

*Element* . gradientshapeok = "*expressão*"

*expressão* = de *elemento*. gradientshapeok

**Comentários**

Se **for true**, o caminho será preenchido com um preenchimento gradiente concêntrico usando o caminho como a forma repetida do gradiente. O padrão é **false**.

*Atributo padrão da VML*

**Exemplo**

O caminho será preenchido com um preenchimento gradiente concêntrico formado por retângulos repetidos.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:path gradientshapeok="True"/>
   </v:shape>
```



 

 