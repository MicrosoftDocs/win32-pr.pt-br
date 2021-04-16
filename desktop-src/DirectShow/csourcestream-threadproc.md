---
description: 'O método ThreadProc é o procedimento de thread para o thread de trabalho. Esse método implementa o método puramente virtual CAMThread:: ThreadProc.'
ms.assetid: 8e66b609-d795-45a8-8fe5-774c659ee350
title: Método CSourceStream. ThreadProc (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.ThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6dc7d08643cc0ca76d3d05f0b9090f30200eb181
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757688"
---
# <a name="csourcestreamthreadproc-method"></a>Método CSourceStream. ThreadProc

O `ThreadProc` método é o procedimento de thread para o thread de trabalho. Esse método implementa o método puramente virtual [**CAMThread:: ThreadProc**](camthread-threadproc.md) .

## <a name="syntax"></a>Sintaxe


```C++
virtual DWORD ThreadProc();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retornará 0 se o thread tiver sido concluído com êxito ou 1 caso contrário. Se o valor de retorno for 1, os recursos do thread ainda poderão ser alocados.

## <a name="remarks"></a>Comentários

Esse método aguarda indefinidamente as solicitações de thread, chamando o método [**CAMThread:: GetRequest**](camthread-getrequest.md) . Se receber uma solicitação [**CSourceStream:: Run**](csourcestream-run.md) ou [**CSourceStream::P ause**](csourcestream-pause.md) , ele chamará o método [**CSourceStream::D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) . O método **DoBufferProcessingLoop** envia dados por push até receber uma solicitação [**CSourceStream:: Stop**](csourcestream-stop.md) . O procedimento de thread é encerrado quando recebe uma solicitação [**CSourceStream:: Exit**](csourcestream-exit.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Source. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




