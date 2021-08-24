---
description: O método SetActualDataLength define o comprimento dos dados válidos no buffer. Esse método implementa o método IMediaSample::SetActualDataLength.
ms.assetid: a80a67ef-e490-4874-a123-f2d193cec4d7
title: Método CMediaSample.SetActualDataLength (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetActualDataLength
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: db090ad96f6c53f725aef7864e729b8083bfd1a02b30f0d699d30b5c6f8f71aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634366"
---
# <a name="cmediasamplesetactualdatalength-method"></a>Método CMediaSample.SetActualDataLength

O `SetActualDataLength` método define o comprimento dos dados válidos no buffer. Esse método implementa o [**método IMediaSample::SetActualDataLength.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setactualdatalength)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetActualDataLength(
   long lLen
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lLen* 
</dt> <dd>

Comprimento dos dados válidos, em bytes.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos **valores HRESULT** mostrados na tabela a seguir.



| Código de retorno                                                                                             | Descrição                                                 |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                    | Êxito.<br/>                                         |
| <dl> <dt>**ESTOURO DE BUFFER DO VFW \_ E \_ \_**</dt> </dl> | *lLen* é maior que o tamanho do buffer alocado.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método define a [**variável de membro CMediaSample::m \_ lActual.**](cmediasample-m-lactual.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




