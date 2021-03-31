---
title: Atributo StrokeWeight de VML
description: Atributo StrokeWeight de VML
ms.assetid: 364882b2-e5f4-4a86-b7d7-352f8780ebdc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a8da9f7220315b066676f2439f37b97250cc7c8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641292"
---
# <a name="vml-strokeweight-attribute"></a>Atributo StrokeWeight de VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define a espessura do pincel que traça o caminho de uma forma. Leitura/gravação. **VGLength**.

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *Element* strokeweight = " *expressão* " >

**Sintaxe do script**

*Element* . strokeweight = "*expressão*"

*expressão* = de *elemento*. strokeweight

**Comentários**

O valor é duplicado do atributo **Weight** do elemento **Stroke** . Se um número for especificado, mas nenhuma das unidades for adicionada, a unidade de medida padrão será a emu. Se nenhum valor for especificado, o padrão será 1 pixel (1px).

No entanto, para scripts, a unidade de medida padrão é em pontos.

*Atributo padrão da VML*

**Consulte também**

[Stroke](msdn-online-vml-stroke-element.md), [IVgLength](msdn-online-vml-vglength.md), [unidades](msdn-online-vml-units.md)

**Exemplo**

O peso do traço da forma é 1 ponto.


```HTML
   <v:shape id="rect01" strokeweight="1pt"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[Exemplo do atributo StrokeWeight](/previous-versions/bb264095(v=vs.85)). (Requer o Microsoft Internet Explorer 5 ou superior.)

 

 