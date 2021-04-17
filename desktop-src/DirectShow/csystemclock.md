---
description: A classe CSystemClock implementa um relógio que retorna a hora do sistema.
ms.assetid: 22f8b641-6472-433f-bff4-4e62eae25c9b
title: Classe CSystemClock
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock
api_type:
- COM
api_location: ''
ms.openlocfilehash: e9cc5e0bde8983cfd8c544d3898d4af628e10f87
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104558531"
---
# <a name="csystemclock-class"></a>Classe CSystemClock

![hierarquia de classe CSystemClock](images/sclock01.png)

A `CSystemClock` classe implementa um relógio que retorna a hora do sistema.

Essa classe deriva da classe [**CBaseReferenceClock**](cbasereferenceclock.md) e adiciona suporte para as interfaces **IPersist** e [**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust) .



| Métodos públicos                                        | Descrição                                         |
|-------------------------------------------------------|-----------------------------------------------------|
| [**CreateInstance**](csystemclock-createinstance.md) | Cria uma nova instância desse objeto.              |
| [**CSystemClock**](csystemclock-csystemclock.md)     | Método de construtor.                                 |
| Métodos IAMClockAdjust                                | Descrição                                         |
| [**SetClockDelta**](csystemclock-setclockdelta.md)   | Ajusta a hora do relógio.                             |
| Métodos IPersist                                      | Descrição                                         |
| [**GetClassID**](csystemclock-getclassid.md)         | Retorna o identificador de classe (CLSID) do objeto. |



 

 

 



