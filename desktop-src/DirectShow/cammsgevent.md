---
description: A classe CAMMsgEvent é um wrapper para objetos de evento que executam o processamento de mensagens.
ms.assetid: 4b94febe-169f-4f04-be93-043a8c75e3b4
title: Classe CAMMsgEvent (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMMsgEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4ebac7aae11f7a7b7d6b846e262e93b5759210b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105787433"
---
# <a name="cammsgevent-class"></a>Classe CAMMsgEvent

![hierarquia de classe CAMMsgEvent](images/util06.png)

A `CAMMsgEvent` classe é um wrapper para objetos de evento que executam o processamento de mensagens.

Essa classe deriva do objeto [**CAMEvent**](camevent.md) . Ele adiciona um método, [**CAMMsgEvent:: WaitMsg**](cammsgevent-waitmsg.md), que despacha mensagens de entrada enquanto aguarda.



| Métodos públicos                                 | Descrição                                                          |
|------------------------------------------------|----------------------------------------------------------------------|
| [**CAMMsgEvent**](cammsgevent-cammsgevent.md) | Construtor.                                                         |
| [**WaitMsg**](cammsgevent-waitmsg.md)         | Aguarda o evento ser sinalizado, durante a expedição de mensagens enviadas. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




