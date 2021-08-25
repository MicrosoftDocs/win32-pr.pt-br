---
description: Altera o sinalizador sujo para o fluxo atual.
ms.assetid: 65fa7fbe-4fa7-45a3-91a4-4a3547b035b9
title: Método CPersistStream.SetDirty (Pstream.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.SetDirty
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 31a00de873f33cedd1451ebebd0ec21f1dfaa83690923712d867ec4a8d34d502
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909296"
---
# <a name="cpersiststreamsetdirty-method"></a>Método CPersistStream.SetDirty

Altera o sinalizador sujo para o fluxo atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetDirty(
   BOOL fDirty
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*fDirty* 
</dt> <dd>

Novo sinalizador sujo para esse fluxo. **TRUE** significa que os dados não foram salvos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Pstream.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CPersistStream**](cpersiststream.md)
</dt> </dl>

 

 




