---
description: O método Wait é bloqueado até que o evento seja sinalizado ou até que ocorra um tempo limite.
ms.assetid: bcc13723-a59b-4e8a-bfc8-eadb6facf116
title: Método CAMEvent. Wait (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.Wait
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0ab5bc2aabf77fb73739528e99cda7961ae87e9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752116"
---
# <a name="cameventwait-method"></a>Método CAMEvent. Wait

O `Wait` método é bloqueado até que o evento seja sinalizado ou até que ocorra um tempo limite.

## <a name="syntax"></a>Sintaxe


```C++
BOOL Wait(
   DWORD dwTimeout = INFINITE
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwTimeout* 
</dt> <dd>

Valor de tempo limite opcional, representado em milissegundos.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará **true** se o evento for sinalizado. Caso contrário, retornará **false**.

## <a name="remarks"></a>Comentários

Para eventos de redefinição automática, o evento é redefinido para um estado não sinalizado quando esse método retorna.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CAMEvent**](camevent.md)
</dt> </dl>

 

 




