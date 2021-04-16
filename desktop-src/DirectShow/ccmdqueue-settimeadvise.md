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
ms.openlocfilehash: 24313b908f1271f270e28b08058c415ed82396fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768667"
---
# <a name="ccmdqueuesettimeadvise-method"></a>Método CCmdQueue. SetTimeAdvise

O `SetTimeAdvise` método configura um evento de temporizador com o relógio de referência.

## <a name="syntax"></a>Sintaxe


```C++
void SetTimeAdvise();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Essa função de membro chama o método [**IReferenceClock:: aconselhetime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) para configurar uma notificação para a hora mais antiga necessária na fila. Os comandos de tempo de apresentação que são adiados sempre são verificados. Se o gráfico de filtro estiver no modo de execução, os comandos adiados usando o tempo de transmissão também serão verificados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CCmdQueue**](ccmdqueue.md)
</dt> </dl>

 

 




