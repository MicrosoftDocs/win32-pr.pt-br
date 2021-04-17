---
title: DeducingStringGetter (D2d1effecthelpers. h)
description: Deduz a classe e os argumentos e, em seguida, chama um retorno de chamada getter de propriedade de função de membro para uma propriedade de tipo de cadeia de caracteres.
ms.assetid: 434E3360-D6C3-46CB-818E-15A185F4BB84
keywords:
- DeducingStringGetter Direct2D
topic_type:
- apiref
api_name:
- DeducingStringGetter
api_location:
- d2d1effecthelpers.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac65b9e5d7e37e2db83f06f80172e90f9f27f80b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749651"
---
# <a name="deducingstringgetter"></a><span data-ttu-id="7a791-104">DeducingStringGetter</span><span class="sxs-lookup"><span data-stu-id="7a791-104">DeducingStringGetter</span></span>

<span data-ttu-id="7a791-105">Deduz a classe e os argumentos e, em seguida, chama um retorno de chamada getter de propriedade de função de membro para uma propriedade de tipo de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="7a791-105">Deduces the class and arguments and then calls a member-function property getter callback for a string-type property.</span></span>

> [!Note]  
> <span data-ttu-id="7a791-106">DeducingStringGetter não deve ser chamado diretamente.</span><span class="sxs-lookup"><span data-stu-id="7a791-106">DeducingStringGetter should not be called directly.</span></span>

 

``` syntax
template<class C, typename I>  
HRESULT DeducingStringGetter(
    _In_ HRESULT (C::*callback)(PWSTR, UINT32, UINT32*) const,
    _In_ const I *effect,
    _Out_writes_opt_(dataSize) BYTE *data,
    UINT32 dataSize,
    _Out_opt_ UINT32 *actualSize 
    ) 
```

## <a name="requirements"></a><span data-ttu-id="7a791-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a791-107">Requirements</span></span>



| <span data-ttu-id="7a791-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a791-108">Requirement</span></span> | <span data-ttu-id="7a791-109">Valor</span><span class="sxs-lookup"><span data-stu-id="7a791-109">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a791-110">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7a791-110">Header</span></span><br/> | <dl> <span data-ttu-id="7a791-111"><dt>D2d1effecthelpers. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a791-111"><dt>D2d1effecthelpers.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a791-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="7a791-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a791-113">**Direct2D::D educingStringSetter**</span><span class="sxs-lookup"><span data-stu-id="7a791-113">**Direct2D::DeducingStringSetter**</span></span>](deducingstringsetter.md)
</dt> </dl>

 

 





