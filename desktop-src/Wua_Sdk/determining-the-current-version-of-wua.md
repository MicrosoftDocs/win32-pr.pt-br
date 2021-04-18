---
description: Determine a versão do WUA (agente de Windows Update) antes de usá-lo.
ms.assetid: fc915535-f87d-43fb-8755-fa6c80fedea5
title: Determinando a versão atual do WUA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af79371839bb621bed9eea199817c0fd9fe7fd8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760661"
---
# <a name="determining-the-current-version-of-wua"></a><span data-ttu-id="b9310-103">Determinando a versão atual do WUA</span><span class="sxs-lookup"><span data-stu-id="b9310-103">Determining the Current Version of WUA</span></span>

<span data-ttu-id="b9310-104">Para obter informações gerais sobre como atualizar o WUA, incluindo instruções passo a passo para determinar programaticamente de dentro de seu aplicativo se a versão do WUA em execução no computador atende às suas necessidades, consulte [atualizando o agente de Windows Update](updating-the-windows-update-agent.md).</span><span class="sxs-lookup"><span data-stu-id="b9310-104">For general information on updating the WUA, including step by step instructions to programmatically determine from within your app whether the version of WUA that is running on the computer meets your needs, see [Updating the Windows Update Agent](updating-the-windows-update-agent.md).</span></span>

<span data-ttu-id="b9310-105">Nas versões do Windows anteriores ao Windows 7 e ao Windows Server 2008 R2, você deve determinar a versão instalada do WUA (agente de Windows Update) antes de usá-lo.</span><span class="sxs-lookup"><span data-stu-id="b9310-105">On versions of Windows prior to Windows 7 and Windows Server 2008 R2, you should determine the installed version of Windows Update Agent (WUA) before you use it.</span></span> <span data-ttu-id="b9310-106">A versão atual do WUA é determinada pela versão do Wuaueng.dll que está em execução no \\ subdiretório system32 da instalação atual do Windows.</span><span class="sxs-lookup"><span data-stu-id="b9310-106">The current version of WUA is determined by the version of the Wuaueng.dll that is running in the \\System32 subdirectory of the current Windows installation.</span></span> <span data-ttu-id="b9310-107">Se a versão do Wuaueng.dll for a versão 5.4.3790.1000 ou posterior, o WUA será instalado.</span><span class="sxs-lookup"><span data-stu-id="b9310-107">If the version of Wuaueng.dll is version 5.4.3790.1000 or a later version, WUA is installed.</span></span> <span data-ttu-id="b9310-108">Uma versão anterior a 5.4.3790.1000 indica que o SUS (Software Update Services) 1,0 está instalado.</span><span class="sxs-lookup"><span data-stu-id="b9310-108">A version that is earlier than 5.4.3790.1000 indicates that Software Update Services (SUS) 1.0 is installed.</span></span>

<span data-ttu-id="b9310-109">Quando é feita uma chamada ao SUS 1,0 usando a API do WUA, um **HRESULT** de Wu \_ E \_ au \_ LEGACYSERVER é retornado.</span><span class="sxs-lookup"><span data-stu-id="b9310-109">When a call is made to SUS 1.0 by using the WUA API, an **HRESULT** of WU\_E\_AU\_LEGACYSERVER is returned.</span></span>

<span data-ttu-id="b9310-110">Você também pode usar o método [**IWindowsUpdateAgentInfo:: GetInfo**](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsupdateagentinfo-getinfo) para recuperar a versão atual do arquivo do Wuapi.dll que está sendo executado em um computador.</span><span class="sxs-lookup"><span data-stu-id="b9310-110">You can also use the [**IWindowsUpdateAgentInfo::GetInfo**](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsupdateagentinfo-getinfo) method to retrieve the current file version of Wuapi.dll that is running on a computer.</span></span> <span data-ttu-id="b9310-111">Não há suporte para a interface [**IWindowsUpdateAgentInfo**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsupdateagentinfo) no WUA 1,0.</span><span class="sxs-lookup"><span data-stu-id="b9310-111">The [**IWindowsUpdateAgentInfo**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsupdateagentinfo) interface is not supported in WUA 1.0.</span></span>
