---
description: ICE78 verifica se a tabela AdvtUISequence não existe ou está vazia. Isso é necessário porque nenhuma interface do usuário é permitida durante o anúncio.
ms.assetid: 8ed1c68f-331d-42f9-80df-bdcb42962482
title: ICE78
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8993a0a03b0f70bf2d99511782bc9b7d259d4c9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090780"
---
# <a name="ice78"></a><span data-ttu-id="697bd-104">ICE78</span><span class="sxs-lookup"><span data-stu-id="697bd-104">ICE78</span></span>

<span data-ttu-id="697bd-105">ICE78 verifica se a [tabela AdvtUISequence](advtuisequence-table.md) não existe ou está vazia.</span><span class="sxs-lookup"><span data-stu-id="697bd-105">ICE78 verifies that the [AdvtUISequence table](advtuisequence-table.md) either does not exist or is empty.</span></span> <span data-ttu-id="697bd-106">Isso é necessário porque nenhuma interface do usuário é permitida durante o anúncio.</span><span class="sxs-lookup"><span data-stu-id="697bd-106">This is required because no user interface is allowed during advertising.</span></span>

## <a name="result"></a><span data-ttu-id="697bd-107">Resultado</span><span class="sxs-lookup"><span data-stu-id="697bd-107">Result</span></span>

<span data-ttu-id="697bd-108">ICE78 lançará um erro se a tabela AdvtUISequence existir e não estiver vazia.</span><span class="sxs-lookup"><span data-stu-id="697bd-108">ICE78 posts an error if the AdvtUISequence table exists and is not empty.</span></span>

## <a name="example"></a><span data-ttu-id="697bd-109">Exemplo</span><span class="sxs-lookup"><span data-stu-id="697bd-109">Example</span></span>

<span data-ttu-id="697bd-110">ICE78 relata o seguinte erro para o exemplo:</span><span class="sxs-lookup"><span data-stu-id="697bd-110">ICE78 reports the following error for the example:</span></span>

<span data-ttu-id="697bd-111">Ação ' Action1 ' encontrada na tabela AdvtUISequence.</span><span class="sxs-lookup"><span data-stu-id="697bd-111">Action 'Action1' found in AdvtUISequence table.</span></span> <span data-ttu-id="697bd-112">Nenhuma interface do usuário é permitida durante o anúncio.</span><span class="sxs-lookup"><span data-stu-id="697bd-112">No UI is allowed during advertising.</span></span> <span data-ttu-id="697bd-113">Portanto, a tabela AdvtUISequence deve estar vazia ou não estar presente.</span><span class="sxs-lookup"><span data-stu-id="697bd-113">Therefore AdvtUISequence table must be empty or not present.</span></span>

<span data-ttu-id="697bd-114">[Tabela AdvtUISequence](advtuisequence-table.md)(parcial)</span><span class="sxs-lookup"><span data-stu-id="697bd-114">[AdvtUISequence table](advtuisequence-table.md)(partial)</span></span>



| <span data-ttu-id="697bd-115">Ação</span><span class="sxs-lookup"><span data-stu-id="697bd-115">Action</span></span>  | <span data-ttu-id="697bd-116">Condição</span><span class="sxs-lookup"><span data-stu-id="697bd-116">Condition</span></span> | <span data-ttu-id="697bd-117">Sequência</span><span class="sxs-lookup"><span data-stu-id="697bd-117">Sequence</span></span> |
|---------|-----------|----------|
| <span data-ttu-id="697bd-118">Action1</span><span class="sxs-lookup"><span data-stu-id="697bd-118">Action1</span></span> | <span data-ttu-id="697bd-119">TRUE</span><span class="sxs-lookup"><span data-stu-id="697bd-119">TRUE</span></span>      | <span data-ttu-id="697bd-120">1</span><span class="sxs-lookup"><span data-stu-id="697bd-120">1</span></span>        |



 

<span data-ttu-id="697bd-121">Para corrigir o erro, remova "Action1" da tabela ou remova a tabela.</span><span class="sxs-lookup"><span data-stu-id="697bd-121">To fix the error, either remove "Action1" from the table, or remove the table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="697bd-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="697bd-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="697bd-123">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="697bd-123">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



