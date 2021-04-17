---
description: O método EOS atualiza os carimbos de data/hora em cache após uma notificação de fim de fluxo.
ms.assetid: 7fb2f964-ec15-47f5-902b-29b9b121e876
title: Método CRendererPosPassThru. EOS (Ctlutil. h)
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
ms.openlocfilehash: a9e6990d946f32b441f0a33ceba8c0a59fdae488
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752694"
---
# <a name="crendererpospassthrueos-method"></a>Método CRendererPosPassThru. EOS

O `EOS` método atualiza os carimbos de data/hora em cache após uma notificação de fim de fluxo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT EOS();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os valores possíveis incluem os listados na tabela a seguir.



| Código de retorno                                                                            | Descrição                                               |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Êxito.<br/>                                       |
| <dl> <dt>**E \_ falha**</dt> </dl> | Falha. Possivelmente, o filtro não é transmitido.<br/> |



 

## <a name="remarks"></a>Comentários

O filtro deve chamar esse método quando ele recebe uma notificação de fim de fluxo ([**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)). O método define os carimbos de data/hora em cache iguais à posição de parada, garantindo que o método [**IMediaSeeking:: getCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) retorne os valores corretos no final do fluxo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




