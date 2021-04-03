---
title: Serviços críticos do sistema
description: Serviços críticos do sistema não podem ser interrompidos e reiniciados pelo Gerenciador de reinicialização sem a reinicialização do sistema. As atualizações em qualquer arquivo ou recurso em uso por um desses serviços exigem uma reinicialização do sistema.
ms.assetid: 8db7c91c-2f96-4d0c-a5b8-59c41a7e4845
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14a8fcc921d065dda0670e27e240c93515bc8cb9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006211"
---
# <a name="critical-system-services"></a><span data-ttu-id="39a2f-104">Serviços críticos do sistema</span><span class="sxs-lookup"><span data-stu-id="39a2f-104">Critical System Services</span></span>

<span data-ttu-id="39a2f-105">Serviços críticos do sistema não podem ser interrompidos e reiniciados pelo Gerenciador de reinicialização sem a reinicialização do sistema.</span><span class="sxs-lookup"><span data-stu-id="39a2f-105">Critical system services cannot be stopped and restarted by the Restart Manager without a system restart.</span></span> <span data-ttu-id="39a2f-106">As atualizações em qualquer arquivo ou recurso em uso por um desses serviços exigem uma reinicialização do sistema.</span><span class="sxs-lookup"><span data-stu-id="39a2f-106">Updates to any file or resource in use by one of these services requires a system restart.</span></span>

<span data-ttu-id="39a2f-107">**Para determinar se um processo é um serviço de sistema crítico.**</span><span class="sxs-lookup"><span data-stu-id="39a2f-107">**To determine whether a process is a critical system service.**</span></span>

1.  <span data-ttu-id="39a2f-108">Registre o processo usando a função [**RmRegisterResources**](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources) .</span><span class="sxs-lookup"><span data-stu-id="39a2f-108">Register the process using the [**RmRegisterResources**](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources) function.</span></span>
2.  <span data-ttu-id="39a2f-109">Chame a função [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) para obter a estrutura de [**\_ \_ informações do processo do RM**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) .</span><span class="sxs-lookup"><span data-stu-id="39a2f-109">Call the [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) function to get the [**RM\_PROCESS\_INFO**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) structure.</span></span>
3.  <span data-ttu-id="39a2f-110">O membro **ApplicationType** da estrutura de [**\_ \_ informações do processo RM**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) retornado contém um valor de enumeração de [**\_ \_ tipo de aplicativo RM**](/windows/desktop/api/RestartManager/ne-restartmanager-rm_app_type) .</span><span class="sxs-lookup"><span data-stu-id="39a2f-110">The **ApplicationType** member of the returned [**RM\_PROCESS\_INFO**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) structure contains a [**RM\_APP\_TYPE**](/windows/desktop/api/RestartManager/ne-restartmanager-rm_app_type) enumeration value.</span></span> <span data-ttu-id="39a2f-111">Esse valor é definido como **RmCriticial** para um processo crítico do sistema.</span><span class="sxs-lookup"><span data-stu-id="39a2f-111">This value is set to **RmCriticial** for a critical system process.</span></span>

<span data-ttu-id="39a2f-112">Os serviços críticos do sistema incluem smss.exe, csrss.exe, wininit.exe, logonui.exe, lsass.exe, services.exe, winlogon.exe, sistema, svchost.exe com RPCSs e svchost.exe com DCOM/PnP.</span><span class="sxs-lookup"><span data-stu-id="39a2f-112">Critical system services include smss.exe, csrss.exe, wininit.exe, logonui.exe, lsass.exe, services.exe, winlogon.exe, System, svchost.exe with RPCSS, and svchost.exe with Dcom/PnP.</span></span>

 

 




