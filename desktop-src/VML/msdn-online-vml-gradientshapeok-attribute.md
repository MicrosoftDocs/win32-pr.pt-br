---
title: Atributo GradientShapeOK do VML
description: Atributo GradientShapeOK do VML
ms.assetid: c26ac4cb-f7f0-4666-b32f-d9fcaf9044a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53c25620f8ebc05905b83f3abab7b52f7a206b6bafb522b0104f06fd8f46d6bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118124769"
---
# <a name="vml-gradientshapeok-attribute"></a>Atributo GradientShapeOK do VML

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Determina se um caminho de gradiente será feito de caminhos concêntricos repetidos. Leitura/gravação. **VgTriState.**

**Aplica-se a**

[Caminho](msdn-online-vml-path-element.md)

**Sintaxe de marca**

<v: *elemento* gradientshapeok=" *expressão* ">

**Sintaxe do script**

*elemento* .gradientshapeok="*expression*"

*expressão* = *elemento*.gradientshapeok

**Comentários**

Se **True**, o caminho será preenchido com um preenchimento de gradiente concêntrico usando o caminho como a forma repetida do gradiente. O padrão é **False.**

*Atributo padrão VML*

**Exemplo**

O caminho será preenchido com um preenchimento de gradiente concêntrico, com retângulos repetidos.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:path gradientshapeok="True"/>
   </v:shape>
```



 

 