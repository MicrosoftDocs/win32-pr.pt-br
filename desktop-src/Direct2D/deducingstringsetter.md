---
title: DeducingStringSetter (D2d1effecthelpers. h)
description: Deduz a classe e os argumentos e, em seguida, chama um retorno de chamada setter de propriedade de função de membro para uma propriedade de tipo de cadeia de caracteres.
ms.assetid: D3075B7B-D253-4F85-9FD2-3487C4207122
keywords:
- DeducingStringSetter Direct2D
topic_type:
- apiref
api_name:
- DeducingStringSetter
api_location:
- d2d1effecthelpers.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7860978fd271b2ff395caae068cd651d3057020
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758654"
---
# <a name="deducingstringsetter"></a><span data-ttu-id="d1a69-104">DeducingStringSetter</span><span class="sxs-lookup"><span data-stu-id="d1a69-104">DeducingStringSetter</span></span>

<span data-ttu-id="d1a69-105">Deduz a classe e os argumentos e, em seguida, chama um retorno de chamada setter de propriedade de função de membro para uma propriedade de tipo de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d1a69-105">Deduces the class and arguments and then calls a member-function property setter callback for a string-type property.</span></span>

> [!Note]  
> <span data-ttu-id="d1a69-106">DeducingStringSetter não deve ser chamado diretamente.</span><span class="sxs-lookup"><span data-stu-id="d1a69-106">DeducingStringSetter should not be called directly.</span></span>

 

``` syntax
template<class C, typename I>  
HRESULT DeducingStringSetter(  
    _In_ HRESULT (C::*callback)(PCWSTR string),
    _In_ I *effect,
    _In_reads_(dataSize) const BYTE *data,
    UINT32 dataSize  
    ) 
```

## <a name="requirements"></a><span data-ttu-id="d1a69-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1a69-107">Requirements</span></span>



| <span data-ttu-id="d1a69-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1a69-108">Requirement</span></span> | <span data-ttu-id="d1a69-109">Valor</span><span class="sxs-lookup"><span data-stu-id="d1a69-109">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1a69-110">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d1a69-110">Header</span></span><br/> | <dl> <span data-ttu-id="d1a69-111"><dt>D2d1effecthelpers. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1a69-111"><dt>D2d1effecthelpers.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1a69-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="d1a69-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1a69-113">**Direct2D::D educingStringGetter**</span><span class="sxs-lookup"><span data-stu-id="d1a69-113">**Direct2D::DeducingStringGetter**</span></span>](deducingstringgetter.md)
</dt> </dl>

 

 





