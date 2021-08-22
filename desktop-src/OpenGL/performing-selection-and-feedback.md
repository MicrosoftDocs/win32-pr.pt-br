---
title: Executando seleção e comentários
description: Executando seleção e comentários
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
ms.openlocfilehash: 95efe3f07e86056cd0364daaed1e6a9c0ef402afc18b14d74cca313c9835479f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118936277"
---
# <a name="performing-selection-and-feedback"></a>Executando seleção e comentários

Seleção, comentários e renderização são modos mutuamente exclusivos de operação. A renderização é o modo padrão normal durante o qual os fragmentos são produzidos por rasterização.

Nos modos de seleção e comentários, nenhum fragmento é produzido; portanto, nenhuma modificação de framebuffer ocorre. No modo de seleção, você pode determinar quais primitivos serão desenhados em alguma região de uma janela; no modo de comentários, informações sobre primitivos que serão rasterizados são alimentadas de volta para o aplicativo.

Você seleciona entre esses três modos com [**glRenderMode.**](glrendermode.md)

-   [Seleção](selection.md)
-   [Comentários](feedback.md)
-   [Referência de seleção e comentários](selection-and-feedback-reference.md)

 

 




