---
description: O método SetSubtype especifica o subtipo .
ms.assetid: cf52e0dc-d75b-408e-a63c-481d55151d4a
title: Método CMediaType.SetSubtype (Mtype.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetSubtype
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 96445074ce2f0cc5a27a4988087f2fd910444beca88e5dc89c84585a8a98b338
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119566366"
---
# <a name="cmediatypesetsubtype-method"></a>Método CMediaType.SetSubtype

O `SetSubtype` método especifica o subtipo .

## <a name="syntax"></a>Sintaxe


```C++
void SetSubtype(
   const GUID *psubtype
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*psubtype* 
</dt> <dd>

Ponteiro para um **GUID** que especifica o subtipo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Mtype.h (incluir Fluxos.h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 




