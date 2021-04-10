---
title: Compartilhando listas de exibição
description: Quando você cria um contexto de renderização, ele tem seu próprio espaço de lista de exibição.
ms.assetid: 8ace5684-a27b-4d6e-a80b-58a0b7064879
keywords:
- OpenGL no Windows, compartilhando listas de exibição
- compartilhando listas de exibição OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87d8d012e8e04455f76ca5d7bfe74229ac0b0ac8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292704"
---
# <a name="sharing-display-lists"></a>Compartilhando listas de exibição

Quando você cria um contexto de renderização, ele tem seu próprio espaço de lista de exibição. A função [**wglShareLists**](/windows/desktop/api/wingdi/nf-wingdi-wglsharelists) permite que um contexto de renderização Compartilhe o espaço da lista de exibição de outro contexto de renderização. Qualquer número de contextos de renderização pode compartilhar um único espaço de lista de exibição.

 

 




