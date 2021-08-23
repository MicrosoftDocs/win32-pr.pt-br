---
title: Atributo VML V-Text-Anchor
description: Atributo VML V-Text-Anchor
ms.assetid: d6e2f60c-5cc7-4340-a9cd-b6c2b0b5b0be
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7c4b355aa4e56e3b0320200a092a66aa1f504b16be02f697e1335cd295627c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057694"
---
# <a name="vml-v-text-anchor-attribute"></a>Atributo VML V-Text-Anchor

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Define a ancoragem vertical do texto em uma caixa de texto. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[TextBox](msdn-online-vml-textbox-element.md)

**Sintaxe de marca**

<v: *elemento* v-text-anchor=" *expressão* ">

**Comentários**

Os valores são:

-   **top** (padrão)
-   **Meio**
-   **parte inferior**
-   **centro superior**
-   **centro central**
-   **centro inferior**
-   **linha de base superior**
-   **linha de base inferior**
-   **top-center-baseline**
-   **bottom-center-baseline**

O texto será ancorado em uma posição vertical na caixa de texto, conforme indicado pelo valor do atributo. O alinhamento de uma âncora de texto só se torna evidente [se MSO-Fit-Text-To-Shape](msdn-online-vml-mso-fit-text-to-shape-attribute.md) for **False.** Esse atributo é diferente do atributo **Estilo de Alinhamento Vertical,** que é usado para linguagens idegráficas.

Esse atributo é usado pelo Microsoft Office para armazenar dados em documentos da Web, mas não renderiza no Microsoft Internet Explorer 5 ou superior.

*Atributo padrão VML*

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



 

 