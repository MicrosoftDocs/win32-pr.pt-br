---
description: A tabela AdminExecuteSequence lista as ações que o instalador executa ao chamar a ação de administrador de nível superior. Confira o grupo tabelas de procedimentos de instalação, usando uma tabela de sequência e o exemplo de tabela de sequência detalhado.
ms.assetid: 8b1da4a3-0b82-4b71-8a32-59e90025cbfa
title: Importando o AdminExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60e5cfef89ada780d9ce647f45667fdc34cc5b01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647470"
---
# <a name="importing-the-adminexecutesequence"></a><span data-ttu-id="4a645-104">Importando o AdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="4a645-104">Importing the AdminExecuteSequence</span></span>

<span data-ttu-id="4a645-105">A [tabela AdminExecuteSequence](adminexecutesequence-table.md) lista as ações que o instalador executa ao chamar a [ação de administrador](admin-action.md)de nível superior.</span><span class="sxs-lookup"><span data-stu-id="4a645-105">The [AdminExecuteSequence table](adminexecutesequence-table.md) lists actions that the installer executes when it calls the top-level [ADMIN action](admin-action.md).</span></span> <span data-ttu-id="4a645-106">Confira o [grupo tabelas de procedimentos de instalação](installation-procedure-tables-group.md), [usando uma tabela de sequência](using-a-sequence-table.md)e o exemplo de tabela de [sequência detalhado](sequence-table-detailed-example.md).</span><span class="sxs-lookup"><span data-stu-id="4a645-106">See [Installation Procedure Tables Group](installation-procedure-tables-group.md), [Using a Sequence Table](using-a-sequence-table.md), and the [Sequence Table Detailed Example](sequence-table-detailed-example.md).</span></span>

<span data-ttu-id="4a645-107">Se na seção [importando um banco de dados em branco](importing-a-blank-database.md) usado uisample.msi do SDK do Windows Installer, as tabelas de sequência em sua cópia do MNP2000.msi já contêm as sequências de ações sugeridas descritas em [usando uma tabela de sequência](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="4a645-107">If in the section [Importing a Blank Database](importing-a-blank-database.md) you used uisample.msi from the Windows Installer SDK, the sequence tables in your copy of MNP2000.msi already contains the suggested action sequences described in [Using a Sequence Table](using-a-sequence-table.md).</span></span> <span data-ttu-id="4a645-108">Nenhuma alteração nessas sequências deve ser necessária para criar o pacote de instalação de exemplo do bloco de notas.</span><span class="sxs-lookup"><span data-stu-id="4a645-108">No changes to these sequences should be necessary to author the Notepad sample installation package.</span></span>

<span data-ttu-id="4a645-109">Use o editor de banco de dados para abrir MNP2000.msi e insira os dados a seguir na tabela AdminExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="4a645-109">Use your database editor to open MNP2000.msi and enter the following data into the AdminExecuteSequence table.</span></span>

[<span data-ttu-id="4a645-110">Tabela AdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="4a645-110">AdminExecuteSequence Table</span></span>](adminexecutesequence-table.md)



| <span data-ttu-id="4a645-111">Ação</span><span class="sxs-lookup"><span data-stu-id="4a645-111">Action</span></span>              | <span data-ttu-id="4a645-112">Condição</span><span class="sxs-lookup"><span data-stu-id="4a645-112">Condition</span></span> | <span data-ttu-id="4a645-113">Sequência</span><span class="sxs-lookup"><span data-stu-id="4a645-113">Sequence</span></span> |
|---------------------|-----------|----------|
| <span data-ttu-id="4a645-114">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="4a645-114">CostFinalize</span></span>        |           | <span data-ttu-id="4a645-115">1000</span><span class="sxs-lookup"><span data-stu-id="4a645-115">1000</span></span>     |
| <span data-ttu-id="4a645-116">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="4a645-116">CostInitialize</span></span>      |           | <span data-ttu-id="4a645-117">800</span><span class="sxs-lookup"><span data-stu-id="4a645-117">800</span></span>      |
| <span data-ttu-id="4a645-118">Custo de</span><span class="sxs-lookup"><span data-stu-id="4a645-118">FileCost</span></span>            |           | <span data-ttu-id="4a645-119">900</span><span class="sxs-lookup"><span data-stu-id="4a645-119">900</span></span>      |
| <span data-ttu-id="4a645-120">InstallAdminPackage</span><span class="sxs-lookup"><span data-stu-id="4a645-120">InstallAdminPackage</span></span> |           | <span data-ttu-id="4a645-121">3900</span><span class="sxs-lookup"><span data-stu-id="4a645-121">3900</span></span>     |
| <span data-ttu-id="4a645-122">InstallFiles</span><span class="sxs-lookup"><span data-stu-id="4a645-122">InstallFiles</span></span>        |           | <span data-ttu-id="4a645-123">4000</span><span class="sxs-lookup"><span data-stu-id="4a645-123">4000</span></span>     |
| <span data-ttu-id="4a645-124">InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="4a645-124">InstallFinalize</span></span>     |           | <span data-ttu-id="4a645-125">6600</span><span class="sxs-lookup"><span data-stu-id="4a645-125">6600</span></span>     |
| <span data-ttu-id="4a645-126">InstallInitialize</span><span class="sxs-lookup"><span data-stu-id="4a645-126">InstallInitialize</span></span>   |           | <span data-ttu-id="4a645-127">1500</span><span class="sxs-lookup"><span data-stu-id="4a645-127">1500</span></span>     |
| <span data-ttu-id="4a645-128">InstallValidate</span><span class="sxs-lookup"><span data-stu-id="4a645-128">InstallValidate</span></span>     |           | <span data-ttu-id="4a645-129">1.400</span><span class="sxs-lookup"><span data-stu-id="4a645-129">1400</span></span>     |



 

[<span data-ttu-id="4a645-130">Continuar</span><span class="sxs-lookup"><span data-stu-id="4a645-130">Continue</span></span>](importing-the-adminuisequence.md)

 

 



