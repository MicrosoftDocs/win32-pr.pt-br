---
description: Método CTransformInputPin.Receive – o método Receive recebe o próximo exemplo de mídia no fluxo. Esse método implementa o método IMemInputPin::Receive.
ms.assetid: 65e4f8f5-2aa2-435b-84b4-e65af3f51afc
title: Método CTransformInputPin.Receive (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 51ae6614544cd7045689f674ce90e672e3bce4ea8ee36486775892f95a5385fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538537"
---
# <a name="ctransforminputpinreceive-method"></a>Método CTransformInputPin.Receive

O `Receive` método recebe o próximo exemplo de mídia no fluxo. Esse método implementa o [**método IMemInputPin::Receive.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSample* 
</dt> <dd>

Ponteiro para a interface [**IMediaSample do**](/windows/desktop/api/Strmif/nn-strmif-imediasample) exemplo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.** Os valores possíveis incluem aqueles mostrados na tabela a seguir.



| Código de retorno                                                                             | Descrição                                                |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | O pino está sendo liberado no momento; O exemplo foi rejeitado.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Êxito.<br/>                                        |



 

## <a name="remarks"></a>Comentários

Esse método chama o método [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) do pino, que verifica o estado de streaming do pino e verifica se há alterações de formato no tipo de mídia. Em seguida, ele chama o método [**CTransformFilter::Receive**](ctransformfilter-receive.md) do filtro, que processa o exemplo e o entrega downstream.

Se o filtro precisar acessar o exemplo após o retorno desse método, ele deverá conter uma contagem de referência chamando o método **IUnknown::AddRef** no exemplo. Por exemplo, alguns filtros de decodificador precisam do exemplo atual para decodificar o próximo exemplo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



 

 




