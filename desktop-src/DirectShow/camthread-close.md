---
description: O método Close aguarda até que o thread saia e, em seguida, libera seus recursos.
ms.assetid: 57e27ff7-3665-416e-8a6e-660483c5aed2
title: Método CAMThread. Close (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.Close
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9cac5ee4a1e1a9cc3fecc8d09096d031e9fc9a63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760286"
---
# <a name="camthreadclose-method"></a>Método CAMThread. Close

O `Close` método aguarda até que o thread saia e, em seguida, libera seus recursos.

## <a name="syntax"></a>Sintaxe


```C++
void Close();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Antes de chamar esse método, você deve fornecer uma maneira para o thread sair. Por exemplo, no método [**CAMThread:: ThreadProc**](camthread-threadproc.md) , defina uma solicitação que sinaliza o thread para sair. Em seguida, chame o método [**CAMThread:: CallWorker**](camthread-callworker.md) com esse valor.

O método destruidor [**~ CAMThread**](camthread--camthread.md) chama esse método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CAMThread**](camthread.md)
</dt> </dl>

 

 




