---
description: Os monitores são projetados para usar Instrumentação de Gerenciamento do Windows (WMI) para acionar eventos em computadores locais ou remotos.
ms.assetid: b20746dd-d8d9-49b6-95b7-5151ee02901d
title: Monitorar eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d98241081d8a59c33ab173447eaedd903e72eb09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461166"
---
# <a name="monitor-events"></a><span data-ttu-id="e16e5-103">Monitorar eventos</span><span class="sxs-lookup"><span data-stu-id="e16e5-103">Monitor Events</span></span>

<span data-ttu-id="e16e5-104">Os monitores são projetados para usar [Instrumentação de gerenciamento do Windows](/windows/desktop/WmiSdk/wmi-start-page) (WMI) para acionar eventos em computadores locais ou remotos.</span><span class="sxs-lookup"><span data-stu-id="e16e5-104">Monitors are designed to use [Windows Management Instrumentation](/windows/desktop/WmiSdk/wmi-start-page) (WMI) to fire events to local or remote computers.</span></span>

> [!Note]  
> <span data-ttu-id="e16e5-105">Como os monitores usam uma captura em tempo real, eles só podem capturar dados no computador local.</span><span class="sxs-lookup"><span data-stu-id="e16e5-105">Because monitors use a real-time capture they can only capture data at the local computer.</span></span> <span data-ttu-id="e16e5-106">Essa é uma limitação da interface **IRTC** do provedor de pacotes de rede.</span><span class="sxs-lookup"><span data-stu-id="e16e5-106">This is a limitation of the network packet provider's **IRTC** interface.</span></span> <span data-ttu-id="e16e5-107">No entanto, usando eventos WMI, os dados capturados podem ser examinados localmente enquanto os eventos podem ser enviados a computadores locais ou remotos.</span><span class="sxs-lookup"><span data-stu-id="e16e5-107">However, by using WMI events, the captured data can be examined locally while events can be sent to local or remote computers.</span></span>

 

<span data-ttu-id="e16e5-108">Os monitores não se comunicam diretamente com o WMI.</span><span class="sxs-lookup"><span data-stu-id="e16e5-108">Monitors do not communicate directly with WMI.</span></span> <span data-ttu-id="e16e5-109">O [*serviço de controle de monitor*](m.md) (MCSVC) fornece uma interface (chamada de [IMonitorEventer](imonitoreventer.md)), que o monitor pode usar para obter uma estrutura de dados de evento e preenchê-la com as informações relevantes.</span><span class="sxs-lookup"><span data-stu-id="e16e5-109">The [*Monitor Control Service*](m.md) (MCSVC) provides an interface (called [IMonitorEventer](imonitoreventer.md)), which the monitor can use to obtain an event data structure and fill it with the relevant information.</span></span> <span data-ttu-id="e16e5-110">O MCSVC pode então enviar a estrutura de dados de evento para o WMI que, por sua vez, dispara o evento.</span><span class="sxs-lookup"><span data-stu-id="e16e5-110">The MCSVC can then send the event data structure to WMI, which in turn fires the event.</span></span>

 

 
