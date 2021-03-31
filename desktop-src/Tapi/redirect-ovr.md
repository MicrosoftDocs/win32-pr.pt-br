---
description: O redirecionamento de sessão permite que um aplicativo desviar uma sessão oferecida para outro endereço sem responder à chamada.
ms.assetid: b52cd5c2-fdd6-4240-b07b-b22733a89d27
title: Redirecionar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 100ade9315c3b5e8e68c17bf34a0b6d54a9d9663
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663591"
---
# <a name="redirect"></a><span data-ttu-id="7e0c8-103">Redirecionar</span><span class="sxs-lookup"><span data-stu-id="7e0c8-103">Redirect</span></span>

<span data-ttu-id="7e0c8-104">O redirecionamento de sessão permite que um aplicativo desviar uma sessão oferecida para outro endereço sem responder à chamada.</span><span class="sxs-lookup"><span data-stu-id="7e0c8-104">Session redirection allows an application to deflect an offered session to another address without answering the call.</span></span> <span data-ttu-id="7e0c8-105">O aplicativo pode fazer o redirecionamento em uma base chamada por chamada.</span><span class="sxs-lookup"><span data-stu-id="7e0c8-105">The application can do redirection on a call-by-call basis.</span></span> <span data-ttu-id="7e0c8-106">Por exemplo, um aplicativo pode permitir que um usuário especifique diferentes redirecionamentos com base nas informações de ID do chamador.</span><span class="sxs-lookup"><span data-stu-id="7e0c8-106">For example, an application might allow a user to specify different redirections based on caller ID information.</span></span> <span data-ttu-id="7e0c8-107">Depois que uma chamada for redirecionada com êxito, o estado normalmente será transferido para ocioso e os recursos associados deverão ser liberados.</span><span class="sxs-lookup"><span data-stu-id="7e0c8-107">After a call has been successfully redirected, the state typically transitions to idle and associated resources must be released.</span></span>

<span data-ttu-id="7e0c8-108">O redirecionamento difere do [encaminhamento](forward-ovr.md) , uma vez que o encaminhamento foi configurado, a operação é executada pela TAPI, pelo provedor de serviços ou pela opção sem envolvimento adicional do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7e0c8-108">Redirect differs from [forward](forward-ovr.md) in that once forwarding has been set up, the operation is performed by TAPI, the service provider, or the switch without further involvement of the application.</span></span> <span data-ttu-id="7e0c8-109">O redirecionamento difere da [transferência](transfer-ovr.md) , pois o redirecionamento não requer a resposta da chamada primeiro.</span><span class="sxs-lookup"><span data-stu-id="7e0c8-109">Redirect differs from [transfer](transfer-ovr.md) in that redirect does not require answering the call first.</span></span>

<span data-ttu-id="7e0c8-110">Nem todos os provedores de serviço dão suporte ao uso desta operação.</span><span class="sxs-lookup"><span data-stu-id="7e0c8-110">Not all service providers support use of this operation.</span></span>

<span data-ttu-id="7e0c8-111">**TAPI 2. x:** Consulte [**lineRedirect**](/windows/win32/api/tapi/nf-tapi-lineredirect).</span><span class="sxs-lookup"><span data-stu-id="7e0c8-111">**TAPI 2.x:** See [**lineRedirect**](/windows/win32/api/tapi/nf-tapi-lineredirect).</span></span>

 

 
