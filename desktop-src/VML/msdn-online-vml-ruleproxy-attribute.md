---
title: Atributo RuleProxy de VML
description: Atributo RuleProxy de VML
ms.assetid: 040e80f8-65b6-491d-812d-421800801374
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50c76116fc1f31c379f15c3229fcbe70dc7938f7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105760799"
---
# <a name="vml-ruleproxy-attribute"></a>Atributo RuleProxy de VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina se um proxy para o mecanismo de regras será usado. Leitura/gravação. **VgTriState**.

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *Element* ruleproxy = " *expressão* " >

**Comentários**

O valor padrão é **Falso**. Se for **true**, um proxy será usado.

*Atributo de extensões de Microsoft Office*

**Exemplo**

Um proxy é usado para processar a forma.


```HTML
   <v:rect id=myrect fillcolor="red" ruleproxy="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 