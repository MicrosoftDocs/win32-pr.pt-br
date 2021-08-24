---
title: BlobGetter (D2d1effecthelpers. h)
description: Chama um retorno de chamada getter de propriedade da função de membro para uma propriedade do tipo BLOB.
ms.assetid: 55A41BE4-2AAE-480B-A143-86E8E7533210
keywords:
- Direct2D BlobGetter
topic_type:
- apiref
api_name:
- BlobGetter
api_location:
- d2d1effecthelpers.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91e7c918965fc2d7cdf8948806ffffea32f35cafc061ff0d81addd5499c37072
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119653256"
---
# <a name="blobgetter"></a>BlobGetter

Chama um retorno de chamada getter de propriedade da função de membro para uma propriedade do tipo BLOB.

``` syntax
template<typename T, T P, typename I>
HRESULT CALLBACK BlobGetter(
    _In_ const IUnknown *effect,
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

[**Direct2D:: BlobSetter**](blobsetter.md)
</dt> </dl>

 

 





