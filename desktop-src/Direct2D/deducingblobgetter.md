---
title: DeducingBlobGetter (D2d1effecthelpers.h)
description: Deduz a classe e os argumentos e, em seguida, chama um retorno de chamada getter da propriedade member-function para uma propriedade de tipo blob.
ms.assetid: 1B8800CB-2AD0-4684-99D7-986F6C53A6F1
keywords:
- DeduçãoBlobGetter Direct2D
topic_type:
- apiref
api_name:
- DeducingBlobGetter
api_location:
- d2d1effecthelpers.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f045f781ae22aa4550a298ba7becfe2bc4a939528657f663ec021870bf3afa78
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918276"
---
# <a name="deducingblobgetter"></a>DeduçãoBlobGetter

Deduz a classe e os argumentos e, em seguida, chama um retorno de chamada getter da propriedade member-function para uma propriedade de tipo blob.

> [!Note]  
> DeducingBlobGetter não deve ser chamado diretamente.

 

``` syntax
template<class C, typename I>  
HRESULT DeducingBlobGetter(  
    _In_ HRESULT (C::*callback)(BYTE *, UINT32, UINT32*) const,  
    _In_ const I *effect,  
    _Out_writes_opt_(dataSize) BYTE *data,  
    UINT32 dataSize,  
    _Out_opt_ UINT32 *actualSize  
    ) 
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D2d1effecthelpers.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Direct2D::D educingBlobSetter**](deducingblobsetter.md)
</dt> </dl>

 

 





