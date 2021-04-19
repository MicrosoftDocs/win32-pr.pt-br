---
description: 'O método NotifyAllocator especifica um alocador para a conexão. Esse método implementa o método IMemInputPin:: NotifyAllocator.'
ms.assetid: 16167bd5-2d33-4329-87ec-6a6c578e0060
title: Método CBaseInputPin. NotifyAllocator (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.NotifyAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ce5bc3cfe165b1adb6b5b970ca43d31c8ace98f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753363"
---
# <a name="cbaseinputpinnotifyallocator-method"></a>Método CBaseInputPin. NotifyAllocator

O `NotifyAllocator` método especifica um alocador para a conexão. Esse método implementa o método [**IMemInputPin:: NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT NotifyAllocator(
   IMemAllocator *pAllocator,
   BOOL          bReadOnly
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pAllocator* 
</dt> <dd>

Ponteiro para a interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) do alocador.

</dd> <dt>

*bReadOnly* 
</dt> <dd>

Sinalizador que especifica se os exemplos deste alocador são somente leitura. Se **for true**, os exemplos serão somente leitura.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Durante a conexão do PIN, o pino de saída escolhe um alocador e chama esse método para notificar o PIN de entrada. O pino de saída pode usar o alocador que o PIN de entrada propôs no método [**IMemInputPin:: Getalocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) ou pode fornecer seu próprio alocador.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseInputPin**](cbaseinputpin.md)
</dt> </dl>

 

 




