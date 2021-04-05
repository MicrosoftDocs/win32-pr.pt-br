---
title: Autorização de serviço
description: Um aplicativo pode implementar a autorização personalizada para mensagens de entrada em um host de serviço.
ms.assetid: 75bcf051-3983-48fc-8121-0984ac9cdcb9
keywords:
- Serviços Web de autorização de serviço para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c296dc6b4900bd20df7d1e70631e758599a0028d
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104085002"
---
# <a name="service-authorization"></a><span data-ttu-id="09a0a-106">Autorização de serviço</span><span class="sxs-lookup"><span data-stu-id="09a0a-106">Service Authorization</span></span>

<span data-ttu-id="09a0a-107">Um aplicativo pode implementar a autorização personalizada para mensagens de entrada em um host de serviço.</span><span class="sxs-lookup"><span data-stu-id="09a0a-107">An application can implement custom authorization for incoming messages on a service host .</span></span>


<span data-ttu-id="09a0a-108">Um host de serviço recebe um [**retorno de \_ \_ \_ chamada**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback) de segurança de serviço WS de retorno de chamada como parte do [**ponto de \_ \_ extremidade do serviço WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) , que é passado para a função [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) .</span><span class="sxs-lookup"><span data-stu-id="09a0a-108">A service host receives a security callback [**WS\_SERVICE\_SECURITY\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback) as part of the [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) which is passed to the [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) function.</span></span> <span data-ttu-id="09a0a-109">Esse retorno de chamada é invocado quando a [ \_ mensagem WS](ws-message.md) é recebida.</span><span class="sxs-lookup"><span data-stu-id="09a0a-109">This callback is invoked when the [WS\_MESSAGE](ws-message.md) is received.</span></span>

<span data-ttu-id="09a0a-110">O aplicativo pode contar com esse retorno de chamada para implementar a autorização personalizada para mensagens de entrada no host de serviço.</span><span class="sxs-lookup"><span data-stu-id="09a0a-110">The application can rely on this callback to implement custom authorization for incoming messages on the service host.</span></span> <span data-ttu-id="09a0a-111">Se a autorização falhar, a função de retorno de chamada de segurança retornará um HR de falha e o host de serviço abortará o canal.</span><span class="sxs-lookup"><span data-stu-id="09a0a-111">If the authorization fails the security callback function returns a failure HR, and the service host aborts the channel.</span></span>

<span data-ttu-id="09a0a-112">Consulte o nome de usuário sobre SSL example, [HttpCalculatorWithUserNameOverSslServiceExample](httpcalculatorwithusernameoversslserviceexample.md), para obter um exemplo de implementação.</span><span class="sxs-lookup"><span data-stu-id="09a0a-112">See the user name over SSL example, [HttpCalculatorWithUserNameOverSslServiceExample](httpcalculatorwithusernameoversslserviceexample.md), for an example implementation.</span></span>

 

 




