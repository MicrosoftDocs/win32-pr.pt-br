---
description: Método CBaseInputPin.NotifyAllocator – o método NotifyAllocator especifica um alocador para a conexão. Esse método implementa o método IMemInputPin::NotifyAllocator.
ms.assetid: 16167bd5-2d33-4329-87ec-6a6c578e0060
title: Método CBaseInputPin.NotifyAllocator (Amfilter.h)
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
ms.openlocfilehash: 37bcd7d8d69f18dce98339a34a4641ddd2502e946e29a0097fe6c381f4af5c2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017004"
---
# <a name="cbaseinputpinnotifyallocator-method"></a>Método CBaseInputPin.NotifyAllocator

O `NotifyAllocator` método especifica um alocador para a conexão. Esse método implementa o [**método IMemInputPin::NotifyAllocator.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator)

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

Ponteiro para a interface [**IMemAllocator do**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) alocador.

</dd> <dt>

*bReadOnly* 
</dt> <dd>

Sinalizador que especifica se os exemplos desse alocador são somente leitura. Se **TRUE**, os exemplos serão somente leitura.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Durante a conexão de pino, o pino de saída escolhe um alocador e chama esse método para notificar o pino de entrada. O pino de saída pode usar o alocador que o pino de entrada proposto no método [**IMemInputPin::GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) ou pode fornecer seu próprio alocador.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseInputPin**](cbaseinputpin.md)
</dt> </dl>

 

 




