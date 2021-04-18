---
description: O método ReconnectPin quebra uma conexão de PIN existente e a reconecta ao mesmo PIN, usando um tipo de mídia especificado.
ms.assetid: 9e2dea49-a2bd-4abd-b896-54b13b2271bb
title: Método CBaseFilter. ReconnectPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.ReconnectPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 22507995621d708e40437175d7004d10f68fedb5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749038"
---
# <a name="cbasefilterreconnectpin-method"></a>Método CBaseFilter. ReconnectPin

O `ReconnectPin` método quebra uma conexão de PIN existente e a reconecta ao mesmo PIN, usando um tipo de mídia especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ReconnectPin(
   IPin                *pPin,
   AM_MEDIA_TYPE const *pmt
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pPin* 
</dt> <dd>

Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do PIN.

</dd> <dt>

*PMT* 
</dt> <dd>

Ponteiro para uma estrutura de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) que especifica o tipo de mídia ou **nulo**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os valores possíveis incluem os listados na tabela a seguir.



| Código de retorno                                                                                   | Descrição                                                                       |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Êxito.<br/>                                                               |
| <dl> <dt>**E \_ NOinterface**</dt> </dl> | a variável de membro [**\_ pGraph m**](cbasefilter-m-pgraph.md) é **nula**.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método chama o método [**IFilterGraph2:: ReconnectEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) no Gerenciador do grafo de filtro. Se a interface [**IFilterGraph2**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2) não estiver disponível, o método chamará [**IFilterGraph:: Reconnect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-reconnect).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




