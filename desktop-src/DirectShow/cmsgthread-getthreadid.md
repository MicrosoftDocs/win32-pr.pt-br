---
description: Recupera o identificador do thread.
ms.assetid: c2b25342-841a-46cb-862c-01761fc60363
title: Método CMsgThread.GetThreadID (Msgthrd.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.GetThreadID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f3b0837a7f050f09794b06e490f45012e0704e187b02668cd2af2a5bf8edf34
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119214095"
---
# <a name="cmsgthreadgetthreadid-method"></a>Método CMsgThread.GetThreadID

Recupera o identificador do thread.

## <a name="syntax"></a>Sintaxe


```C++
DWORD GetThreadID();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna o membro de dados privados **\_ m ThreadId.**

## <a name="remarks"></a>Comentários

Essa função retorna o identificador do Microsoft Win32 para o thread de trabalho. Você pode chamar essa função de membro no thread de trabalho ou em um thread de cliente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Msgthrd.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMsgThread**](cmsgthread.md)
</dt> </dl>

 

 




