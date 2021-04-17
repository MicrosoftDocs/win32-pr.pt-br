---
title: Comentários
description: No modo de comentários, cada primitivo a ser rasterizado gera um bloco de valores que é copiado para a matriz de comentários.
ms.assetid: 92f14fe2-71f7-4b59-94a5-9669e986fb30
keywords:
- modo de comentários, OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af46ecbef5c371c4c4344cb480ef77f4fcc6a7d3
ms.sourcegitcommit: 628fda3e63fd1d513ce9a5f55be8bbc4af4b2a4b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105775671"
---
# <a name="feedback-mode"></a>Modo de comentários

No modo de comentários, cada primitivo a ser rasterizado gera um bloco de valores que é copiado para a matriz de comentários. Forneça essa matriz com [**glFeedbackBuffer**](glfeedbackbuffer.md), que você deve chamar antes de colocar o OpenGL no modo de comentários. Cada bloco de valores começa com um código que indica o tipo primitivo, seguido por valores que descrevem os vértices e os dados associados do primitivo. As entradas também são escritas para bitmaps e retângulos de pixel. Não há garantia de que os valores sejam gravados na matriz de comentários até que você chame [**glRenderMode**](glrendermode.md) para retirar o OpenGL do modo de comentários. Você pode usar [**glPassThrough**](glpassthrough.md) para fornecer um marcador que é retornado no modo de comentários como se fosse um primitivo.

 

 




