---
description: O método SetMediaType é chamado quando o tipo de mídia é definido em um dos Pins do filtro.
ms.assetid: 3e505036-7fa6-42cf-a683-3a39a43d209d
title: Método CTransformFilter. SetMediaType (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 86e9eac76ccc178659935511d75b1676a136a1c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789652"
---
# <a name="ctransformfiltersetmediatype-method"></a>Método CTransformFilter. SetMediaType

O `SetMediaType` método é chamado quando o tipo de mídia é definido em um dos Pins do filtro.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT SetMediaType(
         PIN_DIRECTION direction,
   const CMediaType    *pmt
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*direction* 
</dt> <dd>

Membro do tipo enumerado de [**\_ direção do PIN**](/windows/win32/api/strmif/ne-strmif-pin_direction) , especificando um PIN no filtro (entrada ou saída).

</dd> <dt>

*PMT* 
</dt> <dd>

Ponteiro para um objeto [**CMediaType**](cmediatype.md) que especifica o tipo de mídia.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Os métodos [**CTransformInputPin:: SetMediaType**](ctransforminputpin-setmediatype.md) e [**CTransformOutputPin:: SetMediaType**](ctransformoutputpin-setmediatype.md) chamam esse método quando o tipo de mídia de um PIN é definido. Esse método não faz nada na classe base, mas a classe derivada pode substituí-la.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




