---
description: O método AbortPlayback é usado para sinalizar um erro de streaming. ele envia um \_ evento ERRORABORT do EC para o gerenciador de Graph de filtro e envia um downstream de notificação de fim de fluxo.
ms.assetid: b48ec72f-d220-4b27-98fc-88eaa4f663eb
title: Método CVideoTransformFilter. AbortPlayback (Vtrans. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.AbortPlayback
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6560e7ce704423bfecc519c709c2c08733fe90a2346324f9e1282571530293ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821931"
---
# <a name="cvideotransformfilterabortplayback-method"></a>Método CVideoTransformFilter. AbortPlayback

O `AbortPlayback` método é usado para sinalizar um erro de streaming. ele envia um [**evento \_ ERRORABORT do EC**](ec-errorabort.md) para o gerenciador de Graph de filtro e envia um downstream de notificação de fim de fluxo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AbortPlayback(
   HRESULT hr
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*h* 
</dt> <dd>

Valor **HRESULT** da operação que falhou. Esse valor é usado como o primeiro parâmetro de evento para o \_ evento ERRORABORT do EC.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o valor do parâmetro *HR* .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Vtrans. h (incluir Fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CVideoTransformFilter**](cvideotransformfilter.md)
</dt> </dl>

 

 




