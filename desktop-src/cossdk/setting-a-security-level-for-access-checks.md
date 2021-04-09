---
description: Depois de habilitar as verificações de acesso, para seu aplicativo COM+, você deve selecionar o nível no qual deseja que as verificações de acesso sejam executadas.
ms.assetid: 9c044add-7761-4378-b7eb-bf4e84e913b3
title: Configurando um nível de segurança para verificações de acesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 646a49a4966bff7c593f12cb7481f4a4aad8859e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089494"
---
# <a name="setting-a-security-level-for-access-checks"></a><span data-ttu-id="a7f5d-103">Configurando um nível de segurança para verificações de acesso</span><span class="sxs-lookup"><span data-stu-id="a7f5d-103">Setting a Security Level for Access Checks</span></span>

<span data-ttu-id="a7f5d-104">Depois de habilitar as [verificações de acesso](enabling-access-checks-for-an-application.md), para seu aplicativo com+, você deve selecionar o nível no qual deseja que as verificações de acesso sejam executadas.</span><span class="sxs-lookup"><span data-stu-id="a7f5d-104">After you have enabled [access checks](enabling-access-checks-for-an-application.md), for your COM+ application, you must select the level at which you wish to have access checks performed.</span></span>

<span data-ttu-id="a7f5d-105">**Para selecionar um nível de segurança**</span><span class="sxs-lookup"><span data-stu-id="a7f5d-105">**To select a security level**</span></span>

1.  <span data-ttu-id="a7f5d-106">Na árvore de console da ferramenta administrativa serviços de componentes, clique com o botão direito do mouse no aplicativo COM+ para o qual você deseja habilitar as verificações de acesso e clique em **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="a7f5d-106">In the console tree of the Component Services administrative tool, right-click the COM+ application for which you want to enable access checks, and then click **Properties**.</span></span>

2.  <span data-ttu-id="a7f5d-107">Na caixa de diálogo Propriedades do aplicativo, clique na guia **segurança** .</span><span class="sxs-lookup"><span data-stu-id="a7f5d-107">In the application properties dialog box, click the **Security** tab.</span></span>

3.  <span data-ttu-id="a7f5d-108">Em **nível de segurança**, selecione uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="a7f5d-108">Under **Security level**, select one of the following:</span></span>

    -   <span data-ttu-id="a7f5d-109">**Executar verificações de acesso somente no nível do processo**– essa configuração indica que os usuários em funções atribuídas ao aplicativo serão adicionados ao descritor de segurança do processo.</span><span class="sxs-lookup"><span data-stu-id="a7f5d-109">**Perform access checks only at the process level**— This setting indicates that users in roles that are assigned to the application will be added to the process security descriptor.</span></span> <span data-ttu-id="a7f5d-110">Isso tem os seguintes efeitos e implicações:</span><span class="sxs-lookup"><span data-stu-id="a7f5d-110">This has the following effects and implications:</span></span>

        <span data-ttu-id="a7f5d-111">A verificação de função refinada é desativada nos níveis de componente, método e interface.</span><span class="sxs-lookup"><span data-stu-id="a7f5d-111">Fine-grained role checking is turned off at the component, method, and interface levels.</span></span> <span data-ttu-id="a7f5d-112">As verificações de segurança são executadas somente no nível do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a7f5d-112">Security checks are performed only at the application level.</span></span>

        <span data-ttu-id="a7f5d-113">A propriedade de segurança não está incluída no contexto de todos os objetos em execução no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a7f5d-113">The security property is not included on the context for any objects running within the application.</span></span> <span data-ttu-id="a7f5d-114">Isso pode afetar potencialmente o modo como os objetos são ativados.</span><span class="sxs-lookup"><span data-stu-id="a7f5d-114">This can potentially affect how objects are activated.</span></span> <span data-ttu-id="a7f5d-115">Consulte [propriedade de contexto de segurança](security-context-property.md).</span><span class="sxs-lookup"><span data-stu-id="a7f5d-115">See [Security Context Property](security-context-property.md).</span></span>

        <span data-ttu-id="a7f5d-116">O contexto de chamada de segurança não será disponibilizado.</span><span class="sxs-lookup"><span data-stu-id="a7f5d-116">The security call context will not be made available.</span></span> <span data-ttu-id="a7f5d-117">A segurança programática que se baseia em informações de contexto de chamada de segurança não funcionará.</span><span class="sxs-lookup"><span data-stu-id="a7f5d-117">Programmatic security that relies on security call context information will not function.</span></span> <span data-ttu-id="a7f5d-118">Consulte [informações de contexto de chamada de segurança](security-call-context-information.md).</span><span class="sxs-lookup"><span data-stu-id="a7f5d-118">See [Security Call Context Information](security-call-context-information.md).</span></span>

    -   <span data-ttu-id="a7f5d-119">**Executar verificações de acesso no nível do processo e do componente**– essa configuração indica que as verificações do descritor de segurança em nível de processo e verificações completas de segurança baseadas em função serão executadas.</span><span class="sxs-lookup"><span data-stu-id="a7f5d-119">**Perform access checks at the process and component level**—This setting indicates that process-level security descriptor checks and full role-based security checks will be performed.</span></span> <span data-ttu-id="a7f5d-120">Isso tem os seguintes efeitos e implicações:</span><span class="sxs-lookup"><span data-stu-id="a7f5d-120">This has the following effects and implications:</span></span>

        <span data-ttu-id="a7f5d-121">Para habilitar a verificação de função para componentes específicos, você deve [habilitar as verificações de acesso no nível do componente](enabling-access-checks-at-the-component-level.md).</span><span class="sxs-lookup"><span data-stu-id="a7f5d-121">To enable role checking for particular components, you must [enable access checks at the component level](enabling-access-checks-at-the-component-level.md).</span></span>

        <span data-ttu-id="a7f5d-122">A propriedade de segurança é incluída no contexto de todos os objetos em execução no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a7f5d-122">The security property is included on the context for any objects running within the application.</span></span> <span data-ttu-id="a7f5d-123">Isso pode afetar potencialmente o modo como os objetos são ativados.</span><span class="sxs-lookup"><span data-stu-id="a7f5d-123">This can potentially affect how objects are activated.</span></span> <span data-ttu-id="a7f5d-124">Consulte [propriedade de contexto de segurança](security-context-property.md).</span><span class="sxs-lookup"><span data-stu-id="a7f5d-124">See [Security Context Property](security-context-property.md).</span></span>

        <span data-ttu-id="a7f5d-125">O contexto de chamada de segurança está disponível.</span><span class="sxs-lookup"><span data-stu-id="a7f5d-125">The security call context is available.</span></span> <span data-ttu-id="a7f5d-126">A segurança baseada em função programática está habilitada.</span><span class="sxs-lookup"><span data-stu-id="a7f5d-126">Programmatic role-based security is enabled.</span></span> <span data-ttu-id="a7f5d-127">Consulte [informações de contexto de chamada de segurança](security-call-context-information.md).</span><span class="sxs-lookup"><span data-stu-id="a7f5d-127">See [Security Call Context Information](security-call-context-information.md).</span></span>

        > [!Note]  
        > <span data-ttu-id="a7f5d-128">Para aplicativos de biblioteca COM+, você deve optar por verificar tanto no processo quanto em níveis de componente para qualquer verificação de acesso significativa para funcionar.</span><span class="sxs-lookup"><span data-stu-id="a7f5d-128">For COM+ library applications, you must choose to check both at process and at component levels for any meaningful access checking to work.</span></span> <span data-ttu-id="a7f5d-129">Os aplicativos de biblioteca dependem do processo de host para segurança em nível de processo.</span><span class="sxs-lookup"><span data-stu-id="a7f5d-129">Library applications rely on the host process for process-level security.</span></span> <span data-ttu-id="a7f5d-130">Você pode determinar como o aplicativo de biblioteca interage com a autenticação executada pelo processo de host [definindo a autenticação](enabling-authentication-for-a-library-application.md).</span><span class="sxs-lookup"><span data-stu-id="a7f5d-130">You can determine how the library application interacts with authentication performed by the host process by [setting authentication](enabling-authentication-for-a-library-application.md).</span></span> <span data-ttu-id="a7f5d-131">Para obter mais informações, consulte [segurança do aplicativo de biblioteca](library-application-security.md).</span><span class="sxs-lookup"><span data-stu-id="a7f5d-131">For more information, see [Library Application Security](library-application-security.md).</span></span>

         

4.  <span data-ttu-id="a7f5d-132">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="a7f5d-132">Click **OK**.</span></span>

<span data-ttu-id="a7f5d-133">Na próxima vez em que o aplicativo for iniciado, a segurança será verificada automaticamente no nível especificado.</span><span class="sxs-lookup"><span data-stu-id="a7f5d-133">The next time the application is started, security will automatically be checked at the specified level.</span></span> <span data-ttu-id="a7f5d-134">Somente os usuários atribuídos às funções atribuídas ao aplicativo receberão acesso ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a7f5d-134">Only users assigned to roles assigned to the application will be given access to the application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a7f5d-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a7f5d-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7f5d-136">Atribuindo funções a componentes, interfaces ou métodos</span><span class="sxs-lookup"><span data-stu-id="a7f5d-136">Assigning Roles to Components, Interfaces, or Methods</span></span>](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[<span data-ttu-id="a7f5d-137">Configurando a segurança do Role-Based</span><span class="sxs-lookup"><span data-stu-id="a7f5d-137">Configuring Role-Based Security</span></span>](configuring-role-based-security.md)
</dt> <dt>

[<span data-ttu-id="a7f5d-138">Definindo funções para um aplicativo</span><span class="sxs-lookup"><span data-stu-id="a7f5d-138">Defining Roles for an Application</span></span>](defining-roles-for-an-application.md)
</dt> <dt>

[<span data-ttu-id="a7f5d-139">Habilitando verificações de acesso para um aplicativo</span><span class="sxs-lookup"><span data-stu-id="a7f5d-139">Enabling Access Checks for an Application</span></span>](enabling-access-checks-for-an-application.md)
</dt> <dt>

[<span data-ttu-id="a7f5d-140">Habilitando verificações de acesso no nível do componente</span><span class="sxs-lookup"><span data-stu-id="a7f5d-140">Enabling Access Checks at the Component Level</span></span>](enabling-access-checks-at-the-component-level.md)
</dt> </dl>

 

 



