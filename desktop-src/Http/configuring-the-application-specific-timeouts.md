---
title: Configurando os tempos limite específicos do aplicativo
description: .
ms.assetid: 24526320-4174-4fc7-b45a-c1ec605e1666
keywords:
- Configurando o tempo limite de HTTP específico do aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35827b797ad6c9f19b728064f6fe65b0d89b2a3b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005457"
---
# <a name="configuring-the-application-specific-timeouts"></a><span data-ttu-id="c23aa-104">Configurando os tempos limite específicos do aplicativo</span><span class="sxs-lookup"><span data-stu-id="c23aa-104">Configuring the Application Specific Timeouts</span></span>

<span data-ttu-id="c23aa-105">As configurações de toda a API do servidor HTTP se aplicam a todas as sessões de servidor e a grupos de URLs no computador.</span><span class="sxs-lookup"><span data-stu-id="c23aa-105">The HTTP Server API-wide settings apply to all the server sessions and URL groups on the computer.</span></span> <span data-ttu-id="c23aa-106">Essas configurações podem ser substituídas pelo aplicativo definindo os valores de tempo limite específicos do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c23aa-106">These configurations can be overridden by the application by setting the application-specific timeout values.</span></span> <span data-ttu-id="c23aa-107">Os tempos limite da sessão do servidor substituem os tempos limite de toda a API do servidor HTTP e se aplicam a todos os grupos de URLs criados sob eles.</span><span class="sxs-lookup"><span data-stu-id="c23aa-107">The server session timeouts override the HTTP Server API-wide timeouts and apply to all the URL groups created under them.</span></span> <span data-ttu-id="c23aa-108">Configurar a propriedade timeouts em um grupo de URLs substitui os tempos limite de sessão de servidor para todas as URLs no grupo.</span><span class="sxs-lookup"><span data-stu-id="c23aa-108">Configuring the timeouts property on a URL group overrides the server session timeouts for all the URLs in the group.</span></span>

<span data-ttu-id="c23aa-109">A especificação de zero para qualquer um dos temporizadores na estrutura de [**\_ informações de \_ limite \_ de tempo limite http**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) para um grupo de URLs faz com que a API do servidor http reverta para os tempos limite da sessão do servidor, se existirem, ou as configurações padrão da API do servidor http se os tempos limite da sessão do servidor não existirem.</span><span class="sxs-lookup"><span data-stu-id="c23aa-109">Specifying zero for any of the timers in the [**HTTP\_TIMEOUT\_LIMIT\_INFO**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) structure for a URL group causes the HTTP Server API to revert to the server session timeouts, if they exist, or the HTTP Server API default settings if the server session timeouts do not exist.</span></span> <span data-ttu-id="c23aa-110">Por exemplo, quando a Propriedade Timeout do servidor está presente em um grupo de URLs e o temporizador **EntityBody** é zero, o tempo limite da sessão do servidor é usado.</span><span class="sxs-lookup"><span data-stu-id="c23aa-110">For example, when the server timeout property is present on a URL group and the **EntityBody** timer is zero, the server session timeout is used.</span></span> <span data-ttu-id="c23aa-111">Se a propriedade timeouts não estiver definida em uma sessão de servidor, a configuração padrão da API do servidor HTTP será usada.</span><span class="sxs-lookup"><span data-stu-id="c23aa-111">If the timeouts property is not set on a server session, the HTTP Server API default configuration is used.</span></span> <span data-ttu-id="c23aa-112">Para desabilitar um temporizador, defina o valor como **MAXUSHORT**, exceto para o temporizador **MinSendRate** que está definido como **MAXULONG**.</span><span class="sxs-lookup"><span data-stu-id="c23aa-112">To disable a timer, set the value to **MAXUSHORT**, except for the **MinSendRate** timer which is set to **MAXULONG**.</span></span>

<span data-ttu-id="c23aa-113">A API do servidor HTTP só pode configurar o **HeaderWait** específico do aplicativo e os temporizadores **IdleConnection** são efetivos somente depois que a primeira solicitação é recebida.</span><span class="sxs-lookup"><span data-stu-id="c23aa-113">The HTTP Server API can only configure the application-specific **HeaderWait** and the **IdleConnection** timers are only effective after the first request has been received.</span></span> <span data-ttu-id="c23aa-114">Antes que a primeira solicitação seja recebida, os valores de tempo limite de toda a API do servidor HTTP são aplicados.</span><span class="sxs-lookup"><span data-stu-id="c23aa-114">Before the first request is received, the HTTP Server API-wide timeout values are enforced.</span></span> <span data-ttu-id="c23aa-115">Depois que a primeira solicitação chega e é associada a uma fila de solicitações, os temporizadores **HeaderWait** e **IdleConnection** específicos do aplicativo podem ser aplicados.</span><span class="sxs-lookup"><span data-stu-id="c23aa-115">After the first request arrives and is associated with a request queue, the application-specific **HeaderWait** and **IdleConnection** timers can be applied.</span></span> <span data-ttu-id="c23aa-116">Os temporizadores específicos do aplicativo são aplicados a todas as solicitações subsequentes que chegam na fila de solicitações para uma conexão Keep-Alive.</span><span class="sxs-lookup"><span data-stu-id="c23aa-116">The application-specific timers are applied to all subsequent requests that arrive on the request queue for a keep-alive connection.</span></span>

<span data-ttu-id="c23aa-117">Para obter mais informações sobre como configurar temporizadores, consulte os tópicos [Configurando o grupo de URLs](configuring-the-url-group.md) e [Configurando a sessão de servidor](configuring-the-server-session.md) .</span><span class="sxs-lookup"><span data-stu-id="c23aa-117">For more information about configuring timers, see the [Configuring the URL Group](configuring-the-url-group.md) and [Configuring the Server Session](configuring-the-server-session.md) topics.</span></span>

 

 




