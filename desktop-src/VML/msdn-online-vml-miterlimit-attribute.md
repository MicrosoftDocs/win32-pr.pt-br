---
title: Atributo MiterLimit de VML
description: Atributo MiterLimit de VML
ms.assetid: 74744b8a-df73-4a2e-8df7-07fd0e423a47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fef82ce7e8e0d3bf99fc532a9e746a94006a6bb9deba282ce8edd6ab91d41902
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119308366"
---
# <a name="vml-miterlimit-attribute"></a>Atributo MiterLimit de VML

este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). para obter informações, recomendações e orientações sobre a versão atual do Windows Internet explorer, consulte [internet explorer developer Center](https://msdn.microsoft.com/ie/).

 

Define a suavidade da junção de mitre. Leitura/gravação. **VgNumber**.

**Aplica-se a**

[Pincel](msdn-online-vml-stroke-element.md)

**Sintaxe de marca**

<v: *Element* MiterLimit = " *expressão* " >

**Sintaxe do script**

*Element* . MiterLimit = "*expressão*"

*expressão* = de *elemento*. MiterLimit

**Comentários**

A distância máxima entre o ponto interno e o ponto externo de uma junção. Esse número é um múltiplo da espessura da linha.

O valor padrão é 8.

*Atributo padrão da VML*

**Exemplo**

As junções na polilinha são Mitre com um limite de 10, ou seja, 5 vezes 2 pontos.


```HTML
   <v:polyline
   strokecolor="red" strokeweight="2pt"
   points="18pt,54pt,90pt,-9pt,180pt,63pt,261pt,27pt">
   <v:stroke miterlimit="5" joinstyle="miter"/>
   </v:polyline>
```



 

 