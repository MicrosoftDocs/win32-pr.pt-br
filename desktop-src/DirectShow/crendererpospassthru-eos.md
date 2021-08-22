---
description: O método EOS atualiza os carimbos de data/hora armazenados em cache após uma notificação de fim do fluxo.
ms.assetid: 7fb2f964-ec15-47f5-902b-29b9b121e876
title: Método CRendererPosPassThru.EOS (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.EOS
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 10f87fbb66f8ad1d89ff31c6653780b3fde23ecbaf55d72b6f3de2f59546b49b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073410"
---
# <a name="crendererpospassthrueos-method"></a>Método CRendererPosPassThru.EOS

O `EOS` método atualiza os carimbos de data/hora armazenados em cache após uma notificação de fim de fluxo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT EOS();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.** Os valores possíveis incluem aqueles listados na tabela a seguir.



| Código de retorno                                                                            | Descrição                                               |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Êxito.<br/>                                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Falha. Possivelmente, o filtro não está transmitindo.<br/> |



 

## <a name="remarks"></a>Comentários

O filtro deve chamar esse método quando receber uma notificação de fim de fluxo ([**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)). O método define os carimbos de data/hora armazenados em cache iguais à posição de parada, garantindo que o método [**IMediaSeeking:: GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) retorne os valores corretos no final do fluxo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



 

 




