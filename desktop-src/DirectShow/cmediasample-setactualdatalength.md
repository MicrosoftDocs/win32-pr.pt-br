---
description: 'O método SetActualDataLength define o comprimento dos dados válidos no buffer. Esse método implementa o método IMediaSample:: SetActualDataLength.'
ms.assetid: a80a67ef-e490-4874-a123-f2d193cec4d7
title: Método CMediaSample. SetActualDataLength (Amfilter. h)
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
ms.openlocfilehash: 825b02f43195424f9ceb5ecd23c4dcf26727ef8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811327"
---
# <a name="cmediasamplesetactualdatalength-method"></a>Método CMediaSample. SetActualDataLength

O `SetActualDataLength` método define o comprimento dos dados válidos no buffer. Esse método implementa o método [**IMediaSample:: SetActualDataLength**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setactualdatalength) .

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

## <a name="return-value"></a>Retornar valor

Retorna um dos valores **HRESULT** mostrados na tabela a seguir.



| Código de retorno                                                                                             | Descrição                                                 |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                    | Êxito.<br/>                                         |
| <dl> <dt>**\_estouro de \_ buffer VFW E \_**</dt> </dl> | *llen* é maior do que o tamanho do buffer alocado.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método define a variável de membro [**CMediaSample:: m \_ lActual**](cmediasample-m-lactual.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




