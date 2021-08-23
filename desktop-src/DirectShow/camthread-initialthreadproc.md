---
description: O método InitialThreadProc chama o procedimento de thread principal.
ms.assetid: 1546c214-7ea9-4484-974b-dbd4b2b3e296
title: CAMThread.Inimétodo tialThreadProc (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.InitialThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d12e8d41ac0c6e1fd2af06c21accbb5c62e4eb25f2fc3f6c36988101a9b64d89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540296"
---
# <a name="camthreadinitialthreadproc-method"></a>CAMThread.Inimétodo tialThreadProc

O `InitialThreadProc` método chama o procedimento de thread principal.

## <a name="syntax"></a>Sintaxe


```C++
DWORD InitialThreadProc(
   LPVOID pv
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Pv* 
</dt> <dd>

`this` Ponteiro.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o **DWORD** retornado por [**CAMThread::ThreadProc.**](camthread-threadproc.md) A classe derivada define esse valor.

## <a name="remarks"></a>Comentários

O [**método CAMThread::Create**](camthread-create.md) usa esse método para o procedimento de thread quando ele cria o thread. Ele usa o `this` ponteiro como o argumento de thread.

Esse método chama o [**método CAMThread::CoInitializeHelper**](camthread-coinitializehelper.md) e, em seguida, ThreadProc.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil.h (incluir Fluxos.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CAMThread**](camthread.md)
</dt> </dl>

 

 




