---
description: 'O método Run executa o filtro. Esse método implementa o método IMediaFilter:: Run.'
ms.assetid: fab2cef7-cad1-4933-92a4-5f41cd947c2f
title: Método CBaseFilter. Run (Amfilter. h)
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
ms.openlocfilehash: 0555733f53b4870a43dbcbf36c69061db19490a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749037"
---
# <a name="cbasefilterrun-method"></a>Método CBaseFilter. Run

O `Run` método executa o filtro. Esse método implementa o método [**IMediaFilter:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Run(
   REFERENCE_TIME tStart
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*tStart* 
</dt> <dd>

Tempo de referência correspondente ao tempo de transmissão 0.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK se bem-sucedido ou um valor **HRESULT** que indica a causa do erro.

## <a name="remarks"></a>Comentários

Se o filtro for interrompido, esse método pausará o filtro chamando o método [**CBaseFilter::P ause**](cbasefilter-pause.md) . Em seguida, ele chama o método [**CBasePin:: Run**](cbasepin-run.md) em cada um dos Pins conectados do filtro. Por fim, ele define a variável de membro de [**\_ estado CBaseFilter:: m**](cbasefilter-m-state.md) para o estado \_ em execução.

O tempo de fluxo é calculado como o tempo de referência atual menos *tStart*. Um exemplo de mídia com um carimbo de data/hora igual a zero deve ser renderizado no horário *tStart*.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




