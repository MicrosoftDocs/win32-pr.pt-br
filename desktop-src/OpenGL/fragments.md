---
title: Fragmentos
description: Fragmentos
ms.assetid: bc400251-32c4-4477-ba0c-a0046fe85327
keywords:
- OpenGL, fragmentos
- Pipeline de processamento de OpenGL, fragmentos
- fragmentos OpenGL
- framebuffers, fragmentos modificando pixels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00e2b4c2dc36e24c4fd9baa82b28fa4d336f69b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105757003"
---
# <a name="fragments"></a>Fragmentos

Um fragmento produzido pela rasterização modifica o pixel correspondente no framebuffer somente se ele passar os seguintes testes:

-   [Teste de propriedade de pixel](pixel-ownership-test.md)
-   [Teste de tesoura](scissor-test.md)
-   [Teste alfa](alpha-test.md)
-   [Teste de estêncil](stencil-test.md)
-   [Teste de buffer de profundidade](depth-buffer-test.md)

Se ele passar, os dados do fragmento poderão substituir os valores de framebuffer existentes, ou você poderá combiná-los com os dados existentes no framebuffer, dependendo do estado de determinados modos. Você pode combinar o fragmento com dados no framebuffer por:

-   [Mesclagem](blending.md)
-   [Pontilhado](dithering.md)
-   [Operações lógicas](logical-operations.md)

 

 




