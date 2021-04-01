---
title: Atributo de inserção de VML
description: Atributo de inserção de VML
ms.assetid: b50f900a-b0dc-4042-af9e-050011307765
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d83f2ea38ef4ca90f6687196335d2edd2d39c09c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084621"
---
# <a name="vml-inset-attribute"></a>Atributo de inserção de VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Especifica valores de margem interna para texto de TextBox. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[TextBox](msdn-online-vml-textbox-element.md)

**Sintaxe de marca**

<v: *Element* relevo = " *expression* " >

**Sintaxe do script**

*Element* . relevo = "*expressão*"

*expressão* = de *elemento*. relevo

**Comentários**

O valor da margem de texto interna é especificado como uma cadeia de caracteres que contém quatro valores, cada um separado por vírgulas ou espaços. Os valores medem a margem interna das bordas esquerda, superior, direita e inferior da caixa especificada pelo atributo [TextBoxRect](msdn-online-vml-textboxrect-attribute.md) do **caminho**. Os valores ausentes são definidos como o padrão, que é "0,1 in, 0,05 in, 0,1 in, 0,05 in".

Para formas giradas em navegadores que não dão suporte à rotação, a caixa delimitadora se ajustará ao múltiplo mais próximo de 90 graus.

*Atributo padrão da VML*

**Exemplo**

A caixa de texto terá uma margem de margem interna de 10 pixels.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:10pt;left:10pt;width:50pt;height:50pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:textbox id="mytextbox" inset="10px, 10px, 10px, 10px">
   VML
   </v:textbox/>
   </v:shape>
```



 

 