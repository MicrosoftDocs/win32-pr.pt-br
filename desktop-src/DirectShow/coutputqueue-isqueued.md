---
description: O método IsQueued determina se o objeto está usando um thread de trabalho para fornecer amostras.
ms.assetid: 8d26661f-6cd7-42ea-bc4b-8746d22a7ca0
title: Método COutputQueue.IsQueued (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.IsQueued
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5e261127e16cd1190fb711d81a9f5fd5606738b7f9a3f8697902170662b99f04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813576"
---
# <a name="coutputqueueisqueued-method"></a>Método COutputQueue.IsQueued

O `IsQueued` método determina se o objeto está usando um thread de trabalho para fornecer amostras.

## <a name="syntax"></a>Sintaxe


```C++
BOOL IsQueued();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retornará **TRUE** se o objeto estiver usando um thread de trabalho ou **FALSE** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Outputq.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




