---
description: 'Usa a função ResumeThread do Microsoft Win32 para continuar a operação do thread de trabalho após uma chamada anterior para a função de membro CMsgThread:: SuspendThread.'
ms.assetid: 5c94a079-5c74-4024-8fb0-71c7ef9c7e73
title: Método CMsgThread. ResumeThread (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.ResumeThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e0a20bb60f4a10a06ef50f58c449496cae8050d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759312"
---
# <a name="cmsgthreadresumethread-method"></a>Método CMsgThread. ResumeThread

Usa a função **ResumeThread** do Microsoft Win32 para continuar a operação do thread de trabalho após uma chamada anterior para a função de membro [**CMsgThread:: SuspendThread**](cmsgthread-suspendthread.md) .

## <a name="syntax"></a>Sintaxe


```C++
DWORD ResumeThread();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Se a função de membro for realizada com sucesso, o valor de retorno será a contagem de suspensão anterior do thread. Se a função de membro falhar, o valor de retorno será 0xFFFFFFFF. Para obter informações de erro estendidas, chame a função **GetLastError** do Microsoft Win32.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Msgthrd. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMsgThread**](cmsgthread.md)
</dt> </dl>

 

 




