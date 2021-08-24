---
description: Enfileiro uma solicitação de execução pelo thread de trabalho.
ms.assetid: a854f962-143d-4776-bf98-119d003867df
title: Método CMsgThread.PutThreadMsg (Msgthrd.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.PutThreadMsg
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7eefa95c4fd6ab19c895b4d1d47dba3a19302023985a4631708c3cf7ccc10d06
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119585636"
---
# <a name="cmsgthreadputthreadmsg-method"></a>Método CMsgThread.PutThreadMsg

Enfileiro uma solicitação de execução pelo thread de trabalho.

## <a name="syntax"></a>Sintaxe


```C++
void PutThreadMsg(
   UINT     uMsg,
   DWORD    dwMsgFlags,
   LPVOID   lpMsgParam,
   CAMEvent *pEvent = NULL
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Umsg* 
</dt> <dd>

Solicitar código.

</dd> <dt>

*dwMsgFlags* 
</dt> <dd>

Parâmetro de sinalizadores opcional.

</dd> <dt>

*lpMsgParam* 
</dt> <dd>

Ponteiro opcional para um bloco de dados que contém parâmetros adicionais ou valores de retorno. Deve ser estaticamente ou alocado em heap e não automático.

</dd> <dt>

*pEvent* 
</dt> <dd>

Ponteiro opcional para um objeto de evento a ser sinalizado após a conclusão.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Essa função membro enfileiro uma solicitação de execução pelo thread de trabalho. Os parâmetros dessa função membro serão enxuados (em um objeto [**CMsg)**](cmsg.md) e passados para a função de membro [**CMsgThread::ThreadMessageProc**](cmsgthread-threadmessageproc.md) do thread de trabalho. Essa função membro retorna imediatamente após a fila da solicitação e não aguarda o thread atender à solicitação. A **função membro CMsgThread::ThreadMessageProc** da classe derivada define os quatro parâmetros.

Essa função membro usa uma lista segura multithread, portanto, várias chamadas para essa função membro de threads diferentes podem ser feitas com segurança.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Msgthrd.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMsgThread**](cmsgthread.md)
</dt> </dl>

 

 




