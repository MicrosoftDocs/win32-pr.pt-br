---
description: Método CTransInPlaceFilter.CompleteConnect – o método CompleteConnect conclui uma conexão de pino.
ms.assetid: 0c02c455-dbd0-4606-b1b1-f965c2a5805b
title: Método CTransInPlaceFilter.CompleteConnect (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6185204c41e177207d32c321985c021a93ea20506da5f4279cd3134a12952097
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907315"
---
# <a name="ctransinplacefiltercompleteconnect-method"></a>Método CTransInPlaceFilter.CompleteConnect

O `CompleteConnect` método conclui uma conexão de pino.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CompleteConnect(
   PIN_DIRECTION direction,
   IPin          *pReceivePin
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*direction* 
</dt> <dd>

Membro do tipo [**enumerado PIN \_ DIRECTION,**](/windows/win32/api/strmif/ne-strmif-pin_direction) especificando qual pino no filtro está fazendo a conexão.

</dd> <dt>

*pReceivePin* 
</dt> <dd>

Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do outro pino nesta tentativa de conexão.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **HRESULT.** Os valores possíveis incluem aqueles mostrados na tabela a seguir.



| Código de retorno                                                                                           | Descrição                                     |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Êxito.<br/>                             |
| <dl> <dt>**VFW \_ E NÃO ESTÃO NO \_ \_ \_ GRAPH**</dt> </dl> | O filtro não está em um grafo de filtro.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método substitui o [**método CTransformFilter::CompleteConnect.**](ctransformfilter-completeconnect.md)

O comportamento do filtro depende da ordem das conexões de pino:

-   Se o pino de entrada for conectado primeiro, a conexão usará um alocador temporário. Quando o pino de saída está conectado, o filtro reconecta o pino de entrada. Reconectar o pino de entrada faz com que o filtro upstream desconexe o alocador. Nesse ponto, o pino de entrada propõe um alocador do filtro downstream. Para obter mais informações, [**consulte CTransInPlaceInputPin::GetAllocator**](ctransinplaceinputpin-getallocator.md).
-   Se o pino de saída for conectado primeiro, o pino de saída não selecionará um alocador. Quando o pino de entrada está conectado, ele negocia um alocador para ambas as conexões. Se os tipos de mídia de entrada e saída não são os mesmos, o filtro reconectará o pino de saída usando o tipo de entrada.

O filtro executa todas as reconexões de pino chamando o [**método CBaseFilter::ReconnectPin.**](cbasefilter-reconnectpin.md) O **método ReconnectPin,** por sua vez, chama o [**método IFilterGraph2::ReconnectEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) no gerenciador de grafo de filtro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transip.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CTransInPlaceFilter**](ctransinplacefilter.md)
</dt> </dl>

 

 




