---
title: DeducingValueSetter (D2d1effecthelpers. h)
description: Deduz a classe e os argumentos e, em seguida, chama um retorno de chamada setter de propriedade de função de membro para uma propriedade de tipo de valor.
ms.assetid: 4C3D64A8-0CC0-405A-A5B3-627C2DF25EA1
keywords:
- DeducingValueSetter Direct2D
topic_type:
- apiref
api_name:
- DeducingValueSetter
api_location:
- d2d1effecthelpers.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e002c5a36c8ac0b196dfc5fb25e11f7f9d63806
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760718"
---
# <a name="deducingvaluesetter"></a><span data-ttu-id="74ca8-104">DeducingValueSetter</span><span class="sxs-lookup"><span data-stu-id="74ca8-104">DeducingValueSetter</span></span>

<span data-ttu-id="74ca8-105">Deduz a classe e os argumentos e, em seguida, chama um retorno de chamada setter de propriedade de função de membro para uma propriedade de tipo de valor.</span><span class="sxs-lookup"><span data-stu-id="74ca8-105">Deduces the class and arguments and then calls a member-function property setter callback for a value-type property.</span></span>

> [!Note]  
> <span data-ttu-id="74ca8-106">DeducingValueSetter não deve ser chamado diretamente.</span><span class="sxs-lookup"><span data-stu-id="74ca8-106">DeducingValueSetter should not be called directly.</span></span>

 

``` syntax
template<class C, typename P, typename I>
HRESULT DeducingValueSetter(
    _In_ HRESULT (C::*callback)(P),
    _In_ I *effect,
    _In_reads_(dataSize) const BYTE *data,
    UINT32 dataSize  
    ) 
```

## <a name="requirements"></a><span data-ttu-id="74ca8-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74ca8-107">Requirements</span></span>



| <span data-ttu-id="74ca8-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="74ca8-108">Requirement</span></span> | <span data-ttu-id="74ca8-109">Valor</span><span class="sxs-lookup"><span data-stu-id="74ca8-109">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74ca8-110">parâmetro</span><span class="sxs-lookup"><span data-stu-id="74ca8-110">Header</span></span><br/> | <dl> <span data-ttu-id="74ca8-111"><dt>D2d1effecthelpers. h</dt></span><span class="sxs-lookup"><span data-stu-id="74ca8-111"><dt>D2d1effecthelpers.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74ca8-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="74ca8-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74ca8-113">**Direct2D::D educingValueGetter**</span><span class="sxs-lookup"><span data-stu-id="74ca8-113">**Direct2D::DeducingValueGetter**</span></span>](deducingvaluegetter.md)
</dt> </dl>

 

 





