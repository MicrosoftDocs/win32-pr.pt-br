---
description: Método CTransInPlaceFilter. CompleteConnect – o método CompleteConnect conclui uma conexão de PIN.
ms.assetid: 0c02c455-dbd0-4606-b1b1-f965c2a5805b
title: Método CTransInPlaceFilter. CompleteConnect (TRANSip. h)
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
ms.openlocfilehash: d9cc0bc839a4e35c4ce896acdf50da10f0c2bb0c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084784"
---
# <a name="ctransinplacefiltercompleteconnect-method"></a>Método CTransInPlaceFilter. CompleteConnect

O `CompleteConnect` método conclui uma conexão de PIN.

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

Membro do tipo enumerado de [**\_ direção do PIN**](/windows/win32/api/strmif/ne-strmif-pin_direction) , especificando qual Pin no filtro está fazendo a conexão.

</dd> <dt>

*pReceivePin* 
</dt> <dd>

Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do outro PIN nesta tentativa de conexão.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **HRESULT**. Os valores possíveis incluem os mostrados na tabela a seguir.



| Código de retorno                                                                                           | Descrição                                     |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Sucesso.<br/>                             |
| <dl> <dt>**VFW \_ E \_ não \_ no \_ grafo**</dt> </dl> | O filtro não está em um grafo de filtro.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método substitui o método [**CTransformFilter:: CompleteConnect**](ctransformfilter-completeconnect.md) .

O comportamento do filtro depende da ordem das conexões do PIN:

-   Se o PIN de entrada for conectado primeiro, a conexão usará um alocador temporário. Quando o pino de saída é conectado, o filtro reconecta o PIN de entrada. Reconectar o PIN de entrada faz com que o filtro upstream renegocie o alocador. Nesse ponto, o PIN de entrada propõe um alocador do filtro downstream. Para obter mais informações, consulte [**CTransInPlaceInputPin:: Getalocador**](ctransinplaceinputpin-getallocator.md).
-   Se o pino de saída for conectado primeiro, o pino de saída não selecionará um alocador. Quando o pino de entrada é conectado, ele negocia um alocador para ambas as conexões. Se os tipos de mídia de entrada e saída não forem iguais, o filtro reconectará o pino de saída usando o tipo de entrada.

O filtro executa todas as reconexões de PIN chamando o método [**CBaseFilter:: ReconnectPin**](cbasefilter-reconnectpin.md) . O método **ReconnectPin** , por sua vez, chama o método [**IFilterGraph2:: ReconnectEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) no Gerenciador do grafo de filtro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>TRANSip. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe CTransInPlaceFilter**](ctransinplacefilter.md)
</dt> </dl>

 

 




