---
title: Atributo de matriz (distorção)(VML)
description: Atributo de matriz (distorção)(VML)
ms.assetid: 8d039865-2261-458b-8edf-01374af65cea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d7fd3989807951f06df963c6899a2c81ce6e7faaa76432172e4391a4ce11029
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768439"
---
# <a name="matrix-attribute-skewvml"></a>Atributo de matriz (distorção)(VML)

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Define uma transformação de perspectiva de uma distorção. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Inclinar](msdn-online-vml-skew-element.md)

**Sintaxe de marca**

<o: *element* matrix=" *expressão* ">

**Sintaxe do script**

*expressão element* .matrix=""

*expressão* = *elemento*.matrix

**Comentários**

A matriz é uma cadeia de caracteres no formato "sxx, sxy, syx, syy, px, py" em que s é escala, p é perspectiva e x e y são valores x e y. Se [Offset](offset-attribute--skew--vml.md) estiver em unidades absolutas, px e py estão em unidades emu^-1 [](msdn-online-vml-units.md) (caso contrário, eles são uma fração inversa do tamanho da forma). O valor padrão é "1,0,0,1,0,0".

*Microsoft Office Atributo Extensions*

 

 