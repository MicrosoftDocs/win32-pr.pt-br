---
description: 'O método InitialThreadProc chama o método COutputQueue:: ThreadProc quando o thread é criado.'
ms.assetid: 6093f0c3-ec58-418d-bb8c-618163c43ac7
title: COutputQueue.Inimétodo tialThreadProc (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.InitialThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dfc7b8660d838b6ad31dd298c509b6282ab61810
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105786983"
---
# <a name="coutputqueueinitialthreadproc-method"></a>COutputQueue.Inimétodo tialThreadProc

O `InitialThreadProc` método chama o método [**COutputQueue:: ThreadProc**](coutputqueue-threadproc.md) quando o thread é criado.

## <a name="syntax"></a>Sintaxe


```C++
static DWORD WINAPI InitialThreadProc(
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

Retorna o valor retornado pelo método [**COutputQueue:: ThreadProc**](coutputqueue-threadproc.md) .

## <a name="remarks"></a>Comentários

Esse método é o procedimento de thread para o thread de trabalho do objeto. O ponteiro do objeto `this` é o parâmetro de thread. O método faz referência a isso para chamar **ThreadProc**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Outputq. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




