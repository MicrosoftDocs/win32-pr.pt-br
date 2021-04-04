---
description: ICE28 é normalmente usado para validar que a ação ForceReboot é colocada antes ou depois, e nunca em um grupo específico de ações nas tabelas de sequência de ação. Consulte o tópico de ação ForceReboot para determinar as ações que compõem esse grupo.
ms.assetid: 746d907a-33e1-479a-bcb0-93e7fd5dd975
title: ICE28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc65878bdc3db4f9b79ba95b4a170b694a4728ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646807"
---
# <a name="ice28"></a><span data-ttu-id="10432-104">ICE28</span><span class="sxs-lookup"><span data-stu-id="10432-104">ICE28</span></span>

<span data-ttu-id="10432-105">ICE28 é normalmente usado para validar que a ação ForceReboot é colocada antes ou depois, e nunca em um grupo específico de ações nas tabelas de sequência de ação.</span><span class="sxs-lookup"><span data-stu-id="10432-105">ICE28 is commonly used to validate that the ForceReboot action is placed before or after, and never within, a specific group of actions in the action sequence tables.</span></span> <span data-ttu-id="10432-106">Consulte o tópico de [ação ForceReboot](forcereboot-action.md) para determinar as ações que compõem esse grupo.</span><span class="sxs-lookup"><span data-stu-id="10432-106">See the [ForceReboot action](forcereboot-action.md) topic to determine the actions that comprise this group.</span></span>

<span data-ttu-id="10432-107">ICE28 valida ações nas seguintes tabelas de sequência:</span><span class="sxs-lookup"><span data-stu-id="10432-107">ICE28 validates actions in the following sequence tables:</span></span>

[<span data-ttu-id="10432-108">Tabela AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="10432-108">AdminUISequence table</span></span>](adminuisequence-table.md)

[<span data-ttu-id="10432-109">Tabela AdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="10432-109">AdminExecuteSequence table</span></span>](adminexecutesequence-table.md)

[<span data-ttu-id="10432-110">Tabela InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="10432-110">InstallUISequence table</span></span>](installuisequence-table.md)

[<span data-ttu-id="10432-111">Tabela InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="10432-111">InstallExecuteSequence table</span></span>](installexecutesequence-table.md)

## <a name="result"></a><span data-ttu-id="10432-112">Resultado</span><span class="sxs-lookup"><span data-stu-id="10432-112">Result</span></span>

<span data-ttu-id="10432-113">ICE28 posta uma mensagem de erro se ForceReboot for sequenciado dentro do grupo de ações especificado.</span><span class="sxs-lookup"><span data-stu-id="10432-113">ICE28 posts an error message if ForceReboot is sequenced within the specified action group.</span></span>

## <a name="example"></a><span data-ttu-id="10432-114">Exemplo</span><span class="sxs-lookup"><span data-stu-id="10432-114">Example</span></span>

<span data-ttu-id="10432-115">Para o exemplo mostrado, ICE28 posta a seguinte mensagem de erro:</span><span class="sxs-lookup"><span data-stu-id="10432-115">For the example shown, ICE28 posts the following error message:</span></span>

``` syntax
Action: 'ForceReboot' of table InstallExecuteSequence is not permitted in the range 5 to 15 because it cannot separate a set of actions contained in this range.
```

[<span data-ttu-id="10432-116">Tabela InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="10432-116">InstallExecuteSequence Table</span></span>](installexecutesequence-table.md)



| <span data-ttu-id="10432-117">Ação</span><span class="sxs-lookup"><span data-stu-id="10432-117">Action</span></span>             | <span data-ttu-id="10432-118">Sequência</span><span class="sxs-lookup"><span data-stu-id="10432-118">Sequence</span></span> |
|--------------------|----------|
| <span data-ttu-id="10432-119">ForceReboot</span><span class="sxs-lookup"><span data-stu-id="10432-119">ForceReboot</span></span>        | <span data-ttu-id="10432-120">10</span><span class="sxs-lookup"><span data-stu-id="10432-120">10</span></span>       |
| <span data-ttu-id="10432-121">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="10432-121">RegisterMIMEInfo</span></span>   |   <span data-ttu-id="10432-122">5</span><span class="sxs-lookup"><span data-stu-id="10432-122">5</span></span>      |
| <span data-ttu-id="10432-123">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="10432-123">RegisterProgIdInfo</span></span> | <span data-ttu-id="10432-124">15</span><span class="sxs-lookup"><span data-stu-id="10432-124">15</span></span>       |



 

<span data-ttu-id="10432-125">O número de sequência de 10 fornecido para quebras de ForceReboot gera o erro, pois ele vem entre os números de sequência de RegisterMIMEInfo e RegisterProgIdInfo.</span><span class="sxs-lookup"><span data-stu-id="10432-125">The sequence number of 10 given to ForceReboot breaks generates the error, because it comes between the sequence numbers of RegisterMIMEInfo and RegisterProgIdInfo.</span></span>

## <a name="related-topics"></a><span data-ttu-id="10432-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="10432-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10432-127">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="10432-127">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



