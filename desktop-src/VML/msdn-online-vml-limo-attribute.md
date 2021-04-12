---
title: Atributo limo de VML
description: Atributo limo de VML
ms.assetid: 61919d48-0cc8-4693-a8bb-a8a4498ef840
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a364aebfc2384ac9e19c9dc5f2f0ae52f09228a8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366077"
---
# <a name="vml-limo-attribute"></a>Atributo limo de VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define um ponto de ampliação no caminho. Leitura/gravação. **Vector2D**.

**Aplica-se a**

[Caminho](msdn-online-vml-path-element.md)

**Sintaxe de marca**

<v: *Element* limo = " *expressão* " >

**Sintaxe do script**

*Element* . limo = "*expressão*"

*expressão* = de *elemento*. limo

**Comentários**

O valor padrão é "0 0". Limo stretchs são pontos na borda de uma forma que definem onde e como uma forma pode ser ampliada por um usuário em um editor gráfico.

*Atributo padrão da VML*

**Exemplo**

Um ponto de ampliação limo é definido em meio ao longo da linha horizontal.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" from="20pt,20pt" to="100pt,20pt">
   <v:path limo="60pt,20pt"/>
   </v:line>
```



 

 