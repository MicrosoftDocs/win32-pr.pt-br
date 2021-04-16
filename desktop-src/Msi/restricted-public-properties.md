---
description: Em determinados casos, um usuário que não é um administrador do sistema só pode substituir uma lista aprovada de propriedades públicas Windows Installerdas restritas.
ms.assetid: e16e8187-75b6-4104-a53c-928a56fcee6b
title: Propriedades públicas restritas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e4f08be7f625cd45cdb48373eb0107ade708949
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105747525"
---
# <a name="restricted-public-properties"></a><span data-ttu-id="e70fe-103">Propriedades públicas restritas</span><span class="sxs-lookup"><span data-stu-id="e70fe-103">Restricted Public Properties</span></span>

<span data-ttu-id="e70fe-104">No caso de uma instalação gerenciada, o autor do pacote pode precisar limitar quais [Propriedades públicas](public-properties.md) são passadas para o lado do servidor e podem ser alteradas por um usuário que não seja um administrador do sistema.</span><span class="sxs-lookup"><span data-stu-id="e70fe-104">In the case of a managed installation, the package author may need to limit which [public properties](public-properties.md) are passed to the server side and can be changed by a user that is not a system administrator.</span></span> <span data-ttu-id="e70fe-105">Algumas restrições são comumente necessárias para manter um ambiente seguro quando a instalação requer que o instalador use privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="e70fe-105">Some restrictions are commonly necessary to maintain a secure environment when the installation requires the installer to use elevated privileges.</span></span> <span data-ttu-id="e70fe-106">Se todas as condições a seguir forem atendidas, um usuário que não seja um administrador do sistema só poderá substituir uma lista aprovada de propriedades públicas restritas:</span><span class="sxs-lookup"><span data-stu-id="e70fe-106">If all of the following conditions are met, a user that is not a system administrator can only override an approved list of restricted public properties:</span></span>

-   <span data-ttu-id="e70fe-107">O sistema é o Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="e70fe-107">The system is Windows 2000.</span></span>
-   <span data-ttu-id="e70fe-108">O usuário não é um administrador do sistema.</span><span class="sxs-lookup"><span data-stu-id="e70fe-108">The user is not a system administrator.</span></span>
-   <span data-ttu-id="e70fe-109">O aplicativo ou produto está sendo instalado com privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="e70fe-109">The application or product is being installed with elevated privileges.</span></span>

<span data-ttu-id="e70fe-110">Se todas as condições acima forem verdadeiras, o instalador usa como padrão a seguinte lista de propriedades públicas restritas que podem ser alteradas por qualquer usuário:</span><span class="sxs-lookup"><span data-stu-id="e70fe-110">If all of the above conditions are true, the installer defaults to the following list of restricted public properties that can be changed by any user:</span></span>

-   [<span data-ttu-id="e70fe-111">**ACTION**</span><span class="sxs-lookup"><span data-stu-id="e70fe-111">**ACTION**</span></span>](action.md)
-   [<span data-ttu-id="e70fe-112">**AFTERREBOOT**</span><span class="sxs-lookup"><span data-stu-id="e70fe-112">**AFTERREBOOT**</span></span>](afterreboot.md)
-   [<span data-ttu-id="e70fe-113">**ALLUSERS**</span><span class="sxs-lookup"><span data-stu-id="e70fe-113">**ALLUSERS**</span></span>](allusers.md)
-   [<span data-ttu-id="e70fe-114">**EXECUTEACTION**</span><span class="sxs-lookup"><span data-stu-id="e70fe-114">**EXECUTEACTION**</span></span>](executeaction.md)
-   [<span data-ttu-id="e70fe-115">**EXECUTEmode**</span><span class="sxs-lookup"><span data-stu-id="e70fe-115">**EXECUTEMODE**</span></span>](executemode.md)
-   [<span data-ttu-id="e70fe-116">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="e70fe-116">**FILEADDDEFAULT**</span></span>](fileadddefault.md)
-   [<span data-ttu-id="e70fe-117">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="e70fe-117">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
-   [<span data-ttu-id="e70fe-118">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="e70fe-118">**FILEADDSOURCE**</span></span>](fileaddsource.md)
-   [<span data-ttu-id="e70fe-119">**INSTALLLEVEL**</span><span class="sxs-lookup"><span data-stu-id="e70fe-119">**INSTALLLEVEL**</span></span>](installlevel.md)
-   [<span data-ttu-id="e70fe-120">**LIMITUI**</span><span class="sxs-lookup"><span data-stu-id="e70fe-120">**LIMITUI**</span></span>](limitui.md)
-   [<span data-ttu-id="e70fe-121">**LOGACTION**</span><span class="sxs-lookup"><span data-stu-id="e70fe-121">**LOGACTION**</span></span>](logaction.md)
-   [<span data-ttu-id="e70fe-122">**Nocompanyname**</span><span class="sxs-lookup"><span data-stu-id="e70fe-122">**NOCOMPANYNAME**</span></span>](nocompanyname.md)
-   [<span data-ttu-id="e70fe-123">**NOUSERNAME**</span><span class="sxs-lookup"><span data-stu-id="e70fe-123">**NOUSERNAME**</span></span>](nousername.md)
-   [<span data-ttu-id="e70fe-124">**MSIENFORCEUPGRADECOMPONENTRULES**</span><span class="sxs-lookup"><span data-stu-id="e70fe-124">**MSIENFORCEUPGRADECOMPONENTRULES**</span></span>](msienforceupgradecomponentrules.md)
-   [<span data-ttu-id="e70fe-125">**MSIINSTANCEGUID**</span><span class="sxs-lookup"><span data-stu-id="e70fe-125">**MSIINSTANCEGUID**</span></span>](msiinstanceguid.md)
-   [<span data-ttu-id="e70fe-126">**MSINEWINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="e70fe-126">**MSINEWINSTANCE**</span></span>](msinewinstance.md)
-   [<span data-ttu-id="e70fe-127">**MSIPATCHREMOVE**</span><span class="sxs-lookup"><span data-stu-id="e70fe-127">**MSIPATCHREMOVE**</span></span>](msipatchremove.md)
-   [<span data-ttu-id="e70fe-128">**DISTRIBUÍDO**</span><span class="sxs-lookup"><span data-stu-id="e70fe-128">**PATCH**</span></span>](patch.md)
-   [<span data-ttu-id="e70fe-129">**PRIMARYFOLDER**</span><span class="sxs-lookup"><span data-stu-id="e70fe-129">**PRIMARYFOLDER**</span></span>](primaryfolder.md)
-   [<span data-ttu-id="e70fe-130">**PROMPTROLLBACKCOST**</span><span class="sxs-lookup"><span data-stu-id="e70fe-130">**PROMPTROLLBACKCOST**</span></span>](promptrollbackcost.md)
-   [<span data-ttu-id="e70fe-131">**Inicialize**</span><span class="sxs-lookup"><span data-stu-id="e70fe-131">**REBOOT**</span></span>](reboot.md)
-   [<span data-ttu-id="e70fe-132">**Install**</span><span class="sxs-lookup"><span data-stu-id="e70fe-132">**REINSTALL**</span></span>](reinstall.md)
-   [<span data-ttu-id="e70fe-133">**REINSTALLMODE**</span><span class="sxs-lookup"><span data-stu-id="e70fe-133">**REINSTALLMODE**</span></span>](reinstallmode.md)
-   [<span data-ttu-id="e70fe-134">**Volte**</span><span class="sxs-lookup"><span data-stu-id="e70fe-134">**RESUME**</span></span>](resume.md)
-   [<span data-ttu-id="e70fe-135">**SEQUENCE**</span><span class="sxs-lookup"><span data-stu-id="e70fe-135">**SEQUENCE**</span></span>](sequence.md)
-   [<span data-ttu-id="e70fe-136">**SHORTFILENAMES**</span><span class="sxs-lookup"><span data-stu-id="e70fe-136">**SHORTFILENAMES**</span></span>](shortfilenames.md)
-   [<span data-ttu-id="e70fe-137">**TRANSFORMAÇÕES**</span><span class="sxs-lookup"><span data-stu-id="e70fe-137">**TRANSFORMS**</span></span>](transforms.md)
-   [<span data-ttu-id="e70fe-138">**TRANSFORMSATSOURCE**</span><span class="sxs-lookup"><span data-stu-id="e70fe-138">**TRANSFORMSATSOURCE**</span></span>](transformsatsource.md)

<span data-ttu-id="e70fe-139">O autor de um pacote de instalação pode estender essa lista padrão para incluir propriedades públicas adicionais usando a propriedade [**SecureCustomProperties**](securecustomproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="e70fe-139">The author of an installation package can extend this default list to include additional public properties by using the [**SecureCustomProperties**](securecustomproperties.md) property.</span></span>

<span data-ttu-id="e70fe-140">Definir a propriedade [**EnableUserControl**](-enableusercontrol.md) ou a [política do sistema](system-policy.md) [EnableUserControl](enableusercontrol.md)estende a lista para todas as propriedades públicas.</span><span class="sxs-lookup"><span data-stu-id="e70fe-140">Setting the [**EnableUserControl**](-enableusercontrol.md) property or the [EnableUserControl](enableusercontrol.md)[system policy](system-policy.md) extends the list to all public properties.</span></span> <span data-ttu-id="e70fe-141">Todos os usuários podem então alterar qualquer propriedade pública.</span><span class="sxs-lookup"><span data-stu-id="e70fe-141">All users can then change any public property.</span></span>

<span data-ttu-id="e70fe-142">O instalador define a propriedade [**RestrictedUserControl**](restrictedusercontrol.md) sempre que a lista de propriedades públicas passadas para o servidor por usuários não administradores é restrita.</span><span class="sxs-lookup"><span data-stu-id="e70fe-142">The installer sets the [**RestrictedUserControl**](restrictedusercontrol.md) property whenever the list of public properties passed to the server by non-administrator users is restricted.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e70fe-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e70fe-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e70fe-144">Sobre propriedades</span><span class="sxs-lookup"><span data-stu-id="e70fe-144">About Properties</span></span>](about-properties.md)
</dt> </dl>

 

 



