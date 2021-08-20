---
description: Você pode usar a mensagem WM \_ PAINT para executar o desenho necessário para exibir informações.
ms.assetid: cc56745f-95d0-4607-a206-1e7ed7109bf0
title: Usando a WM_PAINT mensagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1969d5aae7e64ad74d8070c7515daa6e9e782135ce0af54b49c7faab07f5d34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037444"
---
# <a name="using-the-wm_paint-message"></a>Usando a mensagem WM \_ PAINT

Você pode usar a [**mensagem WM \_ PAINT**](wm-paint.md) para executar o desenho necessário para exibir informações. Como o sistema envia mensagens WM PAINT para seu aplicativo quando a janela deve ser atualizada ou quando você solicita explicitamente uma atualização, você pode consolidar o código para desenho no procedimento de \_ janela do aplicativo. Em seguida, você pode usar esse código sempre que seu aplicativo precisa desenhar informações novas ou existentes.

As seções a seguir mostram uma variedade de maneiras de usar a mensagem WM \_ PAINT para desenhar em uma janela:

-   [Desenho na área do cliente](drawing-in-the-client-area.md)
-   [Redesenhar toda a área do cliente](redrawing-the-entire-client-area.md)
-   [Redesenhar na região de atualização](redrawing-in-the-update-region.md)
-   [Invalidando a área do cliente](invalidating-the-client-area.md)
-   [Desenhando uma janela minimizada](drawing-a-minimized-window.md)
-   [Desenhando um plano de fundo de janela personalizado](drawing-a-custom-window-background.md)

 

 



