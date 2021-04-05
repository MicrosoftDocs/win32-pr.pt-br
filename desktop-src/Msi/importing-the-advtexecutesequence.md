---
description: A tabela AdvtExecuteSequence lista ações que o instalador chama quando executa a ação de anúncio de nível superior. Confira o grupo tabelas de procedimentos de instalação, usando uma tabela de sequência e o exemplo de tabela de sequência detalhado.
ms.assetid: 269bd28c-fa45-42b8-a610-1c4c5fcabc19
title: Importando o AdvtExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e4d7622670973a622b1376456ecfef445684cf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662594"
---
# <a name="importing-the-advtexecutesequence"></a><span data-ttu-id="b5cb8-104">Importando o AdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="b5cb8-104">Importing the AdvtExecuteSequence</span></span>

<span data-ttu-id="b5cb8-105">A [tabela AdvtExecuteSequence](advtexecutesequence-table.md) lista ações que o instalador chama quando executa a [ação de anúncio](advertise-action.md)de nível superior.</span><span class="sxs-lookup"><span data-stu-id="b5cb8-105">The [AdvtExecuteSequence table](advtexecutesequence-table.md) lists actions the installer calls when it executes the top-level [ADVERTISE action](advertise-action.md).</span></span> <span data-ttu-id="b5cb8-106">Confira o [grupo tabelas de procedimentos de instalação](installation-procedure-tables-group.md), [usando uma tabela de sequência](using-a-sequence-table.md)e o exemplo de tabela de [sequência detalhado](sequence-table-detailed-example.md).</span><span class="sxs-lookup"><span data-stu-id="b5cb8-106">See [Installation Procedure Tables Group](installation-procedure-tables-group.md), [Using a Sequence Table](using-a-sequence-table.md), and the [Sequence Table Detailed Example](sequence-table-detailed-example.md).</span></span>

<span data-ttu-id="b5cb8-107">Se na seção [importando um banco de dados em branco](importing-a-blank-database.md) usado uisample.msi do SDK do Windows Installer, as tabelas de sequência em sua cópia do MNP2000.msi já contêm as sequências de ações sugeridas descritas em [usando uma tabela de sequência](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="b5cb8-107">If in the section [Importing a Blank Database](importing-a-blank-database.md) you used uisample.msi from the Windows Installer SDK, the sequence tables in your copy of MNP2000.msi already contains the suggested action sequences described in [Using a Sequence table](using-a-sequence-table.md).</span></span> <span data-ttu-id="b5cb8-108">Nenhuma alteração nessas sequências deve ser necessária para criar o pacote de instalação de exemplo do bloco de notas.</span><span class="sxs-lookup"><span data-stu-id="b5cb8-108">No changes to these sequences should be necessary to author the Notepad sample installation package.</span></span>

<span data-ttu-id="b5cb8-109">Use o editor de banco de dados para abrir MNP2000.msi e insira os dados a seguir na [tabela AdvtExecuteSequence](advtexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="b5cb8-109">Use your database editor to open MNP2000.msi and enter the following data into the [AdvtExecuteSequence table](advtexecutesequence-table.md).</span></span>

[<span data-ttu-id="b5cb8-110">Tabela AdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="b5cb8-110">AdvtExecuteSequence Table</span></span>](advtexecutesequence-table.md)



| <span data-ttu-id="b5cb8-111">Ação</span><span class="sxs-lookup"><span data-stu-id="b5cb8-111">Action</span></span>                | <span data-ttu-id="b5cb8-112">Condição</span><span class="sxs-lookup"><span data-stu-id="b5cb8-112">Condition</span></span> | <span data-ttu-id="b5cb8-113">Sequência</span><span class="sxs-lookup"><span data-stu-id="b5cb8-113">Sequence</span></span> |
|-----------------------|-----------|----------|
| <span data-ttu-id="b5cb8-114">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="b5cb8-114">CostFinalize</span></span>          |           | <span data-ttu-id="b5cb8-115">1000</span><span class="sxs-lookup"><span data-stu-id="b5cb8-115">1000</span></span>     |
| <span data-ttu-id="b5cb8-116">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="b5cb8-116">CostInitialize</span></span>        |           | <span data-ttu-id="b5cb8-117">800</span><span class="sxs-lookup"><span data-stu-id="b5cb8-117">800</span></span>      |
| <span data-ttu-id="b5cb8-118">Createatalhos</span><span class="sxs-lookup"><span data-stu-id="b5cb8-118">CreateShortcuts</span></span>       |           | <span data-ttu-id="b5cb8-119">4500</span><span class="sxs-lookup"><span data-stu-id="b5cb8-119">4500</span></span>     |
| <span data-ttu-id="b5cb8-120">InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="b5cb8-120">InstallFinalize</span></span>       |           | <span data-ttu-id="b5cb8-121">6600</span><span class="sxs-lookup"><span data-stu-id="b5cb8-121">6600</span></span>     |
| <span data-ttu-id="b5cb8-122">InstallInitialize</span><span class="sxs-lookup"><span data-stu-id="b5cb8-122">InstallInitialize</span></span>     |           | <span data-ttu-id="b5cb8-123">1500</span><span class="sxs-lookup"><span data-stu-id="b5cb8-123">1500</span></span>     |
| <span data-ttu-id="b5cb8-124">InstallValidate</span><span class="sxs-lookup"><span data-stu-id="b5cb8-124">InstallValidate</span></span>       |           | <span data-ttu-id="b5cb8-125">1.400</span><span class="sxs-lookup"><span data-stu-id="b5cb8-125">1400</span></span>     |
| <span data-ttu-id="b5cb8-126">PublishComponents</span><span class="sxs-lookup"><span data-stu-id="b5cb8-126">PublishComponents</span></span>     |           | <span data-ttu-id="b5cb8-127">6200</span><span class="sxs-lookup"><span data-stu-id="b5cb8-127">6200</span></span>     |
| <span data-ttu-id="b5cb8-128">PublishFeatures</span><span class="sxs-lookup"><span data-stu-id="b5cb8-128">PublishFeatures</span></span>       |           | <span data-ttu-id="b5cb8-129">6300</span><span class="sxs-lookup"><span data-stu-id="b5cb8-129">6300</span></span>     |
| <span data-ttu-id="b5cb8-130">PublishProduct</span><span class="sxs-lookup"><span data-stu-id="b5cb8-130">PublishProduct</span></span>        |           | <span data-ttu-id="b5cb8-131">6400</span><span class="sxs-lookup"><span data-stu-id="b5cb8-131">6400</span></span>     |
| <span data-ttu-id="b5cb8-132">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="b5cb8-132">RegisterClassInfo</span></span>     |           | <span data-ttu-id="b5cb8-133">4600</span><span class="sxs-lookup"><span data-stu-id="b5cb8-133">4600</span></span>     |
| <span data-ttu-id="b5cb8-134">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="b5cb8-134">RegisterExtensionInfo</span></span> |           | <span data-ttu-id="b5cb8-135">4700</span><span class="sxs-lookup"><span data-stu-id="b5cb8-135">4700</span></span>     |
| <span data-ttu-id="b5cb8-136">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="b5cb8-136">RegisterMIMEInfo</span></span>      |           | <span data-ttu-id="b5cb8-137">4900</span><span class="sxs-lookup"><span data-stu-id="b5cb8-137">4900</span></span>     |
| <span data-ttu-id="b5cb8-138">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="b5cb8-138">RegisterProgIdInfo</span></span>    |           | <span data-ttu-id="b5cb8-139">4800</span><span class="sxs-lookup"><span data-stu-id="b5cb8-139">4800</span></span>     |



 

<span data-ttu-id="b5cb8-140">A [tabela AdvtUISequence](advtuisequence-table.md) não é usada pelo instalador.</span><span class="sxs-lookup"><span data-stu-id="b5cb8-140">The [AdvtUISequence table](advtuisequence-table.md) is not used by the installer.</span></span> <span data-ttu-id="b5cb8-141">Essa tabela não deve existir ou deixada vazia no banco de dados de instalação.</span><span class="sxs-lookup"><span data-stu-id="b5cb8-141">This table should not exist or be left empty in the installation database.</span></span>

[<span data-ttu-id="b5cb8-142">Continuar</span><span class="sxs-lookup"><span data-stu-id="b5cb8-142">Continue</span></span>](adding-summary-information.md)

 

 



