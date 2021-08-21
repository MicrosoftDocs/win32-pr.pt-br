---
title: Atributo Ext (distorção)(VML)
description: Atributo Ext (distorção)(VML)
ms.assetid: ff1dfb2f-9098-4418-a2f7-c7159328bd09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b0a001812a5504940509fac82333b2ca637ae76a913218f44cd3a06b4c18bfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125356"
---
# <a name="ext-attribute-skewvml"></a>Atributo Ext (distorção)(VML)

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Define a maneira como uma distorção é exibida. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Inclinar](msdn-online-vml-skew-element.md)

**Sintaxe de marca**

<o: *elemento* v:ext=" *expressão* ">

**Sintaxe do script**

*expressão* element .ext=""

*expressão* = *elemento*.ext

**Comentários**

Esse atributo é usado para dizer aos editores gráficos como processar o **elemento Skew.** Os valores são:

-   **edit**
-   **exibição** (padrão)
-   **backwardCompatible**

Se uma extensão for definida para **editar**, ela poderá ser ignorada por um visualizador de software. Se definido para **exibir**, o visualizador deverá renderizar a representação de bitmap em vez disso.

*Microsoft Office Atributo Extensions*

 

 