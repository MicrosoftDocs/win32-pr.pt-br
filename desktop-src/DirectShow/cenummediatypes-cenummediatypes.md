---
description: Método de construtor.
ms.assetid: fae2e05c-3f7b-4511-9b9d-5a37ea03f851
title: Construtor CEnumMediaTypes. CEnumMediaTypes (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes.CEnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e17357d90c57f1a7d489d07fa56206343f50788
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747595"
---
# <a name="cenummediatypescenummediatypes-constructor"></a>Construtor CEnumMediaTypes. CEnumMediaTypes

Método de construtor.

## <a name="syntax"></a>Sintaxe


```C++
CEnumMediaTypes(
   CBasePin        *pPin,
   CEnumMediaTypes *pEnumMediaTypes
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pPin* 
</dt> <dd>

Ponteiro para o PIN no qual a enumeração deve ser executada.

</dd> <dt>

*pEnumMediaTypes* 
</dt> <dd>

Ponteiro para a interface [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) de um enumerador para clonar ou **NULL**.

</dd> </dl>

## <a name="remarks"></a>Comentários

Se *pEnumMediaTypes* for **NULL**, esse método inicializará o enumerador para o início da sequência de enumeração. Caso contrário, ele duplica o estado interno do enumerador especificado por *pEnumMediaTypes*.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CEnumMediaTypes**](cenummediatypes.md)
</dt> </dl>

 

 




