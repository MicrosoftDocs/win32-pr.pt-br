---
title: EFFECTs. effecttype
description: O método effecttype recupera o nome do registro da visualização com o índice de registro especificado. Esse nome é uma ID exclusiva definida pelo autor da visualização.
ms.assetid: 47da4f3f-8552-4404-ad46-5dc6afca849a
keywords:
- EFFECTs. effecttype Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.effectType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3eda9cbd1a4634062683536f1f132393a2874691
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813166"
---
# <a name="effectseffecttype"></a><span data-ttu-id="48475-105">EFFECTs. effecttype</span><span class="sxs-lookup"><span data-stu-id="48475-105">EFFECTS.effectType</span></span>

<span data-ttu-id="48475-106">O método **effecttype** recupera o nome do registro da visualização com o índice de registro especificado.</span><span class="sxs-lookup"><span data-stu-id="48475-106">The **effectType** method retrieves the registry name of the visualization with the specified registry index.</span></span> <span data-ttu-id="48475-107">Esse nome é uma ID exclusiva definida pelo autor da visualização.</span><span class="sxs-lookup"><span data-stu-id="48475-107">This name is a unique ID defined by the visualization author.</span></span>

``` syntax
        elementID.effectType(index)
```

## <a name="parameters"></a><span data-ttu-id="48475-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="48475-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48475-109"><span id="index"></span><span id="INDEX"></span>*index*</span><span class="sxs-lookup"><span data-stu-id="48475-109"><span id="index"></span><span id="INDEX"></span>*index*</span></span>
</dt> <dd>

<span data-ttu-id="48475-110">**Número** (**longo**) que contém o índice de uma visualização do registro.</span><span class="sxs-lookup"><span data-stu-id="48475-110">**Number** (**long**) containing the registry index of a visualization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48475-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="48475-111">Return Value</span></span>

<span data-ttu-id="48475-112">Esse método retorna uma **cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="48475-112">This method returns a **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="48475-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="48475-113">Remarks</span></span>

<span data-ttu-id="48475-114">Esse método é útil para alternar entre visualizações no script.</span><span class="sxs-lookup"><span data-stu-id="48475-114">This method is useful for switching between visualizations in script.</span></span> <span data-ttu-id="48475-115">Uma interface do usuário pode exibir o conjunto de títulos, mas quando o usuário seleciona um, o script deve usar **currentEffectType** para alternar as visualizações.</span><span class="sxs-lookup"><span data-stu-id="48475-115">A user interface could display the set of titles, but when the user selects one, the script must use **currentEffectType** to switch visualizations.</span></span>

## <a name="requirements"></a><span data-ttu-id="48475-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48475-116">Requirements</span></span>



| <span data-ttu-id="48475-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="48475-117">Requirement</span></span> | <span data-ttu-id="48475-118">Valor</span><span class="sxs-lookup"><span data-stu-id="48475-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="48475-119">Versão</span><span class="sxs-lookup"><span data-stu-id="48475-119">Version</span></span><br/> | <span data-ttu-id="48475-120">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="48475-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="48475-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="48475-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48475-122">**Elemento EFFECTs**</span><span class="sxs-lookup"><span data-stu-id="48475-122">**EFFECTS Element**</span></span>](effects-element.md)
</dt> <dt>

[<span data-ttu-id="48475-123">**EFFECTs. currentEffectType**</span><span class="sxs-lookup"><span data-stu-id="48475-123">**EFFECTS.currentEffectType**</span></span>](effects-currenteffecttype.md)
</dt> </dl>

 

 





