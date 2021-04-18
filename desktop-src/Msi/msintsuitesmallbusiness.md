---
description: No Windows 2000 e sistemas operacionais posteriores, o instalador definirá a propriedade MsiNTSuiteSmallBusiness como 1 se o Microsoft Small Business Server estiver instalado.
ms.assetid: 9ac578b9-316f-413c-aae0-4f414109583b
title: Propriedade MsiNTSuiteSmallBusiness
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d8b1e523ff038e4639cb0f92762c3914bbf5f6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769314"
---
# <a name="msintsuitesmallbusiness-property"></a><span data-ttu-id="dd660-103">Propriedade MsiNTSuiteSmallBusiness</span><span class="sxs-lookup"><span data-stu-id="dd660-103">MsiNTSuiteSmallBusiness property</span></span>

<span data-ttu-id="dd660-104">No Windows 2000 e sistemas operacionais posteriores, o instalador definirá a propriedade **MsiNTSuiteSmallBusiness** como 1 se o Microsoft Small Business Server estiver instalado.</span><span class="sxs-lookup"><span data-stu-id="dd660-104">On Windows 2000 and later operating systems, the installer sets the **MsiNTSuiteSmallBusiness** property to 1 if Microsoft Small Business Server is installed.</span></span> <span data-ttu-id="dd660-105">O instalador definirá essa propriedade como 1 somente se o \_ sinalizador do SMALLBUSINESS do pacote do ver \_ estiver definido na estrutura [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) .</span><span class="sxs-lookup"><span data-stu-id="dd660-105">The installer sets this property to 1 only if the VER\_SUITE\_SMALLBUSINESS flag is set in the [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span> <span data-ttu-id="dd660-106">Caso contrário, o instalador não definirá essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="dd660-106">Otherwise the installer does not set this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd660-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd660-107">Requirements</span></span>



| <span data-ttu-id="dd660-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd660-108">Requirement</span></span> | <span data-ttu-id="dd660-109">Valor</span><span class="sxs-lookup"><span data-stu-id="dd660-109">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd660-110">Versão</span><span class="sxs-lookup"><span data-stu-id="dd660-110">Version</span></span><br/> | <span data-ttu-id="dd660-111">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="dd660-111">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="dd660-112">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="dd660-112">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="dd660-113">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="dd660-113">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="dd660-114">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="dd660-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dd660-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="dd660-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd660-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="dd660-116">Properties</span></span>](properties.md)
</dt> </dl>

 

 
