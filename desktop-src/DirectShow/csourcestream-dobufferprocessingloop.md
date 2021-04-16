---
description: O método DoBufferProcessingLoop gera dados de mídia e os entrega para o pino de entrada downstream.
ms.assetid: a8dce761-eed6-402d-9115-e21822d7a853
title: Método CSourceStream. DoBufferProcessingLoop (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.DoBufferProcessingLoop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 809694cacf0c30acf88ddf7d14c7f5ea1f654436
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105787145"
---
# <a name="csourcestreamdobufferprocessingloop-method"></a>Método CSourceStream. DoBufferProcessingLoop

O `DoBufferProcessingLoop` método gera dados de mídia e os entrega para o pino de entrada downstream.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT DoBufferProcessingLoop();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os valores possíveis incluem os mostrados na tabela a seguir.



| Código de retorno                                                                             | Descrição                                                             |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**\_falso**</dt> </dl> | O thread recebeu uma solicitação de interrupção.<br/>                              |
| <dl> <dt>**S \_ OK**</dt> </dl>    | O fluxo terminou ou o filtro downstream não está aceitando exemplos.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método implementa o loop principal que processa os dados e os entrega por downstream. Cada vez que passa pelo loop, o método recupera um exemplo de mídia vazio do alocador. Ele passa o exemplo para o método [**CSourceStream:: FillBuffer**](csourcestream-fillbuffer.md) . O método **FillBuffer** , que a classe derivada deve implementar, gera dados de mídia e os coloca no buffer de exemplo.

O loop termina quando ocorre um dos seguintes:

-   O método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) do pino de entrada rejeita um exemplo.
-   O método **FillBuffer** retorna S \_ false, indicando o final do fluxo ou retorna um código de erro.
-   O thread recebe uma solicitação [**CSourceStream:: Stop**](csourcestream-stop.md) .

O `DoBufferProcessingLoop` método manipula a notificação de fim de fluxo. Se ocorrer um erro, ele enviará um evento [**\_ ERRORABORT do EC**](ec-errorabort.md) para o Gerenciador do grafo de filtro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Source. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




