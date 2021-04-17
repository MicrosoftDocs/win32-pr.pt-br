---
description: No Microsoft Telephony, os provedores de serviços de telefonia são executados em um processo separado de aplicativos de telefonia.
ms.assetid: ccc40d3c-6764-469a-baac-fa625d664ea7
title: A interface DLL da interface do usuário do provedor de serviços de telefonia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdab33dd9c9630aed7d7aed168982cfac2daee2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811919"
---
# <a name="the-telephony-service-provider-ui-dll-interface"></a><span data-ttu-id="e7895-103">A interface DLL da interface do usuário do provedor de serviços de telefonia</span><span class="sxs-lookup"><span data-stu-id="e7895-103">The Telephony Service Provider UI DLL Interface</span></span>

<span data-ttu-id="e7895-104">No Microsoft Telephony, os provedores de serviços de telefonia são executados em um processo separado de aplicativos de telefonia.</span><span class="sxs-lookup"><span data-stu-id="e7895-104">In Microsoft Telephony, telephony service providers execute in a separate process from telephony applications.</span></span> <span data-ttu-id="e7895-105">Os provedores de serviço se comunicam com o TAPISRV por meio da TSPI (interface do provedor de serviços de telefonia) e executam em seu processo; interface de aplicativos para TAPI, que são carregados no contexto do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e7895-105">Service providers communicate with TAPISRV through the Telephony service provider interface (TSPI) and execute in its process; applications interface to TAPI, which are loaded in the application context.</span></span>

<span data-ttu-id="e7895-106">Os componentes da TAPI usam vários mecanismos de comunicação entre processos para transmitir solicitações de função e mensagens entre aplicativos e provedores de serviço.</span><span class="sxs-lookup"><span data-stu-id="e7895-106">The components of TAPI use various interprocess communications mechanisms to convey function requests and messages between applications and service providers.</span></span> <span data-ttu-id="e7895-107">Os aplicativos e os provedores de serviços podem estar sendo executados não apenas em processos separados, mas em sistemas completamente separados.</span><span class="sxs-lookup"><span data-stu-id="e7895-107">The applications and the service providers may be executing not only in separate processes, but on completely separate systems.</span></span> <span data-ttu-id="e7895-108">Os provedores de serviço, portanto, não podem exibir caixas de diálogo no processo ou mesmo no computador no qual estão sendo executados; A interface do usuário deve ser chamada de dentro do contexto do aplicativo, no computador no qual o aplicativo está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="e7895-108">Service providers therefore cannot display dialog boxes in the process or even on the computer on which they are executing; UI must be invoked from within the application context, on the computer on which the application is executing.</span></span>

<span data-ttu-id="e7895-109">Esta seção define o mecanismo pelo qual as funções de interface do usuário do provedor de serviços são carregadas e invocadas dentro do contexto do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e7895-109">This section defines the mechanism by which service provider UI functions are loaded and invoked within the application context.</span></span> <span data-ttu-id="e7895-110">Um mecanismo também é definido por meio do qual os provedores de serviço podem abrir espontaneamente caixas de diálogo no contexto do aplicativo, quando não seriam esperados pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e7895-110">A mechanism is also defined by which service providers can spontaneously open dialog boxes in the application context when they would not otherwise be expected by the application.</span></span> <span data-ttu-id="e7895-111">Um exemplo desse último caso seria a caixa de diálogo de **fala/desligamento** que é exibida por um provedor de serviços de modem de dados quando o modem está sendo usado como um discador para chamadas de voz interativas, e o usuário deve ser instruído a pegar o telefone e informar ao provedor de serviços quando colocar o modem onhook.</span><span class="sxs-lookup"><span data-stu-id="e7895-111">An example of this latter case would be the **Talk/Hangup** dialog box that is displayed by a data modem service provider when the modem is being used as a dialer for interactive voice calls, and the user must be told to pick up the phone and inform the service provider when to place the modem onhook.</span></span>

 

 



