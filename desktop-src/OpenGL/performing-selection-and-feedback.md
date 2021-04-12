---
title: Executando a seleção e os comentários
description: Executando a seleção e os comentários
ms.assetid: 908114b3-ac0e-4fd5-ad28-137e6af7ffc7
keywords:
- OpenGL, seleção
- OpenGL, comentários
- OpenGL, renderização
- modo de seleção OpenGL
- modo de comentários OpenGL
- modo de renderização OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be13ae103d33039c996851582823c23c30316731
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292188"
---
# <a name="performing-selection-and-feedback"></a>Executando a seleção e os comentários

A seleção, os comentários e a renderização são modos mutuamente exclusivos de operação. A renderização é o modo padrão normal durante o qual os fragmentos são produzidos pela rasterização.

Nos modos de seleção e de comentários, nenhum fragmento é produzido; Portanto, nenhuma modificação framebuffer ocorre. No modo de seleção, você pode determinar quais primitivos serão desenhados em alguma região de uma janela; no modo de comentários, as informações sobre primitivas que serão rasterizadas são alimentadas de volta para o aplicativo.

Você seleciona entre esses três modos com [**glRenderMode**](glrendermode.md).

-   [Seleção](selection.md)
-   [Comentários](feedback.md)
-   [Referência de seleção e comentários](selection-and-feedback-reference.md)

 

 




