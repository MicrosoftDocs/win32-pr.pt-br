---
description: Os monitores podem examinar quadros no modo somente local ou no modo promíscuo.
ms.assetid: 4646f5bb-e3e3-4929-91b7-f68c5b70ccb3
title: Modos Local-Only e promíscuo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd1188760d8de31836de3fbd437854a5df138402
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753248"
---
# <a name="local-only-and-promiscuous-modes"></a><span data-ttu-id="4d781-103">Modos Local-Only e promíscuo</span><span class="sxs-lookup"><span data-stu-id="4d781-103">Local-Only and Promiscuous Modes</span></span>

<span data-ttu-id="4d781-104">Os monitores podem examinar quadros no modo somente local ou no modo promíscuo.</span><span class="sxs-lookup"><span data-stu-id="4d781-104">Monitors can examine frames in local-only mode or promiscuous mode.</span></span>

<span data-ttu-id="4d781-105">No modo somente local, o NPP (provedor de pacotes de rede) retorna os quadros que são enviados de ou para o computador no qual o monitor está em execução, incluindo difusões e multicast direcionados para o computador local.</span><span class="sxs-lookup"><span data-stu-id="4d781-105">In local-only mode, the network packet provider (NPP) returns frames that are sent to or from the computer on which the monitor is running, including broadcasts and multicasts directed to the local machine.</span></span> <span data-ttu-id="4d781-106">Embora seja limitado a quadros direcionados localmente, o modo local também é muito menos intensivo do processador.</span><span class="sxs-lookup"><span data-stu-id="4d781-106">Although limited to locally directed frames, local-mode is also much less processor intensive.</span></span>

<span data-ttu-id="4d781-107">No modo promíscuo, o monitor também pode observar o tráfego que não é direcionado para ou do computador local.</span><span class="sxs-lookup"><span data-stu-id="4d781-107">In promiscuous mode, the monitor can also watch for traffic that is not directed to or from the local computer.</span></span> <span data-ttu-id="4d781-108">A menos que o monitor tenha especificado o sinalizador \_ , \_ o MCS Create pmode não é \_ \_ necessário, na função [OnLoadingDLL](onloadingdll.md) , o serviço de controle de monitor (MCSVC) pressupõe que o monitor requer o modo promíscuo ao carregar a DLL do monitor.</span><span class="sxs-lookup"><span data-stu-id="4d781-108">Unless the monitor has specified the flag, MCS\_CREATE\_PMODE\_NOT\_REQUIRED, in the [OnLoadingDLL](onloadingdll.md) function, the Monitor Control Service (MCSVC) assumes that the monitor requires promiscuous mode when it loads the monitor DLL.</span></span>

 

 



