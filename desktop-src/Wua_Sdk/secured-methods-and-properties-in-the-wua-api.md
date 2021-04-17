---
description: Quando o WUA detecta que um chamador não tem permissão para acessar uma interface, um método ou uma propriedade, o HRESULT E \_ ACCESSDENIED é retornado.
ms.assetid: 4535ce8d-c329-4335-8b0a-8f63c22f111d
title: Protegendo interfaces, métodos e propriedades na API do WUA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6680f616e1ca0596aba04edf4f7ddf7615e0c7f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811494"
---
# <a name="securing-interfaces-methods-and-properties-in-the-wua-api"></a><span data-ttu-id="e2a9a-103">Protegendo interfaces, métodos e propriedades na API do WUA</span><span class="sxs-lookup"><span data-stu-id="e2a9a-103">Securing Interfaces, Methods, and Properties in the WUA API</span></span>

<span data-ttu-id="e2a9a-104">Algumas interfaces, métodos e propriedades do WUA (Windows Update Agent) são acessíveis somente a chamadores que pertencem aos seguintes grupos de segurança do Windows:</span><span class="sxs-lookup"><span data-stu-id="e2a9a-104">Some interfaces, methods, and properties of Windows Update Agent (WUA) are accessible only to callers who belong to the following Windows security groups:</span></span>

-   <span data-ttu-id="e2a9a-105">Administrador</span><span class="sxs-lookup"><span data-stu-id="e2a9a-105">Administrator</span></span>
-   <span data-ttu-id="e2a9a-106">Usuário</span><span class="sxs-lookup"><span data-stu-id="e2a9a-106">User</span></span>
-   <span data-ttu-id="e2a9a-107">Usuário avançado</span><span class="sxs-lookup"><span data-stu-id="e2a9a-107">Power User</span></span>

<span data-ttu-id="e2a9a-108">Quando o WUA detecta que um chamador não tem permissão para acessar uma interface, um método ou uma propriedade, o **HRESULT** E \_ ACCESSDENIED é retornado.</span><span class="sxs-lookup"><span data-stu-id="e2a9a-108">When WUA detects that a caller does not have permission to access an interface, method, or property, the **HRESULT** E\_ACCESSDENIED is returned.</span></span>

<span data-ttu-id="e2a9a-109">As seguintes interfaces estão disponíveis para os grupos de segurança administrador, usuário e usuário avançado:</span><span class="sxs-lookup"><span data-stu-id="e2a9a-109">The following interfaces are available to the Administrator, User, and Power User security groups:</span></span>

-   [<span data-ttu-id="e2a9a-110">**IAutomaticUpdates**</span><span class="sxs-lookup"><span data-stu-id="e2a9a-110">**IAutomaticUpdates**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdates)
-   [<span data-ttu-id="e2a9a-111">**IAutomaticUpdatesSettings**</span><span class="sxs-lookup"><span data-stu-id="e2a9a-111">**IAutomaticUpdatesSettings**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings)
-   [<span data-ttu-id="e2a9a-112">**IAutomaticUpdatesSettings2**</span><span class="sxs-lookup"><span data-stu-id="e2a9a-112">**IAutomaticUpdatesSettings2**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings2)
-   [<span data-ttu-id="e2a9a-113">**ISystemInformation**</span><span class="sxs-lookup"><span data-stu-id="e2a9a-113">**ISystemInformation**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-isysteminformation)
-   [<span data-ttu-id="e2a9a-114">**IUpdateSearcher**</span><span class="sxs-lookup"><span data-stu-id="e2a9a-114">**IUpdateSearcher**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher)
-   <span data-ttu-id="e2a9a-115">[**IUpdateSession**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession) e [ **IUpdateSession2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession2)</span><span class="sxs-lookup"><span data-stu-id="e2a9a-115">[**IUpdateSession**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession) and [**IUpdateSession2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession2)</span></span>

> [!Note]  
> <span data-ttu-id="e2a9a-116">Se as seguintes condições forem verdadeiras, uma pesquisa falhará:</span><span class="sxs-lookup"><span data-stu-id="e2a9a-116">If the following conditions are true, a search fails:</span></span>
>
> -   <span data-ttu-id="e2a9a-117">Um usuário que não é um administrador define a [**Propriedade UserLocale da interface IUpdateSession2**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession2-get_userlocale) como uma localidade que corresponde a um idioma que não está instalado no computador.</span><span class="sxs-lookup"><span data-stu-id="e2a9a-117">A user who is not an administrator sets the [**UserLocale property of the IUpdateSession2**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession2-get_userlocale) interface to a locale that corresponds to a language that is not installed on the computer.</span></span>
> -   <span data-ttu-id="e2a9a-118">A pesquisa usa um objeto UpdateSearch criado a partir do objeto UpdateSession.</span><span class="sxs-lookup"><span data-stu-id="e2a9a-118">The search uses an UpdateSearch object created from the UpdateSession object.</span></span>

 

<span data-ttu-id="e2a9a-119">As seguintes interfaces e métodos de download estão disponíveis para os grupos de usuários avançados e de administrador:</span><span class="sxs-lookup"><span data-stu-id="e2a9a-119">The following download interfaces and methods are available to the Administrator and Power User groups:</span></span>

-   [<span data-ttu-id="e2a9a-120">**IUpdateDownloader**</span><span class="sxs-lookup"><span data-stu-id="e2a9a-120">**IUpdateDownloader**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader)
-   [<span data-ttu-id="e2a9a-121">**IUpdate::CopyFromCache**</span><span class="sxs-lookup"><span data-stu-id="e2a9a-121">**IUpdate::CopyFromCache**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-copyfromcache)
-   [<span data-ttu-id="e2a9a-122">**IAutomaticUpdatesSettings2::CheckPermission**</span><span class="sxs-lookup"><span data-stu-id="e2a9a-122">**IAutomaticUpdatesSettings2::CheckPermission**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-checkpermission)
    > [!Note]  
    > <span data-ttu-id="e2a9a-123">Administradores, usuários e usuários avançados podem chamar [**IAutomaticUpdatesSettings2:: CheckPermission**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-checkpermission).</span><span class="sxs-lookup"><span data-stu-id="e2a9a-123">Administrators, users, and power users can call [**IAutomaticUpdatesSettings2::CheckPermission**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-checkpermission).</span></span>

     

<span data-ttu-id="e2a9a-124">As seguintes interfaces, métodos e propriedades de instalação estão disponíveis para os grupos de administradores:</span><span class="sxs-lookup"><span data-stu-id="e2a9a-124">The following installation interfaces, methods, and properties are available to the Administrator groups:</span></span>

-   [<span data-ttu-id="e2a9a-125">**IAutomaticUpdates::P ause**</span><span class="sxs-lookup"><span data-stu-id="e2a9a-125">**IAutomaticUpdates::Pause**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-pause)
-   [<span data-ttu-id="e2a9a-126">**IAutomaticUpdates:: retomar**</span><span class="sxs-lookup"><span data-stu-id="e2a9a-126">**IAutomaticUpdates::Resume**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-resume)
-   [<span data-ttu-id="e2a9a-127">**IAutomaticUpdates::EnableService**</span><span class="sxs-lookup"><span data-stu-id="e2a9a-127">**IAutomaticUpdates::EnableService**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-enableservice)
-   [<span data-ttu-id="e2a9a-128">**IUpdateInstaller**</span><span class="sxs-lookup"><span data-stu-id="e2a9a-128">**IUpdateInstaller**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstaller)
-   [<span data-ttu-id="e2a9a-129">**Propriedade IsHidden de IUpdate**</span><span class="sxs-lookup"><span data-stu-id="e2a9a-129">**IsHidden Property of IUpdate**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden)
    > [!Note]  
    > <span data-ttu-id="e2a9a-130">Administradores, usuários e usuários avançados podem recuperar os valores da [**Propriedade IsHidden de IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden).</span><span class="sxs-lookup"><span data-stu-id="e2a9a-130">Administrators, users, and power users can retrieve the values of the [**IsHidden Property of IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden).</span></span> <span data-ttu-id="e2a9a-131">No entanto, somente administradores e usuários avançados podem definir os valores.</span><span class="sxs-lookup"><span data-stu-id="e2a9a-131">However, only administrators and power users can set the values.</span></span>

     

-   [<span data-ttu-id="e2a9a-132">**IUpdate:: AcceptEula**</span><span class="sxs-lookup"><span data-stu-id="e2a9a-132">**IUpdate::AcceptEula**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-accepteula)
    > [!Note]  
    > <span data-ttu-id="e2a9a-133">Os administradores e os usuários avançados podem chamar o [**método AcceptEula de IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-accepteula).</span><span class="sxs-lookup"><span data-stu-id="e2a9a-133">Administrators and power users can call the [**AcceptEula method of IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-accepteula).</span></span>

     

-   [<span data-ttu-id="e2a9a-134">**IAutomaticUpdatesSettings:: salvar**</span><span class="sxs-lookup"><span data-stu-id="e2a9a-134">**IAutomaticUpdatesSettings::Save**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save)
-   [<span data-ttu-id="e2a9a-135">**Propriedade NotificationLevel de IAutomaticUpdatesSettings**</span><span class="sxs-lookup"><span data-stu-id="e2a9a-135">**NotificationLevel Property of IAutomaticUpdatesSettings**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel)
    > [!Note]  
    > <span data-ttu-id="e2a9a-136">Administradores, usuários e usuários avançados podem recuperar os valores da [**Propriedade notificationLevel de IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel).</span><span class="sxs-lookup"><span data-stu-id="e2a9a-136">Administrators, users, and power users can retrieve the values of the [**NotificationLevel Property of IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel).</span></span> <span data-ttu-id="e2a9a-137">No entanto, somente os administradores podem definir os valores.</span><span class="sxs-lookup"><span data-stu-id="e2a9a-137">However, only administrators can set the values.</span></span>

     

-   [<span data-ttu-id="e2a9a-138">**Propriedade ScheduledInstallationDay de IAutomaticUpdatesSettings**</span><span class="sxs-lookup"><span data-stu-id="e2a9a-138">**ScheduledInstallationDay Property of IAutomaticUpdatesSettings**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday)
    > [!Note]  
    > <span data-ttu-id="e2a9a-139">Administradores, usuários e usuários avançados podem recuperar os valores da [**Propriedade ScheduledInstallationDay de IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday).</span><span class="sxs-lookup"><span data-stu-id="e2a9a-139">Administrators, users, and power users can retrieve the values of the [**ScheduledInstallationDay Property of IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday).</span></span> <span data-ttu-id="e2a9a-140">No entanto, somente os administradores podem definir os valores.</span><span class="sxs-lookup"><span data-stu-id="e2a9a-140">However, only administrators can set the values.</span></span>

     

-   [<span data-ttu-id="e2a9a-141">**Propriedade ScheduledInstallationTime de IAutomaticUpdatesSettings**</span><span class="sxs-lookup"><span data-stu-id="e2a9a-141">**ScheduledInstallationTime Property of IAutomaticUpdatesSettings**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime)
    > [!Note]  
    > <span data-ttu-id="e2a9a-142">Administradores, usuários e usuários avançados podem recuperar os valores da [**Propriedade ScheduledInstallationTime de IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime).</span><span class="sxs-lookup"><span data-stu-id="e2a9a-142">Administrators, users, and power users can retrieve the values of the [**ScheduledInstallationTime Property of IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime).</span></span> <span data-ttu-id="e2a9a-143">No entanto, somente os administradores podem definir os valores.</span><span class="sxs-lookup"><span data-stu-id="e2a9a-143">However, only administrators can set the values.</span></span>

     

-   [<span data-ttu-id="e2a9a-144">**Propriedade IncludeRecommendedUpdates de IAutomaticUpdatesSettings2**</span><span class="sxs-lookup"><span data-stu-id="e2a9a-144">**IncludeRecommendedUpdates Property of IAutomaticUpdatesSettings2**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-get_includerecommendedupdates)
    > [!Note]  
    > <span data-ttu-id="e2a9a-145">Administradores, usuários e usuários avançados podem recuperar os valores da [**Propriedade IncludeRecommendedUpdates de IAutomaticUpdatesSettings2**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-get_includerecommendedupdates).</span><span class="sxs-lookup"><span data-stu-id="e2a9a-145">Administrators, users, and power users can retrieve the values of the [**IncludeRecommendedUpdates Property of IAutomaticUpdatesSettings2**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-get_includerecommendedupdates).</span></span> <span data-ttu-id="e2a9a-146">No entanto, somente os administradores podem definir os valores.</span><span class="sxs-lookup"><span data-stu-id="e2a9a-146">However, only administrators can set the values.</span></span>

     

 

 



