---
title: Atributo de âncora de texto V do VML
description: Atributo de âncora de texto V do VML
ms.assetid: d6e2f60c-5cc7-4340-a9cd-b6c2b0b5b0be
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 603f118a260c8ce9c271128fa642e9e2ae569806
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366365"
---
# <a name="vml-v-text-anchor-attribute"></a>Atributo de âncora de texto V do VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define a ancoragem vertical do texto em uma caixa de texto. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[TextBox](msdn-online-vml-textbox-element.md)

**Sintaxe de marca**

<v: *elemento* v-Text-Anchor = " *expressão* " >

**Comentários**

Os valores são:

-   **superior** (padrão)
-   **meio**
-   **parte inferior**
-   **superior central**
-   **Centro-médio**
-   **inferior central**
-   **linha de base superior**
-   **parte inferior da linha de base**
-   **Top-Center-linha de base**
-   **inferior central-linha de base**

O texto será ancorado a uma posição vertical na caixa de texto, conforme indicado pelo valor do atributo. O alinhamento de uma âncora de texto só fica evidente se [mso-Fit-Text-to-Shape](msdn-online-vml-mso-fit-text-to-shape-attribute.md) for **false**. Esse atributo é diferente do atributo de estilo de **alinhamento vertical** , que é usado para idiomas ideográficos.

Esse atributo é usado pelo Microsoft Office para armazenar dados em documentos da Web, mas não é renderizado no Microsoft Internet Explorer 5 ou superior.

*Atributo padrão da VML*

**Exemplo**

O texto é alinhado à parte inferior da caixa de texto.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:10pt;left:10pt;width:50pt;height:50pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:textbox style="v-text-anchor:bottom" id="mytextbox">
   VML
   </v:textbox/>
   </v:shape>
```



 

 