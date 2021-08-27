---
description: Método CBaseMediaFilter.StreamTime – o método StreamTime recupera a hora do fluxo atual.
ms.assetid: 2e1ff6f1-9815-4ee6-97e8-a5ab5f472b27
title: Método CBaseMediaFilter.StreamTime (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.StreamTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 99205cb7065b7bd57d0f49a7f4942df8c1548ba5d4b4f8b26c8a13387ddc7d1e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076586"
---
# <a name="cbasemediafilterstreamtime-method"></a>Método CBaseMediaFilter.StreamTime

O `StreamTime` método recupera a hora do fluxo atual.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT StreamTime(
  [ref] CRefTime &rtStream
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*rtStream* \[ Ref\]
</dt> <dd>

Referência a um [**objeto CRefTime**](creftime.md) que recebe a hora do fluxo atual.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.** Os valores possíveis incluem aqueles listados na tabela a seguir.



| Código de retorno                                                                                      | Descrição                                 |
|--------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>             | Êxito.<br/>                         |
| <dl> <dt>**VFW \_ E \_ SEM \_ RELÓGIO**</dt> </dl> | Nenhum relógio de referência está disponível.<br/> |



 

## <a name="remarks"></a>Comentários

A hora do fluxo é definida como a hora de referência atual (conforme determinado pelo relógio de referência) menos a hora de início (especificada por [**CBaseMediaFilter::m \_ tStart**](cbasemediafilter-m-tstart.md)). O carimbo de data/hora de um exemplo de mídia especifica a hora do fluxo quando ele deve ser renderizado. Se um exemplo com um carimbo de data/hora menor que a hora do fluxo atual ainda não tiver sido renderizado, será tarde.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseMediaFilter**](cbasemediafilter.md)
</dt> </dl>

 

 




