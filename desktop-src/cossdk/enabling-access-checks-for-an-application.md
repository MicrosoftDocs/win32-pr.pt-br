---
description: A execução desta etapa habilita as verificações de acesso do processo ou a segurança total baseada em função, dependendo do nível de segurança que você selecionar e se você habilita a verificação de acesso para componentes individuais.
ms.assetid: 266bdac1-41be-45a5-a8c7-f9c6fe08445c
title: Habilitando verificações de acesso para um aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3d64a32b23467f85c368e088a870ebe5e4d683e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770631"
---
# <a name="enabling-access-checks-for-an-application"></a><span data-ttu-id="71b7d-103">Habilitando verificações de acesso para um aplicativo</span><span class="sxs-lookup"><span data-stu-id="71b7d-103">Enabling Access Checks for an Application</span></span>

<span data-ttu-id="71b7d-104">A execução desta etapa habilita as verificações de acesso do processo ou a segurança total baseada em função, dependendo do nível de segurança que você selecionar e se você habilita a verificação de acesso para componentes individuais.</span><span class="sxs-lookup"><span data-stu-id="71b7d-104">Performing this step enables either process access checks or full role-based security, depending on what security level you select and whether you enable access checking for individual components.</span></span>

<span data-ttu-id="71b7d-105">**Para habilitar verificações de acesso para um aplicativo**</span><span class="sxs-lookup"><span data-stu-id="71b7d-105">**To enable access checks for an application**</span></span>

1.  <span data-ttu-id="71b7d-106">Na árvore de console da ferramenta administrativa serviços de componentes, clique com o botão direito do mouse no aplicativo COM+ para o qual você deseja habilitar as verificações de acesso e clique em **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="71b7d-106">In the console tree of the Component Services administrative tool, right-click the COM+ application for which you want to enable access checks, and then click **Properties**.</span></span>

2.  <span data-ttu-id="71b7d-107">Na caixa de diálogo Propriedades do aplicativo, clique na guia **segurança** .</span><span class="sxs-lookup"><span data-stu-id="71b7d-107">In the application properties dialog box, click the **Security** tab.</span></span>

3.  <span data-ttu-id="71b7d-108">Marque a caixa de seleção **impor verificações de acesso para este aplicativo** .</span><span class="sxs-lookup"><span data-stu-id="71b7d-108">Select the **Enforce access checks for this application** check box.</span></span>

4.  <span data-ttu-id="71b7d-109">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="71b7d-109">Click **OK**.</span></span>

> [!Note]  
> <span data-ttu-id="71b7d-110">A partir do Windows Server 2003, as verificações de acesso são habilitadas por padrão ao criar um aplicativo COM+.</span><span class="sxs-lookup"><span data-stu-id="71b7d-110">As of Windows Server 2003, access checks are enabled by default when creating a COM+ application.</span></span> <span data-ttu-id="71b7d-111">As verificações de acesso são habilitadas por padrão no nível do aplicativo e desabilitadas por padrão no nível do componente.</span><span class="sxs-lookup"><span data-stu-id="71b7d-111">Access checks are enabled by default at the application level and disabled by default at the component level.</span></span> <span data-ttu-id="71b7d-112">Anteriormente, as verificações de acesso foram desabilitadas por padrão no nível do aplicativo e habilitadas por padrão no nível do componente.</span><span class="sxs-lookup"><span data-stu-id="71b7d-112">Previously, access checks were disabled by default at the application level and enabled by default at the component level.</span></span>

 

<span data-ttu-id="71b7d-113">Depois de habilitar as verificações de acesso, você deve selecionar o nível de segurança apropriado.</span><span class="sxs-lookup"><span data-stu-id="71b7d-113">After enabling access checks, you should select the appropriate security level.</span></span> <span data-ttu-id="71b7d-114">Consulte [definindo um nível de segurança para verificações de acesso](setting-a-security-level-for-access-checks.md).</span><span class="sxs-lookup"><span data-stu-id="71b7d-114">See [Setting a Security Level for Access Checks](setting-a-security-level-for-access-checks.md).</span></span> <span data-ttu-id="71b7d-115">Além disso, você deve ter certeza de definir funções e adicioná-las ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="71b7d-115">Also, you must be sure to define roles and add them to the application.</span></span> <span data-ttu-id="71b7d-116">Se as verificações de acesso estiverem habilitadas, mas nenhuma função tiver sido adicionada, todas as chamadas para o aplicativo falharão.</span><span class="sxs-lookup"><span data-stu-id="71b7d-116">If access checks are enabled but no roles have been added, all calls to the application will fail.</span></span> <span data-ttu-id="71b7d-117">Consulte [definindo funções para um aplicativo](defining-roles-for-an-application.md).</span><span class="sxs-lookup"><span data-stu-id="71b7d-117">See [Defining Roles for an Application](defining-roles-for-an-application.md).</span></span>

> [!Note]  
> <span data-ttu-id="71b7d-118">Ao depurar seu aplicativo, pode ser útil desabilitar a segurança para que você possa se concentrar em outros aspectos do comportamento e do design do seu programa.</span><span class="sxs-lookup"><span data-stu-id="71b7d-118">When debugging your application, it might be helpful to disable security so that you can concentrate on other aspects of your program's behavior and design.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="71b7d-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="71b7d-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71b7d-120">Atribuindo funções a componentes, interfaces ou métodos</span><span class="sxs-lookup"><span data-stu-id="71b7d-120">Assigning Roles to Components, Interfaces, or Methods</span></span>](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[<span data-ttu-id="71b7d-121">Configurando a segurança do Role-Based</span><span class="sxs-lookup"><span data-stu-id="71b7d-121">Configuring Role-Based Security</span></span>](configuring-role-based-security.md)
</dt> <dt>

[<span data-ttu-id="71b7d-122">Definindo funções para um aplicativo</span><span class="sxs-lookup"><span data-stu-id="71b7d-122">Defining Roles for an Application</span></span>](defining-roles-for-an-application.md)
</dt> <dt>

[<span data-ttu-id="71b7d-123">Habilitando verificações de acesso no nível do componente</span><span class="sxs-lookup"><span data-stu-id="71b7d-123">Enabling Access Checks at the Component Level</span></span>](enabling-access-checks-at-the-component-level.md)
</dt> <dt>

[<span data-ttu-id="71b7d-124">Configurando um nível de segurança para verificações de acesso</span><span class="sxs-lookup"><span data-stu-id="71b7d-124">Setting a Security Level for Access Checks</span></span>](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 



