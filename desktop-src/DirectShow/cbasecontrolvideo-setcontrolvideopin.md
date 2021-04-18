---
description: O método SetControlVideoPin define o PIN usado pelo filtro.
ms.assetid: 4346f828-4380-4150-9ecb-74eb690bdcdf
title: Método CBaseControlVideo. SetControlVideoPin (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetControlVideoPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4cf47469800a4d1ecd8abe373d6f3c1fd53ece5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755396"
---
# <a name="cbasecontrolvideosetcontrolvideopin-method"></a>Método CBaseControlVideo. SetControlVideoPin

O `SetControlVideoPin` método define o PIN usado pelo filtro.

## <a name="syntax"></a>Sintaxe


```C++
void SetControlVideoPin(
   CBasePin *pPin
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pPin* 
</dt> <dd>

Ponteiro para o PIN com o qual a interface é sincronizada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

A interface pode ser chamada somente quando o filtro tiver sido conectado com êxito. O objeto é passado por esse método para o PIN com o qual ele é sincronizado; na maioria dos casos, ele determinará se o PIN está conectado quando tiver um método de interface chamado e retornará VFW \_ e \_ não \_ conectado se falhar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




