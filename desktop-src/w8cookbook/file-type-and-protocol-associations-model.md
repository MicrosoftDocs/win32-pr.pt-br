---
title: Tipo de arquivo e modelo de associações de URI
description: Tipo de arquivo e modelo de associações de URI
ms.assetid: 4DE7DD08-088A-4E09-B1C7-AE9033EA533D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c78540a072405aade01a9f94503999ad105d2078
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "104008502"
---
# <a name="file-type-and-uri-associations-model"></a><span data-ttu-id="f4c56-103">Tipo de arquivo e modelo de associações de URI</span><span class="sxs-lookup"><span data-stu-id="f4c56-103">File type and URI associations model</span></span>

## <a name="platforms"></a><span data-ttu-id="f4c56-104">Plataformas</span><span class="sxs-lookup"><span data-stu-id="f4c56-104">Platforms</span></span>

 <span data-ttu-id="f4c56-105">**Clientes** -Windows 8</span><span class="sxs-lookup"><span data-stu-id="f4c56-105">**Clients** - Windows 8</span></span>  
<span data-ttu-id="f4c56-106">**Servidores** -Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f4c56-106">**Servers** - Windows Server 2012</span></span>  



## <a name="description"></a><span data-ttu-id="f4c56-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="f4c56-107">Description</span></span>

<span data-ttu-id="f4c56-108">O tipo de arquivo e o modelo de associação de URI foram alterados no Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f4c56-108">The file type and URI association model has changed in Windows 8.</span></span> <span data-ttu-id="f4c56-109">Os aplicativos não são mais capazes de se definir por meio de programação como o manipulador padrão para um tipo de arquivo ou URI.</span><span class="sxs-lookup"><span data-stu-id="f4c56-109">Apps are no longer able to programmatically set themselves as the default handler for a file type or URI.</span></span> <span data-ttu-id="f4c56-110">Em vez disso, agora o usuário controla o que é o manipulador padrão para um tipo de arquivo ou esquema de URI.</span><span class="sxs-lookup"><span data-stu-id="f4c56-110">Instead, now the user always controls what the default handler is for a file type or URI scheme.</span></span>

## <a name="manifestation"></a><span data-ttu-id="f4c56-111">Manifestação</span><span class="sxs-lookup"><span data-stu-id="f4c56-111">Manifestation</span></span>

<span data-ttu-id="f4c56-112">A maneira como essa alteração apresenta ao usuário depende de como o aplicativo foi projetado, por exemplo:</span><span class="sxs-lookup"><span data-stu-id="f4c56-112">How this change presents to the user depends upon how the app is designed, for example:</span></span>

-   <span data-ttu-id="f4c56-113">Muitos aplicativos verificam se são o padrão sempre que são executados e, se não forem, eles solicitam que o usuário os defina como padrão.</span><span class="sxs-lookup"><span data-stu-id="f4c56-113">Many apps check to see if they are the default every time they run and, if they are not, they prompt the user to set them as default.</span></span> <span data-ttu-id="f4c56-114">No entanto, como os aplicativos não podem mais ser consultados com precisão para determinar qual aplicativo é o manipulador padrão para um tipo de arquivo ou esquema de URI, nenhuma dessas operações funciona.</span><span class="sxs-lookup"><span data-stu-id="f4c56-114">However, because apps can no longer accurately query to determine which app is the default handler for a file type or URI scheme, neither of these operations works.</span></span>
-   <span data-ttu-id="f4c56-115">Muitos aplicativos têm uma caixa de diálogo ou menu interno ou em seu instalador que especifica os tipos de arquivo para os quais o aplicativo deve servir como padrão.</span><span class="sxs-lookup"><span data-stu-id="f4c56-115">Many apps have a dialog box or menu built in or in their installer that specifies the file types for which the app should serve as the default.</span></span> <span data-ttu-id="f4c56-116">No entanto, como os aplicativos não podem mais ser definidos por meio de programação como o manipulador padrão para um tipo de arquivo ou esquema de URI, isso não funciona mais.</span><span class="sxs-lookup"><span data-stu-id="f4c56-116">However, because apps can no longer programmatically set themselves as the default handler for a file type or URI scheme, this no longer works.</span></span>

## <a name="mitigation"></a><span data-ttu-id="f4c56-117">Atenuação</span><span class="sxs-lookup"><span data-stu-id="f4c56-117">Mitigation</span></span>

<span data-ttu-id="f4c56-118">Há várias coisas que os usuários podem fazer para acomodar essas alterações:</span><span class="sxs-lookup"><span data-stu-id="f4c56-118">There are several things users can do to accommodate these changes:</span></span>

-   <span data-ttu-id="f4c56-119">Os usuários são solicitados a escolher um aplicativo padrão para manipular tipos de arquivo, esquemas de URI ou ambos quando um não tiver sido especificado</span><span class="sxs-lookup"><span data-stu-id="f4c56-119">Users are prompted contextually to choose a default app to handle file types, URI schemes, or both when one has not been specified</span></span>
-   <span data-ttu-id="f4c56-120">Os usuários recebem a opção de alterar seu manipulador padrão depois de instalar novos aplicativos que podem manipular um tipo de arquivo ou esquema de URI</span><span class="sxs-lookup"><span data-stu-id="f4c56-120">Users are offered the option to change their default handler after installing new apps that can handle a file type or URI scheme</span></span>
-   <span data-ttu-id="f4c56-121">O painel de controle programas padrão permite que os usuários definam padrões para um aplicativo ou para um tipo de arquivo, esquema de URI ou ambos; os aplicativos podem vincular ao painel de controle</span><span class="sxs-lookup"><span data-stu-id="f4c56-121">The default programs control panel allows users to set defaults for an app, or for a file type, URI scheme, or both; apps can link to the control panel</span></span>
-   <span data-ttu-id="f4c56-122">Os padrões podem ser alterados no Windows Explorer</span><span class="sxs-lookup"><span data-stu-id="f4c56-122">Defaults can be changed from Windows Explorer</span></span>

## <a name="solution"></a><span data-ttu-id="f4c56-123">Solução</span><span class="sxs-lookup"><span data-stu-id="f4c56-123">Solution</span></span>

<span data-ttu-id="f4c56-124">Como resultado dessas alterações, estas diretrizes de API são fornecidas:</span><span class="sxs-lookup"><span data-stu-id="f4c56-124">As a result of these changes, this API guidance is provided:</span></span>

-   <span data-ttu-id="f4c56-125">A funcionalidade de algumas chamadas de método na API [IApplicationAssociationRegistration](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration) foi alterada e não deve mais ser usada.</span><span class="sxs-lookup"><span data-stu-id="f4c56-125">The functionality of some method calls within the [IApplicationAssociationRegistration](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration) API has changed, and should no longer be used.</span></span>

    -   <span data-ttu-id="f4c56-126">**Não chame** [QueryAppIsDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefault) / [QueryAppIsDefaultAll](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefaultall) para determinar se um aplicativo é o padrão</span><span class="sxs-lookup"><span data-stu-id="f4c56-126">**Do not** call [QueryAppIsDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefault)/[QueryAppIsDefaultAll](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefaultall) to determine if an app is the default</span></span>
    -   <span data-ttu-id="f4c56-127">**Não chame** [QueryCurrentDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-querycurrentdefault) para determinar qual aplicativo (se houver) é o padrão atual</span><span class="sxs-lookup"><span data-stu-id="f4c56-127">**Do not** call [QueryCurrentDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-querycurrentdefault) to determine which app (if any) is the current default</span></span>
    -   <span data-ttu-id="f4c56-128">**Não chame** [SetAppIsDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefault) / [SetAppIsDefaultAll](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefaultall) para definir o aplicativo padrão</span><span class="sxs-lookup"><span data-stu-id="f4c56-128">**Do not** call [SetAppIsDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefault)/[SetAppIsDefaultAll](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefaultall) to set the default app</span></span>

-   <span data-ttu-id="f4c56-129">A orientação que avança é:</span><span class="sxs-lookup"><span data-stu-id="f4c56-129">The guidance going forward is:</span></span>

    -   <span data-ttu-id="f4c56-130">**Não consultar para** ver qual aplicativo é o manipulador padrão para tipos de arquivo ou esquemas de URI</span><span class="sxs-lookup"><span data-stu-id="f4c56-130">**Do not** query to see which app is the default handler for file types or URI schemes</span></span>

    -   <span data-ttu-id="f4c56-131">**Não** tente monitorar as alterações no manipulador padrão para tipos de arquivo ou esquemas de URI</span><span class="sxs-lookup"><span data-stu-id="f4c56-131">**Do not** attempt to monitor changes in the default handler for file types or URI schemes</span></span>

    -   <span data-ttu-id="f4c56-132">**Não** tente definir um aplicativo como o manipulador padrão para os tipos de arquivo ou esquemas de URI</span><span class="sxs-lookup"><span data-stu-id="f4c56-132">**Do not** attempt to set an app as the default handler for file types or URI schemes</span></span>

    -   <span data-ttu-id="f4c56-133">**Não** tentar gerenciar padrões para tipos de arquivo ou esquemas de URI de dentro de um aplicativo</span><span class="sxs-lookup"><span data-stu-id="f4c56-133">**Do not** attempt to manage defaults for file types or URI schemes from within an app</span></span>

    -   <span data-ttu-id="f4c56-134">**Integre com** o painel de controle [definir programas padrão](../shell/default-programs.md) se desejar permitir que os usuários do seu aplicativo acessem a interface do usuário de gerenciamento padrão (a interface do usuário de gerenciamento no aplicativo não tem mais suporte)</span><span class="sxs-lookup"><span data-stu-id="f4c56-134">**Do** integrate with the [Set Default Programs](../shell/default-programs.md) control panel if you want to allow users of your app to access the default management UI (the management UI within the app is no longer supported)</span></span>

        -   <span data-ttu-id="f4c56-135">Chamar [IApplicationAssociationRegistrationUI:: LaunchAdvancedAssociationUI](/windows/win32/api/shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui) permite que o usuário acesse a página '[definir programas padrão](../shell/default-programs.md)' do painel de controle para o aplicativo especificado</span><span class="sxs-lookup"><span data-stu-id="f4c56-135">Calling [IApplicationAssociationRegistrationUI::LaunchAdvancedAssociationUI](/windows/win32/api/shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui) allows the user to access the ‘[Set Default Programs](../shell/default-programs.md)’ control panel page for the specified app</span></span>

## <a name="tests"></a><span data-ttu-id="f4c56-136">Testes</span><span class="sxs-lookup"><span data-stu-id="f4c56-136">Tests</span></span>

-   <span data-ttu-id="f4c56-137">Teste para verificar se os aplicativos são registrados corretamente no painel de controle definir programas padrão</span><span class="sxs-lookup"><span data-stu-id="f4c56-137">Test to verify that apps register properly in Set Default Programs control panel</span></span>
-   <span data-ttu-id="f4c56-138">Teste para verificar se os aplicativos são registrados corretamente para aparecer na lista de OpenWith para os tipos de arquivo, esquemas de URI ou ambos, que eles registram para manipular</span><span class="sxs-lookup"><span data-stu-id="f4c56-138">Test to verify that apps register properly to appear in the OpenWith list for the file types, URI schemes, or both, that they register to handle</span></span>
-   <span data-ttu-id="f4c56-139">Teste para verificar se as novas notificações de aplicativo aparecem depois que seu aplicativo está instalado e o usuário invoca um tipo de arquivo, esquema de URI ou ambos, que seu aplicativo registrou para manipular</span><span class="sxs-lookup"><span data-stu-id="f4c56-139">Test to verify that new app notifications appear after your app is installed and the user invokes a file type, URI scheme, or both, that your app has registered to handle</span></span>

## <a name="resources"></a><span data-ttu-id="f4c56-140">Recursos</span><span class="sxs-lookup"><span data-stu-id="f4c56-140">Resources</span></span>

-   <span data-ttu-id="f4c56-141">[Práticas recomendadas para tipos de arquivo e associações de URI em aplicativos de área de trabalho do Windows 8](/previous-versions/windows/desktop/legacy/cc144156(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f4c56-141">[Best Practices for File Type and URI Associations in Windows 8 Desktop Apps](/previous-versions/windows/desktop/legacy/cc144156(v=vs.85))</span></span>
-   [<span data-ttu-id="f4c56-142">Associação de tipo de arquivo e apresentação de conferência de Build de reprodução automática</span><span class="sxs-lookup"><span data-stu-id="f4c56-142">File Type Associations and AutoPlay Build Conference Presentation</span></span>](https://channel9.msdn.com/events/BUILD/BUILD2011/PLAT-282T)

 

 