---
description: O Windows 10 ajuda seu aplicativo a otimizar o consumo de energia quando ele está em execução em um dispositivo móvel.
ms.assetid: a956b88c-8a75-4c1c-af27-53c69feb1596
title: Novidades no gerenciamento de energia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e6c8394c2e5e6750b5d01fd997d374a9f87e10d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105775666"
---
# <a name="whats-new-in-power-management"></a><span data-ttu-id="b0609-103">Novidades do gerenciamento de energia</span><span class="sxs-lookup"><span data-stu-id="b0609-103">What's New in Power Management</span></span>

<span data-ttu-id="b0609-104">O Windows 10 ajuda seu aplicativo a otimizar o consumo de energia quando ele está em execução em um dispositivo móvel.</span><span class="sxs-lookup"><span data-stu-id="b0609-104">Windows 10 helps your application optimize power consumption when it's running on a mobile device.</span></span>

## <a name="battery-saver"></a><span data-ttu-id="b0609-105">Economia de bateria</span><span class="sxs-lookup"><span data-stu-id="b0609-105">Battery saver</span></span>

<span data-ttu-id="b0609-106">Nesta versão, seu aplicativo poderá ser notificado quando a economia de bateria estiver ativada ou desativada.</span><span class="sxs-lookup"><span data-stu-id="b0609-106">In this release, your application can be notified when battery saver is turned on or off.</span></span> <span data-ttu-id="b0609-107">Ao responder às condições de energia em constante mudança, seu aplicativo pode trabalhar em conjunto com a economia de bateria para economizar energia e ajudar a estender a vida útil da bateria.</span><span class="sxs-lookup"><span data-stu-id="b0609-107">By responding to changing power conditions, your application can work in concert with battery saver to save energy and help extend battery life.</span></span> <span data-ttu-id="b0609-108">Para obter informações gerais sobre a economia de bateria, consulte [economia de bateria (nas diretrizes de componente de hardware)](/windows-hardware/design/component-guidelines/battery-saver).</span><span class="sxs-lookup"><span data-stu-id="b0609-108">For general information about battery saver, see [battery saver (in the hardware component guidelines)](/windows-hardware/design/component-guidelines/battery-saver).</span></span>

-   <span data-ttu-id="b0609-109">[**GUID \_ do \_ \_ Status de economia de energia**](power-setting-guids.md) : Use esse novo GUID com a função [**PowerSettingRegisterNotification**](/windows/desktop/api/Powersetting/nf-powersetting-powersettingregisternotification) para ser notificado quando a economia de bateria estiver ativada ou desativada.</span><span class="sxs-lookup"><span data-stu-id="b0609-109">[**GUID\_POWER\_SAVING\_STATUS**](power-setting-guids.md) : Use this new GUID with the [**PowerSettingRegisterNotification**](/windows/desktop/api/Powersetting/nf-powersetting-powersettingregisternotification) function to be notified when battery saver is turned on or off.</span></span>

-   <span data-ttu-id="b0609-110">[**Sistema \_ \_Status de energia**](/windows/desktop/api/Winbase/ns-winbase-system_power_status) : essa estrutura foi atualizada para dar suporte à economia de bateria.</span><span class="sxs-lookup"><span data-stu-id="b0609-110">[**SYSTEM\_POWER\_STATUS**](/windows/desktop/api/Winbase/ns-winbase-system_power_status) : This structure has been updated to support battery saver.</span></span> <span data-ttu-id="b0609-111">O quarto membro, **SystemStatusFlag** (anteriormente chamado de **Reserved1**), agora indica se a economia de bateria está encarregado ou não.</span><span class="sxs-lookup"><span data-stu-id="b0609-111">The fourth member, **SystemStatusFlag** (previously named **Reserved1**), now indicates if battery saver is engaged or not.</span></span> <span data-ttu-id="b0609-112">Use a função [**GetSystemPowerStatus**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus) para recuperar um ponteiro para essa estrutura.</span><span class="sxs-lookup"><span data-stu-id="b0609-112">Use the [**GetSystemPowerStatus**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus) function to retrieve a pointer to this structure.</span></span>

 

 
