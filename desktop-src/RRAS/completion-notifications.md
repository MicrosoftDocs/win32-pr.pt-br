---
title: Notificações de conclusão
description: O Gerenciador de conexões de acesso remoto continua as notificações de progresso até que a operação de conexão seja concluída.
ms.assetid: 2c3b0d03-1cb7-4fa4-a7fa-bcfe623b791f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4b949eb7dcc0f09d05d2fb272f4f3d36da40fac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005559"
---
# <a name="completion-notifications"></a><span data-ttu-id="b6663-103">Notificações de conclusão</span><span class="sxs-lookup"><span data-stu-id="b6663-103">Completion Notifications</span></span>

<span data-ttu-id="b6663-104">O Gerenciador de conexões de acesso remoto continua as notificações de progresso até que a operação de conexão seja concluída.</span><span class="sxs-lookup"><span data-stu-id="b6663-104">The Remote Access Connection Manager continues progress notifications until the connection operation has been completed.</span></span> <span data-ttu-id="b6663-105">Isso ocorre nas seguintes situações:</span><span class="sxs-lookup"><span data-stu-id="b6663-105">This occurs in the following situations:</span></span>

-   <span data-ttu-id="b6663-106">O manipulador recebe uma \_ notificação RASCS conectada ou RASCS \_ desconectada.</span><span class="sxs-lookup"><span data-stu-id="b6663-106">The handler receives a RASCS\_Connected, or RASCS\_Disconnected notification.</span></span> <span data-ttu-id="b6663-107">O aplicativo cliente RAS pode sair sem interromper nenhuma conexão estabelecida.</span><span class="sxs-lookup"><span data-stu-id="b6663-107">The RAS client application can exit without breaking any established connection.</span></span>
-   <span data-ttu-id="b6663-108">Ocorre um erro.</span><span class="sxs-lookup"><span data-stu-id="b6663-108">An error occurs.</span></span> <span data-ttu-id="b6663-109">O manipulador recebe uma notificação indicando o erro e o estado da conexão quando o erro ocorreu.</span><span class="sxs-lookup"><span data-stu-id="b6663-109">The handler receives a notification indicating the error and the connection state when the error occurred.</span></span> <span data-ttu-id="b6663-110">O aplicativo cliente RAS pode sair.</span><span class="sxs-lookup"><span data-stu-id="b6663-110">The RAS client application can exit.</span></span>

<span data-ttu-id="b6663-111">O aplicativo cliente RAS não deve assumir que a operação de conexão foi concluída após chamar [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa).</span><span class="sxs-lookup"><span data-stu-id="b6663-111">The RAS client application should not assume the connection operation is complete after calling [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa).</span></span> <span data-ttu-id="b6663-112">Ele deve aguardar uma das condições anteriores antes de sair.</span><span class="sxs-lookup"><span data-stu-id="b6663-112">It should wait for one of the preceding conditions before exiting.</span></span>

 

 




