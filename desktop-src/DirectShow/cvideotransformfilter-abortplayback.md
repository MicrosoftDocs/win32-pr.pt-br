---
description: O método AbortPlayback é usado para sinalizar um erro de streaming. Ele envia um \_ evento ERRORABORT do EC para o Gerenciador do grafo de filtro e envia um downstream de notificação de fim de fluxo.
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
ms.openlocfilehash: 952987dec315408920e92d79003480a01640d14e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779497"
---
# <a name="cvideotransformfilterabortplayback-method"></a>Método CVideoTransformFilter. AbortPlayback

O `AbortPlayback` método é usado para sinalizar um erro de streaming. Ele envia um [**evento \_ ERRORABORT do EC**](ec-errorabort.md) para o Gerenciador do grafo de filtro e envia um downstream de notificação de fim de fluxo.

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

## <a name="return-value"></a>Retornar valor

Retorna o valor do parâmetro *HR* .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Vtrans. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CVideoTransformFilter**](cvideotransformfilter.md)
</dt> </dl>

 

 




