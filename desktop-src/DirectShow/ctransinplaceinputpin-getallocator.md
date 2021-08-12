---
description: 'Método CTransInPlaceInputPin. getalocador – o método getalocador recupera o alocador de memória proposto por esse PIN. Esse método implementa o método IMemInputPin:: getalocator.'
ms.assetid: e9db4aa0-4f53-4ca4-babb-5e0215c7c284
title: Método CTransInPlaceInputPin. getalocador (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.GetAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c3c90587cbd0a9cc9b0abed834db68de3edac6f73d98dac3c8bb283e77f978fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118654842"
---
# <a name="ctransinplaceinputpingetallocator-method"></a>Método CTransInPlaceInputPin. getalocador

O `GetAllocator` método recupera o alocador de memória proposto por esse PIN. Esse método implementa o método [**IMemInputPin:: Getalocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetAllocator(
   IMemAllocator **ppAllocator
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppAllocator* 
</dt> <dd>

Recebe um ponteiro para a interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) do alocador.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor **HRESULT** . Os valores possíveis incluem os mostrados na tabela a seguir.



| Código de retorno                                                                                          | Descrição                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                 | Êxito.<br/>                   |
| <dl> <dt>**VFW \_ E \_ nenhum \_ alocador**</dt> </dl> | Nenhum alocador disponível.<br/> |



 

## <a name="remarks"></a>Comentários

Se o pino de saída do filtro estiver conectado, esse método solicitará um alocador do PIN de entrada do filtro downstream.

Se o pino de saída do filtro não estiver conectado, esse método criará um alocador temporário. Posteriormente, quando o pino de saída estiver conectado, o filtro reconectará o PIN de entrada e renegociará o alocador.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transip. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CTransInPlaceInputPin**](ctransinplaceinputpin.md)
</dt> </dl>

 

 




