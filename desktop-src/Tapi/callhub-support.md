---
description: O acompanhamento de CallHub é um novo recurso da TAPI versão 3,0.
ms.assetid: 29b6e585-6da8-46a2-a612-f42d0f65f68e
title: Suporte do CallHub
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9efe6891cfdad956a87745f8e4b35dd117fe775e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758415"
---
# <a name="callhub-support"></a><span data-ttu-id="8ec99-103">Suporte do CallHub</span><span class="sxs-lookup"><span data-stu-id="8ec99-103">CallHub Support</span></span>

<span data-ttu-id="8ec99-104">O acompanhamento de CallHub é um novo recurso da TAPI versão 3,0.</span><span class="sxs-lookup"><span data-stu-id="8ec99-104">CallHub tracking is a new feature in TAPI version 3.0.</span></span> <span data-ttu-id="8ec99-105">A funcionalidade CallHub foi adicionada aos elementos de programação TAPI 2,1 com a entrega do Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="8ec99-105">CallHub functionality was added to the TAPI 2.1 programming elements with the delivery of Windows 2000.</span></span> <span data-ttu-id="8ec99-106">Um *CallHub* representa uma exibição de terceiros de uma chamada, e os identificadores de chamada da TAPI representam a exibição de primeira parte de uma chamada.</span><span class="sxs-lookup"><span data-stu-id="8ec99-106">A *CallHub* represents a third-party view of a call, and TAPI's call handles represent the first-party view of a call.</span></span> <span data-ttu-id="8ec99-107">Com o acompanhamento de CallHub, o provedor de serviços é solicitado a seguir CallHubs e fornecer informações sobre a chamada durante o tempo de vida de um CallHub.</span><span class="sxs-lookup"><span data-stu-id="8ec99-107">With CallHub tracking, the service provider is requested to follow CallHubs and give information about the call during the lifetime of a CallHub.</span></span> <span data-ttu-id="8ec99-108">À medida que novas partes ingressam e deixam o CallHub, o provedor de serviços deve informar a TAPI.</span><span class="sxs-lookup"><span data-stu-id="8ec99-108">As new parties join and leave the CallHub, the service provider should inform TAPI.</span></span>

<span data-ttu-id="8ec99-109">Um provedor de serviços não precisa implementar nenhuma função nova para dar suporte a CallHub.</span><span class="sxs-lookup"><span data-stu-id="8ec99-109">A service provider does not need to implement any new functions in order to support CallHub.</span></span> <span data-ttu-id="8ec99-110">Ele simplesmente precisa preencher o membro **dwCallID** da estrutura [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo) .</span><span class="sxs-lookup"><span data-stu-id="8ec99-110">It simply needs to fill in the **dwCallID** member of the [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo) structure.</span></span> <span data-ttu-id="8ec99-111">Na TAPI 3, a TAPI coleta todas as chamadas com o mesmo **dwCallID** e cria um identificador CallHub que o aplicativo pode usar para rastrear a chamada.</span><span class="sxs-lookup"><span data-stu-id="8ec99-111">In TAPI 3, TAPI collects all calls with the same **dwCallID** and creates a CallHub handle that the application can use to track the call.</span></span>

 

 
