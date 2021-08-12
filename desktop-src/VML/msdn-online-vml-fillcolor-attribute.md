---
title: Atributo FillColor da VML
description: Atributo FillColor da VML
ms.assetid: c18302e1-86a5-4046-811f-576a746ea398
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e626e017437d14cf1088c188e659e1099dc38c7ba88215438a6c9a45166c7732
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118601356"
---
# <a name="vml-fillcolor-attribute"></a>Atributo FillColor da VML

este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). para obter informações, recomendações e orientações sobre a versão atual do Windows Internet explorer, consulte [internet explorer developer Center](https://msdn.microsoft.com/ie/).

 

Define a cor do pincel que preenche o caminho fechado de uma forma. Leitura/gravação. [IVgColor](msdn-online-vml-ivgcolor.md) .

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *Element* FillColor = " *expressão* " >

**Sintaxe do script**

*Element* . FillColor = "*expressão*"

*expressão* = de *Element*. FillColor

**Comentários**

O valor **FillColor** é duplicado do atributo **Color** do elemento **Fill** .

*Atributo padrão da VML*

**Consulte também**

[Forma](shape-element--vml.md), [preenchimento](msdn-online-vml-fill-element.md), [IVgColor](msdn-online-vml-ivgcolor.md)

**Exemplo**

A cor de preenchimento do retângulo é vermelha.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



[Exemplo do atributo FillColor](/previous-versions/bb229668(v=vs.85)). (Requer o Microsoft Internet Explorer 5 ou superior.)

 

 