---
description: 'O método getalocador recupera o alocador de memória proposto por esse PIN. Esse método implementa o método IMemInputPin:: getalocator.'
ms.assetid: 07bc77f8-a877-4403-b424-20bda715a818
title: Método CBaseInputPin. getalocador (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.GetAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 098738fc63ba1834b1eefb4b2518e3309db35c43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747612"
---
# <a name="cbaseinputpingetallocator-method"></a>Método CBaseInputPin. getalocador

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

Endereço de uma variável que recebe um ponteiro para a interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) do alocador.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK se for bem-sucedido ou um código de erro da função **CoCreateInstance** .

## <a name="remarks"></a>Comentários

Esse método cria um objeto [**CMemAllocator**](cmemallocator.md) . Substitua esse método se o filtro usar um alocador de um PIN de downstream ou um alocador personalizado.

Se o método tiver sucesso, a interface **IMemAllocator** terá uma contagem de referência pendente. Certifique-se de liberá-lo quando terminar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseInputPin**](cbaseinputpin.md)
</dt> </dl>

 

 




