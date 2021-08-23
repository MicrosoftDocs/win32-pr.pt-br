---
description: O método AddPin adiciona um novo pino de saída ao filtro.
ms.assetid: 48850a1f-ecb7-460c-9bfc-ce1d1103a00b
title: Método CSource.AddPin (Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.AddPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a1c221d2fd032445587b52b0d0ae7f7744889254983fab82c7b282d06fee195e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953775"
---
# <a name="csourceaddpin-method"></a>Método CSource.AddPin

O `AddPin` método adiciona um novo pino de saída ao filtro.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AddPin(
   CSourceStream *pStream
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pStream* 
</dt> <dd>

Ponteiro para o [**objeto CSourceStream**](csourcestream.md) que implementa o pino.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos **valores HRESULT** mostrados na tabela a seguir.



| Código de retorno                                                                                   | Descrição                    |
|-----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Êxito<br/>             |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memória insuficiente<br/> |



 

## <a name="remarks"></a>Comentários

Quando você cria um novo pin derivado de **CSourceStream,** o construtor **CSourceStream** chama automaticamente esse método para adicionar o pino de saída ao filtro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Source.h (incluir Fluxos.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSource**](csource.md)
</dt> </dl>

 

 




