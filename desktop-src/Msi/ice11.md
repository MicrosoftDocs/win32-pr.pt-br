---
description: O ICE11 é usado com instalações simultâneas. As instalações simultâneas não são recomendadas para a instalação de aplicativos destinados ao lançamento para o público. Para obter informações sobre instalações simultâneas, consulte instalações simultâneas.
ms.assetid: fbcc94fa-be94-4ad1-a3f0-ea7d50ee0a15
title: ICE11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d3f85a4dc4d736acfbd4385324aa35565f399bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922022"
---
# <a name="ice11"></a><span data-ttu-id="474be-105">ICE11</span><span class="sxs-lookup"><span data-stu-id="474be-105">ICE11</span></span>

<span data-ttu-id="474be-106">O ICE11 é usado com instalações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="474be-106">The ICE11 is used with concurrent installations.</span></span> <span data-ttu-id="474be-107">As instalações simultâneas não são recomendadas para a instalação de aplicativos destinados ao lançamento para o público.</span><span class="sxs-lookup"><span data-stu-id="474be-107">Concurrent installations are not recommended for the installation of applications intended for release to the public.</span></span> <span data-ttu-id="474be-108">Para obter informações sobre instalações simultâneas, consulte [instalações simultâneas](concurrent-installations.md).</span><span class="sxs-lookup"><span data-stu-id="474be-108">For information about concurrent installations please see [Concurrent Installations](concurrent-installations.md).</span></span>

## <a name="result"></a><span data-ttu-id="474be-109">Resultado</span><span class="sxs-lookup"><span data-stu-id="474be-109">Result</span></span>

<span data-ttu-id="474be-110">ICE11 valida a coluna de origem da [tabela CustomAction](customaction-table.md) de ações personalizadas de instalação simultânea.</span><span class="sxs-lookup"><span data-stu-id="474be-110">ICE11 validates the Source column of the [CustomAction table](customaction-table.md) of concurrent installation custom actions.</span></span> <span data-ttu-id="474be-111">A coluna de origem deve conter um [GUID](guid.md) (código de produto msi) válido.</span><span class="sxs-lookup"><span data-stu-id="474be-111">The Source column must contain a valid [GUID](guid.md) (MSI product code).</span></span>

<span data-ttu-id="474be-112">ICE11 posta um erro se a coluna de origem da tabela CustomAction é criada incorretamente para ações personalizadas de instalação simultânea.</span><span class="sxs-lookup"><span data-stu-id="474be-112">ICE11 posts an error if the Source column of the CustomAction table is authored incorrectly for concurrent installation custom actions.</span></span>

## <a name="example"></a><span data-ttu-id="474be-113">Exemplo</span><span class="sxs-lookup"><span data-stu-id="474be-113">Example</span></span>

<span data-ttu-id="474be-114">ICE posta as seguintes mensagens de erro para o exemplo mostrado.</span><span class="sxs-lookup"><span data-stu-id="474be-114">ICE posts the following error messages for the example shown.</span></span>

``` syntax
CustomAction: CA4 is a nested install of an advertised MSI.  The 'Source' must contain a valid MSI product code.  Current: ProductCode.
CustomAction: CA1 is a nested install of an advertised MSI.  It duplicates the ProductCode of the base MSI package.  Current: {BFB69273-F0AE-45C4-9853-0AF946714768}.
CustomAction: CA2 is a nested install of an advertised MSI.  The GUID must be all upper-case.  Current: {BFB69273-F0AE-55c5-9853-0AF946714768}.
```

<span data-ttu-id="474be-115">[Tabela de propriedades](property-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="474be-115">[Property Table](property-table.md) (partial)</span></span>



| <span data-ttu-id="474be-116">Propriedade</span><span class="sxs-lookup"><span data-stu-id="474be-116">Property</span></span>        | <span data-ttu-id="474be-117">Valor</span><span class="sxs-lookup"><span data-stu-id="474be-117">Value</span></span>                                  |
|-----------------|----------------------------------------|
| <span data-ttu-id="474be-118">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="474be-118">**ProductCode**</span></span> | <span data-ttu-id="474be-119">{BFB69273-F0AE-45C4-9853-0AF946714768}</span><span class="sxs-lookup"><span data-stu-id="474be-119">{BFB69273-F0AE-45C4-9853-0AF946714768}</span></span> |



 

<span data-ttu-id="474be-120">[Tabela CustomAction](customaction-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="474be-120">[CustomAction Table](customaction-table.md) (partial)</span></span>



| <span data-ttu-id="474be-121">CustomAction</span><span class="sxs-lookup"><span data-stu-id="474be-121">CustomAction</span></span> | <span data-ttu-id="474be-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="474be-122">Type</span></span> | <span data-ttu-id="474be-123">Fonte</span><span class="sxs-lookup"><span data-stu-id="474be-123">Source</span></span>                                 |
|--------------|------|----------------------------------------|
| <span data-ttu-id="474be-124">CA1</span><span class="sxs-lookup"><span data-stu-id="474be-124">CA1</span></span>          | <span data-ttu-id="474be-125">39</span><span class="sxs-lookup"><span data-stu-id="474be-125">39</span></span>   | <span data-ttu-id="474be-126">{BFB69273-F0AE-45C4-9853-0AF946714768}</span><span class="sxs-lookup"><span data-stu-id="474be-126">{BFB69273-F0AE-45C4-9853-0AF946714768}</span></span> |
| <span data-ttu-id="474be-127">CA2</span><span class="sxs-lookup"><span data-stu-id="474be-127">CA2</span></span>          | <span data-ttu-id="474be-128">39</span><span class="sxs-lookup"><span data-stu-id="474be-128">39</span></span>   | <span data-ttu-id="474be-129">{BFB69273-F0AE-55c5-9853-0AF946714768}</span><span class="sxs-lookup"><span data-stu-id="474be-129">{BFB69273-F0AE-55c5-9853-0AF946714768}</span></span> |
| <span data-ttu-id="474be-130">CA3</span><span class="sxs-lookup"><span data-stu-id="474be-130">CA3</span></span>          | <span data-ttu-id="474be-131">39</span><span class="sxs-lookup"><span data-stu-id="474be-131">39</span></span>   | <span data-ttu-id="474be-132">{BFB69273-F0AE-66C6-9853-0AF946714768}</span><span class="sxs-lookup"><span data-stu-id="474be-132">{BFB69273-F0AE-66C6-9853-0AF946714768}</span></span> |
| <span data-ttu-id="474be-133">CA4</span><span class="sxs-lookup"><span data-stu-id="474be-133">CA4</span></span>          | <span data-ttu-id="474be-134">39</span><span class="sxs-lookup"><span data-stu-id="474be-134">39</span></span>   | <span data-ttu-id="474be-135">ProductCode</span><span class="sxs-lookup"><span data-stu-id="474be-135">ProductCode</span></span>                            |



 

<span data-ttu-id="474be-136">Para corrigir os erros, para CA1, você não pode fazer uma instalação simultânea do "pacote base".</span><span class="sxs-lookup"><span data-stu-id="474be-136">To fix the errors, for CA1, you cannot do a concurrent installation of the "base package".</span></span> <span data-ttu-id="474be-137">Isso resultaria em uma instalação recursiva.</span><span class="sxs-lookup"><span data-stu-id="474be-137">This would result in a recursive installation.</span></span> <span data-ttu-id="474be-138">Essa entrada deve ser removida ou a coluna de origem deve ser alterada para um GUID de um MSI anunciado que seja diferente do GUID do pacote base.</span><span class="sxs-lookup"><span data-stu-id="474be-138">This entry should be removed or the Source column should be changed to a GUID for an advertised MSI that differs from the base package's GUID.</span></span> <span data-ttu-id="474be-139">Para CA2, torne todos os caracteres do GUID de maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="474be-139">For CA2, make all characters of the GUID uppercase.</span></span> <span data-ttu-id="474be-140">Por fim, altere a coluna de origem CA4's para fazer referência a um GUID válido de um MSI anunciado.</span><span class="sxs-lookup"><span data-stu-id="474be-140">Lastly, change CA4's Source column to reference a valid GUID of an advertised MSI.</span></span>

## <a name="related-topics"></a><span data-ttu-id="474be-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="474be-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="474be-142">Instalações simultâneas</span><span class="sxs-lookup"><span data-stu-id="474be-142">Concurrent Installations</span></span>](concurrent-installations.md)
</dt> <dt>

[<span data-ttu-id="474be-143">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="474be-143">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



