---
description: As ações personalizadas ProcessAccounts e UninstallAccounts geram as ações personalizadas adiadas que criam, removem ou rerecuperam contas de usuário.
ms.assetid: 245b576b-96cc-4eab-8848-5ff78ba32873
title: Criando a tabela InstallExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aa09895d5e5d2543b5594f4795734d26163a4f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768480"
---
# <a name="authoring-the-installexecutesequence-table"></a><span data-ttu-id="3ed46-103">Criando a tabela InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="3ed46-103">Authoring the InstallExecuteSequence Table</span></span>

<span data-ttu-id="3ed46-104">As ações personalizadas ProcessAccounts e UninstallAccounts geram as ações personalizadas adiadas que criam, removem ou rerecuperam contas de usuário.</span><span class="sxs-lookup"><span data-stu-id="3ed46-104">The custom actions ProcessAccounts and UninstallAccounts generate the deferred custom actions that create, remove, or rollback user accounts.</span></span> <span data-ttu-id="3ed46-105">As ações personalizadas ProcessAccounts e UninstallAccounts devem ser inseridas na [tabela InstallExecuteSequence](installexecutesequence-table.md) para serem executadas.</span><span class="sxs-lookup"><span data-stu-id="3ed46-105">The custom actions ProcessAccounts and UninstallAccounts must be entered into the [InstallExecuteSequence table](installexecutesequence-table.md) to be executed.</span></span> <span data-ttu-id="3ed46-106">Adicione as entradas a seguir à [tabela InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="3ed46-106">Add the following entries to the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="3ed46-107">Como essas ações personalizadas devem fazer parte da geração de script, ambas as ações personalizadas devem ser sequenciadas após a [ação InstallInitialize](installinitialize-action.md).</span><span class="sxs-lookup"><span data-stu-id="3ed46-107">Because these custom actions must be a part of the script generation, both custom actions must be sequenced after the [InstallInitialize action](installinitialize-action.md).</span></span>

<span data-ttu-id="3ed46-108">A condição em ProcessAccounts garante o seguinte.</span><span class="sxs-lookup"><span data-stu-id="3ed46-108">The condition on ProcessAccounts ensures the following.</span></span> <span data-ttu-id="3ed46-109">Consulte [sintaxe de instrução condicional](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="3ed46-109">See [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

-   <span data-ttu-id="3ed46-110">ProcessAccounts será executado somente se o componente TestAccount estiver sendo instalado localmente no computador.</span><span class="sxs-lookup"><span data-stu-id="3ed46-110">ProcessAccounts runs only if the component TestAccount is being installed locally on the computer.</span></span>
-   <span data-ttu-id="3ed46-111">A conta de teste de componente não está instalada no momento ou está instalada para ser executada a partir da origem.</span><span class="sxs-lookup"><span data-stu-id="3ed46-111">The component Test Account is currently not installed or is installed to run from the source.</span></span>

<span data-ttu-id="3ed46-112">A condição em UninstallAccount garante o seguinte:</span><span class="sxs-lookup"><span data-stu-id="3ed46-112">The condition on UninstallAccount ensures the following:</span></span>

-   <span data-ttu-id="3ed46-113">UninstallAccounts será executado somente se o componente TestAccount estiver instalado localmente no computador.</span><span class="sxs-lookup"><span data-stu-id="3ed46-113">UninstallAccounts runs only if the component TestAccount is installed locally on the computer.</span></span>
-   <span data-ttu-id="3ed46-114">A conta de teste de componente está sendo removida ou instalada para ser executada da origem.</span><span class="sxs-lookup"><span data-stu-id="3ed46-114">The component Test Account is being removed or being installed to run from the source.</span></span>

[<span data-ttu-id="3ed46-115">Tabela InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="3ed46-115">InstallExecuteSequence Table</span></span>](installexecutesequence-table.md)



| <span data-ttu-id="3ed46-116">Ação</span><span class="sxs-lookup"><span data-stu-id="3ed46-116">Action</span></span>            | <span data-ttu-id="3ed46-117">Condição</span><span class="sxs-lookup"><span data-stu-id="3ed46-117">Condition</span></span>                                                           | <span data-ttu-id="3ed46-118">Sequência</span><span class="sxs-lookup"><span data-stu-id="3ed46-118">Sequence</span></span> |
|-------------------|---------------------------------------------------------------------|----------|
| <span data-ttu-id="3ed46-119">ProcessAccounts</span><span class="sxs-lookup"><span data-stu-id="3ed46-119">ProcessAccounts</span></span>   | <span data-ttu-id="3ed46-120">VersionNT e (? TestAccount = 2 ou? TestAccount = 4) e $TestAccount = 3</span><span class="sxs-lookup"><span data-stu-id="3ed46-120">VersionNT AND (?TestAccount=2 OR ?TestAccount=4) AND $TestAccount=3</span></span> | <span data-ttu-id="3ed46-121">1550</span><span class="sxs-lookup"><span data-stu-id="3ed46-121">1550</span></span>     |
| <span data-ttu-id="3ed46-122">UninstallAccounts</span><span class="sxs-lookup"><span data-stu-id="3ed46-122">UninstallAccounts</span></span> | <span data-ttu-id="3ed46-123">VersionNT e? TestAccount = 3 e ($TestAccount = 4 ou $TestAccount = 2)</span><span class="sxs-lookup"><span data-stu-id="3ed46-123">VersionNT AND ?TestAccount=3 AND ($TestAccount=4 OR $TestAccount=2)</span></span> | <span data-ttu-id="3ed46-124">1560</span><span class="sxs-lookup"><span data-stu-id="3ed46-124">1560</span></span>     |



 

<span data-ttu-id="3ed46-125">Continue a [criar a interface do usuário para entrada de senha](authoring-the-user-interface-for-password-input.md).</span><span class="sxs-lookup"><span data-stu-id="3ed46-125">Continue to [Authoring the user interface for password input](authoring-the-user-interface-for-password-input.md).</span></span>

 

 



