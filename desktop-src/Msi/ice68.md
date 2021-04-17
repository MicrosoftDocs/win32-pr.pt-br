---
description: ICE68 verifica se todos os tipos de ação personalizados necessários para uma instalação são válidos.
ms.assetid: a37d6d6c-3005-425b-883a-6fe074b9d708
title: ICE68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1392db6ec05085c672ed70c8f035ea8eed3015e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754641"
---
# <a name="ice68"></a><span data-ttu-id="3b56d-103">ICE68</span><span class="sxs-lookup"><span data-stu-id="3b56d-103">ICE68</span></span>

<span data-ttu-id="3b56d-104">ICE68 verifica se todos os tipos de ação personalizados necessários para uma instalação são válidos.</span><span class="sxs-lookup"><span data-stu-id="3b56d-104">ICE68 checks that all custom action types needed for an installation are valid.</span></span> <span data-ttu-id="3b56d-105">Falha ao corrigir o erro relatado pelo ICE68 faz com que uma instalação que tenta executar a ação falhe.</span><span class="sxs-lookup"><span data-stu-id="3b56d-105">Failure to fix the error reported by ICE68 causes an installation that attempts to execute the action to fail.</span></span> <span data-ttu-id="3b56d-106">ICE68 emitirá um aviso se o atributo **msidbCustomActionTypeNoImpersonate** estiver definido sem definir também o atributo **msidbCustomActionTypeInScript** .</span><span class="sxs-lookup"><span data-stu-id="3b56d-106">ICE68 issues a warning if the **msidbCustomActionTypeNoImpersonate** attribute is set without also setting the **msidbCustomActionTypeInScript** attribute.</span></span>

## <a name="result"></a><span data-ttu-id="3b56d-107">Resultado</span><span class="sxs-lookup"><span data-stu-id="3b56d-107">Result</span></span>

<span data-ttu-id="3b56d-108">ICE68 retornará um erro se um tipo de ação necessário para uma instalação for inválido.</span><span class="sxs-lookup"><span data-stu-id="3b56d-108">ICE68 returns an error if an action type needed for an installation is invalid.</span></span>

## <a name="example"></a><span data-ttu-id="3b56d-109">Exemplo</span><span class="sxs-lookup"><span data-stu-id="3b56d-109">Example</span></span>

<span data-ttu-id="3b56d-110">ICE68 lança o seguinte aviso se uma ação personalizada tiver o conjunto de bits **msidbCustomActionTypeNoImpersonate** no campo tipo da tabela CustomAction sem o **msidbCustomActionTypeInScript** também definido.</span><span class="sxs-lookup"><span data-stu-id="3b56d-110">ICE68 posts the following warning if a custom action has the **msidbCustomActionTypeNoImpersonate** bit set in the Type field of the CustomAction table without the **msidbCustomActionTypeInScript** also set.</span></span>

``` syntax
Even though custom action '[2]' is marked to be elevated (with 
attribute msidbCustomActionTypeNoImpersonate), it will not be run with elevated 
privileges because it's not deferred (with attribute msidbCustomActionTypeInScript).
```

<span data-ttu-id="3b56d-111">Para corrigir esse aviso, inclua **msidbCustomActionTypeInScript** (0x400) se a ação personalizada incluir **msidbCustomActionTypeNoImpersonate** (0x800).</span><span class="sxs-lookup"><span data-stu-id="3b56d-111">To fix this warning, include **msidbCustomActionTypeInScript** (0x400) if the custom action includes **msidbCustomActionTypeNoImpersonate** (0x800).</span></span> <span data-ttu-id="3b56d-112">Caso contrário, o instalador ignora o atributo **msidbCustomActionTypeNoImpersonate** .</span><span class="sxs-lookup"><span data-stu-id="3b56d-112">Otherwise the installer ignores the **msidbCustomActionTypeNoImpersonate** attribute.</span></span> <span data-ttu-id="3b56d-113">Para obter mais informações, consulte [Opções de execução de In-Script de ação personalizada](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="3b56d-113">For more information, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

<span data-ttu-id="3b56d-114">ICE68 relata o seguinte erro para o exemplo mostrado:</span><span class="sxs-lookup"><span data-stu-id="3b56d-114">ICE68 reports the following error for the example shown:</span></span>

``` syntax
Invalid custom action type for action 'Action1'.
```

<span data-ttu-id="3b56d-115">1027 não é um tipo de ação válido.</span><span class="sxs-lookup"><span data-stu-id="3b56d-115">1027 is not a valid action type.</span></span>

<span data-ttu-id="3b56d-116">Para corrigir esse erro, escolha um tipo de ação personalizada válido.</span><span class="sxs-lookup"><span data-stu-id="3b56d-116">To fix this error, choose a valid custom action type.</span></span>

<span data-ttu-id="3b56d-117">[Tabela CustomAction](customaction-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="3b56d-117">[CustomAction Table](customaction-table.md) (partial)</span></span>



| <span data-ttu-id="3b56d-118">Ação</span><span class="sxs-lookup"><span data-stu-id="3b56d-118">Action</span></span>  | <span data-ttu-id="3b56d-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="3b56d-119">Type</span></span> | <span data-ttu-id="3b56d-120">Fonte</span><span class="sxs-lookup"><span data-stu-id="3b56d-120">Source</span></span>   | <span data-ttu-id="3b56d-121">Destino</span><span class="sxs-lookup"><span data-stu-id="3b56d-121">Target</span></span>     |
|---------|------|----------|------------|
| <span data-ttu-id="3b56d-122">Action1</span><span class="sxs-lookup"><span data-stu-id="3b56d-122">Action1</span></span> | <span data-ttu-id="3b56d-123">1027</span><span class="sxs-lookup"><span data-stu-id="3b56d-123">1027</span></span> | <span data-ttu-id="3b56d-124">Argumento</span><span class="sxs-lookup"><span data-stu-id="3b56d-124">Argument</span></span> | <span data-ttu-id="3b56d-125">Component1</span><span class="sxs-lookup"><span data-stu-id="3b56d-125">Component1</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="3b56d-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3b56d-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b56d-127">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="3b56d-127">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



