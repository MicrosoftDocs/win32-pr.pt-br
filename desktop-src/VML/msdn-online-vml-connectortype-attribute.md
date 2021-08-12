---
title: Atributo ConnectorType VML
description: Atributo ConnectorType VML
ms.assetid: acb9050d-c9e4-4d87-96c2-0bd2a1cf6e6b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a552324582729c74ae87c9fcf1cd512334423bb84c43992f265c0b47fffcd98d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118601969"
---
# <a name="vml-connectortype-attribute"></a>Atributo ConnectorType VML

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Indica o tipo de conector usado para unir formas. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *elemento* o:connectortype=" *expressão* ">

**Comentários**

Os valores são:



| Valor    | Descrição                    |
|----------|--------------------------------|
| nenhum     | Nenhum conector.                  |
| Direto | Padrão. Um conector reto. |
| Cotovelo    | Um conector em forma de pino.     |
| Curva   | Um conector curvado.            |



 

Esse atributo também pode ser usado por um mecanismo de regras de um editor gráfico.

*Microsoft Office Atributo Extensions*

**Exemplo**

A forma usa uma linha reta como um conector.


```HTML
   <v:rect id=myrect fillcolor="red" o:connectortype="straight"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 