---
description: Você pode usar a mensagem do WM \_ Paint para executar o desenho necessário para exibir informações.
ms.assetid: cc56745f-95d0-4607-a206-1e7ed7109bf0
title: Usando a mensagem de WM_PAINT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba77246e04effc74de8158aef9bfc4aaf27471c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169134"
---
# <a name="using-the-wm_paint-message"></a>Usando a mensagem de pintura do WM \_

Você pode usar a mensagem do [**WM \_ Paint**](wm-paint.md) para executar o desenho necessário para exibir informações. Como o sistema envia \_ mensagens do WM Paint para seu aplicativo quando a janela deve ser atualizada ou quando você solicita uma atualização explicitamente, você pode consolidar o código para desenhar no procedimento de janela do aplicativo. Você pode usar esse código sempre que seu aplicativo precisar desenhar informações novas ou existentes.

As seções a seguir mostram várias maneiras de usar a mensagem do WM \_ Paint para desenhar em uma janela:

-   [Desenho na área do cliente](drawing-in-the-client-area.md)
-   [Redesenhando toda a área do cliente](redrawing-the-entire-client-area.md)
-   [Redesenhando na região de atualização](redrawing-in-the-update-region.md)
-   [Invalidando a área do cliente](invalidating-the-client-area.md)
-   [Desenhando uma janela minimizada](drawing-a-minimized-window.md)
-   [Desenhando um plano de fundo de janela personalizada](drawing-a-custom-window-background.md)

 

 



