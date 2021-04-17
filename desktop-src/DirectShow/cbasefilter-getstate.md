---
description: 'O método GetState recupera o estado do filtro (em execução, parado ou pausado). Esse método implementa o método IMediaFilter:: GetState.'
ms.assetid: e32e3a1d-857f-4db3-b52c-5b6b802ded42
title: Método CBaseFilter. GetState (Amfilter. h)
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
ms.openlocfilehash: 0c9470e5d71bf71f4e37e6eef84015becdf05f65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749042"
---
# <a name="cbasefiltergetstate-method"></a>Método CBaseFilter. GetState

O `GetState` método recupera o estado do filtro (em execução, parado ou pausado). Esse método implementa o método [**IMediaFilter:: GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) .

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

Retorna S \_ OK ou o \_ ponteiro.

## <a name="remarks"></a>Comentários

Na classe base, todas as transições de estado são síncronas e o parâmetro *dwMilliSecsTimeout* é ignorado. Se uma classe derivada executar transições de estado assíncronas, ela deverá substituir esse método para aguardar durante as transições de estado, com um tempo limite de milissegundos de *dwMilliSecsTimeout* .

Se o filtro não entregar dados enquanto estiver em pausa, substitua o `GetState` método para retornar o valor VFW \_ S \_ \_ não consegue se marcar quando o filtro está em pausa (consulte [entregando exemplos](delivering-samples.md)). Por exemplo:


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
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




