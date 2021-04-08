---
description: Ao longo do tempo, podem existir versões diferentes para aplicativos TAPI, TAPI e provedores de serviços.
ms.assetid: 39b16328-931e-4d75-a6ec-1edc97f1a287
title: Negociação de versão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beffff7ceeb90ccf419e138986562ca90f83c204
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922515"
---
# <a name="version-negotiation"></a><span data-ttu-id="759ee-103">Negociação de versão</span><span class="sxs-lookup"><span data-stu-id="759ee-103">Version Negotiation</span></span>

<span data-ttu-id="759ee-104">Ao longo do tempo, podem existir versões diferentes para aplicativos TAPI, TAPI e provedores de serviços.</span><span class="sxs-lookup"><span data-stu-id="759ee-104">Over time, different versions may exist for TAPI applications, TAPI, and the service providers.</span></span> <span data-ttu-id="759ee-105">A interoperabilidade ideal de um aplicativo TAPI requer conhecimento apenas da versão da TAPI do aplicativo, mas também das versões da DLL TAPI, TAPISVR e provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="759ee-105">Optimal interoperability of a TAPI application requires knowledge of not just the application's TAPI version, but also of the TAPI DLL, TAPISVR, and service provider versions.</span></span>

<span data-ttu-id="759ee-106">A falha na negociação da versão apropriada pode resultar em problemas sérios.</span><span class="sxs-lookup"><span data-stu-id="759ee-106">Failure to do proper version negotiation can result in serious problems.</span></span> <span data-ttu-id="759ee-107">Por exemplo, algumas estruturas muito usadas têm membros de dados adicionados de uma versão para a próxima.</span><span class="sxs-lookup"><span data-stu-id="759ee-107">For example, some heavily used structures have data members added from one version to the next.</span></span> <span data-ttu-id="759ee-108">Se o tamanho da estrutura não corresponder ao que o aplicativo ou a TAPI espera, as consequências vão desde vazamentos de memória até a sincronização intermitente.</span><span class="sxs-lookup"><span data-stu-id="759ee-108">If the structure size does not match what the application or TAPI expects, the consequences range from memory leaks to intermittent AVs.</span></span>

<span data-ttu-id="759ee-109">Para obter informações adicionais, consulte [controle de versão da TAPI](./tapi-versioning.md).</span><span class="sxs-lookup"><span data-stu-id="759ee-109">For additional information, see [TAPI Versioning](./tapi-versioning.md).</span></span>

<span data-ttu-id="759ee-110">**TAPI 2. x:** Os aplicativos negociam com TAPI e TAPISVR durante o [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa).</span><span class="sxs-lookup"><span data-stu-id="759ee-110">**TAPI 2.x:** Applications negotiate with TAPI and TAPISVR during [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa).</span></span> <span data-ttu-id="759ee-111">Os aplicativos executam a negociação de dispositivo com provedores de serviço chamando [**lineNegotiateAPIVersion**](/windows/win32/api/tapi/nf-tapi-linenegotiateapiversion) para cada linha que o aplicativo pode usar.</span><span class="sxs-lookup"><span data-stu-id="759ee-111">Applications perform device negotiation with service providers by calling [**lineNegotiateAPIVersion**](/windows/win32/api/tapi/nf-tapi-linenegotiateapiversion) for each line that the application might use.</span></span>

<span data-ttu-id="759ee-112">**TAPI 3. x:** Não é necessário realizar a negociação de versão; no entanto, você pode usar [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para determinar se uma interface está disponível em sua versão.</span><span class="sxs-lookup"><span data-stu-id="759ee-112">**TAPI 3.x:** There is no need to perform version negotiation; however, you can use [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to determine if an interface is available on their version.</span></span>

 

 
