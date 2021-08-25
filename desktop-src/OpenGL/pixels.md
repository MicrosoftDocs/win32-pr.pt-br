---
title: Pixels
description: Os fragmentos são convertidos em pixels no framebuffer.
ms.assetid: 1925b455-ae6e-4f95-899c-4bcac641f549
keywords:
- OpenGL, pixels
- Pipeline de processamento openGL, pixels
- Pixels OpenGL
- framebuffers, convertendo fragmentos em pixels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cbaf4e2263cd1978fe16d0fb1b4b96c6dfb6065986bb8648c124fec5b56b810
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777266"
---
# <a name="pixels"></a>Pixels

Os fragmentos são convertidos em pixels no framebuffer. O framebuffer é organizado em um conjunto de buffers lógicos de cor, profundidade, estêncil e buffers de acúmulo. O buffer de cores em si consiste em um buffer frontal esquerdo, frontal direito, voltar à esquerda, voltar à direita e algum número de buffers auxiliares. Você pode emitir funções para controlar esses buffers e ler ou copiar pixels diretamente deles. (Observe que o contexto específico do OpenGL que você está usando pode não fornecer todos esses buffers.)

-   [Operações framebuffer](framebuffer-operations.md)
-   [Lendo ou copiando pixels](reading-or-copying-pixels.md)
-   [Referência de pixels](pixels-reference.md)

 

 




