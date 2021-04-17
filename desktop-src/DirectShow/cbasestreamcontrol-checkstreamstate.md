---
description: O método CheckStreamState determina se um exemplo de mídia deve ser entregue ou descartado.
ms.assetid: 1533f4b9-e13e-458b-9614-96d733cef4ed
title: Método CBaseStreamControl. CheckStreamState (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.CheckStreamState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e469e288e853ca88a0cf15c209882a8114e33509
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748213"
---
# <a name="cbasestreamcontrolcheckstreamstate-method"></a>Método CBaseStreamControl. CheckStreamState

O `CheckStreamState` método determina se um exemplo de mídia deve ser entregue ou descartado.

## <a name="syntax"></a>Sintaxe


```C++
enum CheckStreamState(
   IMediaSample *pSample
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSample* 
</dt> <dd>

Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do exemplo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos valores a seguir.



| Código de retorno                                                                                       | Descrição                     |
|---------------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <dt>**descartando o fluxo \_**</dt> </dl> | Descartar este exemplo.<br/> |
| <dl> <dt>**FLUXO \_ fluindo**</dt> </dl>    | Forneça este exemplo.<br/> |



 

## <a name="remarks"></a>Comentários

Chame esse método quando o PIN receber uma amostra. Entregue o exemplo somente se o valor de retorno for fluxo \_ fluindo. Se o valor de retorno for \_ DEScartando o fluxo, descarte o exemplo.

Se o PIN descartar quaisquer exemplos, ele deverá marcar o próximo exemplo que ele fornece como uma descontinuidade, chamando o método [**IMediaSample:: SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) .

Se o filtro implementar a interface [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes) para contar quantos quadros eles descartam, não conte um quadro Descartado como um quadro solto.

Quando o valor de retorno é \_ DEScartando o fluxo, o método é bloqueado até que o tempo de referência atinja a hora de início do exemplo. Isso impede que seu PIN descartasse amostras muito rapidamente. Se o filtro for pausado, o tempo de espera será infinito, até que o filtro seja executado, pare ou libere dados. (As alterações de estado de filtro e o streaming acontecem em threads separados, portanto, isso não causa nenhum deadlock.)

A enumeração **CBaseStreamControl:: StreamControlState** é definida da seguinte maneira:


```C++
enum StreamControlState{ 
    STREAM_FLOWING = 0x1000,
    STREAM_DISCARDING
};
```



## <a name="examples"></a>Exemplos

O exemplo a seguir pressupõe que o PIN usa uma variável de membro chamada m \_ fLastSampleDiscarded para controlar o descontinuidades.


```C++
CMyPin::Receive(IMediaSample *pSample)
{
    if (!pSample) return E_POINTER;

    int iStreamState = CheckStreamState(pSample);
    if (iStreamState == STREAM_FLOWING) 
    {
        if (m_fLastSampleDiscarded)
            pSample->SetDiscontinuity(TRUE);
        m_fLastSampleDiscarded = FALSE;
        /* Deliver the sample. */
    } 
    else 
    {
        m_fLastSampleDiscarded = TRUE;  
       // Discard this sample. Do not deliver it.
    }
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Strmctl. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseStreamControl**](cbasestreamcontrol.md)
</dt> </dl>

 

 




