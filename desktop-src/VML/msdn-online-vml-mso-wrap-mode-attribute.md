---
title: Atributo VML MSO-Wrap-Mode
description: Atributo VML MSO-Wrap-Mode
ms.assetid: 51c4e90d-62cc-4646-9c71-8a6bf3366b2f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88e3743522b9286da8a7f30e9100e06205430b1b18fa3c62def60b57f54b65d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136979"
---
# <a name="vml-mso-wrap-mode-attribute"></a>Atributo VML MSO-Wrap-Mode

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Define o modo de quebra de texto. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *element* style="mso-wrap-mode: *expression* ">

**Comentários**

Os valores são:



| Valor          | Descrição                          |
|----------------|--------------------------------------|
| square         | Envolve o texto em torno da forma em um quadrado. |
| Apertado          | O texto é envolvido próximo à forma.  |
| superior e inferior | O texto salta de cima para baixo.       |
| ao        | O texto é exibido pela forma.     |
| nenhum           | O texto não é wrap.                   |



 

Usado pelo Microsoft PowerPoint para salvar em HTML para indicar se o quebra-cabeça de palavra dentro de um AutoShape está em (**quadrado**) ou desligado (**nenhum**).

*Microsoft Office Atributo Extensions*

**Exemplo**

O código a seguir indica que wordwrap dentro de um AutoShape está ligado em PowerPoint.


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-mode:square"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



 

 