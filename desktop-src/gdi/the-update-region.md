---
description: A região de atualização identifica a parte de uma janela que está desatualizada ou inválida e precisa de redesenho.
ms.assetid: 21228620-9491-4e1b-8658-15e9605951f2
title: A região de atualização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e670bac065782a1e09c4d142f964aaea97d4b96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104989086"
---
# <a name="the-update-region"></a><span data-ttu-id="9cac3-103">A região de atualização</span><span class="sxs-lookup"><span data-stu-id="9cac3-103">The Update Region</span></span>

<span data-ttu-id="9cac3-104">A *região de atualização* identifica a parte de uma janela que está desatualizada ou inválida e precisa de redesenho.</span><span class="sxs-lookup"><span data-stu-id="9cac3-104">The *update region* identifies the portion of a window that is out-of-date or invalid and in need of redrawing.</span></span> <span data-ttu-id="9cac3-105">O sistema usa a região de atualização para gerar mensagens de [**\_ pintura do WM**](wm-paint.md) para aplicativos e minimizar o tempo gasto pelos aplicativos colocando o conteúdo de suas janelas atualizadas.</span><span class="sxs-lookup"><span data-stu-id="9cac3-105">The system uses the update region to generate [**WM\_PAINT**](wm-paint.md) messages for applications and to minimize the time applications spend bringing the contents of their windows up to date.</span></span> <span data-ttu-id="9cac3-106">O sistema adiciona apenas a parte inválida da janela à região de atualização, exigindo que apenas essa parte seja desenhada.</span><span class="sxs-lookup"><span data-stu-id="9cac3-106">The system adds only the invalid portion of the window to the update region, requiring only that portion to be drawn.</span></span>

<span data-ttu-id="9cac3-107">Quando o sistema determina que uma janela precisa ser atualizada, ele define as dimensões da região de atualização para a parte inválida da janela.</span><span class="sxs-lookup"><span data-stu-id="9cac3-107">When the system determines that a window needs updating, it sets the dimensions of the update region to the invalid portion of the window.</span></span> <span data-ttu-id="9cac3-108">Definir a região de atualização não faz com que o aplicativo seja desenhado imediatamente.</span><span class="sxs-lookup"><span data-stu-id="9cac3-108">Setting the update region does not immediately cause the application to draw.</span></span> <span data-ttu-id="9cac3-109">Em vez disso, o aplicativo continua recuperando mensagens da fila de mensagens do aplicativo até que nenhuma mensagem permaneça.</span><span class="sxs-lookup"><span data-stu-id="9cac3-109">Instead, the application continues retrieving messages from the application message queue until no messages remain.</span></span> <span data-ttu-id="9cac3-110">Em seguida, o sistema verifica a região de atualização e, se a região não estiver vazia (não nula), ela enviará uma mensagem de [**\_ pintura do WM**](wm-paint.md) para o procedimento de janela.</span><span class="sxs-lookup"><span data-stu-id="9cac3-110">The system then checks the update region, and if the region is not empty (non-NULL), it sends a [**WM\_PAINT**](wm-paint.md) message to the window procedure.</span></span>

<span data-ttu-id="9cac3-111">Um aplicativo pode usar a região de atualização para gerar suas mensagens do [**WM \_ Paint**](wm-paint.md) .</span><span class="sxs-lookup"><span data-stu-id="9cac3-111">An application can use the update region to generate its [**WM\_PAINT**](wm-paint.md) messages.</span></span> <span data-ttu-id="9cac3-112">Por exemplo, um aplicativo que carrega dados de arquivos abertos normalmente define a região de atualização durante o carregamento para que novos dados sejam desenhados durante o processamento da próxima mensagem do **WM \_ Paint** .</span><span class="sxs-lookup"><span data-stu-id="9cac3-112">For example, an application that loads data from open files typically sets the update region while loading so that new data is drawn during processing of the next **WM\_PAINT** message.</span></span> <span data-ttu-id="9cac3-113">Em geral, um aplicativo não deve ser desenhado no momento em que seus dados são alterados, mas roteia todas as operações de desenho por meio da mensagem do **WM \_ Paint** .</span><span class="sxs-lookup"><span data-stu-id="9cac3-113">In general, an application should not draw at the time its data changes, but route all drawing operations through the **WM\_PAINT** message.</span></span>

 

 



