---
title: Atributo AltHRef (ImageData) (VML)
description: Atributo AltHRef (ImageData) (VML)
ms.assetid: c55ede90-3d57-4f27-9940-1fe4751cef71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 004625d769c12e67de024bf537ee04c377a18c8c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007734"
---
# <a name="althref-attribute-imagedatavml"></a>Atributo AltHRef (ImageData) (VML)

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Especifica uma referência alternativa para uma imagem. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintaxe de marca**

<v: *Element* o:althref = " *expressão* " >

**Sintaxe do script**

*Element* . althref = "*expressão*"

*expressão* = de *elemento*. althref

**Comentários**

Dá suporte à preservação de dados PICT por meio de roundtripping HTML. Na gravação em HTML, a representação alternativa (ou seja, os dados originais da PICT se o arquivo originado do Macintosh) é salva. Em uma leitura HTML, **AltHRef** é favorecedo sobre **src**.

*Atributo de extensões de Microsoft Office*

 

 