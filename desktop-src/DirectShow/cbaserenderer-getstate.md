---
description: O método GetState recupera o estado do filtro (em execução, parado ou pausado).
ms.assetid: 5d35824c-2509-499a-bbb1-1fb916b51808
title: Método CBaseRenderer. GetState (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 451078a6167ff7ca89ad4153c416826af8ac6d05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769240"
---
# <a name="cbaserenderergetstate-method"></a>Método CBaseRenderer. GetState

O `GetState` método recupera o estado do filtro (em execução, parado ou pausado).

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

Ponteiro para uma variável que recebe um membro do tipo enumerado de [**\_ estado de filtro**](/windows/win32/api/strmif/ne-strmif-filter_state) , indicando o estado do filtro.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos valores **HRESULT** mostrados na tabela a seguir.



| Código de retorno                                                                                                | Descrição                                                    |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Êxito.<br/>                                            |
| <dl> <dt>**VFW \_ S \_ State \_ intermediário**</dt> </dl> | O filtro está em transição para o estado indicado.<br/> |
| <dl> <dt>**\_ponteiro E**</dt> </dl>                  | Argumento de ponteiro **nulo** .<br/>                          |



 

## <a name="remarks"></a>Comentários

Esse método substitui o método [**CBaseFilter:: GetState**](cbasefilter-getstate.md) . Quando o renderizador é pausado, ele não conclui a transição de estado até receber um exemplo para renderizar. Se o tempo limite expirar antes da conclusão da transição de estado, o método retornará VFW \_ S \_ State \_ intermediário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




