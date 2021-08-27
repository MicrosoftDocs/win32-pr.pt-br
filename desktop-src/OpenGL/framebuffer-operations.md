---
title: Operações de framebuffer
description: Para selecionar o buffer no qual os valores de cores são gravados, use glDrawBuffer.
ms.assetid: 5469a183-1dc0-4ec2-bd7e-54060b5a2876
keywords:
- Pipeline de processamento OpenGL, operações framebuffer
- framebuffers, operações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83ad9d3bb04d9c063ecd9ec588843577cc577bbe62f686f136a40cdaddcbfc77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082326"
---
# <a name="framebuffer-operations"></a>Operações de framebuffer

Para selecionar o buffer no qual os valores de cores são gravados, use [**glDrawBuffer**](gldrawbuffer.md). Você usa quatro funções diferentes para mascarar a gravação de bits para cada um dos framebuffers lógicos após a execução de todas as operações por fragmento:

-   [**glIndexMask**](glindexmask.md)
-   [**glColorMask**](glcolormask.md)
-   [**glDepthMask**](gldepthmask.md)
-   [**glStencilMask**](glstencilmask.md)

A função [**glAccum**](glaccum.md) controla a operação do buffer de acumulação. Por fim [**, glClear**](glclear.md) define cada pixel em um subconjunto especificado dos buffers para o valor especificado com [**glClearColor**](glclearcolor.md), [**glClearIndex**](glclearindex.md), [**glClearDepth**](glcleardepth.md), [**glClearStencil**](glclearstencil.md)ou [**glClearAccum**](glclearaccum.md).

 

 




