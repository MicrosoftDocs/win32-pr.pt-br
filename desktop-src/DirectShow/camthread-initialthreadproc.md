---
description: O método InitialThreadProc chama o procedimento de thread principal.
ms.assetid: 1546c214-7ea9-4484-974b-dbd4b2b3e296
title: CAMThread.Inimétodo tialThreadProc (Wxutil. h)
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
ms.openlocfilehash: cd7fd0aa12d0659776db7e39fb223095762fc209
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757049"
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

*PV* 
</dt> <dd>

`this` refere.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o **DWORD** retornado por [**CAMThread:: ThreadProc**](camthread-threadproc.md). A classe derivada define esse valor.

## <a name="remarks"></a>Comentários

O método [**CAMThread:: Create**](camthread-create.md) usa esse método para o procedimento de thread quando ele cria o thread. Ele usa o `this` ponteiro como o argumento de thread.

Esse método chama o método [**CAMThread:: CoInitializeHelper**](camthread-coinitializehelper.md) e, em seguida, ThreadProc.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CAMThread**](camthread.md)
</dt> </dl>

 

 




