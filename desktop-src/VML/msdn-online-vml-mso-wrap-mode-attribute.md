---
title: Atributo VML MSO-Wrap-Mode
description: Atributo VML MSO-Wrap-Mode
ms.assetid: 51c4e90d-62cc-4646-9c71-8a6bf3366b2f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5657192fcf9da72ff99dc25cff7930b6d2d9b6b9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294214"
---
# <a name="vml-mso-wrap-mode-attribute"></a>Atributo VML MSO-Wrap-Mode

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define o modo de disposição para texto. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *Element* Style = "Die-Wrap-Mode: *expression* " >

**Comentários**

Os valores são:



| Valor          | Descrição                          |
|----------------|--------------------------------------|
| square         | Quebra o texto em uma forma em um quadrado. |
| rigida          | O texto é ajustado próximo à forma.  |
| de cima para baixo | O texto salta de cima para baixo.       |
| ao        | O texto é exibido por meio da forma.     |
| none           | O texto não quebra.                   |



 

Usado pelo Microsoft PowerPoint para salvar em HTML para indicar se a quebra automática de texto dentro de uma AutoForma está ativada (**quadrado**) ou desativada (**nenhuma**).

*Atributo de extensões de Microsoft Office*

**Exemplo**

O código a seguir indica que a WordWrap dentro de uma AutoForma está ativada no PowerPoint.


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-mode:square"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



 

 