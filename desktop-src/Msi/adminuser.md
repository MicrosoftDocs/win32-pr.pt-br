---
description: O instalador definirá essa propriedade se o usuário tiver privilégios de administrador.
ms.assetid: 2e7fd269-bd5f-40b7-b123-36b9c783a917
title: Propriedade AdminUser
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11651f0d7103edabbcf7b40087db91f999b1a5b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751863"
---
# <a name="adminuser-property"></a><span data-ttu-id="387d9-103">Propriedade AdminUser</span><span class="sxs-lookup"><span data-stu-id="387d9-103">AdminUser property</span></span>

<span data-ttu-id="387d9-104">O instalador definirá essa propriedade se o usuário tiver privilégios de administrador.</span><span class="sxs-lookup"><span data-stu-id="387d9-104">The installer sets this property if the user has administrator privileges.</span></span>

<span data-ttu-id="387d9-105">**Windows Server 2008 e Windows Vista:** A propriedade **AdminUser** é igual à propriedade [**Privileged**](privileged.md) .</span><span class="sxs-lookup"><span data-stu-id="387d9-105">**Windows Server 2008 and Windows Vista:** The **AdminUser** property is the same as the [**Privileged**](privileged.md) property.</span></span> <span data-ttu-id="387d9-106">Os autores devem ter usado a propriedade **Privileged** .</span><span class="sxs-lookup"><span data-stu-id="387d9-106">Authors should used the **Privileged** property.</span></span> <span data-ttu-id="387d9-107">O instalador definirá essas propriedades se o usuário tiver privilégios de administrador, se o aplicativo tiver sido atribuído por um administrador de sistema ou se as políticas de usuário e máquina AlwaysInstallElevated estiverem definidas como true.</span><span class="sxs-lookup"><span data-stu-id="387d9-107">The installer sets these properties if the user has administrator privileges, if the application has been assigned by a system administrator, or if both the user and machine policies AlwaysInstallElevated are set to true.</span></span>

## <a name="remarks"></a><span data-ttu-id="387d9-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="387d9-108">Remarks</span></span>

<span data-ttu-id="387d9-109">As diferenças entre essas propriedades podem ter sido usadas em alguns pacotes herdados.</span><span class="sxs-lookup"><span data-stu-id="387d9-109">The differences between these properties may have been used in some legacy packages.</span></span> <span data-ttu-id="387d9-110">Por exemplo, **AdminUser** pode ter sido usado em vez de [**Privileged**](privileged.md) em instruções condicionais, pois o instalador só define a propriedade **AdminUser** se o usuário for um administrador.</span><span class="sxs-lookup"><span data-stu-id="387d9-110">For example, **AdminUser** may have been used instead of [**Privileged**](privileged.md) in conditional statements, because the installer only sets the **AdminUser** property if the user is an administrator.</span></span> <span data-ttu-id="387d9-111">O instalador definirá a propriedade **privilegiada** se o usuário for um administrador ou se a política permitir que o usuário instale com privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="387d9-111">The installer sets the **Privileged** property if the user is an administrator, or if policy enables the user to install with elevated privileges.</span></span>

<span data-ttu-id="387d9-112">**Windows Server 2008 e Windows Vista:** Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="387d9-112">**Windows Server 2008 and Windows Vista:** Not supported.</span></span> <span data-ttu-id="387d9-113">[**Privileged**](privileged.md) e **AdminUser** são os mesmos.</span><span class="sxs-lookup"><span data-stu-id="387d9-113">The [**Privileged**](privileged.md) and **AdminUser** are the same.</span></span> <span data-ttu-id="387d9-114">Os pacotes que exigem Propriedades distintas **privilegiadas** e **AdminUser** podem restaurar a diferença definindo a propriedade [**MSIUSEREALADMINDETECTION**](msiuserealadmindetection.md) .</span><span class="sxs-lookup"><span data-stu-id="387d9-114">Packages that require distinct **Privileged** and **AdminUser** properties can restore the difference by setting the [**MSIUSEREALADMINDETECTION**](msiuserealadmindetection.md) property.</span></span>

<span data-ttu-id="387d9-115">Para obter mais informações, consulte [instalando um pacote com privilégios elevados para uma propriedade não administrativa](installing-a-package-with-elevated-privileges-for-a-non-admin.md)e [**privilegiada**](privileged.md) .</span><span class="sxs-lookup"><span data-stu-id="387d9-115">For more information, see [Installing a Package with Elevated Privileges for a Non-Admin](installing-a-package-with-elevated-privileges-for-a-non-admin.md), and [**Privileged**](privileged.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="387d9-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="387d9-116">Requirements</span></span>



| <span data-ttu-id="387d9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="387d9-117">Requirement</span></span> | <span data-ttu-id="387d9-118">Valor</span><span class="sxs-lookup"><span data-stu-id="387d9-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="387d9-119">Versão</span><span class="sxs-lookup"><span data-stu-id="387d9-119">Version</span></span><br/> | <span data-ttu-id="387d9-120">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="387d9-120">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="387d9-121">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Vista ou no Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="387d9-121">Windows Installer 4.0 or Windows Installer 4.5 on Windows Vista or Windows Server 2008.</span></span> <span data-ttu-id="387d9-122">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="387d9-122">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="387d9-123">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="387d9-123">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="387d9-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="387d9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="387d9-125">Propriedades</span><span class="sxs-lookup"><span data-stu-id="387d9-125">Properties</span></span>](properties.md)
</dt> </dl>

 

 




