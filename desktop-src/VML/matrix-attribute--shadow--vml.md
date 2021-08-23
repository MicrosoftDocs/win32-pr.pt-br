---
title: Atributo Matrix (Sombra)(VML)
description: Atributo Matrix (Sombra)(VML)
ms.assetid: 29bebd2f-7f66-4883-8c12-57fef4a0ac9e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6124005ef3202e11dc8a4e7eeeaacba8e87e9c3a7cb3a1dd1eee55c595e40ecb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057924"
---
# <a name="matrix-attribute-shadowvml"></a>Atributo Matrix (Sombra)(VML)

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Define uma transformação de perspectiva para uma sombra. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Shadow](msdn-online-vml-shadow-element.md)

**Sintaxe de marca**

<v: *element* matrix=" *expressão* ">

**Sintaxe do script**

*expressão element* .matrix=""

*expressão* = *elemento*.matrix

**Comentários**

Uma matriz de transformação de perspectiva no formato "sxx, sxy, syx, syy, px,py" em que s= escala e p = perspectiva. Se offset estiver em unidades absolutas, px, py serão em unidades de 1/emu; caso contrário, eles serão uma fração inversa do tamanho da forma.

*Atributo padrão VML*

 

 