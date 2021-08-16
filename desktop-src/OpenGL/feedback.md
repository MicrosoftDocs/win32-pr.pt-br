---
title: Comentários
description: No modo de comentários, cada primitivo a ser rasterizado gera um bloco de valores copiados para a matriz de comentários.
ms.assetid: 92f14fe2-71f7-4b59-94a5-9669e986fb30
keywords:
- modo de comentários, OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb5d307b9033a60a03b585cb4df6109293d3b9b0b276bde822ca595eb37fcd19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082446"
---
# <a name="feedback-mode"></a>Modo de comentários

No modo de comentários, cada primitivo a ser rasterizado gera um bloco de valores copiados para a matriz de comentários. Fornecer essa matriz com [**glFeedbackBuffer,**](glfeedbackbuffer.md)que você deve chamar antes de colocar o OpenGL no modo de comentários. Cada bloco de valores começa com um código que indica o tipo primitivo, seguido por valores que descrevem os vértices e os dados associados do primitivo. As entradas também são escritas para bitmaps e retângulos de pixel. Não há garantia de que os valores sejam gravados na matriz de comentários até que você chame [**glRenderMode**](glrendermode.md) para tirar o OpenGL do modo de comentários. Você pode usar [**glPassThrough**](glpassthrough.md) para fornecer um marcador que é retornado no modo de comentários como se fosse um primitivo.

 

 




