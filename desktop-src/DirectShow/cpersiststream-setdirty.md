---
description: Altera o sinalizador sujo para o fluxo atual.
ms.assetid: 65fa7fbe-4fa7-45a3-91a4-4a3547b035b9
title: Método CPersistStream. SetDirty (pStream. h)
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
ms.openlocfilehash: 382b74f6314beb586b1e51c02a257cad8904c188
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759306"
---
# <a name="cpersiststreamsetdirty-method"></a>Método CPersistStream. SetDirty

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

Novo sinalizador sujo para este fluxo. **Verdadeiro** significa que os dados não foram salvos.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PStream. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CPersistStream**](cpersiststream.md)
</dt> </dl>

 

 




