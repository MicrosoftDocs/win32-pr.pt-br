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
ms.openlocfilehash: 7ab5d4124445455e518e4f091730e6e38e899442785b9f86ef73a230b99fbd41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082406"
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

 

 




