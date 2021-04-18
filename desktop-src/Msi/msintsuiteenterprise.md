---
description: No Windows 2000 e sistemas operacionais posteriores, o instalador definirá a propriedade MsiNTSuiteEnterprise como 1 se o Windows 2000 Advanced Server estiver instalado.
ms.assetid: f5384467-3791-4b0b-a70e-b5343c70db46
title: Propriedade MsiNTSuiteEnterprise
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 137b4ece4dbaecdd83b78fd2ce7cfd57820e029d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747755"
---
# <a name="msintsuiteenterprise-property"></a><span data-ttu-id="6f223-103">Propriedade MsiNTSuiteEnterprise</span><span class="sxs-lookup"><span data-stu-id="6f223-103">MsiNTSuiteEnterprise property</span></span>

<span data-ttu-id="6f223-104">No Windows 2000 e sistemas operacionais posteriores, o instalador definirá a propriedade **MsiNTSuiteEnterprise** como 1 se o Windows 2000 Advanced Server estiver instalado.</span><span class="sxs-lookup"><span data-stu-id="6f223-104">On Windows 2000 and later operating systems, the installer sets the **MsiNTSuiteEnterprise** property to 1 if Windows 2000 Advanced Server is installed.</span></span> <span data-ttu-id="6f223-105">O instalador definirá essa propriedade como 1 somente se o \_ sinalizador de Enterprise do pacote de ver \_ estiver definido na estrutura [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) .</span><span class="sxs-lookup"><span data-stu-id="6f223-105">The installer sets this property to 1 only if the VER\_SUITE\_ENTERPRISE flag is set in the [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span> <span data-ttu-id="6f223-106">Caso contrário, o instalador não definirá essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="6f223-106">Otherwise, the installer does not set this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f223-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f223-107">Requirements</span></span>



| <span data-ttu-id="6f223-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f223-108">Requirement</span></span> | <span data-ttu-id="6f223-109">Valor</span><span class="sxs-lookup"><span data-stu-id="6f223-109">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f223-110">Versão</span><span class="sxs-lookup"><span data-stu-id="6f223-110">Version</span></span><br/> | <span data-ttu-id="6f223-111">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6f223-111">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="6f223-112">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6f223-112">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="6f223-113">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6f223-113">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="6f223-114">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="6f223-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6f223-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="6f223-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f223-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6f223-116">Properties</span></span>](properties.md)
</dt> </dl>

 

 
