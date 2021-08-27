---
description: O método NotifyFilterState notifica o pino quando o estado do filtro muda.
ms.assetid: 0eb3b0e5-9c44-464e-b4ca-bcded731e813
title: Método CBaseStreamControl.NotifyFilterState (Strmctl.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.NotifyFilterState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a3433e5c40f86a9e333696774fe671eb7bb90d9803cb9cd6501d7971111e5d36
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131416"
---
# <a name="cbasestreamcontrolnotifyfilterstate-method"></a>Método CBaseStreamControl.NotifyFilterState

O `NotifyFilterState` método notifica o pino quando o estado do filtro muda.

## <a name="syntax"></a>Sintaxe


```C++
void NotifyFilterState(
   FILTER_STATE   new_state,
   REFERENCE_TIME tStart = 0
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*novo \_ estado* 
</dt> <dd>

Especifica o novo estado, como um membro da [**enumeração FILTER \_ STATE.**](/windows/win32/api/strmif/ne-strmif-filter_state)

</dd> <dt>

*Tstart* 
</dt> <dd>

Especifica a hora de início. Se o novo estado do filtro for State \_ Running, passe o valor do [**método IMediaFilter::Run.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) Caso contrário, use o valor padrão.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método faz com que [**o método CBaseStreamControl::CheckStreamState**](cbasestreamcontrol-checkstreamstate.md) pare de esperar. Chame esse método sempre que o filtro de propriedade mudar de estado.

## <a name="examples"></a>Exemplos


```C++
STDMETHODIMP CMyFilter::Run(REFERENCE_TIME tStart)
{
   /* Do other things needed by the filter ... */
   m_pMyPin->NotifyFilterState(State_Running, tStart);
   return CBaseFilter::Run(tStart); // Call the filter base class.
}

STDMETHODIMP CMyFilter::Pause()
{
   /* Do other things needed by the filter ... */
   m_pMyPin->NotifyFilterState(State_Paused);
   return CBaseFilter::Pause();
}

STDMETHODIMP CMyFilter::Stop()
{
   /* Do other things needed by the filter ... */
   m_pMyPin->NotifyFilterState(State_Stopped);
   return CBaseFilter::Stop();
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Strmctl.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseStreamControl**](cbasestreamcontrol.md)
</dt> </dl>

 

 




