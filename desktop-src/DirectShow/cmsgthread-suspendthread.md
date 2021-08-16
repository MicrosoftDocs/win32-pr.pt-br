---
description: Usa a função SuspendThread do Microsoft Win32 para suspender a operação de um thread em execução.
ms.assetid: 07d919a2-797d-47c3-83e3-c8e2d2b2cddd
title: Método CMsgThread.SuspendThread (Msgthrd.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.SuspendThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f5242c8708c07beb85d297dff706dbe192f59f1f7b46b05eba7362c9f0182d52
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915736"
---
# <a name="cmsgthreadsuspendthread-method"></a>Método CMsgThread.SuspendThread

Usa a função **SuspendThread** do Microsoft Win32 para suspender a operação de um thread em execução.

## <a name="syntax"></a>Sintaxe


```C++
DWORD SuspendThread();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Se a função membro for bem-sucedida, o valor de retorno será a contagem de suspensão anterior do thread. Se a função membro falhar, o valor de retorno será 0xFFFFFFFF. Para obter informações de erro estendidas, chame a função **GetLastError** do Microsoft Win32.

## <a name="remarks"></a>Comentários

O thread do cliente chama essa função de membro para suspender a operação do thread de trabalho. O thread de trabalho permanece suspenso e não será executado até que uma chamada adicional para a função membro [**CMsgThread::ResumeThread**](cmsgthread-resumethread.md) seja feita.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Msgthrd.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMsgThread**](cmsgthread.md)
</dt> </dl>

 

 




