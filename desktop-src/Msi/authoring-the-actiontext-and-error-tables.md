---
description: As especificações de exemplo incluem o envio de mensagens ActionData quando uma ação personalizada cria ou remove uma conta de usuário e relata um erro se uma conta não puder ser criada.
ms.assetid: ee90fe3d-51f4-433b-a5ce-950a03e1d8fb
title: Criando as tabelas de erro e ActionText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e20646a90ca76c159a88bdd8a6d026ff10845da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828056"
---
# <a name="authoring-the-actiontext-and-error-tables"></a><span data-ttu-id="5d5ca-103">Criando as tabelas de erro e ActionText</span><span class="sxs-lookup"><span data-stu-id="5d5ca-103">Authoring the ActionText and Error Tables</span></span>

<span data-ttu-id="5d5ca-104">As especificações de exemplo incluem o envio de mensagens ActionData quando uma ação personalizada cria ou remove uma conta de usuário e relata um erro se uma conta não puder ser criada.</span><span class="sxs-lookup"><span data-stu-id="5d5ca-104">The sample specifications include sending ActionData messages when a custom action creates or removes a user account, and reporting an error if an account cannot be created.</span></span>

<span data-ttu-id="5d5ca-105">Insira as entradas a seguir na tabela ActionText para fornecer informações usadas pelas mensagens ActionText.</span><span class="sxs-lookup"><span data-stu-id="5d5ca-105">Enter the following entries into the ActionText table to provide information used by ActionText messages.</span></span>

[<span data-ttu-id="5d5ca-106">Tabela ActionText</span><span class="sxs-lookup"><span data-stu-id="5d5ca-106">ActionText Table</span></span>](actiontext-table.md)



| <span data-ttu-id="5d5ca-107">Ação</span><span class="sxs-lookup"><span data-stu-id="5d5ca-107">Action</span></span>            | <span data-ttu-id="5d5ca-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="5d5ca-108">Description</span></span>                                                       | <span data-ttu-id="5d5ca-109">Modelo</span><span class="sxs-lookup"><span data-stu-id="5d5ca-109">Template</span></span>                          |
|-------------------|-------------------------------------------------------------------|-----------------------------------|
| <span data-ttu-id="5d5ca-110">ProcessAccounts</span><span class="sxs-lookup"><span data-stu-id="5d5ca-110">ProcessAccounts</span></span>   | <span data-ttu-id="5d5ca-111">Gerando ações para criar contas de usuário no computador local.</span><span class="sxs-lookup"><span data-stu-id="5d5ca-111">Generating actions to create user accounts on the local computer.</span></span> | <span data-ttu-id="5d5ca-112">Conta: \[ 1 \] , atributos: \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="5d5ca-112">Account: \[1\], Attributes: \[2\]</span></span> |
| <span data-ttu-id="5d5ca-113">CreateAccount</span><span class="sxs-lookup"><span data-stu-id="5d5ca-113">CreateAccount</span></span>     | <span data-ttu-id="5d5ca-114">Criando conta de usuário no computador local.</span><span class="sxs-lookup"><span data-stu-id="5d5ca-114">Creating user account on the local computer.</span></span>                      | <span data-ttu-id="5d5ca-115">Conta: \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="5d5ca-115">Account: \[1\]</span></span>                    |
| <span data-ttu-id="5d5ca-116">RemoveAccount</span><span class="sxs-lookup"><span data-stu-id="5d5ca-116">RemoveAccount</span></span>     | <span data-ttu-id="5d5ca-117">Removendo a conta de usuário do computador local.</span><span class="sxs-lookup"><span data-stu-id="5d5ca-117">Removing user account from the local computer.</span></span>                    | <span data-ttu-id="5d5ca-118">Conta: \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="5d5ca-118">Account: \[1\]</span></span>                    |
| <span data-ttu-id="5d5ca-119">RollbackAccount</span><span class="sxs-lookup"><span data-stu-id="5d5ca-119">RollbackAccount</span></span>   | <span data-ttu-id="5d5ca-120">Reverter a criação de contas de usuário no computador local.</span><span class="sxs-lookup"><span data-stu-id="5d5ca-120">Rolling back the creation of user accounts on the local computer.</span></span> | <span data-ttu-id="5d5ca-121">Conta: \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="5d5ca-121">Account: \[1\]</span></span>                    |
| <span data-ttu-id="5d5ca-122">UninstallAccounts</span><span class="sxs-lookup"><span data-stu-id="5d5ca-122">UninstallAccounts</span></span> | <span data-ttu-id="5d5ca-123">Gerando ações para remover contas de usuário no computador local.</span><span class="sxs-lookup"><span data-stu-id="5d5ca-123">Generating actions to remove user accounts on the local computer.</span></span> | <span data-ttu-id="5d5ca-124">Conta: \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="5d5ca-124">Account: \[1\]</span></span>                    |



 

<span data-ttu-id="5d5ca-125">Insira as entradas a seguir na tabela de erros para fornecer informações usadas pelo relatório de erros.</span><span class="sxs-lookup"><span data-stu-id="5d5ca-125">Enter the following entries into the Error table to provide information used by error reporting.</span></span>

[<span data-ttu-id="5d5ca-126">Tabela de erros</span><span class="sxs-lookup"><span data-stu-id="5d5ca-126">Error Table</span></span>](error-table.md)



| <span data-ttu-id="5d5ca-127">Erro</span><span class="sxs-lookup"><span data-stu-id="5d5ca-127">Error</span></span> | <span data-ttu-id="5d5ca-128">Mensagem</span><span class="sxs-lookup"><span data-stu-id="5d5ca-128">Message</span></span>                                                                        |
|-------|--------------------------------------------------------------------------------|
| <span data-ttu-id="5d5ca-129">25001</span><span class="sxs-lookup"><span data-stu-id="5d5ca-129">25001</span></span> | <span data-ttu-id="5d5ca-130">Não é possível criar a conta de usuário ' \[ 2 \] ' no computador local.</span><span class="sxs-lookup"><span data-stu-id="5d5ca-130">Unable to create user account '\[2\]' on the local machine.</span></span> <span data-ttu-id="5d5ca-131">Código de erro: \[ 3 \] .</span><span class="sxs-lookup"><span data-stu-id="5d5ca-131">Error Code: \[3\].</span></span> |
| <span data-ttu-id="5d5ca-132">25002</span><span class="sxs-lookup"><span data-stu-id="5d5ca-132">25002</span></span> | <span data-ttu-id="5d5ca-133">A conta de usuário ' \[ 2 \] ' já existe no computador local.</span><span class="sxs-lookup"><span data-stu-id="5d5ca-133">User account '\[2\]' already exists on the local machine.</span></span>                      |
| <span data-ttu-id="5d5ca-134">25003</span><span class="sxs-lookup"><span data-stu-id="5d5ca-134">25003</span></span> | <span data-ttu-id="5d5ca-135">Não é possível remover a conta de usuário ' \[ 2 \] ' no computador local.</span><span class="sxs-lookup"><span data-stu-id="5d5ca-135">Unable to remove user account '\[2\]' on the local machine.</span></span> <span data-ttu-id="5d5ca-136">Código de erro: \[ 3 \] .</span><span class="sxs-lookup"><span data-stu-id="5d5ca-136">Error Code: \[3\].</span></span> |
| <span data-ttu-id="5d5ca-137">25004</span><span class="sxs-lookup"><span data-stu-id="5d5ca-137">25004</span></span> | <span data-ttu-id="5d5ca-138">A conta de usuário ' \[ 2 \] ' não existe no computador local.</span><span class="sxs-lookup"><span data-stu-id="5d5ca-138">User account '\[2\]' does not exist on the local machine.</span></span>                      |



 

<span data-ttu-id="5d5ca-139">Continue a [criar a tabela InstallExecuteSequence](authoring-the-installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="5d5ca-139">Continue to [Authoring the InstallExecuteSequence Table](authoring-the-installexecutesequence-table.md).</span></span>

 

 



