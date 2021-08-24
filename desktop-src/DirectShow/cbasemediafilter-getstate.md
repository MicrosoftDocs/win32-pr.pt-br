---
description: 'O método GetState recupera o estado do objeto (em execução, parado ou pausado). Esse método implementa o método IMediaFilter:: GetState.'
ms.assetid: d4cc7e2b-5ea5-4165-842f-becc3a81cbce
title: Método CBaseMediaFilter. GetState (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.GetState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2a4c70412311be5ea4843a823e961fae34de2974f7365f51286ff6da36e41dcb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966696"
---
# <a name="cbasemediafiltergetstate-method"></a>Método CBaseMediaFilter. GetState

O `GetState` método recupera o estado do objeto (em execução, parado ou pausado). Esse método implementa o método [**IMediaFilter:: GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetState(
   DWORD        dwMilliSecsTimeout,
   FILTER_STATE *State
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwMilliSecsTimeout* 
</dt> <dd>

Intervalo de tempo limite, em milissegundos.

</dd> <dt>

*State* 
</dt> <dd>

Ponteiro para uma variável que recebe um membro do tipo enumerado de [**\_ estado de filtro**](/windows/win32/api/strmif/ne-strmif-filter_state) , indicando o estado do objeto.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK ou o \_ ponteiro.

## <a name="remarks"></a>Comentários

Na classe base, todas as transições de estado são síncronas e o parâmetro *dwMilliSecsTimeout* é ignorado. Se uma classe derivada executar transições de estado assíncronas, ela deverá substituir esse método para aguardar durante as transições de estado, com um tempo limite de milissegundos de *dwMilliSecsTimeout* .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseMediaFilter**](cbasemediafilter.md)
</dt> </dl>

 

 




