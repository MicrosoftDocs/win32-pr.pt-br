---
description: O método SetTimeAdvise configura um evento de temporizador com o relógio de referência.
ms.assetid: d0ab5c21-3585-413b-ba75-8591ed4527e4
title: Método CCmdQueue. SetTimeAdvise (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.SetTimeAdvise
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ecfa02354ad3662a6fd9060fff80b74635c63ade57539fbbd1307fa1d65e8872
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757126"
---
# <a name="ccmdqueuesettimeadvise-method"></a>Método CCmdQueue. SetTimeAdvise

O `SetTimeAdvise` método configura um evento de temporizador com o relógio de referência.

## <a name="syntax"></a>Sintaxe


```C++
void SetTimeAdvise();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Essa função de membro chama o método [**IReferenceClock:: aconselhetime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) para configurar uma notificação para a hora mais antiga necessária na fila. Os comandos de tempo de apresentação que são adiados sempre são verificados. Se o gráfico de filtro estiver no modo de execução, os comandos adiados usando o tempo de transmissão também serão verificados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CCmdQueue**](ccmdqueue.md)
</dt> </dl>

 

 




