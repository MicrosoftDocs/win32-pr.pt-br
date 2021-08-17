---
description: Se o fim do fluxo for atingido, o método SendEndOfStream agendará um \_ evento de conclusão do EC para o Gerenciador do grafo de filtro.
ms.assetid: 3c10c956-e352-4796-a8cd-cc69a02066f2
title: Método CBaseRenderer. SendEndOfStream (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SendEndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 344783d8e8aac755d157f125b02827c9f362ca96271dccb84134f451b31d1bc3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954815"
---
# <a name="cbaserenderersendendofstream-method"></a>Método CBaseRenderer. SendEndOfStream

Se o fim do fluxo for atingido, o `SendEndOfStream` método agendará um \_ evento de conclusão do EC para o Gerenciador do grafo de filtro.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT SendEndOfStream();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um valor **HRESULT** . Os valores possíveis incluem os da tabela a seguir.



| Código de retorno                                                                             | Descrição                                                               |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**\_falso**</dt> </dl> | O Gerenciador do grafo de filtro não está aceitando notificações de eventos.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Êxito.<br/>                                                       |



 

## <a name="remarks"></a>Comentários

O filtro pode receber uma notificação de fim de fluxo antes da hora de parada do exemplo atual. Nesse caso, o filtro deve aguardar antes de lançar uma notificação de [**\_ conclusão do EC**](ec-complete.md) para o Gerenciador do grafo de filtro.

Portanto:

-   Se o filtro tiver recebido uma notificação de fim de fluxo (EOS) antecipada, esse método agendará um evento de temporizador. Quando o evento de timer é ativado, o filtro posta o \_ evento de conclusão do EC.
-   Se o filtro tiver recebido uma notificação de EOS que não foi cedo, esse método lançará o evento de conclusão do EC \_ imediatamente.
-   Se o filtro não tiver nenhuma notificação de EOS pendente, o método retornará sem fazer nada.

O método de retorno de chamada do temporizador é [**CBaseRenderer:: TimerCallback**](cbaserenderer-timercallback.md). Para entregar o \_ evento EC Complete, o filtro chama o método [**CBaseRenderer:: NotifyEndOfStream**](cbaserenderer-notifyendofstream.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




