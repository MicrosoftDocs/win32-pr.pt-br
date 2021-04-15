---
title: Operações de framebuffer
description: Para selecionar o buffer no qual os valores de cores são gravados, use glDrawBuffer.
ms.assetid: 5469a183-1dc0-4ec2-bd7e-54060b5a2876
keywords:
- Pipeline de processamento OpenGL, operações framebuffer
- framebuffers, operações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6199700d00a6628548404870dd6ef6ce3e2c825
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498647"
---
# <a name="framebuffer-operations"></a>Operações de framebuffer

Para selecionar o buffer no qual os valores de cores são gravados, use [**glDrawBuffer**](gldrawbuffer.md). Você usa quatro funções diferentes para mascarar a gravação de bits para cada um dos framebuffers lógicos após a execução de todas as operações por fragmento:

-   [**glIndexMask**](glindexmask.md)
-   [**glColorMask**](glcolormask.md)
-   [**glDepthMask**](gldepthmask.md)
-   [**glStencilMask**](glstencilmask.md)

A função [**glAccum**](glaccum.md) controla a operação do buffer de acumulação. Por fim [**, glClear**](glclear.md) define cada pixel em um subconjunto especificado dos buffers para o valor especificado com [**glClearColor**](glclearcolor.md), [**glClearIndex**](glclearindex.md), [**glClearDepth**](glcleardepth.md), [**glClearStencil**](glclearstencil.md)ou [**glClearAccum**](glclearaccum.md).

 

 




