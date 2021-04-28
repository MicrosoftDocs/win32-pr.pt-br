---
description: Construtor de CEnumMediaTypes. CEnumMediaTypes-método de construtor.
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
ms.openlocfilehash: 2d243ed25cc48c5d30d467f97e2ec20e1f0f2b58
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095674"
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



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe CEnumMediaTypes**](cenummediatypes.md)
</dt> </dl>

 

 




