---
description: O Windows Sockets 1,1 introduziu o mecanismo Async-SELECT para fornecer indicações de eventos de rede que não envolveram a sondagem ou o bloqueio.
ms.assetid: d536f796-c532-4b57-8dc7-3415661b736b
title: Mensagens do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac0f60bb597a7dd92c0039dd805a971bb8587ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105785139"
---
# <a name="windows-messages"></a><span data-ttu-id="7711e-103">Mensagens do Windows</span><span class="sxs-lookup"><span data-stu-id="7711e-103">Windows Messages</span></span>

<span data-ttu-id="7711e-104">O Windows Sockets 1,1 introduziu o mecanismo Async-SELECT para fornecer indicações de eventos de rede que não envolveram a sondagem ou o bloqueio.</span><span class="sxs-lookup"><span data-stu-id="7711e-104">Windows Sockets 1.1 introduced the async-select mechanism to provide network event indications that did not involve either polling or blocking.</span></span> <span data-ttu-id="7711e-105">A função [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) é usada para registrar um interesse em um ou mais eventos de rede, conforme listado no anterior, e fornecer um identificador de janela a ser usado para notificação.</span><span class="sxs-lookup"><span data-stu-id="7711e-105">The [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) function is used to register an interest in one or more network events as listed in the preceding, and supply a window handle to be used for notification.</span></span> <span data-ttu-id="7711e-106">Quando ocorre um evento de rede indicado, uma mensagem do Windows especificada pelo cliente é enviada para a janela indicada.</span><span class="sxs-lookup"><span data-stu-id="7711e-106">When a nominated network event occurs, a client-specified Windows message is sent to the indicated window.</span></span> <span data-ttu-id="7711e-107">O provedor de serviços deve usar a função [**WPUPostMessage**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpupostmessage) para fazer isso.</span><span class="sxs-lookup"><span data-stu-id="7711e-107">The service provider must use the [**WPUPostMessage**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpupostmessage) function to accomplish this.</span></span>

<span data-ttu-id="7711e-108">No Windows, esse pode não ser o mecanismo de notificação mais eficiente e é inconveniente para daemons e serviços que não desejam abrir nenhuma janela.</span><span class="sxs-lookup"><span data-stu-id="7711e-108">In Windows, this may not be the most efficient notification mechanism, and is inconvenient for daemons and services that do not want to open any windows.</span></span> <span data-ttu-id="7711e-109">O mecanismo de sinalização de objeto de evento descrito no seguinte é apresentado para resolver esse problema.</span><span class="sxs-lookup"><span data-stu-id="7711e-109">The event object signaling mechanism described in the following is introduced to solve this problem.</span></span>

 

 
