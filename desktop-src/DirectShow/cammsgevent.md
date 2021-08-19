---
description: A classe CAMMsgEvent é um wrapper para objetos de evento que executam o processamento de mensagens.
ms.assetid: 4b94febe-169f-4f04-be93-043a8c75e3b4
title: Classe CAMMsgEvent (Wxutil.h)
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
ms.openlocfilehash: c7c4d3c8268f06e81d1bd1a5285f7e4785459889397ccf249bbde7f0dd627f05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955426"
---
# <a name="cammsgevent-class"></a>Classe CAMMsgEvent

![Hierarquia de classes cammsgevent](images/util06.png)

A `CAMMsgEvent` classe é um wrapper para objetos de evento que executam o processamento de mensagens.

Essa classe deriva do objeto [**CAMEvent.**](camevent.md) Ele adiciona um método, [**CAMMsgEvent::WaitMsg,**](cammsgevent-waitmsg.md)que expedi as mensagens de entrada enquanto aguarda.



| Métodos públicos                                 | Descrição                                                          |
|------------------------------------------------|----------------------------------------------------------------------|
| [**CAMMsgEvent**](cammsgevent-cammsgevent.md) | Construtor.                                                         |
| [**WaitMsg**](cammsgevent-waitmsg.md)         | Aguarda até que o evento seja sinalizado, ao expedir mensagens enviadas. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil.h (incluir Fluxos.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



 

 




