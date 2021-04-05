---
description: Repositórios de política de autorização, aplicativos e escopos representam diferentes níveis de organização da política do Gerenciador de autorização.
ms.assetid: 235f236d-59c9-4a8c-aec6-60d1ddba4d5d
title: Repositórios de política, aplicativos e escopos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4155d7bf60d34474d52c27efd50d2f53741fa73a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827343"
---
# <a name="policy-stores-applications-and-scopes"></a><span data-ttu-id="e06c2-103">Repositórios de política, aplicativos e escopos</span><span class="sxs-lookup"><span data-stu-id="e06c2-103">Policy Stores, Applications, and Scopes</span></span>

<span data-ttu-id="e06c2-104">Repositórios de política de autorização, aplicativos e escopos representam diferentes níveis de organização da política do Gerenciador de autorização.</span><span class="sxs-lookup"><span data-stu-id="e06c2-104">Authorization policy stores, applications, and scopes represent different levels of organization of Authorization Manager policy.</span></span> <span data-ttu-id="e06c2-105">Um repositório de políticas pode conter um ou mais aplicativos, e um aplicativo pode conter um ou mais escopos.</span><span class="sxs-lookup"><span data-stu-id="e06c2-105">A policy store can contain one or more applications, and an application can contain one or more scopes.</span></span>

-   [<span data-ttu-id="e06c2-106">Repositórios de política de autorização</span><span class="sxs-lookup"><span data-stu-id="e06c2-106">Authorization Policy Stores</span></span>](#authorization-policy-stores)
-   [<span data-ttu-id="e06c2-107">Aplicativos</span><span class="sxs-lookup"><span data-stu-id="e06c2-107">Applications</span></span>](#policy-stores-applications-and-scopes)
-   [<span data-ttu-id="e06c2-108">Escopos</span><span class="sxs-lookup"><span data-stu-id="e06c2-108">Scopes</span></span>](#policy-stores-applications-and-scopes)
-   [<span data-ttu-id="e06c2-109">Delegação</span><span class="sxs-lookup"><span data-stu-id="e06c2-109">Delegation</span></span>](#delegation)
-   [<span data-ttu-id="e06c2-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e06c2-110">Related topics</span></span>](#related-topics)

## <a name="authorization-policy-stores"></a><span data-ttu-id="e06c2-111">Repositórios de política de autorização</span><span class="sxs-lookup"><span data-stu-id="e06c2-111">Authorization Policy Stores</span></span>

<span data-ttu-id="e06c2-112">Na API do Gerenciador de autorização, um repositório de política de autorização é representado por um objeto [**IAzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) .</span><span class="sxs-lookup"><span data-stu-id="e06c2-112">In the Authorization Manager API, an authorization policy store is represented by an [**IAzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object.</span></span> <span data-ttu-id="e06c2-113">O repositório de políticas de autorização contém definições e atribuições de aplicativos, escopos, operações, tarefas, funções e grupos de usuários.</span><span class="sxs-lookup"><span data-stu-id="e06c2-113">The authorization policy store contains definitions and assignments of applications, scopes, operations, tasks, roles, and user groups.</span></span>

<span data-ttu-id="e06c2-114">Um repositório de diretivas de autorização pode ser armazenado como um arquivo XML ou em Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e06c2-114">An authorization policy store can be stored either as an XML file or in Active Directory.</span></span>

<span data-ttu-id="e06c2-115">Um aplicativo deve inicializar um repositório de política de autorização antes de alterar as informações na loja ou usar a política de armazenamento para verificar o acesso do cliente aos recursos.</span><span class="sxs-lookup"><span data-stu-id="e06c2-115">An application must initialize an authorization policy store before changing information in the store or using the store policy to check client access to resources.</span></span>

<span data-ttu-id="e06c2-116">Um repositório de diretivas de autorização pode conter um ou mais objetos [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) que representam uma política de autorização para um aplicativo específico.</span><span class="sxs-lookup"><span data-stu-id="e06c2-116">An authorization policy store can contain one or more [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) objects that each represent authorization policy for a specific application.</span></span>

## <a name="applications"></a><span data-ttu-id="e06c2-117">Aplicativos</span><span class="sxs-lookup"><span data-stu-id="e06c2-117">Applications</span></span>

<span data-ttu-id="e06c2-118">Na API do Gerenciador de autorização, um aplicativo é representado por um objeto [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) .</span><span class="sxs-lookup"><span data-stu-id="e06c2-118">In the Authorization Manager API, an application is represented by an [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) object.</span></span> <span data-ttu-id="e06c2-119">Um repositório de diretivas de autorização pode conter informações de política de autorização para muitos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="e06c2-119">An authorization policy store can contain authorization policy information for many applications.</span></span> <span data-ttu-id="e06c2-120">O uso de objetos **IAzApplication** permite que você armazene diferentes políticas de autorização para diferentes aplicativos em um único repositório de políticas.</span><span class="sxs-lookup"><span data-stu-id="e06c2-120">Using **IAzApplication** objects allows you to store different authorization policy for different applications in a single policy store.</span></span>

<span data-ttu-id="e06c2-121">Um repositório de política de autorização deve conter pelo menos um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e06c2-121">An authorization policy store must contain at least one application.</span></span>

## <a name="scopes"></a><span data-ttu-id="e06c2-122">Escopos</span><span class="sxs-lookup"><span data-stu-id="e06c2-122">Scopes</span></span>

<span data-ttu-id="e06c2-123">Na API do Gerenciador de autorização, um escopo é representado por um objeto [**IAzScope**](/windows/desktop/api/Azroles/nn-azroles-iazscope) .</span><span class="sxs-lookup"><span data-stu-id="e06c2-123">In the Authorization Manager API, a scope is represented by an [**IAzScope**](/windows/desktop/api/Azroles/nn-azroles-iazscope) object.</span></span> <span data-ttu-id="e06c2-124">Os escopos fornecem um nível opcional adicional de organização para uma política de autorização.</span><span class="sxs-lookup"><span data-stu-id="e06c2-124">Scopes provide an additional, optional level of organization for an authorization policy.</span></span> <span data-ttu-id="e06c2-125">Um aplicativo pode conter um ou mais escopos, mas não precisa conter nenhum (o Gerenciador de autorização fornece um escopo padrão de todo o aplicativo).</span><span class="sxs-lookup"><span data-stu-id="e06c2-125">An application can contain one or more scopes, but need not contain any (Authorization Manager provides a default, application-wide scope).</span></span>

<span data-ttu-id="e06c2-126">Um escopo é uma subdivisão em um aplicativo que separa recursos de outros recursos que são usados por esse aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e06c2-126">A scope is a subdivision within an application that separates resources from other resources that are used by that application.</span></span> <span data-ttu-id="e06c2-127">Se você tiver grupos do Gerenciador de autorização, atribuições de função, definições de função ou definições de tarefa que não deseja aplicar a um aplicativo inteiro, poderá criá-los no nível de escopo.</span><span class="sxs-lookup"><span data-stu-id="e06c2-127">If you have Authorization Manager groups, role assignments, role definitions, or task definitions that you do not want to apply to an entire application, you can create them at the scope level.</span></span>

## <a name="delegation"></a><span data-ttu-id="e06c2-128">Delegação</span><span class="sxs-lookup"><span data-stu-id="e06c2-128">Delegation</span></span>

<span data-ttu-id="e06c2-129">Os repositórios de diretiva de autorização armazenados no Active Directory dão suporte à delegação de administração.</span><span class="sxs-lookup"><span data-stu-id="e06c2-129">Authorization policy stores that are stored in Active Directory support delegation of administration.</span></span> <span data-ttu-id="e06c2-130">A administração pode ser delegada a usuários e grupos na loja, no aplicativo ou no nível de escopo.</span><span class="sxs-lookup"><span data-stu-id="e06c2-130">Administration can be delegated to users and groups at the store, application, or scope level.</span></span> <span data-ttu-id="e06c2-131">Cada nível define funções administrativas para a política nesse nível.</span><span class="sxs-lookup"><span data-stu-id="e06c2-131">Each level defines administrative roles for the policy at that level.</span></span> <span data-ttu-id="e06c2-132">Para delegar o controle a um usuário ou grupo, atribua-os à função de administrador; para permitir que um usuário ou grupo Leia a política, atribua-os à função leitor.</span><span class="sxs-lookup"><span data-stu-id="e06c2-132">To delegate control to a user or group, assign them to the administrator role; to allow a user or group to read the policy, assign them to the reader role.</span></span>

<span data-ttu-id="e06c2-133">Os administradores de um repositório, aplicativo ou escopo podem ler e modificar o repositório de políticas no nível delegado.</span><span class="sxs-lookup"><span data-stu-id="e06c2-133">Administrators of a store, application, or scope can read and modify the policy store at the delegated level.</span></span> <span data-ttu-id="e06c2-134">Os leitores podem ler o repositório de políticas no nível delegado, mas não podem modificar o repositório.</span><span class="sxs-lookup"><span data-stu-id="e06c2-134">Readers can read the policy store at the delegated level but cannot modify the store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e06c2-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e06c2-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e06c2-136">Criando um objeto de repositório de política de autorização em C++</span><span class="sxs-lookup"><span data-stu-id="e06c2-136">Creating an Authorization Policy Store Object in C++</span></span>](creating-an-authorization-policy-store-object-in-c--.md)
</dt> <dt>

[<span data-ttu-id="e06c2-137">Criando um objeto de aplicativo em C++</span><span class="sxs-lookup"><span data-stu-id="e06c2-137">Creating an Application Object in C++</span></span>](creating-an-application-object-in-c--.md)
</dt> <dt>

[<span data-ttu-id="e06c2-138">Delegando a definição de permissões em C++</span><span class="sxs-lookup"><span data-stu-id="e06c2-138">Delegating the Defining of Permissions in C++</span></span>](delegating-the-defining-of-permissions-in-c--.md)
</dt> </dl>

 

 



