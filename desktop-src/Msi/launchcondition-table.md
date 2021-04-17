---
description: A tabela LaunchCondition é usada pela ação LaunchConditions. Ele contém uma lista de condições que devem ser satisfeitas para que a instalação seja iniciada.
ms.assetid: 6e550cc7-c479-417e-ab89-882d8fece4e1
title: Tabela LaunchCondition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d67834f058575dde297454480040028ef9c5732
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782788"
---
# <a name="launchcondition-table"></a><span data-ttu-id="ea240-104">Tabela LaunchCondition</span><span class="sxs-lookup"><span data-stu-id="ea240-104">LaunchCondition Table</span></span>

<span data-ttu-id="ea240-105">A tabela LaunchCondition é usada pela [ação LaunchConditions](launchconditions-action.md).</span><span class="sxs-lookup"><span data-stu-id="ea240-105">The LaunchCondition table is used by the [LaunchConditions action](launchconditions-action.md).</span></span> <span data-ttu-id="ea240-106">Ele contém uma lista de condições que devem ser satisfeitas para que a instalação seja iniciada.</span><span class="sxs-lookup"><span data-stu-id="ea240-106">It contains a list of conditions that all must be satisfied for the installation to begin.</span></span>

<span data-ttu-id="ea240-107">A tabela LaunchCondition tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="ea240-107">The LaunchCondition table has the following columns.</span></span>



| <span data-ttu-id="ea240-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="ea240-108">Column</span></span>      | <span data-ttu-id="ea240-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="ea240-109">Type</span></span>                       | <span data-ttu-id="ea240-110">Chave</span><span class="sxs-lookup"><span data-stu-id="ea240-110">Key</span></span> | <span data-ttu-id="ea240-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="ea240-111">Nullable</span></span> |
|-------------|----------------------------|-----|----------|
| <span data-ttu-id="ea240-112">Condição</span><span class="sxs-lookup"><span data-stu-id="ea240-112">Condition</span></span>   | [<span data-ttu-id="ea240-113">Condição</span><span class="sxs-lookup"><span data-stu-id="ea240-113">Condition</span></span>](condition.md) | <span data-ttu-id="ea240-114">S</span><span class="sxs-lookup"><span data-stu-id="ea240-114">Y</span></span>   | <span data-ttu-id="ea240-115">N</span><span class="sxs-lookup"><span data-stu-id="ea240-115">N</span></span>        |
| <span data-ttu-id="ea240-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="ea240-116">Description</span></span> | [<span data-ttu-id="ea240-117">Binário</span><span class="sxs-lookup"><span data-stu-id="ea240-117">Formatted</span></span>](formatted.md) | <span data-ttu-id="ea240-118">N</span><span class="sxs-lookup"><span data-stu-id="ea240-118">N</span></span>   | <span data-ttu-id="ea240-119">N</span><span class="sxs-lookup"><span data-stu-id="ea240-119">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="ea240-120">Colunas</span><span class="sxs-lookup"><span data-stu-id="ea240-120">Columns</span></span>

<dl> <dt>

<span data-ttu-id="ea240-121"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Problema</span><span class="sxs-lookup"><span data-stu-id="ea240-121"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="ea240-122">Expressão que deve ser avaliada como true para que a instalação seja iniciada.</span><span class="sxs-lookup"><span data-stu-id="ea240-122">Expression that must evaluate to True for installation to begin.</span></span>

</dd> <dt>

<span data-ttu-id="ea240-123"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Ndescrição</span><span class="sxs-lookup"><span data-stu-id="ea240-123"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="ea240-124">Texto localizável para exibir quando a condição falha e a instalação deve ser encerrada.</span><span class="sxs-lookup"><span data-stu-id="ea240-124">Localizable text to display when the condition fails and the installation must be terminated.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ea240-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="ea240-125">Remarks</span></span>

<span data-ttu-id="ea240-126">Você não pode garantir a ordem na qual as condições de inicialização são avaliadas por meio da criação desta tabela.</span><span class="sxs-lookup"><span data-stu-id="ea240-126">You cannot guarantee the order in which the launch conditions are evaluated by authoring this table.</span></span> <span data-ttu-id="ea240-127">Se for necessário controlar a ordem em que as condições são avaliadas, você deve fazer isso usando ações personalizadas do tipo de ação personalizada 19 em sua instalação.</span><span class="sxs-lookup"><span data-stu-id="ea240-127">If it is necessary to control the order in which conditions are evaluated, you should do this by using Custom Action Type 19 custom actions in your installation.</span></span>

## <a name="validation"></a><span data-ttu-id="ea240-128">Validação</span><span class="sxs-lookup"><span data-stu-id="ea240-128">Validation</span></span>

<dl>

[<span data-ttu-id="ea240-129">ICE03</span><span class="sxs-lookup"><span data-stu-id="ea240-129">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="ea240-130">ICE06</span><span class="sxs-lookup"><span data-stu-id="ea240-130">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="ea240-131">ICE46</span><span class="sxs-lookup"><span data-stu-id="ea240-131">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="ea240-132">ICE79</span><span class="sxs-lookup"><span data-stu-id="ea240-132">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="ea240-133">ICE86</span><span class="sxs-lookup"><span data-stu-id="ea240-133">ICE86</span></span>](ice86.md)  
</dl>

 

 



