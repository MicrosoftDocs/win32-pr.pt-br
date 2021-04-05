---
description: ICE13 valida que as caixas de diálogo em tabelas de sequência aparecem nas tabelas AdminUISequence ou InstallUISequence. As caixas de diálogo não devem ser listadas nas tabelas InstallExecuteSequence, AdminExecuteSequence ou AdvtExecuteSequence.
ms.assetid: 51542a8f-2fb6-4021-b52d-6f7a2b0294d6
title: ICE13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fff440217ccffe41d5e4036f4ea0d03d1eabb0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922021"
---
# <a name="ice13"></a><span data-ttu-id="29265-104">ICE13</span><span class="sxs-lookup"><span data-stu-id="29265-104">ICE13</span></span>

<span data-ttu-id="29265-105">ICE13 valida que as caixas de diálogo em tabelas de sequência aparecem nas tabelas [AdminUISequence](adminuisequence-table.md)ou [InstallUISequence](installuisequence-table.md) .</span><span class="sxs-lookup"><span data-stu-id="29265-105">ICE13 validates that dialogs in sequence tables appear in the [AdminUISequence](adminuisequence-table.md), or [InstallUISequence](installuisequence-table.md) tables.</span></span> <span data-ttu-id="29265-106">As caixas de diálogo não devem ser listadas nas tabelas [InstallExecuteSequence](installexecutesequence-table.md), [AdminExecuteSequence](adminexecutesequence-table.md)ou [AdvtExecuteSequence](advtexecutesequence-table.md) .</span><span class="sxs-lookup"><span data-stu-id="29265-106">Dialogs must not be listed in the [InstallExecuteSequence](installexecutesequence-table.md), [AdminExecuteSequence](adminexecutesequence-table.md), or [AdvtExecuteSequence](advtexecutesequence-table.md) tables.</span></span>

## <a name="result"></a><span data-ttu-id="29265-107">Resultado</span><span class="sxs-lookup"><span data-stu-id="29265-107">Result</span></span>

<span data-ttu-id="29265-108">ICE13 posta uma mensagem de erro se uma caixa de diálogo aparecer em uma tabela de sequência de execução.</span><span class="sxs-lookup"><span data-stu-id="29265-108">ICE13 posts an error message if a dialog appears in an execute sequence table.</span></span>

## <a name="example"></a><span data-ttu-id="29265-109">Exemplo</span><span class="sxs-lookup"><span data-stu-id="29265-109">Example</span></span>

<span data-ttu-id="29265-110">Para o exemplo a seguir, ICE13 posta uma mensagem de erro informando que o ' WelcomeDialog ' não pode ser listado na tabela ' InstallExecuteSequence '.</span><span class="sxs-lookup"><span data-stu-id="29265-110">For the following example, ICE13 posts an error message stating that the 'WelcomeDialog' cannot be listed in the 'InstallExecuteSequence' table.</span></span>

<span data-ttu-id="29265-111">[Tabela InstallExecuteSequence](installexecutesequence-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="29265-111">[InstallExecuteSequence Table](installexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="29265-112">Ação</span><span class="sxs-lookup"><span data-stu-id="29265-112">Action</span></span>          |
|-----------------|
| <span data-ttu-id="29265-113">InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="29265-113">InstallFinalize</span></span> |
| <span data-ttu-id="29265-114">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="29265-114">CostFinalize</span></span>    |
| <span data-ttu-id="29265-115">WelcomeDialog</span><span class="sxs-lookup"><span data-stu-id="29265-115">WelcomeDialog</span></span>   |



 

<span data-ttu-id="29265-116">[Tabela InstallUISequence](installuisequence-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="29265-116">[InstallUISequence Table](installuisequence-table.md) (partial)</span></span>



| <span data-ttu-id="29265-117">Ação</span><span class="sxs-lookup"><span data-stu-id="29265-117">Action</span></span>         |
|----------------|
| <span data-ttu-id="29265-118">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="29265-118">CostFinalize</span></span>   |
| <span data-ttu-id="29265-119">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="29265-119">CostInitialize</span></span> |
| <span data-ttu-id="29265-120">BrowseDialog</span><span class="sxs-lookup"><span data-stu-id="29265-120">BrowseDialog</span></span>   |



 

<span data-ttu-id="29265-121">[Tabela de diálogo](dialog-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="29265-121">[Dialog Table](dialog-table.md) (partial)</span></span>



| <span data-ttu-id="29265-122">caixa de diálogo</span><span class="sxs-lookup"><span data-stu-id="29265-122">Dialog</span></span>        |
|---------------|
| <span data-ttu-id="29265-123">BrowseDialog</span><span class="sxs-lookup"><span data-stu-id="29265-123">BrowseDialog</span></span>  |
| <span data-ttu-id="29265-124">WelcomeDialog</span><span class="sxs-lookup"><span data-stu-id="29265-124">WelcomeDialog</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="29265-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="29265-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29265-126">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="29265-126">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



