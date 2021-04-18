---
description: O método CheckRequest verifica se há uma solicitação de thread, sem bloqueio.
ms.assetid: b4691dde-abec-4671-bea6-0f22cc4e7c61
title: Método CSourceStream. CheckRequest (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.CheckRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3100d449d2f29b2080541c5968cad6abc5643b26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768795"
---
# <a name="csourcestreamcheckrequest-method"></a>Método CSourceStream. CheckRequest

O `CheckRequest` método verifica se há uma solicitação de thread, sem bloqueio.

## <a name="syntax"></a>Sintaxe


```C++
BOOL CheckRequest(
   Command *pCom
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pCom* 
</dt> <dd>

Ponteiro para uma variável que recebe o valor passado na última chamada para o método [**CAMThread:: CallWorker**](camthread-callworker.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **true** se houver uma solicitação pendente ou **false** caso contrário.

## <a name="remarks"></a>Comentários

Esse método substitui o método [**CAMThread:: CheckRequest**](camthread-checkrequest.md) para executar a verificação de tipo. A classe **CSourceStream** define o seguinte tipo enumerado para o parâmetro *Pcom* :


```C++
enum Command {CMD_INIT, CMD_PAUSE, CMD_RUN, CMD_STOP, CMD_EXIT};
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Source. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




