---
description: A sequência da interface do usuário é importada para o banco de dados de exemplo.
ms.assetid: 750e4dc6-91ff-4d9a-a968-abc2515e3b7c
title: Importando o InstallUISequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f20de59a752da6d24a5f3e7fed94e00aa4f0048
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170425"
---
# <a name="importing-the-installuisequence"></a><span data-ttu-id="789c5-103">Importando o InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="789c5-103">Importing the InstallUISequence</span></span>

<span data-ttu-id="789c5-104">A [tabela InstallUISequence](installuisequence-table.md) lista as ações que são executadas quando a ação de [instalação](install-action.md) de nível superior é executada e o nível de interface do usuário interno é definido como interface de usuários completa ou interface reduzida.</span><span class="sxs-lookup"><span data-stu-id="789c5-104">The [InstallUISequence table](installuisequence-table.md) lists actions that are executed when the top-level [INSTALL action](install-action.md) is executed and the internal user interface level is set to full UI or reduced UI.</span></span> <span data-ttu-id="789c5-105">O instalador ignorará as ações nesta tabela se o nível da interface do usuário estiver definido como interface básica ou como sem interface.</span><span class="sxs-lookup"><span data-stu-id="789c5-105">The installer skips the actions in this table if the user interface level is set to basic UI or to no UI.</span></span> <span data-ttu-id="789c5-106">Consulte [interface do usuário](user-interface.md) e [níveis de interface do usuário](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="789c5-106">See [User Interface](user-interface.md) and [User Interface Levels](user-interface-levels.md).</span></span> <span data-ttu-id="789c5-107">Confira o [grupo tabelas de procedimentos de instalação](installation-procedure-tables-group.md), [usando uma tabela de sequência](using-a-sequence-table.md)e o exemplo de tabela de [sequência detalhado](sequence-table-detailed-example.md).</span><span class="sxs-lookup"><span data-stu-id="789c5-107">See [Installation Procedure Tables Group](installation-procedure-tables-group.md), [Using a Sequence Table](using-a-sequence-table.md), and the [Sequence Table Detailed Example](sequence-table-detailed-example.md).</span></span>

<span data-ttu-id="789c5-108">Se na seção [importando um banco de dados em branco](importing-a-blank-database.md) usado uisample.msi do SDK do Windows Installer, as tabelas de sequência em sua cópia do MNP2000.msi já contêm as sequências de ações sugeridas descritas em [usando uma tabela de sequência](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="789c5-108">If in the section [Importing a Blank Database](importing-a-blank-database.md) you used uisample.msi from the Windows Installer SDK, the sequence tables in your copy of MNP2000.msi already contains the suggested action sequences described in [Using a Sequence Table](using-a-sequence-table.md).</span></span> <span data-ttu-id="789c5-109">Nenhuma alteração nessas sequências deve ser necessária para criar o pacote de instalação do bloco de notas.</span><span class="sxs-lookup"><span data-stu-id="789c5-109">No changes to these sequences should be necessary to author the Notepad installation package.</span></span>

<span data-ttu-id="789c5-110">Use o editor de banco de dados para abrir MNP2000.msi e insira os dados a seguir na tabela InstallUISequence.</span><span class="sxs-lookup"><span data-stu-id="789c5-110">Use your database editor to open MNP2000.msi and enter the following data into the InstallUISequence table.</span></span>

[<span data-ttu-id="789c5-111">Tabela InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="789c5-111">InstallUISequence Table</span></span>](installuisequence-table.md)



| <span data-ttu-id="789c5-112">Ação</span><span class="sxs-lookup"><span data-stu-id="789c5-112">Action</span></span>                | <span data-ttu-id="789c5-113">Condição</span><span class="sxs-lookup"><span data-stu-id="789c5-113">Condition</span></span>                                    | <span data-ttu-id="789c5-114">Sequência</span><span class="sxs-lookup"><span data-stu-id="789c5-114">Sequence</span></span> |
|-----------------------|----------------------------------------------|----------|
| <span data-ttu-id="789c5-115">AppSearch</span><span class="sxs-lookup"><span data-stu-id="789c5-115">AppSearch</span></span>             |                                              | <span data-ttu-id="789c5-116">400</span><span class="sxs-lookup"><span data-stu-id="789c5-116">400</span></span>      |
| <span data-ttu-id="789c5-117">CCPSearch</span><span class="sxs-lookup"><span data-stu-id="789c5-117">CCPSearch</span></span>             | <span data-ttu-id="789c5-118">NÃO instalado</span><span class="sxs-lookup"><span data-stu-id="789c5-118">NOT Installed</span></span>                                | <span data-ttu-id="789c5-119">500</span><span class="sxs-lookup"><span data-stu-id="789c5-119">500</span></span>      |
| <span data-ttu-id="789c5-120">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="789c5-120">CostFinalize</span></span>          |                                              | <span data-ttu-id="789c5-121">1000</span><span class="sxs-lookup"><span data-stu-id="789c5-121">1000</span></span>     |
| <span data-ttu-id="789c5-122">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="789c5-122">CostInitialize</span></span>        |                                              | <span data-ttu-id="789c5-123">800</span><span class="sxs-lookup"><span data-stu-id="789c5-123">800</span></span>      |
| <span data-ttu-id="789c5-124">ExecuteAction</span><span class="sxs-lookup"><span data-stu-id="789c5-124">ExecuteAction</span></span>         |                                              | <span data-ttu-id="789c5-125">1300</span><span class="sxs-lookup"><span data-stu-id="789c5-125">1300</span></span>     |
| <span data-ttu-id="789c5-126">ExitDlg</span><span class="sxs-lookup"><span data-stu-id="789c5-126">ExitDlg</span></span>               |                                              | <span data-ttu-id="789c5-127">-1</span><span class="sxs-lookup"><span data-stu-id="789c5-127">-1</span></span>       |
| <span data-ttu-id="789c5-128">FatalErrorDlg</span><span class="sxs-lookup"><span data-stu-id="789c5-128">FatalErrorDlg</span></span>         |                                              | <span data-ttu-id="789c5-129">-3</span><span class="sxs-lookup"><span data-stu-id="789c5-129">-3</span></span>       |
| <span data-ttu-id="789c5-130">Custo de</span><span class="sxs-lookup"><span data-stu-id="789c5-130">FileCost</span></span>              |                                              | <span data-ttu-id="789c5-131">900</span><span class="sxs-lookup"><span data-stu-id="789c5-131">900</span></span>      |
| <span data-ttu-id="789c5-132">LaunchConditions</span><span class="sxs-lookup"><span data-stu-id="789c5-132">LaunchConditions</span></span>      |                                              | <span data-ttu-id="789c5-133">100</span><span class="sxs-lookup"><span data-stu-id="789c5-133">100</span></span>      |
| <span data-ttu-id="789c5-134">MaintenanceWelcomeDlg</span><span class="sxs-lookup"><span data-stu-id="789c5-134">MaintenanceWelcomeDlg</span></span> | <span data-ttu-id="789c5-135">Instalado e não retomado e não selecionado</span><span class="sxs-lookup"><span data-stu-id="789c5-135">Installed AND NOT RESUME AND NOT Preselected</span></span> | <span data-ttu-id="789c5-136">1250</span><span class="sxs-lookup"><span data-stu-id="789c5-136">1250</span></span>     |
| <span data-ttu-id="789c5-137">PrepareDlg</span><span class="sxs-lookup"><span data-stu-id="789c5-137">PrepareDlg</span></span>            |                                              | <span data-ttu-id="789c5-138">140</span><span class="sxs-lookup"><span data-stu-id="789c5-138">140</span></span>      |
| <span data-ttu-id="789c5-139">ProgressDlg</span><span class="sxs-lookup"><span data-stu-id="789c5-139">ProgressDlg</span></span>           |                                              | <span data-ttu-id="789c5-140">1280</span><span class="sxs-lookup"><span data-stu-id="789c5-140">1280</span></span>     |
| <span data-ttu-id="789c5-141">ResumeDlg</span><span class="sxs-lookup"><span data-stu-id="789c5-141">ResumeDlg</span></span>             | <span data-ttu-id="789c5-142">Instalado e (retomado ou preselecionado)</span><span class="sxs-lookup"><span data-stu-id="789c5-142">Installed AND (RESUME OR Preselected)</span></span>        | <span data-ttu-id="789c5-143">1240</span><span class="sxs-lookup"><span data-stu-id="789c5-143">1240</span></span>     |
| <span data-ttu-id="789c5-144">RMCCPSearch</span><span class="sxs-lookup"><span data-stu-id="789c5-144">RMCCPSearch</span></span>           | <span data-ttu-id="789c5-145">NÃO instalado</span><span class="sxs-lookup"><span data-stu-id="789c5-145">NOT Installed</span></span>                                | <span data-ttu-id="789c5-146">600</span><span class="sxs-lookup"><span data-stu-id="789c5-146">600</span></span>      |
| <span data-ttu-id="789c5-147">UserExitDlg</span><span class="sxs-lookup"><span data-stu-id="789c5-147">UserExitDlg</span></span>           |                                              | <span data-ttu-id="789c5-148">-2</span><span class="sxs-lookup"><span data-stu-id="789c5-148">-2</span></span>       |
| <span data-ttu-id="789c5-149">WelcomeDlg</span><span class="sxs-lookup"><span data-stu-id="789c5-149">WelcomeDlg</span></span>            | <span data-ttu-id="789c5-150">NÃO instalado</span><span class="sxs-lookup"><span data-stu-id="789c5-150">NOT Installed</span></span>                                | <span data-ttu-id="789c5-151">1230</span><span class="sxs-lookup"><span data-stu-id="789c5-151">1230</span></span>     |
| <span data-ttu-id="789c5-152">MigrateFeatureStates</span><span class="sxs-lookup"><span data-stu-id="789c5-152">MigrateFeatureStates</span></span>  |                                              | <span data-ttu-id="789c5-153">1200</span><span class="sxs-lookup"><span data-stu-id="789c5-153">1200</span></span>     |
| <span data-ttu-id="789c5-154">FindRelatedProducts</span><span class="sxs-lookup"><span data-stu-id="789c5-154">FindRelatedProducts</span></span>   |                                              | <span data-ttu-id="789c5-155">200</span><span class="sxs-lookup"><span data-stu-id="789c5-155">200</span></span>      |



 

[<span data-ttu-id="789c5-156">Continuar</span><span class="sxs-lookup"><span data-stu-id="789c5-156">Continue</span></span>](importing-the-adminexecutesequence.md)

 

 



