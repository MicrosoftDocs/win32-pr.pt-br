---
description: Defina a propriedade MSIUSEREALADMINDETECTION como 1 para solicitar que o instalador Use informações reais do usuário ao definir a propriedade AdminUser.
ms.assetid: eb0ed6e3-377b-40f4-afee-346a83e310cf
title: Propriedade MSIUSEREALADMINDETECTION
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0989174f41bc4b58f89e440dd9852dfde6249a5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768725"
---
# <a name="msiuserealadmindetection-property"></a><span data-ttu-id="92377-103">Propriedade MSIUSEREALADMINDETECTION</span><span class="sxs-lookup"><span data-stu-id="92377-103">MSIUSEREALADMINDETECTION property</span></span>

<span data-ttu-id="92377-104">Defina a propriedade **MSIUSEREALADMINDETECTION** como 1 para solicitar que o instalador Use informações reais do usuário ao definir a propriedade [**AdminUser**](adminuser.md) .</span><span class="sxs-lookup"><span data-stu-id="92377-104">Set the **MSIUSEREALADMINDETECTION** property to 1 to request that the installer use actual user information when setting the [**AdminUser**](adminuser.md) property.</span></span> <span data-ttu-id="92377-105">Ao executar no Windows Vista, o [**Privileged**](privileged.md) e o **AdminUser** são os mesmos.</span><span class="sxs-lookup"><span data-stu-id="92377-105">When running on Windows Vista, the [**Privileged**](privileged.md) and **AdminUser** are the same.</span></span> <span data-ttu-id="92377-106">Os autores devem ter usado a propriedade **privilegiada** em novos pacotes.</span><span class="sxs-lookup"><span data-stu-id="92377-106">Authors should used the **Privileged** property in new packages.</span></span> <span data-ttu-id="92377-107">Pacotes herdados que exigem Propriedades distintas **privilegiadas** e **AdminUser** podem restaurar a diferença definindo a propriedade **MSIUSEREALADMINDETECTION** .</span><span class="sxs-lookup"><span data-stu-id="92377-107">Legacy packages that require distinct **Privileged** and **AdminUser** properties can restore the difference by setting the **MSIUSEREALADMINDETECTION** property.</span></span>

## <a name="requirements"></a><span data-ttu-id="92377-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92377-108">Requirements</span></span>



| <span data-ttu-id="92377-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="92377-109">Requirement</span></span> | <span data-ttu-id="92377-110">Valor</span><span class="sxs-lookup"><span data-stu-id="92377-110">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92377-111">Versão</span><span class="sxs-lookup"><span data-stu-id="92377-111">Version</span></span><br/> | <span data-ttu-id="92377-112">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="92377-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="92377-113">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="92377-113">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="92377-114">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="92377-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="92377-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="92377-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92377-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="92377-116">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="92377-117">Sem suporte no Windows Installer 3,1 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="92377-117">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




