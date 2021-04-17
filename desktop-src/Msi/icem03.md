---
description: O ICEM03 verifica se todas as ações no módulo são ações básicas ou derivam de uma ação base válida.
ms.assetid: 8e2b5921-32cf-45e8-9906-30002574a712
title: ICEM03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f368fa50a71153c41eebaa9ee5084449cf824993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748592"
---
# <a name="icem03"></a><span data-ttu-id="a35ab-103">ICEM03</span><span class="sxs-lookup"><span data-stu-id="a35ab-103">ICEM03</span></span>

<span data-ttu-id="a35ab-104">O ICEM03 verifica se todas as ações no módulo são ações básicas ou derivam de uma ação base válida.</span><span class="sxs-lookup"><span data-stu-id="a35ab-104">ICEM03 verifies that all actions in the module are either base actions or derive from a valid base action.</span></span>

<span data-ttu-id="a35ab-105">O módulo de mesclagem ICEs é armazenado em um arquivo. Cub do módulo de mesclagem chamado Mergemod. Cub e não no arquivo. Cub que contém a ICEs usada para a validação do pacote.</span><span class="sxs-lookup"><span data-stu-id="a35ab-105">Merge module ICEs are stored in a merge module .cub file called Mergemod.cub and not in the .cub file containing the ICEs used for package validation.</span></span>

## <a name="result"></a><span data-ttu-id="a35ab-106">Resultado</span><span class="sxs-lookup"><span data-stu-id="a35ab-106">Result</span></span>

<span data-ttu-id="a35ab-107">ICEM03 posta as mensagens de erro para um módulo que contém ações em uma tabela de sequência que não é uma ação base ou derivada de uma ação base válida.</span><span class="sxs-lookup"><span data-stu-id="a35ab-107">ICEM03 posts the error messages for a module containing actions in a sequence table that is not a base action or derived from a valid base action.</span></span>

## <a name="example"></a><span data-ttu-id="a35ab-108">Exemplo</span><span class="sxs-lookup"><span data-stu-id="a35ab-108">Example</span></span>

<span data-ttu-id="a35ab-109">ICEM03 posta as seguintes mensagens de erro para um módulo que contém as entradas de banco de dados mostradas abaixo.</span><span class="sxs-lookup"><span data-stu-id="a35ab-109">ICEM03 posts the following error messages for a module containing the database entries shown below.</span></span>

``` syntax
The action 'Action1' in the 'ModuleInstallExecuteSequence' table is 
orphaned. It is not a valid base action and does not derive from a 
valid base action.
The action 'Action2' in the 'ModuleInstallExecuteSequence' table is 
orphaned. It is not a valid base action and does not derive from a 
valid base action.
```

[<span data-ttu-id="a35ab-110">Tabela ModuleInstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="a35ab-110">ModuleInstallExecuteSequence Table</span></span>](moduleinstallexecutesequence-table.md)



| <span data-ttu-id="a35ab-111">Ação</span><span class="sxs-lookup"><span data-stu-id="a35ab-111">Action</span></span>  | <span data-ttu-id="a35ab-112">Sequência</span><span class="sxs-lookup"><span data-stu-id="a35ab-112">Sequence</span></span> | <span data-ttu-id="a35ab-113">Baseaction</span><span class="sxs-lookup"><span data-stu-id="a35ab-113">BaseAction</span></span> | <span data-ttu-id="a35ab-114">After (após)</span><span class="sxs-lookup"><span data-stu-id="a35ab-114">After</span></span> | <span data-ttu-id="a35ab-115">Condição</span><span class="sxs-lookup"><span data-stu-id="a35ab-115">Condition</span></span> |
|---------|----------|------------|-------|-----------|
| <span data-ttu-id="a35ab-116">Action1</span><span class="sxs-lookup"><span data-stu-id="a35ab-116">Action1</span></span> |          | <span data-ttu-id="a35ab-117">Action2</span><span class="sxs-lookup"><span data-stu-id="a35ab-117">Action2</span></span>    | <span data-ttu-id="a35ab-118">0</span><span class="sxs-lookup"><span data-stu-id="a35ab-118">0</span></span>     |           |
| <span data-ttu-id="a35ab-119">Action2</span><span class="sxs-lookup"><span data-stu-id="a35ab-119">Action2</span></span> |          | <span data-ttu-id="a35ab-120">Action1</span><span class="sxs-lookup"><span data-stu-id="a35ab-120">Action1</span></span>    | <span data-ttu-id="a35ab-121">0</span><span class="sxs-lookup"><span data-stu-id="a35ab-121">0</span></span>     |           |



 

<span data-ttu-id="a35ab-122">ICEM03 posta erros para essas duas ações porque elas se referem umas às outras como ações básicas na tabela ModuleInstallExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="a35ab-122">ICEM03 posts errors for these two actions because they refer to each other as base actions in the ModuleInstallExecuteSequence table.</span></span> <span data-ttu-id="a35ab-123">Todas as ações nas tabelas [ModuleAdminUISequence](moduleadminuisequence-table.md), [ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md), [ModuleAdvtUISequence](moduleadvtuisequence-table.md), [ModuleAdvtExecuteSequence](moduleadvtexecutesequence-table.md), [ModuleInstallUISequence](moduleinstalluisequence-table.md)e [ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md) devem ser ações base ou derivar sua posição da combinação de outra ação e um sinalizador de antes e depois.</span><span class="sxs-lookup"><span data-stu-id="a35ab-123">All actions in the [ModuleAdminUISequence](moduleadminuisequence-table.md), [ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md), [ModuleAdvtUISequence](moduleadvtuisequence-table.md), [ModuleAdvtExecuteSequence](moduleadvtexecutesequence-table.md), [ModuleInstallUISequence](moduleinstalluisequence-table.md), and [ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md) tables must either be base actions or derive their position from the combination of another action and a before and after flag.</span></span>

<span data-ttu-id="a35ab-124">Para corrigir esse erro, determine as ações básicas para as duas ações.</span><span class="sxs-lookup"><span data-stu-id="a35ab-124">To fix this error, determine the base actions for the two actions.</span></span> <span data-ttu-id="a35ab-125">Adicione um registro para as ações de base com um número de sequência padrão.</span><span class="sxs-lookup"><span data-stu-id="a35ab-125">Add a record for the base actions with a default sequence number.</span></span> <span data-ttu-id="a35ab-126">Para Action1 e Action2, insira os nomes de ação base na coluna Baseaction e 0 ou 1 na coluna After.</span><span class="sxs-lookup"><span data-stu-id="a35ab-126">For Action1 and Action2 enter the base action names in the BaseAction column and 0 or 1 in the After column.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a35ab-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a35ab-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a35ab-128">Referência de ICE do módulo de mesclagem</span><span class="sxs-lookup"><span data-stu-id="a35ab-128">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



