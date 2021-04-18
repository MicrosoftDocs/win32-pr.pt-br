---
description: O método EndRun alterna para o modo parado ou pausado.
ms.assetid: 2c41262c-a809-4f3b-898c-02c0891dc6f8
title: Método CCmdQueue. EndRun (Winutil. h)
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
ms.openlocfilehash: 367ef026402ff191ceb04657c21d6f3bd11ebe73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755598"
---
# <a name="ccmdqueueendrun-method"></a>Método CCmdQueue. EndRun

O `EndRun` método alterna para o modo parado ou pausado.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT EndRun();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** que depende da implementação.

## <a name="remarks"></a>Comentários

O mapeamento de tempo entre a hora do fluxo e o tempo de apresentação não é conhecido depois que essa função de membro é chamada. Chame a função de membro [**CCmdQueue:: Run**](ccmdqueue-run.md) para executar esse mapeamento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CCmdQueue**](ccmdqueue.md)
</dt> </dl>

 

 




