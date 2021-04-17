---
description: O instalador definirá a propriedade MsiTabletPC como um valor diferente de zero se o sistema operacional atual for o Windows XP Tablet PC Edition.
ms.assetid: b178a98e-b6f8-4ff8-b554-e47c3b39f892
title: Propriedade MsiTabletPC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bf2878dbaa895e0924a50900d331db0b879edc1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754354"
---
# <a name="msitabletpc-property"></a><span data-ttu-id="152a5-103">Propriedade MsiTabletPC</span><span class="sxs-lookup"><span data-stu-id="152a5-103">MsiTabletPC property</span></span>

<span data-ttu-id="152a5-104">O instalador definirá a propriedade **MsiTabletPC** como um valor diferente de zero se o sistema operacional atual for o Windows XP Tablet PC Edition.</span><span class="sxs-lookup"><span data-stu-id="152a5-104">The installer sets the **MsiTabletPC** property to a nonzero value if the current operating system is Windows XP Tablet PC Edition.</span></span> <span data-ttu-id="152a5-105">O instalador usa a função [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) com o **SM \_ Tablet** e a propriedade recebe o valor diferente de zero retornado por essa função.</span><span class="sxs-lookup"><span data-stu-id="152a5-105">The installer uses the [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) function with **SM\_TABLETPC**, and the property receives the nonzero value returned by this function.</span></span> <span data-ttu-id="152a5-106">Se o sistema atual não for o Windows XP Tablet PC Edition, a função **GetSystemMetrics** retornará zero e o instalador não definirá essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="152a5-106">If the current system is not Windows XP Tablet PC Edition, the **GetSystemMetrics** function returns zero and the installer does not set this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="152a5-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="152a5-107">Requirements</span></span>



| <span data-ttu-id="152a5-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="152a5-108">Requirement</span></span> | <span data-ttu-id="152a5-109">Valor</span><span class="sxs-lookup"><span data-stu-id="152a5-109">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="152a5-110">Versão</span><span class="sxs-lookup"><span data-stu-id="152a5-110">Version</span></span><br/> | <span data-ttu-id="152a5-111">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="152a5-111">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="152a5-112">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="152a5-112">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="152a5-113">Windows Installer 4,5 no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="152a5-113">Windows Installer 4.5 on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="152a5-114">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="152a5-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="152a5-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="152a5-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="152a5-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="152a5-116">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="152a5-117">Sem suporte no Windows Installer 3,1 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="152a5-117">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
