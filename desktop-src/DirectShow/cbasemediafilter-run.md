---
description: 'O método Run executa o objeto. Esse método implementa o método IMediaFilter:: Run.'
ms.assetid: a59180df-46b4-4c23-973f-2931d95ace55
title: Método CBaseMediaFilter. Run (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8c4023be7731f9bae60576bc7002010eb0b51823
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749635"
---
# <a name="cbasemediafilterrun-method"></a>Método CBaseMediaFilter. Run

O `Run` método executa o objeto. Esse método implementa o método [**IMediaFilter:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) .

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

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Se o objeto for interrompido, esse método pausará o objeto chamando o método [**CBaseMediaFilter::P ause**](cbasemediafilter-pause.md) . Em seguida, ele define a variável de membro de [**\_ estado CBaseMediaFilter:: m**](cbasemediafilter-m-state.md) para o estado \_ em execução.

O tempo de fluxo é calculado como o tempo de referência atual menos *tStart*. Um exemplo de mídia com um carimbo de data/hora igual a zero deve ser renderizado no horário *tStart*.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseMediaFilter**](cbasemediafilter.md)
</dt> </dl>

 

 




