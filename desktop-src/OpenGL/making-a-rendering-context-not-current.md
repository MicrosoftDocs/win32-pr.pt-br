---
title: Fazendo um contexto de renderização não atual
description: Para desanexar um contexto de renderização de um thread, torne-o não atual. Você pode fazer isso chamando a função wglMakeCurrent com os parâmetros definidos como NULL. Veja a seguir um exemplo dessa tarefa simples.
ms.assetid: fe76e3d3-5480-448d-95aa-a5af0da309f3
keywords:
- OpenGL em Windows, contextos de renderização
- contextos de renderização OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 914bbed6e2d595d23cfcf8dc38820efc18153f4433a2a48446090ec16818b671
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937359"
---
# <a name="making-a-rendering-context-not-current"></a>Fazendo um contexto de renderização não atual

Para desanexar um contexto de renderização de um thread, torne-o não atual. Você pode fazer isso chamando a função [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent) com os parâmetros definidos como **NULL**. Veja a seguir um exemplo dessa tarefa simples.

``` syntax
// detach the current rendering context from the thread  
wglMakeCurrent(NULL, NULL);
```

 

 




