---
description: O método Run alterna para o modo de execução para que os comandos adiados pelo tempo do fluxo possam ser executados.
ms.assetid: c529ae84-c9b7-46f1-a1e4-716fc9e9df13
title: Método CCmdQueue. Run (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 424914e53a12ff0f43e8b7e2a3345c28d84437d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758698"
---
# <a name="ccmdqueuerun-method"></a>Método CCmdQueue. Run

O `Run` método alterna para o modo de execução para que os comandos adiados pelo tempo do fluxo possam ser executados.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT Run(
   REFERENCE_TIME tStreamTimeOffset
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*tStreamTimeOffset* 
</dt> <dd>

Tempo de deslocamento.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Durante o modo de execução, o mapeamento de tempo para apresentação do fluxo é conhecido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CCmdQueue**](ccmdqueue.md)
</dt> </dl>

 

 




