---
description: A propriedade Intel é definida pelo Windows Installer para o nível numérico do processador quando executado em um processador Intel.
ms.assetid: c1190df2-0440-4dd1-bce5-61d899f71437
title: Propriedade Intel
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab73f35b371d3bf8323fe2a3f3de1608666bc181
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782789"
---
# <a name="intel-property"></a><span data-ttu-id="5405b-103">Propriedade Intel</span><span class="sxs-lookup"><span data-stu-id="5405b-103">Intel property</span></span>

<span data-ttu-id="5405b-104">A propriedade **Intel** é definida pelo Windows Installer para o nível numérico do processador quando executado em um processador Intel.</span><span class="sxs-lookup"><span data-stu-id="5405b-104">The **Intel** property is set by the Windows Installer to the numeric processor level when running on an Intel processor.</span></span> <span data-ttu-id="5405b-105">Os valores são os mesmos do campo *wProcessorLevel* da estrutura de [**\_ informações do sistema**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) .</span><span class="sxs-lookup"><span data-stu-id="5405b-105">The values are the same as the *wProcessorLevel* field of the [**SYSTEM\_INFO**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) structure.</span></span> <span data-ttu-id="5405b-106">Durante a execução em um processador x64, o Windows Installer define a propriedade **Intel** para refletir o processador x86 emulado pelo computador x64 conforme relatado pelo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="5405b-106">When running on a x64 processor, the Windows Installer sets the **Intel** property to reflect the x86 processor emulated by the x64 computer as reported by the operating system.</span></span>

## <a name="requirements"></a><span data-ttu-id="5405b-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5405b-107">Requirements</span></span>



| <span data-ttu-id="5405b-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="5405b-108">Requirement</span></span> | <span data-ttu-id="5405b-109">Valor</span><span class="sxs-lookup"><span data-stu-id="5405b-109">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5405b-110">Versão</span><span class="sxs-lookup"><span data-stu-id="5405b-110">Version</span></span><br/> | <span data-ttu-id="5405b-111">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5405b-111">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5405b-112">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5405b-112">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5405b-113">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5405b-113">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="5405b-114">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="5405b-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5405b-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="5405b-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5405b-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5405b-116">Properties</span></span>](properties.md)
</dt> </dl>

 

 
