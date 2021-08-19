---
description: O método GetState recupera o estado dos filtros (em execução, parado ou em pausa). Esse método implementa o método IMediaFilter::GetState.
ms.assetid: e32e3a1d-857f-4db3-b52c-5b6b802ded42
title: Método CBaseFilter.GetState (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9b6ed61b8b1e72652e9590d11827322256d4923bd92405206e5c5419cd5e7ae5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017164"
---
# <a name="cbasefiltergetstate-method"></a>Método CBaseFilter.GetState

O `GetState` método recupera o estado dos filtros (em execução, parado ou em pausa). Esse método implementa o [**método IMediaFilter::GetState.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate)

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

Intervalo de tempo-fora, em milissegundos.

</dd> <dt>

*State* 
</dt> <dd>

Ponteiro para uma variável que recebe um membro do tipo enumerado [**FILTER \_ STATE,**](/windows/win32/api/strmif/ne-strmif-filter_state) indicando o estado do filtro.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK ou E \_ POINTER.

## <a name="remarks"></a>Comentários

Na classe base, todas as transições de estado são síncronas e *o parâmetro dwMilliSecsTimeout* é ignorado. Se uma classe derivada executar transições de estado assíncronas, ela deverá substituir esse método para aguardar durante as transições de estado, com um tempo-out de milissegundos *dwMilliSecsTimeout.*

Se o filtro não entregar dados enquanto estiver em pausa, substitua o método para retornar o valor S CANT CUE do VFW quando o filtro estiver em pausa `GetState` \_ \_ \_ (consulte [Entregando exemplos).](delivering-samples.md) Por exemplo:


```C++
CMyFilter::GetState(DWORD dw, FILTER_STATE *pState)
{
    CheckPointer(pState, E_POINTER);
    *pState = m_State;
    if (m_State == State_Paused)
        return VFW_S_CANT_CUE;
    else
        return S_OK;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




