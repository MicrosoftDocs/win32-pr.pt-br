---
description: 'o método Conexão conecta o pin a outro pin. esse método implementa o método IPin:: Conexão.'
ms.assetid: 8ea99d2f-09da-4b15-a3b0-04ceb7888bc1
title: CBasePin. método de Conexão (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Connect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a134b87e9c7c4d0f665ae37df7ec9cd0ecb3a37c0d0548f27835ead7b8ecca21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074790"
---
# <a name="cbasepinconnect-method"></a>CBasePin. método de Conexão

O `Connect` método conecta o PIN a outro PIN. esse método implementa o método [**IPin:: Conexão**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Connect(
         IPin          *pReceivePin,
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pReceivePin* 
</dt> <dd>

Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do pino de recebimento.

</dd> <dt>

*PMT* 
</dt> <dd>

Ponteiro para uma estrutura de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) que especifica o tipo de mídia para a conexão.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor **HRESULT** . Os valores possíveis incluem os da tabela a seguir.



| Código de retorno                                                                                                  | Descrição                                                                        |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                         | Êxito.<br/>                                                                |
| <dl> <dt>**VFW \_ E \_ já \_ conectado**</dt> </dl>    | O PIN já está conectado.<br/>                                           |
| <dl> <dt>**VFW \_ E \_ nenhum \_ \_ tipo aceitável**</dt> </dl> | Não foi possível encontrar um tipo de mídia aceitável.<br/>                                |
| <dl> <dt>**VFW \_ E \_ não \_ parado**</dt> </dl>          | O filtro está ativo e o PIN não dá suporte à reconexão dinâmica.<br/> |
| <dl> <dt>**\_tipo E \_ VFW \_ não \_ aceito**</dt> </dl>   | O tipo de mídia especificado não é aceitável.<br/>                             |



 

## <a name="remarks"></a>Comentários

O parâmetro *PGTO* pode ser **nulo**. Ele também pode especificar um tipo de mídia parcial, com um valor de GUID \_ NULL para o tipo, subtipo ou formato principal.

Na classe base, esse método testa se o PIN já está conectado e se o filtro está parado. Ele delega o restante do processo de conexão para o método [**CBasePin:: AgreeMediaType**](cbasepin-agreemediatype.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




