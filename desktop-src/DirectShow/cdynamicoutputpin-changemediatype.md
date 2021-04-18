---
description: O método ChangeMediaType altera dinamicamente o tipo de mídia para a conexão.
ms.assetid: 38efdfdc-f636-4cad-b8d3-8c63a277644e
title: Método CDynamicOutputPin. ChangeMediaType (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.ChangeMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 89c15e3076a95f8fee3f2f2970fc59da5cf3bf4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751896"
---
# <a name="cdynamicoutputpinchangemediatype-method"></a>Método CDynamicOutputPin. ChangeMediaType

O `ChangeMediaType` método altera dinamicamente o tipo de mídia para a conexão. A alteração pode ocorrer enquanto o grafo de filtro está em execução. Depois que esse método é chamado, os exemplos com o tipo de mídia antigo não podem ser entregues. O chamador deve garantir que nenhuma amostra antiga esteja pendente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ChangeMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PMT* 
</dt> <dd>

Ponteiro para uma estrutura de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) que especifica o tipo de mídia.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os valores possíveis incluem os mostrados na tabela a seguir.



| Código de retorno                                                                                           | Descrição                                                                                                                              |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Êxito.<br/>                                                                                                                      |
| <dl> <dt>**E \_ falha**</dt> </dl>                | Falha. Possivelmente o filtro proprietário não chamou [**CDynamicOutputPin:: SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md).<br/> |
| <dl> <dt>**VFW \_ E \_ não \_ conectado**</dt> </dl> | O PIN não está conectado.<br/>                                                                                                     |



 

## <a name="remarks"></a>Comentários

Chame o método [**CDynamicOutputPin:: StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) antes de chamar esse método.

Esse método verifica primeiro se o PIN de entrada downstream pode aceitar o novo formato sem reconectar. Ele consulta o pino de entrada para a interface [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) . Se o PIN de entrada der suporte a **IPinConnection**, o método chamará o método [**IPinConnection::D ynamicqueryaccept**](/windows/desktop/api/Strmif/nf-strmif-ipinconnection-dynamicqueryaccept) com o tipo de mídia proposto. Se o PIN de entrada aceitar o novo tipo de mídia, o método chamará o método [**IPin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) e renegociará os requisitos de alocador.

Por outro lado, se o PIN downstream não oferecer suporte a **IPinConnection**, ou se rejeitar o novo tipo de mídia, o método chamará o método [**CDynamicOutputPin::D ynamicreconnect**](cdynamicoutputpin-dynamicreconnect.md) para executar uma reconexão dinâmica.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




