---
description: No Windows 2000 e sistemas operacionais posteriores, o instalador definirá a propriedade MsiNTSuiteDataCenter como 1 se o Windows 2000 Datacenter Server estiver instalado.
ms.assetid: a777e62a-a360-4d8c-b7a6-00d45c17db66
title: Propriedade MsiNTSuiteDataCenter
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 106b9119885e15b94bf5d8f2cd4b6954d0891d98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747536"
---
# <a name="msintsuitedatacenter-property"></a><span data-ttu-id="97625-103">Propriedade MsiNTSuiteDataCenter</span><span class="sxs-lookup"><span data-stu-id="97625-103">MsiNTSuiteDataCenter property</span></span>

<span data-ttu-id="97625-104">No Windows 2000 e sistemas operacionais posteriores, o instalador definirá a propriedade **MsiNTSuiteDataCenter** como 1 se o Windows 2000 Datacenter Server estiver instalado.</span><span class="sxs-lookup"><span data-stu-id="97625-104">On Windows 2000 and later operating systems, the installer sets the **MsiNTSuiteDataCenter** property to 1 if Windows 2000 Datacenter Server is installed.</span></span> <span data-ttu-id="97625-105">O instalador definirá essa propriedade como 1 somente se o \_ sinalizador de datacenter do pacote de ver \_ estiver definido na estrutura [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) .</span><span class="sxs-lookup"><span data-stu-id="97625-105">The installer sets this property to 1 only if the VER\_SUITE\_DATACENTER flag is set in the [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span> <span data-ttu-id="97625-106">Caso contrário, o instalador não definirá essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="97625-106">Otherwise, the installer does not set this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="97625-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97625-107">Requirements</span></span>



| <span data-ttu-id="97625-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="97625-108">Requirement</span></span> | <span data-ttu-id="97625-109">Valor</span><span class="sxs-lookup"><span data-stu-id="97625-109">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97625-110">Versão</span><span class="sxs-lookup"><span data-stu-id="97625-110">Version</span></span><br/> | <span data-ttu-id="97625-111">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="97625-111">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="97625-112">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="97625-112">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="97625-113">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="97625-113">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="97625-114">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="97625-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="97625-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="97625-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97625-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="97625-116">Properties</span></span>](properties.md)
</dt> </dl>

 

 
