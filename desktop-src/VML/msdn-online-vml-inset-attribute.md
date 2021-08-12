---
title: Atributo de inset VML
description: Atributo de inset VML
ms.assetid: b50f900a-b0dc-4042-af9e-050011307765
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e1d4b44756034a3ebc7e46e1cdda43042f347e58cb87c02b00c90a14320a40f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118600232"
---
# <a name="vml-inset-attribute"></a>Atributo de inset VML

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Especifica valores de margem interna para texto da caixa de texto. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[TextBox](msdn-online-vml-textbox-element.md)

**Sintaxe de marca**

<v: *elemento* inset=" *expressão* ">

**Sintaxe do script**

*expressão element* .inset=""

*expressão* = *elemento*.inset

**Comentários**

O valor de margem de texto interno é especificado como uma cadeia de caracteres que contém quatro valores, cada um separado por vírgulas ou espaços. Os valores medem inset das bordas esquerda, superior, direita e inferior da caixa especificada pelo atributo [TextBoxRect](msdn-online-vml-textboxrect-attribute.md) de **Path**. Os valores ausentes são definidos como o padrão, que é "0,1in, 0,05in, 0,1in, 0,05in".

Para formas giradas em navegadores que não suportam rotação, a caixa delimitador se ajustará ao múltiplo mais próximo de 90 graus.

*Atributo padrão VML*

**Exemplo**

A caixa de texto terá uma margem de injunção de 10 pixels.


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



 

 