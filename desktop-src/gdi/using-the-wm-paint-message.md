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
# <a name="using-the-wm_paint-message"></a><span data-ttu-id="79261-103">Usando a mensagem de pintura do WM \_</span><span class="sxs-lookup"><span data-stu-id="79261-103">Using the WM\_PAINT Message</span></span>

<span data-ttu-id="79261-104">Você pode usar a mensagem do [**WM \_ Paint**](wm-paint.md) para executar o desenho necessário para exibir informações.</span><span class="sxs-lookup"><span data-stu-id="79261-104">You can use the [**WM\_PAINT**](wm-paint.md) message to carry out the drawing necessary for displaying information.</span></span> <span data-ttu-id="79261-105">Como o sistema envia \_ mensagens do WM Paint para seu aplicativo quando a janela deve ser atualizada ou quando você solicita uma atualização explicitamente, você pode consolidar o código para desenhar no procedimento de janela do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="79261-105">Because the system sends WM\_PAINT messages to your application when your window must be updated or when you explicitly request an update, you can consolidate the code for drawing in your application's window procedure.</span></span> <span data-ttu-id="79261-106">Você pode usar esse código sempre que seu aplicativo precisar desenhar informações novas ou existentes.</span><span class="sxs-lookup"><span data-stu-id="79261-106">You can then use this code whenever your application must draw either new or existing information.</span></span>

<span data-ttu-id="79261-107">As seções a seguir mostram várias maneiras de usar a mensagem do WM \_ Paint para desenhar em uma janela:</span><span class="sxs-lookup"><span data-stu-id="79261-107">The following sections show a variety of ways to use the WM\_PAINT message to draw in a window:</span></span>

-   [<span data-ttu-id="79261-108">Desenho na área do cliente</span><span class="sxs-lookup"><span data-stu-id="79261-108">Drawing in the Client Area</span></span>](drawing-in-the-client-area.md)
-   [<span data-ttu-id="79261-109">Redesenhando toda a área do cliente</span><span class="sxs-lookup"><span data-stu-id="79261-109">Redrawing the Entire Client Area</span></span>](redrawing-the-entire-client-area.md)
-   [<span data-ttu-id="79261-110">Redesenhando na região de atualização</span><span class="sxs-lookup"><span data-stu-id="79261-110">Redrawing in the Update Region</span></span>](redrawing-in-the-update-region.md)
-   [<span data-ttu-id="79261-111">Invalidando a área do cliente</span><span class="sxs-lookup"><span data-stu-id="79261-111">Invalidating the Client Area</span></span>](invalidating-the-client-area.md)
-   [<span data-ttu-id="79261-112">Desenhando uma janela minimizada</span><span class="sxs-lookup"><span data-stu-id="79261-112">Drawing a Minimized Window</span></span>](drawing-a-minimized-window.md)
-   [<span data-ttu-id="79261-113">Desenhando um plano de fundo de janela personalizada</span><span class="sxs-lookup"><span data-stu-id="79261-113">Drawing a Custom Window Background</span></span>](drawing-a-custom-window-background.md)

 

 



