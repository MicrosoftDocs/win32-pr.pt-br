---
description: A tabela AdminUISequence lista as ações que o instalador chama quando executa a ação de administrador de nível superior e o nível da interface do usuário interna é definido como interface de usuários completa ou interface reduzida.
ms.assetid: f23bd5c2-1d7f-485f-a22b-99436dfab6bf
title: Importando o AdminUISequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6f1b9d2a91a350097ac043c186478e4933f6e81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751441"
---
# <a name="importing-the-adminuisequence"></a><span data-ttu-id="b5057-103">Importando o AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="b5057-103">Importing the AdminUISequence</span></span>

<span data-ttu-id="b5057-104">A [tabela AdminUISequence](adminuisequence-table.md) lista as ações que o instalador chama quando executa a [ação de administrador](admin-action.md) de nível superior e o nível da interface do usuário interna é definido como interface de usuários completa ou interface reduzida.</span><span class="sxs-lookup"><span data-stu-id="b5057-104">The [AdminUISequence table](adminuisequence-table.md) lists actions that the installer calls when it executes the top-level [ADMIN action](admin-action.md) and the internal user interface level is set to full UI or reduced UI.</span></span> <span data-ttu-id="b5057-105">O instalador ignorará as ações nesta tabela se o nível da interface do usuário estiver definido como interface básica ou não.</span><span class="sxs-lookup"><span data-stu-id="b5057-105">The installer skips the actions in this table if the user interface level is set to basic UI or no UI.</span></span> <span data-ttu-id="b5057-106">Consulte [interface do usuário](user-interface.md) e [níveis de interface do usuário](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="b5057-106">See [User Interface](user-interface.md) and [User Interface Levels](user-interface-levels.md).</span></span> <span data-ttu-id="b5057-107">Confira o [grupo tabelas de procedimentos de instalação](installation-procedure-tables-group.md), [usando uma tabela de sequência](using-a-sequence-table.md)e o exemplo de tabela de [sequência detalhado](sequence-table-detailed-example.md).</span><span class="sxs-lookup"><span data-stu-id="b5057-107">See [Installation Procedure Tables Group](installation-procedure-tables-group.md), [Using a Sequence Table](using-a-sequence-table.md), and the [Sequence Table Detailed Example](sequence-table-detailed-example.md).</span></span>

<span data-ttu-id="b5057-108">Se na seção [importando um banco de dados em branco](importing-a-blank-database.md) usado uisample.msi do SDK do Windows Installer, as tabelas de sequência em sua cópia do MNP2000.msi já contêm as sequências de ações sugeridas descritas em [usando uma tabela de sequência](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="b5057-108">If in the section [Importing a Blank Database](importing-a-blank-database.md) you used uisample.msi from the Windows Installer SDK, the sequence tables in your copy of MNP2000.msi already contains the suggested action sequences described in [Using a Sequence Table](using-a-sequence-table.md).</span></span> <span data-ttu-id="b5057-109">Nenhuma alteração nessas sequências deve ser necessária para instalar o exemplo do bloco de notas.</span><span class="sxs-lookup"><span data-stu-id="b5057-109">No changes to these sequences should be necessary to install the Notepad sample.</span></span>

<span data-ttu-id="b5057-110">Use o editor de banco de dados para abrir MNP2000.msi e insira os dados a seguir na tabela AdminExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="b5057-110">Use your database editor to open MNP2000.msi and enter the following data into the AdminExecuteSequence table.</span></span>

[<span data-ttu-id="b5057-111">Tabela AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="b5057-111">AdminUISequence Table</span></span>](adminuisequence-table.md)



| <span data-ttu-id="b5057-112">Ação</span><span class="sxs-lookup"><span data-stu-id="b5057-112">Action</span></span>          | <span data-ttu-id="b5057-113">Condição</span><span class="sxs-lookup"><span data-stu-id="b5057-113">Condition</span></span> | <span data-ttu-id="b5057-114">Sequência</span><span class="sxs-lookup"><span data-stu-id="b5057-114">Sequence</span></span> |
|-----------------|-----------|----------|
| <span data-ttu-id="b5057-115">AdminWelcomeDlg</span><span class="sxs-lookup"><span data-stu-id="b5057-115">AdminWelcomeDlg</span></span> |           | <span data-ttu-id="b5057-116">1230</span><span class="sxs-lookup"><span data-stu-id="b5057-116">1230</span></span>     |
| <span data-ttu-id="b5057-117">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="b5057-117">CostFinalize</span></span>    |           | <span data-ttu-id="b5057-118">1000</span><span class="sxs-lookup"><span data-stu-id="b5057-118">1000</span></span>     |
| <span data-ttu-id="b5057-119">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="b5057-119">CostInitialize</span></span>  |           | <span data-ttu-id="b5057-120">800</span><span class="sxs-lookup"><span data-stu-id="b5057-120">800</span></span>      |
| <span data-ttu-id="b5057-121">ExecuteAction</span><span class="sxs-lookup"><span data-stu-id="b5057-121">ExecuteAction</span></span>   |           | <span data-ttu-id="b5057-122">1300</span><span class="sxs-lookup"><span data-stu-id="b5057-122">1300</span></span>     |
| <span data-ttu-id="b5057-123">ExitDlg</span><span class="sxs-lookup"><span data-stu-id="b5057-123">ExitDlg</span></span>         |           | <span data-ttu-id="b5057-124">-1</span><span class="sxs-lookup"><span data-stu-id="b5057-124">-1</span></span>       |
| <span data-ttu-id="b5057-125">FatalErrorDlg</span><span class="sxs-lookup"><span data-stu-id="b5057-125">FatalErrorDlg</span></span>   |           | <span data-ttu-id="b5057-126">-3</span><span class="sxs-lookup"><span data-stu-id="b5057-126">-3</span></span>       |
| <span data-ttu-id="b5057-127">Custo de</span><span class="sxs-lookup"><span data-stu-id="b5057-127">FileCost</span></span>        |           | <span data-ttu-id="b5057-128">900</span><span class="sxs-lookup"><span data-stu-id="b5057-128">900</span></span>      |
| <span data-ttu-id="b5057-129">PrepareDlg</span><span class="sxs-lookup"><span data-stu-id="b5057-129">PrepareDlg</span></span>      |           | <span data-ttu-id="b5057-130">140</span><span class="sxs-lookup"><span data-stu-id="b5057-130">140</span></span>      |
| <span data-ttu-id="b5057-131">ProgressDlg</span><span class="sxs-lookup"><span data-stu-id="b5057-131">ProgressDlg</span></span>     |           | <span data-ttu-id="b5057-132">1280</span><span class="sxs-lookup"><span data-stu-id="b5057-132">1280</span></span>     |
| <span data-ttu-id="b5057-133">UserExitDlg</span><span class="sxs-lookup"><span data-stu-id="b5057-133">UserExitDlg</span></span>     |           | <span data-ttu-id="b5057-134">-2</span><span class="sxs-lookup"><span data-stu-id="b5057-134">-2</span></span>       |



 

[<span data-ttu-id="b5057-135">Continuar</span><span class="sxs-lookup"><span data-stu-id="b5057-135">Continue</span></span>](importing-the-advtexecutesequence.md)

 

 



