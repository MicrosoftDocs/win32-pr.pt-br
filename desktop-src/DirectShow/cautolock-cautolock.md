---
description: Método de construtor. O Construtor bloqueia o objeto de seção crítica especificado.
ms.assetid: 5a0d74f9-bb99-4922-9a92-2e7c1863421f
title: Construtor CAutoLock. CAutoLock (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoLock.CAutoLock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fed29011d4fe581ed146f64800351a3f1053d957
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778653"
---
# <a name="cautolockcautolock-constructor"></a>Construtor CAutoLock. CAutoLock

Método de construtor. O Construtor bloqueia o objeto de seção crítica especificado.

## <a name="syntax"></a>Sintaxe


```C++
CAutoLock(
   CCritSec *plock
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*plock* 
</dt> <dd>

Ponteiro para um objeto [**CCritSec**](ccritsec.md) , que contém um objeto de seção crítica.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CAutoLock**](cautolock.md)
</dt> </dl>

 

 




