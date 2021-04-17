---
title: Atributo de matriz (sombra) (VML)
description: Atributo de matriz (sombra) (VML)
ms.assetid: 29bebd2f-7f66-4883-8c12-57fef4a0ac9e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d599aa817e87481aefdec43dbe345b7235fc54bd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366620"
---
# <a name="matrix-attribute-shadowvml"></a>Atributo de matriz (sombra) (VML)

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define uma transformação de perspectiva para uma sombra. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Shadow](msdn-online-vml-shadow-element.md)

**Sintaxe de marca**

<v: *Element* matriz = " *expression* " >

**Sintaxe do script**

*Element* . Matrix = "*expressão*"

*expressão* = de *elemento*. Matrix

**Comentários**

Uma matriz de transformação de perspectiva no formato "Sxx, SXY, syx, syy, px, py", em que s = Scale e p = Perspective. Se o deslocamento estiver em unidades absolutas, então px, py estão em unidades de 1/emu; caso contrário, eles são uma fração inversa do tamanho da forma.

*Atributo padrão da VML*

 

 