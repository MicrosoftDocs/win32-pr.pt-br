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
ms.openlocfilehash: c608b1d3f44a82d7aa964e803dec147a7216a71e85c6d797135713cf28af3fa0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119317216"
---
# <a name="csystemclock-class"></a>Classe CSystemClock

![Hierarquia de classes csystemclock](images/sclock01.png)

A `CSystemClock` classe implementa um relógio que retorna a hora do sistema.

Essa classe deriva da [**classe CBaseReferenceClock**](cbasereferenceclock.md) e adiciona suporte para as interfaces **IPersist** e [**IAMClockAdjust.**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust)



| Métodos públicos                                        | Descrição                                         |
|-------------------------------------------------------|-----------------------------------------------------|
| [**CreateInstance**](csystemclock-createinstance.md) | Cria uma nova instância desse objeto.              |
| [**CSystemClock**](csystemclock-csystemclock.md)     | Método do construtor.                                 |
| Métodos IAMClockAdjust                                | Descrição                                         |
| [**SetClockDelta**](csystemclock-setclockdelta.md)   | Ajusta a hora do relógio.                             |
| Métodos IPersist                                      | Descrição                                         |
| [**Getclassid**](csystemclock-getclassid.md)         | Retorna o CLSID (identificador de classe) do objeto . |



 

 

 



