---
description: Usa a função SuspendThread do Microsoft Win32 para suspender a operação de um thread em execução.
ms.assetid: 07d919a2-797d-47c3-83e3-c8e2d2b2cddd
title: Método CMsgThread. SuspendThread (Msgthrd. h)
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
ms.openlocfilehash: 69190015104d712864965e757d82afbdcc852884
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770281"
---
# <a name="cmsgthreadsuspendthread-method"></a>Método CMsgThread. SuspendThread

Usa a função **SuspendThread** do Microsoft Win32 para suspender a operação de um thread em execução.

## <a name="syntax"></a>Sintaxe


```C++
DWORD SuspendThread();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Se a função de membro for realizada com sucesso, o valor de retorno será a contagem de suspensão anterior do thread. Se a função de membro falhar, o valor de retorno será 0xFFFFFFFF. Para obter informações de erro estendidas, chame a função **GetLastError** do Microsoft Win32.

## <a name="remarks"></a>Comentários

O thread do cliente chama essa função de membro para suspender a operação do thread de trabalho. O thread de trabalho permanece suspenso e não será executado até que uma chamada adicional para a função de membro [**CMsgThread:: ResumeThread**](cmsgthread-resumethread.md) seja feita.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Msgthrd. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMsgThread**](cmsgthread.md)
</dt> </dl>

 

 




