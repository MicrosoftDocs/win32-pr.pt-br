---
description: O método ThreadProc é o procedimento de thread para o thread de trabalho. Esse método implementa o método CAMThread::ThreadProc virtual puro.
ms.assetid: 8e66b609-d795-45a8-8fe5-774c659ee350
title: Método CSourceStream.ThreadProc (Source.h)
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
ms.openlocfilehash: 10ef0d29ab46ada118dc97c2d767b8377556086b949b6b9969cf5671b51e5359
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915266"
---
# <a name="csourcestreamthreadproc-method"></a>Método CSourceStream.ThreadProc

O `ThreadProc` método é o procedimento de thread para o thread de trabalho. Esse método implementa o método [**CAMThread::ThreadProc**](camthread-threadproc.md) virtual puro.

## <a name="syntax"></a>Sintaxe


```C++
virtual DWORD ThreadProc();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retornará 0 se o thread for concluído com êxito ou 1 caso contrário. Se o valor de retorno for 1, os recursos do thread ainda poderão ser alocados.

## <a name="remarks"></a>Comentários

Esse método aguarda indefinidamente por solicitações de thread chamando o [**método CAMThread::GetRequest.**](camthread-getrequest.md) Se ele receber uma solicitação [**CSourceStream::Run**](csourcestream-run.md) ou [**CSourceStream::P ause,**](csourcestream-pause.md) ele chamará o [**método CSourceStream::D oBufferProcessingLoop.**](csourcestream-dobufferprocessingloop.md) O **método DoBufferProcessingLoop esboça** push de dados até receber uma [**solicitação CSourceStream::Stop.**](csourcestream-stop.md) O procedimento de thread é final ao receber uma [**solicitação CSourceStream::Exit.**](csourcestream-exit.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Source.h (incluir Fluxos.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




