---
description: Carrega os dados do filtro de um determinado fluxo.
ms.assetid: c2bfd379-2916-4698-bc41-653161723706
title: Método CPersistStream.Load (Pstream.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.Load
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d65ff2d2ba95f66e6153aa78a9ce376ed144ac24ce8945c1fbc678e9f6894802
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813346"
---
# <a name="cpersiststreamload-method"></a>Método CPersistStream.Load

Carrega os dados do filtro de um determinado fluxo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Load(
   LPSTREAM pStm
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pStm* 
</dt> <dd>

Ponteiro para o fluxo do qual será carregado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.**

## <a name="remarks"></a>Comentários

Essa função membro implementa o **método IPersistStream::Load.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Pstream.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CPersistStream**](cpersiststream.md)
</dt> </dl>

 

 




