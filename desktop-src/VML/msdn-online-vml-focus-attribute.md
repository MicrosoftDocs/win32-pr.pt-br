---
title: Atributo de foco da VML
description: Atributo de foco da VML
ms.assetid: 9ed52203-4142-47cd-851f-74230aac934d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 062b2900c2f980c9a1433e5e790a34d463def9be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008343"
---
# <a name="vml-focus-attribute"></a>Atributo de foco da VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define o centro de um preenchimento gradiente linear. Leitura/gravação. **VgFraction**.

**Aplica-se a**

[Preencher](msdn-online-vml-fill-element.md)

**Sintaxe de marca**

<v: *elemento* Focus = " *expressão* " >

**Sintaxe do script**

*elemento* . Focus = "*expressão*"

*expressão* = de *elemento*. Focus

**Comentários**

Define a posição inicial do Blend. Os valores variam de 100% a-100%. O valor padrão é 0. Um valor de 100% (ou-100%) mudará o foco para que a direção do Blend seja invertida (em vigor, revertendo **Color** e **Color2**). Um valor de 50% alterará o Blend para que a **cor** esteja em ambas as extremidades e **Color2** esteja no meio. Um valor de-50% alterará o Blend para que **Color2** esteja em ambas as extremidades e a **cor** esteja no meio.

*Atributo padrão da VML*

**Exemplo**

O foco gradiente do preenchimento é deslocado para que o vermelho (**cor**) seja uma faixa no centro da forma e que a parte superior e inferior seja azul (**Color2**).


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="gradient" color="red" color2="blue"
   method="linear" focus="-50%"/>
   </v:shape>
```



 

 