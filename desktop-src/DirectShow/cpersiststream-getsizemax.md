---
description: Recupera o tamanho máximo de byte necessário para o fluxo atual, incluindo o número de versão.
ms.assetid: 55ea4568-5ca4-4139-8def-bef20071835d
title: Método CPersistStream.GetSizeMax (Pstream.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.GetSizeMax
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 746fb01102642f2d3e6b254ac741c284143aaecfd401fc220bf7a9d97d93e64e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813366"
---
# <a name="cpersiststreamgetsizemax-method"></a>Método CPersistStream.GetSizeMax

Recupera o tamanho máximo de byte necessário para o fluxo atual, incluindo o número de versão.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetSizeMax(
   ULARGE_INTEGER *pcbSize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pcbSize* 
</dt> <dd>

Ponteiro para o tamanho em bytes necessários para salvar esse fluxo, incluindo o número de versão.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.**

## <a name="remarks"></a>Comentários

Essa função membro implementa o **método IPersistStream::GetSizeMax.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Pstream.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CPersistStream**](cpersiststream.md)
</dt> </dl>

 

 




