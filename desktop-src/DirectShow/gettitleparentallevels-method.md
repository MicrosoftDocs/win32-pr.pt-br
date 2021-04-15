---
description: O método GetTitleParentalLevels recupera os níveis de gerenciamento de pais para o título especificado.
ms.assetid: 076808d7-6cb6-4d81-b26d-c7945db298f2
title: Método GetTitleParentalLevels
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6db82ca21c2fdd023aa472e4c3428260464a8612
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370202"
---
# <a name="gettitleparentallevels-method"></a><span data-ttu-id="dde7b-103">Método GetTitleParentalLevels</span><span class="sxs-lookup"><span data-stu-id="dde7b-103">GetTitleParentalLevels Method</span></span>

> [!Note]  
> <span data-ttu-id="dde7b-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="dde7b-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="dde7b-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="dde7b-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="dde7b-106">O `GetTitleParentalLevels` método recupera os níveis de gerenciamento de pais para o título especificado.</span><span class="sxs-lookup"><span data-stu-id="dde7b-106">The `GetTitleParentalLevels` method retrieves the parental management levels for the specified title.</span></span>

``` syntax
[ iLevels = ] MSWebDVD.GetTitleParentalLevels(iTitle)
```

## <a name="parameters"></a><span data-ttu-id="dde7b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dde7b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dde7b-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span><span class="sxs-lookup"><span data-stu-id="dde7b-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span></span>
</dt> <dd>

<span data-ttu-id="dde7b-109">Especifica o título como um inteiro.</span><span class="sxs-lookup"><span data-stu-id="dde7b-109">Specifies the title as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dde7b-110">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="dde7b-110">Return Value</span></span>

<span data-ttu-id="dde7b-111">Retorna um valor inteiro cujos bits individuais indicam quais níveis de gerenciamento de pais (PML) estão definidos no título especificado.</span><span class="sxs-lookup"><span data-stu-id="dde7b-111">Returns an integer value whose individual bits indicate which parental management levels (PML) are set in the specified title.</span></span>

## <a name="remarks"></a><span data-ttu-id="dde7b-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="dde7b-112">Remarks</span></span>

<span data-ttu-id="dde7b-113">Um título pode ter capítulos ou até mesmo segmentos curtos que têm um PML diferente do PML geral para o título.</span><span class="sxs-lookup"><span data-stu-id="dde7b-113">A title may have chapters or even short segments that have a PML different from the overall PML for the title.</span></span> <span data-ttu-id="dde7b-114">Use este método para determinar todos os PMLs que serão encontrados durante a reprodução de um título especificado.</span><span class="sxs-lookup"><span data-stu-id="dde7b-114">Use this method to determine all the PMLs that will be encountered when playing a specified title.</span></span> <span data-ttu-id="dde7b-115">O número inteiro retornado é um conjunto de sinalizadores de bits definidos conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="dde7b-115">The returned integer is a set of bit flags that are defined as shown in the table below.</span></span> <span data-ttu-id="dde7b-116">Execute uma operação AND bit a bit em *iLevels* e cada valor possível.</span><span class="sxs-lookup"><span data-stu-id="dde7b-116">Perform a bitwise AND operation on *iLevels* and each possible value.</span></span> <span data-ttu-id="dde7b-117">Se a operação retornar **true**, isso significará que PML será encontrado em algum ponto deste título.</span><span class="sxs-lookup"><span data-stu-id="dde7b-117">If the operation returns **true**, it means that PML will be encountered at some point in this title.</span></span>



| <span data-ttu-id="dde7b-118">Valor</span><span class="sxs-lookup"><span data-stu-id="dde7b-118">Value</span></span>  | <span data-ttu-id="dde7b-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="dde7b-119">Description</span></span>          |
|--------|----------------------|
| <span data-ttu-id="dde7b-120">0x100</span><span class="sxs-lookup"><span data-stu-id="dde7b-120">0x100</span></span>  | <span data-ttu-id="dde7b-121">Nível pai do DVD 1</span><span class="sxs-lookup"><span data-stu-id="dde7b-121">DVD Parental Level 1</span></span> |
| <span data-ttu-id="dde7b-122">0x200</span><span class="sxs-lookup"><span data-stu-id="dde7b-122">0x200</span></span>  | <span data-ttu-id="dde7b-123">Nível pai do DVD 2</span><span class="sxs-lookup"><span data-stu-id="dde7b-123">DVD Parental Level 2</span></span> |
| <span data-ttu-id="dde7b-124">0x400</span><span class="sxs-lookup"><span data-stu-id="dde7b-124">0x400</span></span>  | <span data-ttu-id="dde7b-125">Nível pai do DVD 3</span><span class="sxs-lookup"><span data-stu-id="dde7b-125">DVD Parental Level 3</span></span> |
| <span data-ttu-id="dde7b-126">0x800</span><span class="sxs-lookup"><span data-stu-id="dde7b-126">0x800</span></span>  | <span data-ttu-id="dde7b-127">Nível pai do DVD 4</span><span class="sxs-lookup"><span data-stu-id="dde7b-127">DVD Parental Level 4</span></span> |
| <span data-ttu-id="dde7b-128">0x1000</span><span class="sxs-lookup"><span data-stu-id="dde7b-128">0x1000</span></span> | <span data-ttu-id="dde7b-129">Nível pai do DVD 5</span><span class="sxs-lookup"><span data-stu-id="dde7b-129">DVD Parental Level 5</span></span> |
| <span data-ttu-id="dde7b-130">0x2000</span><span class="sxs-lookup"><span data-stu-id="dde7b-130">0x2000</span></span> | <span data-ttu-id="dde7b-131">Nível pai do DVD 6</span><span class="sxs-lookup"><span data-stu-id="dde7b-131">DVD Parental Level 6</span></span> |
| <span data-ttu-id="dde7b-132">0x4000</span><span class="sxs-lookup"><span data-stu-id="dde7b-132">0x4000</span></span> | <span data-ttu-id="dde7b-133">Nível pai do DVD 7</span><span class="sxs-lookup"><span data-stu-id="dde7b-133">DVD Parental Level 7</span></span> |
| <span data-ttu-id="dde7b-134">0x8000</span><span class="sxs-lookup"><span data-stu-id="dde7b-134">0x8000</span></span> | <span data-ttu-id="dde7b-135">Nível pai do DVD 8</span><span class="sxs-lookup"><span data-stu-id="dde7b-135">DVD Parental Level 8</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="dde7b-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="dde7b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dde7b-137">**SelectParentalLevel**</span><span class="sxs-lookup"><span data-stu-id="dde7b-137">**SelectParentalLevel**</span></span>](selectparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="dde7b-138">**GetPlayerParentalCountry**</span><span class="sxs-lookup"><span data-stu-id="dde7b-138">**GetPlayerParentalCountry**</span></span>](getplayerparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="dde7b-139">**GetPlayerParentalLevel**</span><span class="sxs-lookup"><span data-stu-id="dde7b-139">**GetPlayerParentalLevel**</span></span>](getplayerparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="dde7b-140">**SelectParentalCountry**</span><span class="sxs-lookup"><span data-stu-id="dde7b-140">**SelectParentalCountry**</span></span>](selectparentalcountry-method.md)
</dt> </dl>

 

 



