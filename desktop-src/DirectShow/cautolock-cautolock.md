---
description: Método do construtor. O construtor bloqueia o objeto de seção crítico especificado.
ms.assetid: 5a0d74f9-bb99-4922-9a92-2e7c1863421f
title: Construtor CAutoLock.CAutoLock (Wxutil.h)
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
ms.openlocfilehash: 11267b444df319e339bcf13b30f200868a0f62d67712ed147513c2f8bc7d000c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017564"
---
# <a name="cautolockcautolock-constructor"></a>Construtor CAutoLock.CAutoLock

Método do construtor. O construtor bloqueia o objeto de seção crítico especificado.

## <a name="syntax"></a>Sintaxe


```C++
CAutoLock(
   CCritSec *plock
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Plock* 
</dt> <dd>

Ponteiro para um [**objeto CCritSec,**](ccritsec.md) que contém um objeto de seção crítico.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil.h (incluir Fluxos.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CAutoLock**](cautolock.md)
</dt> </dl>

 

 




