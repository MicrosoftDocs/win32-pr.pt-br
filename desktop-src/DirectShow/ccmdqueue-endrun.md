---
description: O método EndRun alterna para o modo parado ou em pausa.
ms.assetid: 2c41262c-a809-4f3b-898c-02c0891dc6f8
title: Método CCmdQueue.EndRun (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.EndRun
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2c5a20917c82ba26c941b063941e8667a3a30adce15176aed52362140a15ce90
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757356"
---
# <a name="ccmdqueueendrun-method"></a>Método CCmdQueue.EndRun

O `EndRun` método alterna para o modo parado ou em pausa.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT EndRun();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT** que depende da implementação.

## <a name="remarks"></a>Comentários

O mapeamento de tempo entre a hora do fluxo e o tempo de apresentação não é conhecido depois que essa função membro é chamada. Chame a [**função membro CCmdQueue::Run**](ccmdqueue-run.md) para executar esse mapeamento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CCmdQueue**](ccmdqueue.md)
</dt> </dl>

 

 




