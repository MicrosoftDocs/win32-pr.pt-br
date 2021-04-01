---
description: ICE63 verifica o sequenciamento adequado da ação RemoveExistingProducts.
ms.assetid: 4dd67bb0-c08a-4a44-b687-0394a3afc2c4
title: ICE63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5faa6f2ddbcb95cdf12966c2887fe9438a5d610
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829189"
---
# <a name="ice63"></a><span data-ttu-id="e5659-103">ICE63</span><span class="sxs-lookup"><span data-stu-id="e5659-103">ICE63</span></span>

<span data-ttu-id="e5659-104">ICE63 verifica o sequenciamento adequado da [ação RemoveExistingProducts](removeexistingproducts-action.md).</span><span class="sxs-lookup"><span data-stu-id="e5659-104">ICE63 checks for proper sequencing of the [RemoveExistingProducts action](removeexistingproducts-action.md).</span></span> <span data-ttu-id="e5659-105">A ação RemoveExistingProducts pode ser colocada:</span><span class="sxs-lookup"><span data-stu-id="e5659-105">The RemoveExistingProducts action may be placed:</span></span>

1.  <span data-ttu-id="e5659-106">Entre InstallValidate e InstallInitialize</span><span class="sxs-lookup"><span data-stu-id="e5659-106">Between InstallValidate and InstallInitialize</span></span>
2.  <span data-ttu-id="e5659-107">Imediatamente após InstallInitialize ou depois de InstallInitialize se as ações entre InstallInitialize e RemoveExistingProducts não gerarem nenhuma ação de script.</span><span class="sxs-lookup"><span data-stu-id="e5659-107">Immediately after InstallInitialize, or after InstallInitialize if the actions between InstallInitialize and RemoveExistingProducts do not generate any script actions.</span></span>
3.  <span data-ttu-id="e5659-108">Imediatamente após InstallExecute ou InstallExecuteAgain e antes de InstallFinalize (a mesma restrição que acima se aplica).</span><span class="sxs-lookup"><span data-stu-id="e5659-108">Immediately after InstallExecute or InstallExecuteAgain and before InstallFinalize (the same restriction as above applies).</span></span>
4.  <span data-ttu-id="e5659-109">Após InstallFinalize.</span><span class="sxs-lookup"><span data-stu-id="e5659-109">After InstallFinalize.</span></span>

<span data-ttu-id="e5659-110">Falha ao corrigir um aviso ou erro relatado por ICE63 leva a uma falha da atualização.</span><span class="sxs-lookup"><span data-stu-id="e5659-110">Failure to fix a warning or error reported by ICE63 leads to failure of the upgrade.</span></span>

## <a name="result"></a><span data-ttu-id="e5659-111">Resultado</span><span class="sxs-lookup"><span data-stu-id="e5659-111">Result</span></span>

<span data-ttu-id="e5659-112">ICE63 posta um aviso ou erro se o sequenciamento da ação RemoveExistingProducts não estiver correto.</span><span class="sxs-lookup"><span data-stu-id="e5659-112">ICE63 posts a warning or error if the sequencing of the RemoveExistingProducts action is not correct.</span></span>

## <a name="example"></a><span data-ttu-id="e5659-113">Exemplo</span><span class="sxs-lookup"><span data-stu-id="e5659-113">Example</span></span>

<span data-ttu-id="e5659-114">ICE63 relata o seguinte erro para o exemplo mostrado.</span><span class="sxs-lookup"><span data-stu-id="e5659-114">ICE63 reports the following error for the example shown.</span></span>

``` syntax
WARNING: Some action falls between InstallInitialize and RemoveExistingProducts.
```

<span data-ttu-id="e5659-115">A ação ' mycustomizable ' ocorre entre InstallInitialize e RemoveExistingProducts.</span><span class="sxs-lookup"><span data-stu-id="e5659-115">The action 'MyCustomAction' occurs between InstallInitialize and RemoveExistingProducts.</span></span> <span data-ttu-id="e5659-116">Se mycustomizable gerar qualquer ação no script, isso causará problemas na instalação.</span><span class="sxs-lookup"><span data-stu-id="e5659-116">If MyCustomAction generates any actions in the script, this causes problems in the installation.</span></span>

<span data-ttu-id="e5659-117">Para corrigir esse erro, verifique se mycustomizable não gera nenhuma ação de script ou resequenciar as ações.</span><span class="sxs-lookup"><span data-stu-id="e5659-117">To fix this error, verify that MyCustomAction does not generate any script actions or resequence the actions.</span></span>

[<span data-ttu-id="e5659-118">Tabela InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="e5659-118">InstallExecuteSequence Table</span></span>](installexecutesequence-table.md)



| <span data-ttu-id="e5659-119">Ação</span><span class="sxs-lookup"><span data-stu-id="e5659-119">Action</span></span>                 | <span data-ttu-id="e5659-120">Condição</span><span class="sxs-lookup"><span data-stu-id="e5659-120">Condition</span></span> | <span data-ttu-id="e5659-121">Sequência</span><span class="sxs-lookup"><span data-stu-id="e5659-121">Sequence</span></span> |
|------------------------|-----------|----------|
| <span data-ttu-id="e5659-122">InstallInitialize</span><span class="sxs-lookup"><span data-stu-id="e5659-122">InstallInitialize</span></span>      |           | <span data-ttu-id="e5659-123">1000</span><span class="sxs-lookup"><span data-stu-id="e5659-123">1000</span></span>     |
| <span data-ttu-id="e5659-124">Mycustomizable</span><span class="sxs-lookup"><span data-stu-id="e5659-124">MyCustomAction</span></span>         |           | <span data-ttu-id="e5659-125">1010</span><span class="sxs-lookup"><span data-stu-id="e5659-125">1010</span></span>     |
| <span data-ttu-id="e5659-126">RemoveExistingProducts</span><span class="sxs-lookup"><span data-stu-id="e5659-126">RemoveExistingProducts</span></span> |           | <span data-ttu-id="e5659-127">1020</span><span class="sxs-lookup"><span data-stu-id="e5659-127">1020</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="e5659-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e5659-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5659-129">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="e5659-129">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



