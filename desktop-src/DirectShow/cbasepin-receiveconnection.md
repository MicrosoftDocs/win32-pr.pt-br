---
description: 'O método ReceiveConnection aceita uma conexão de outro PIN. Esse método implementa o método IPin:: ReceiveConnection.'
ms.assetid: f17e7d93-ac45-4b8a-98c6-0c76ec7117c9
title: Método CBasePin. ReceiveConnection (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.ReceiveConnection
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7d0a8134201af1d3c931121f59a20360020a53a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749632"
---
# <a name="cbasepinreceiveconnection-method"></a>Método CBasePin. ReceiveConnection

O `ReceiveConnection` método aceita uma conexão de outro PIN. Esse método implementa o método [**IPin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ReceiveConnection(
   IPin          *pConnector,
   AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pConnector* 
</dt> <dd>

Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do PIN de conexão.

</dd> <dt>

*PMT* 
</dt> <dd>

Ponteiro para uma estrutura de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) que especifica o tipo de mídia.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os valores possíveis incluem os da tabela a seguir.



| Código de retorno                                                                                                | Descrição                                                                        |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Êxito.<br/>                                                                |
| <dl> <dt>**\_ponteiro E**</dt> </dl>                  | Argumento de ponteiro **nulo** .<br/>                                              |
| <dl> <dt>**VFW \_ E \_ já \_ conectado**</dt> </dl>  | O PIN já está conectado.<br/>                                           |
| <dl> <dt>**VFW \_ E \_ não \_ parado**</dt> </dl>        | O filtro está ativo e o PIN não dá suporte à reconexão dinâmica.<br/> |
| <dl> <dt>**\_tipo E \_ VFW \_ não \_ aceito**</dt> </dl> | O tipo de mídia especificado não é aceitável.<br/>                             |



 

## <a name="remarks"></a>Comentários

O pino de saída chama esse método no pino de entrada. Se o PIN de entrada retornar um código de erro, a conexão falhará.

Na classe base, esse método executa as seguintes etapas:

-   Verifica se o PIN já está conectado.
-   Verifica se o filtro está parado.
-   Chama o método [**CBasePin:: CheckConnect**](cbasepin-checkconnect.md) para testar se o PIN de conexão é adequado.
-   Chama o método [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md) para testar se o tipo de mídia é aceitável.

Se todas essas etapas forem bem sucedidos, o método chamará os métodos [**CBasePin:: CompleteConnect**](cbasepin-completeconnect.md) e [**SetMediaType**](cbasepin-setmediatype.md) para concluir a conexão. Esses métodos armazenam o tipo de mídia e um ponteiro para o pino de saída.

Se **CheckConnect** ou **CheckMediaType** falhar, a classe base chamará o método [**CBasePin:: BreakConnect**](cbasepin-breakconnect.md) para interromper a conexão e, em seguida, retornará um código de erro de `ReceiveConnection` .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




