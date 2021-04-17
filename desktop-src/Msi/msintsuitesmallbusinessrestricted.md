---
description: No Windows 2000 e sistemas operacionais posteriores, o instalador definirá a propriedade MsiNTSuiteSmallBusinessRestricted como 1 se o Microsoft Small Business Server estiver instalado com a licença de cliente restritiva em vigor.
ms.assetid: a7100df4-6fe4-4159-ba94-9b5bd1803107
title: Propriedade MsiNTSuiteSmallBusinessRestricted
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71d85fa7fe83c0c8c7cd40788453d1078e7a6b94
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747535"
---
# <a name="msintsuitesmallbusinessrestricted-property"></a><span data-ttu-id="7294b-103">Propriedade MsiNTSuiteSmallBusinessRestricted</span><span class="sxs-lookup"><span data-stu-id="7294b-103">MsiNTSuiteSmallBusinessRestricted property</span></span>

<span data-ttu-id="7294b-104">No Windows 2000 e sistemas operacionais posteriores, o instalador definirá a propriedade **MsiNTSuiteSmallBusinessRestricted** como 1 se o Microsoft Small Business Server estiver instalado com a licença de cliente restritiva em vigor.</span><span class="sxs-lookup"><span data-stu-id="7294b-104">On Windows 2000 and later operating systems, the installer sets the **MsiNTSuiteSmallBusinessRestricted** property to 1 if Microsoft Small Business Server is installed with the restrictive client license in force.</span></span> <span data-ttu-id="7294b-105">O instalador definirá essa propriedade como 1 somente se o \_ sinalizador restrito do SMALLBUSINESS do pacote de ver \_ \_ estiver definido na estrutura [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) .</span><span class="sxs-lookup"><span data-stu-id="7294b-105">The installer sets this property to 1 only if the VER\_SUITE\_SMALLBUSINESS\_RESTRICTED flag is set in the [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span> <span data-ttu-id="7294b-106">Caso contrário, o instalador não definirá essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="7294b-106">Otherwise the installer does not set this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="7294b-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7294b-107">Requirements</span></span>



| <span data-ttu-id="7294b-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="7294b-108">Requirement</span></span> | <span data-ttu-id="7294b-109">Valor</span><span class="sxs-lookup"><span data-stu-id="7294b-109">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7294b-110">Versão</span><span class="sxs-lookup"><span data-stu-id="7294b-110">Version</span></span><br/> | <span data-ttu-id="7294b-111">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7294b-111">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="7294b-112">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7294b-112">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="7294b-113">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7294b-113">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="7294b-114">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="7294b-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7294b-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="7294b-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7294b-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7294b-116">Properties</span></span>](properties.md)
</dt> </dl>

 

 
