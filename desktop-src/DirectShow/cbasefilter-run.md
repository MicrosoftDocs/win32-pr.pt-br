---
description: O método Run executa o filtro. Esse método implementa o método IMediaFilter::Run.
ms.assetid: fab2cef7-cad1-4933-92a4-5f41cd947c2f
title: Método CBaseFilter.Run (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6259e6ce00b0a2f93e0b71d6b44d1c6ed4aa65eaadca21ed0a78f1d16d98a42b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793276"
---
# <a name="cbasefilterrun-method"></a>Método CBaseFilter.Run

O `Run` método executa o filtro. Esse método implementa o [**método IMediaFilter::Run.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Run(
   REFERENCE_TIME tStart
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Tstart* 
</dt> <dd>

Tempo de referência correspondente ao tempo de fluxo 0.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK se bem-sucedido ou **um valor HRESULT** que indica a causa do erro.

## <a name="remarks"></a>Comentários

Se o filtro for interrompido, esse método pausará o filtro chamando o [**método CBaseFilter::P ause.**](cbasefilter-pause.md) Em seguida, ele [**chama o método CBasePin::Run**](cbasepin-run.md) em cada um dos pinos conectados do filtro. Por fim, ele define a variável membro de estado [**CBaseFilter::m \_**](cbasefilter-m-state.md) como State \_ Running.

O tempo de fluxo é calculado como a hora de referência atual menos *tStart*. Um exemplo de mídia com um carimbo de data/hora de zero deve ser renderizado no momento *tStart*.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




