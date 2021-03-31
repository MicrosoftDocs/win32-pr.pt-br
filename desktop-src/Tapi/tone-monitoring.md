---
description: O monitoramento de Tom monitora o fluxo de mídia de uma chamada para os tons especificados.
ms.assetid: c3218013-b71f-41cd-9397-ba717c0cf556
title: Monitoramento de Tom
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9a3275e5207999896792ee04dc1842b01f4ad0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011132"
---
# <a name="tone-monitoring"></a><span data-ttu-id="266d9-103">Monitoramento de Tom</span><span class="sxs-lookup"><span data-stu-id="266d9-103">Tone Monitoring</span></span>

<span data-ttu-id="266d9-104">O monitoramento de Tom monitora o fluxo de mídia de uma chamada para os tons especificados.</span><span class="sxs-lookup"><span data-stu-id="266d9-104">Tone monitoring monitors the media stream of a call for specified tones.</span></span> <span data-ttu-id="266d9-105">Um tom é descrito por suas frequências e cadência de componentes.</span><span class="sxs-lookup"><span data-stu-id="266d9-105">A tone is described by its component frequencies and cadence.</span></span> <span data-ttu-id="266d9-106">Uma implementação da API pode permitir que vários tons diferentes sejam monitorados simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="266d9-106">An implementation of the API may allow several different tones to be monitored simultaneously.</span></span> <span data-ttu-id="266d9-107">Um aplicativo pode marcar cada tom para poder distinguir os diferentes tons para os quais ele solicita a detecção.</span><span class="sxs-lookup"><span data-stu-id="266d9-107">An application can tag each tone to be able to distinguish the different tones for which it requests detection.</span></span>

<span data-ttu-id="266d9-108">Um aplicativo pode habilitar ou desabilitar o monitoramento de Tom em uma chamada especificada com [**lineMonitorTones**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones).</span><span class="sxs-lookup"><span data-stu-id="266d9-108">An application can enable or disable tone monitoring on a specified call with [**lineMonitorTones**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones).</span></span> <span data-ttu-id="266d9-109">Com essa função, o aplicativo indica quais tons detectar em uma chamada especificada.</span><span class="sxs-lookup"><span data-stu-id="266d9-109">With this function, the application indicates which tones to detect on a specified call.</span></span> <span data-ttu-id="266d9-110">Quando o monitoramento de Tom está habilitado, os dígitos detectados fazem com que o aplicativo seja notificado com a mensagem de [**linha \_ MONITORTONE**](line-monitortone.md) .</span><span class="sxs-lookup"><span data-stu-id="266d9-110">When tone monitoring is enabled, detected digits cause the application to be notified with the [**LINE\_MONITORTONE**](line-monitortone.md) message.</span></span> <span data-ttu-id="266d9-111">Essa mensagem fornece o identificador de chamada no qual o Tom foi detectado, bem como a marca do aplicativo para o Tom.</span><span class="sxs-lookup"><span data-stu-id="266d9-111">This message provides the call handle on which the tone was detected as well as the application's tag for the tone.</span></span>

<span data-ttu-id="266d9-112">O escopo do monitoramento de Tom é associado pelo tempo de vida da chamada.</span><span class="sxs-lookup"><span data-stu-id="266d9-112">The scope of tone monitoring is bound by the lifetime of the call.</span></span> <span data-ttu-id="266d9-113">O monitoramento de Tom em uma chamada termina assim que a chamada é *desconectada* ou fica *ociosa*.</span><span class="sxs-lookup"><span data-stu-id="266d9-113">Tone monitoring on a call ends as soon the call *disconnects* or goes *idle*.</span></span>

> [!Note]  
> <span data-ttu-id="266d9-114">O monitoramento de tons, dígitos ou tipos de mídia geralmente requer o uso de recursos dos quais o provedor de serviços pode ter apenas um valor finito.</span><span class="sxs-lookup"><span data-stu-id="266d9-114">The monitoring of tones, digits, or media types often requires the use of resources of which the service provider can only have a finite amount.</span></span> <span data-ttu-id="266d9-115">Uma solicitação de monitoramento poderá ser rejeitada se os recursos não estiverem disponíveis.</span><span class="sxs-lookup"><span data-stu-id="266d9-115">A request for monitoring can be rejected if resources are not available.</span></span> <span data-ttu-id="266d9-116">Pelo mesmo motivo, um aplicativo deve desabilitar qualquer monitoramento desnecessário.</span><span class="sxs-lookup"><span data-stu-id="266d9-116">For the same reason, an application should disable any unnecessary monitoring.</span></span>

 

 

 



