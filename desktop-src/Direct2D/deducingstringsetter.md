---
title: DeducingStringSetter (D2d1effecthelpers. h)
description: Deduz a classe e os argumentos e, em seguida, chama um retorno de chamada setter de propriedade de função de membro para uma propriedade de tipo de cadeia de caracteres.
ms.assetid: D3075B7B-D253-4F85-9FD2-3487C4207122
keywords:
- Direct2D DeducingStringSetter
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
ms.openlocfilehash: 50fdcf97e9df1f77705509a4b93b6936a4c9f7f203ddb16e0b0284630cb42bdc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075280"
---
# <a name="deducingstringsetter"></a>DeducingStringSetter

Deduz a classe e os argumentos e, em seguida, chama um retorno de chamada setter de propriedade de função de membro para uma propriedade de tipo de cadeia de caracteres.

> [!Note]  
> DeducingStringSetter não deve ser chamado diretamente.

 

``` syntax
template<class C, typename I>  
HRESULT DeducingStringSetter(  
    _In_ HRESULT (C::*callback)(PCWSTR string),
    _In_ I *effect,
    _In_reads_(dataSize) const BYTE *data,
    UINT32 dataSize  
    ) 
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D2d1effecthelpers. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Direct2D::D educingstringgetter**](deducingstringgetter.md)
</dt> </dl>

 

 





