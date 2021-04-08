---
description: Insira registros para as cinco ações personalizadas de exemplo criadas na seção anterior para a tabela CustomAction. Para obter mais informações sobre como preencher a tabela CustomAction para esse tipo de ação personalizada, consulte tipo de ação personalizada 1.
ms.assetid: 56828105-bd72-426d-833f-f756c577c77f
title: Criando a tabela CustomAction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56fb7d8cf99a30200e6a5525e3516e2b888c1129
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921490"
---
# <a name="authoring-the-customaction-table"></a><span data-ttu-id="2a258-104">Criando a tabela CustomAction</span><span class="sxs-lookup"><span data-stu-id="2a258-104">Authoring the CustomAction Table</span></span>

<span data-ttu-id="2a258-105">Insira registros para as cinco ações personalizadas de exemplo criadas na seção anterior para a [tabela CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="2a258-105">Enter records for the five sample custom actions created in the previous section to the [CustomAction Table](customaction-table.md).</span></span> <span data-ttu-id="2a258-106">Para obter mais informações sobre como preencher a tabela CustomAction para esse tipo de ação personalizada, consulte [tipo de ação personalizada 1](custom-action-type-1.md).</span><span class="sxs-lookup"><span data-stu-id="2a258-106">For more information on how to populate the CustomAction table for this type of custom action see [Custom Action Type 1](custom-action-type-1.md).</span></span>

[<span data-ttu-id="2a258-107">Tabela CustomAction</span><span class="sxs-lookup"><span data-stu-id="2a258-107">CustomAction Table</span></span>](customaction-table.md)



| <span data-ttu-id="2a258-108">Ação</span><span class="sxs-lookup"><span data-stu-id="2a258-108">Action</span></span>            | <span data-ttu-id="2a258-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="2a258-109">Type</span></span>  | <span data-ttu-id="2a258-110">Fonte</span><span class="sxs-lookup"><span data-stu-id="2a258-110">Source</span></span>      | <span data-ttu-id="2a258-111">Destino</span><span class="sxs-lookup"><span data-stu-id="2a258-111">Target</span></span>                |
|-------------------|-------|-------------|-----------------------|
| <span data-ttu-id="2a258-112">ProcessAccounts</span><span class="sxs-lookup"><span data-stu-id="2a258-112">ProcessAccounts</span></span>   | <span data-ttu-id="2a258-113">1</span><span class="sxs-lookup"><span data-stu-id="2a258-113">1</span></span>     | <span data-ttu-id="2a258-114">Process.dll</span><span class="sxs-lookup"><span data-stu-id="2a258-114">Process.dll</span></span> | <span data-ttu-id="2a258-115">ProcessUserAccounts</span><span class="sxs-lookup"><span data-stu-id="2a258-115">ProcessUserAccounts</span></span>   |
| <span data-ttu-id="2a258-116">UninstallAccounts</span><span class="sxs-lookup"><span data-stu-id="2a258-116">UninstallAccounts</span></span> | <span data-ttu-id="2a258-117">1</span><span class="sxs-lookup"><span data-stu-id="2a258-117">1</span></span>     | <span data-ttu-id="2a258-118">Process.dll</span><span class="sxs-lookup"><span data-stu-id="2a258-118">Process.dll</span></span> | <span data-ttu-id="2a258-119">UninstallUserAccounts</span><span class="sxs-lookup"><span data-stu-id="2a258-119">UninstallUserAccounts</span></span> |
| <span data-ttu-id="2a258-120">CreateAccount</span><span class="sxs-lookup"><span data-stu-id="2a258-120">CreateAccount</span></span>     | <span data-ttu-id="2a258-121">11265</span><span class="sxs-lookup"><span data-stu-id="2a258-121">11265</span></span> | <span data-ttu-id="2a258-122">Create.dll</span><span class="sxs-lookup"><span data-stu-id="2a258-122">Create.dll</span></span>  | <span data-ttu-id="2a258-123">CreateUserAccount</span><span class="sxs-lookup"><span data-stu-id="2a258-123">CreateUserAccount</span></span>     |
| <span data-ttu-id="2a258-124">RemoveAccount</span><span class="sxs-lookup"><span data-stu-id="2a258-124">RemoveAccount</span></span>     | <span data-ttu-id="2a258-125">11265</span><span class="sxs-lookup"><span data-stu-id="2a258-125">11265</span></span> | <span data-ttu-id="2a258-126">Remove.dll</span><span class="sxs-lookup"><span data-stu-id="2a258-126">Remove.dll</span></span>  | <span data-ttu-id="2a258-127">RemoveUserAccount</span><span class="sxs-lookup"><span data-stu-id="2a258-127">RemoveUserAccount</span></span>     |
| <span data-ttu-id="2a258-128">RollbackAccount</span><span class="sxs-lookup"><span data-stu-id="2a258-128">RollbackAccount</span></span>   | <span data-ttu-id="2a258-129">9473</span><span class="sxs-lookup"><span data-stu-id="2a258-129">9473</span></span>  | <span data-ttu-id="2a258-130">Remove.dll</span><span class="sxs-lookup"><span data-stu-id="2a258-130">Remove.dll</span></span>  | <span data-ttu-id="2a258-131">RemoveUserAccount</span><span class="sxs-lookup"><span data-stu-id="2a258-131">RemoveUserAccount</span></span>     |



 

<span data-ttu-id="2a258-132">O código-fonte do C++ para as bibliotecas de vínculo dinâmico são fornecidos no SDK do Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="2a258-132">The C++ source code for the dynamic-link libraries are provided in the Windows Installer SDK.</span></span> <span data-ttu-id="2a258-133">Use o Process. cpp para criar o arquivo Process.dll.</span><span class="sxs-lookup"><span data-stu-id="2a258-133">Use Process.cpp to create the file Process.dll.</span></span> <span data-ttu-id="2a258-134">Use Create. cpp para criar o arquivo Create.dll.</span><span class="sxs-lookup"><span data-stu-id="2a258-134">Use Create.cpp to create the file Create.dll.</span></span> <span data-ttu-id="2a258-135">Use remove. cpp para criar Remove.dll.</span><span class="sxs-lookup"><span data-stu-id="2a258-135">Use Remove.cpp to create Remove.dll.</span></span> <span data-ttu-id="2a258-136">Adicione esses arquivos da biblioteca de vínculo dinâmico à tabela binária.</span><span class="sxs-lookup"><span data-stu-id="2a258-136">Add these dynamic-link library files to the Binary table.</span></span>

[<span data-ttu-id="2a258-137">Tabela binária</span><span class="sxs-lookup"><span data-stu-id="2a258-137">Binary Table</span></span>](binary-table.md)



| <span data-ttu-id="2a258-138">Nome</span><span class="sxs-lookup"><span data-stu-id="2a258-138">Name</span></span>        | <span data-ttu-id="2a258-139">Dados</span><span class="sxs-lookup"><span data-stu-id="2a258-139">Data</span></span>            |
|-------------|-----------------|
| <span data-ttu-id="2a258-140">Process.dll</span><span class="sxs-lookup"><span data-stu-id="2a258-140">Process.dll</span></span> | <span data-ttu-id="2a258-141">{*dados binários*}</span><span class="sxs-lookup"><span data-stu-id="2a258-141">{*binary data*}</span></span> |
| <span data-ttu-id="2a258-142">Create.dll</span><span class="sxs-lookup"><span data-stu-id="2a258-142">Create.dll</span></span>  | <span data-ttu-id="2a258-143">{*dados binários*}</span><span class="sxs-lookup"><span data-stu-id="2a258-143">{*binary data*}</span></span> |
| <span data-ttu-id="2a258-144">Remove.dll</span><span class="sxs-lookup"><span data-stu-id="2a258-144">Remove.dll</span></span>  | <span data-ttu-id="2a258-145">{*dados binários*}</span><span class="sxs-lookup"><span data-stu-id="2a258-145">{*binary data*}</span></span> |



 

<span data-ttu-id="2a258-146">Continue a [Adicionar uma tabela CustomUserAccounts personalizada](adding-a-custom-customuseraccounts-table.md).</span><span class="sxs-lookup"><span data-stu-id="2a258-146">Continue to [Adding a Custom CustomUserAccounts Table](adding-a-custom-customuseraccounts-table.md).</span></span>

 

 



