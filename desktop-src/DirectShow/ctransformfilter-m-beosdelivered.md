---
description: Sinalizador que indica se o filtro enviou uma notificação de fim de fluxo.
ms.assetid: 93f897de-04bb-4de4-a612-39b27c7d6f6c
title: 'Membro CTransformFilter:: m_bEOSDelivered (Transfrm. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bEOSDelivered
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f24b87f9808c53b5f64f66031a8ee2a4e9449089
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747373"
---
# <a name="ctransformfilterm_beosdelivered-member"></a>Membro de CTransformFilter:: m \_ bEOSDelivered

Sinalizador que indica se o filtro enviou uma notificação de fim de fluxo.

## <a name="syntax"></a>Sintaxe


```C++
BOOL m_bEOSDelivered;
```



## <a name="remarks"></a>Comentários

Se o filtro for pausado quando não tiver uma conexão de entrada, ele enviará um downstream de notificação de fim de fluxo e definirá esse sinalizador como **true**. A notificação de fim de fluxo garante que o filtro downstream não espere por exemplos. Observe que o método [**EndOfStream**](ctransformfilter-endofstream.md) do filtro não define esse sinalizador.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




