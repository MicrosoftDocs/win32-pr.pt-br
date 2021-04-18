---
description: Se um aplicativo não quiser nenhuma interferência por eventos externos para uma sessão da TAPI ou do provedor de serviços, ele deverá proteger a chamada.
ms.assetid: 0a3be209-e3ff-4177-abb2-ad0facbdf569
title: Proteger uma sessão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00b1567303efb61f28f9c6b3e92c24287d23d4af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105792614"
---
# <a name="secure-a-session"></a><span data-ttu-id="b8c58-103">Proteger uma sessão</span><span class="sxs-lookup"><span data-stu-id="b8c58-103">Secure a Session</span></span>

<span data-ttu-id="b8c58-104">Se um aplicativo não quiser nenhuma interferência por eventos externos para uma sessão da TAPI ou do provedor de serviços, ele deverá proteger a chamada.</span><span class="sxs-lookup"><span data-stu-id="b8c58-104">If an application does not want any interference by outside events for a session from TAPI or the service provider, it should secure the call.</span></span> <span data-ttu-id="b8c58-105">Por exemplo, em uma chamada de ambiente analógico, os tons de espera podem destruir uma sessão de fax ou modem na chamada original.</span><span class="sxs-lookup"><span data-stu-id="b8c58-105">For example, in an analog environment call-waiting tones can destroy a fax or modem session on the original call.</span></span>

<span data-ttu-id="b8c58-106">Um aplicativo pode proteger uma chamada no momento em que a chamada é feita ou após a chamada já existir.</span><span class="sxs-lookup"><span data-stu-id="b8c58-106">An application can secure a call at the time the call is made or after the call already exists.</span></span>

<span data-ttu-id="b8c58-107">Nem todos os provedores de serviço dão suporte ao uso desta operação.</span><span class="sxs-lookup"><span data-stu-id="b8c58-107">Not all service providers support use of this operation.</span></span>

<span data-ttu-id="b8c58-108">**TAPI 2. x:** Consulte [**lineSecureCall**](/windows/win32/api/tapi/nf-tapi-linesecurecall).</span><span class="sxs-lookup"><span data-stu-id="b8c58-108">**TAPI 2.x:** See [**lineSecureCall**](/windows/win32/api/tapi/nf-tapi-linesecurecall).</span></span>

<span data-ttu-id="b8c58-109">**TAPI 3. x:** Consulte [**ITAddress:: forward**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward).</span><span class="sxs-lookup"><span data-stu-id="b8c58-109">**TAPI 3.x:** See [**ITAddress::Forward**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward).</span></span>

 

 
