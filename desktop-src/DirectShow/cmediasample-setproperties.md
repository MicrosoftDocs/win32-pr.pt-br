---
description: 'O método SetProperties define as propriedades do exemplo. Esse método implementa o método IMediaSample2:: SetProperties.'
ms.assetid: 639aedf5-0c21-4578-b336-91859e40f3be
title: Método CMediaSample. SetProperties (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c5e6ef3c3839825586bf47259cf44783d167f503
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105785364"
---
# <a name="cmediasamplesetproperties-method"></a>Método CMediaSample. SetProperties

O `SetProperties` método define as propriedades do exemplo. Esse método implementa o método [**IMediaSample2:: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-setproperties) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetProperties(
         DWORD cbProperties,
   const BYTE  *pbProperties
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*cbProperties* 
</dt> <dd>

Comprimento dos dados de propriedade a serem definidos, em bytes.

</dd> <dt>

*pbProperties* 
</dt> <dd>

Ponteiro para um buffer de tamanho *cbProperties*.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos valores **HRESULT** mostrados na tabela a seguir.



| Código de retorno                                                                                   | Descrição                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Sucesso<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Argumento inválido<br/>          |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memória insuficiente<br/>       |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | Argumento de ponteiro **nulo**<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




