---
title: Atributo FocusPosition de VML
description: Atributo FocusPosition de VML
ms.assetid: 1aebf79d-c887-4a61-b50c-01a4ebfd68a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92a418916efb1721c41b7db37256ac3a040ea4b5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084882"
---
# <a name="vml-focusposition-attribute"></a>Atributo FocusPosition de VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define o centro de um gradiente radial. Leitura/gravação. **VgVector2D**.

**Aplica-se a**

[Preencher](msdn-online-vml-fill-element.md)

**Sintaxe de marca**

<v: *Element* focusposition = " *expressão* " >

**Sintaxe do script**

*Element* . focusposition = "*expressão*"

*expressão* = de *elemento*. focusposition

**Comentários**

Especifica os gradientes radiais do positionfor Center. O vetor é uma fração da largura e da altura da forma. A primeira é uma porcentagem do preenchimento para a borda esquerda; a segunda é uma porcentagem do preenchimento para a parte superior. O valor padrão é 0,0. Para posicionar um preenchimento radial no centro de uma forma, use o valor de 50%, 50%.

*Atributo padrão da VML*

**Exemplo**

O preenchimento radial será centralizado para que o azul seja iniciado no centro e radiado para fora, mudando gradualmente para vermelho no momento em que atingir as bordas externas e os cantos.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="GradientRadial" color="red" color2="blue"
   focusposition="50%,50%"/>
   </v:shape>
```



 

 