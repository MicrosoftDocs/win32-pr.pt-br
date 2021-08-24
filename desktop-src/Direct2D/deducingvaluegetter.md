---
title: DeducingValueGetter (D2d1effecthelpers. h)
description: Deduz a classe e os argumentos e, em seguida, chama um retorno de chamada getter de propriedade de função de membro para uma propriedade de tipo de valor.
ms.assetid: E2E5CCC3-B112-4D3C-8840-121A55C4F1A2
keywords:
- Direct2D DeducingValueGetter
topic_type:
- apiref
api_name:
- DeducingValueGetter
api_location:
- d2d1effecthelpers.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 743c4e457c9dc3f6e29c4bfc78e539256869a2d30a055168384d287911ca4d4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652946"
---
# <a name="deducingvaluegetter"></a>DeducingValueGetter

Deduz a classe e os argumentos e, em seguida, chama um retorno de chamada getter de propriedade de função de membro para uma propriedade de tipo de valor.

> [!Note]  
> DeducingValueGetter não deve ser chamado diretamente.

 

``` syntax
template<class C, typename P, typename I>
HRESULT DeducingValueGetter(
    _In_ P (C::*callback)() const,
    _In_ const I *effect,
    _Out_writes_opt_(dataSize) BYTE *data,
    UINT32 dataSize,
    _Out_opt_ UINT32 *actualSize  
    ) 
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D2d1effecthelpers. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Direct2D::D educingvaluesetter**](deducingvaluesetter.md)
</dt> </dl>

 

 





