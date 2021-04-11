---
title: Atributo ext (distorção) (VML)
description: Atributo ext (distorção) (VML)
ms.assetid: ff1dfb2f-9098-4418-a2f7-c7159328bd09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 153273f613d188ae9e6fe733b2d0337c5010295d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104162334"
---
# <a name="ext-attribute-skewvml"></a>Atributo ext (distorção) (VML)

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define a maneira como uma distorção é exibida. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Inclinar](msdn-online-vml-skew-element.md)

**Sintaxe de marca**

<o: *Element* v:ext = " *expressão* " >

**Sintaxe do script**

*Element* . ext = "*expressão*"

*expressão* = de *elemento*. ext

**Comentários**

Esse atributo é usado para informar aos editores gráficos como processar o elemento **skew** . Os valores são:

-   **edit**
-   **exibição** (padrão)
-   **backwardCompatible**

Se uma extensão for definida como **Editar**, ela poderá ser ignorada por um visualizador de software. Se definido como **Exibir**, o visualizador deverá renderizar a representação de bitmap em vez disso.

*Atributo de extensões de Microsoft Office*

 

 