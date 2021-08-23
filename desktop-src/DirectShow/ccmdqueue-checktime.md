---
description: O método CheckTime determina se um tempo especificado é devido.
ms.assetid: 522bc7ae-f998-4a7d-8bc3-caf09b4108a6
title: Método CCmdQueue.CheckTime (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.CheckTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 826b59d12c135e9c86ce923f37e1558dca4f13efafb4880aecab1384829a484a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910426"
---
# <a name="ccmdqueuechecktime-method"></a>Método CCmdQueue.CheckTime

O `CheckTime` método determina se um tempo especificado é devido.

## <a name="syntax"></a>Sintaxe


```C++
BOOL CheckTime(
   CRefTime time,
   BOOL     bStream
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*time* 
</dt> <dd>

Hora de verificar.

</dd> <dt>

*bStream* 
</dt> <dd>

**TRUE** se o *parâmetro time* for um valor de tempo de fluxo; **FALSE** se *time* for um valor de tempo de apresentação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **TRUE** se o tempo especificado ainda não tiver passado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CCmdQueue**](ccmdqueue.md)
</dt> </dl>

 

 




