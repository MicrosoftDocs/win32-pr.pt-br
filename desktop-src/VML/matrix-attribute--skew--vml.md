---
title: Atributo de matriz (distorção) (VML)
description: Atributo de matriz (distorção) (VML)
ms.assetid: 8d039865-2261-458b-8edf-01374af65cea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8327acfebfe4d968e673060f2f3cbef69d3e9db6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008072"
---
# <a name="matrix-attribute-skewvml"></a>Atributo de matriz (distorção) (VML)

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define uma transformação de perspectiva de uma distorção. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Inclinar](msdn-online-vml-skew-element.md)

**Sintaxe de marca**

<o: *Element* matriz = " *expression* " >

**Sintaxe do script**

*Element* . Matrix = "*expressão*"

*expressão* = de *elemento*. Matrix

**Comentários**

A matriz é uma cadeia de caracteres no formato "Sxx, SXY, syx, syy, px, py", em que s é escala, p é perspectiva e x e y são valores x e y. Se o [deslocamento](offset-attribute--skew--vml.md) estiver em unidades absolutas, PX e py estão nas [unidades](msdn-online-vml-units.md) da UME ^-1 (caso contrário, eles são uma fração inversa do tamanho da forma). O valor padrão é "1, 0, 0, 1, 0, 0".

*Atributo de extensões de Microsoft Office*

 

 