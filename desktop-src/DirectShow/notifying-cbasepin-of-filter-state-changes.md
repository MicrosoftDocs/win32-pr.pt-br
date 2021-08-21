---
description: Notificando o CBasePin sobre alterações de estado do filtro
ms.assetid: 521ba95b-1f2d-4ad0-ab9b-4f1e3343a2d3
title: Notificando o CBasePin sobre alterações de estado do filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7193402331f150f88217e2d200279e93314c40a9056f52bc31d8100106d4f960
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118152974"
---
# <a name="notifying-cbasepin-of-filter-state-changes"></a>Notificando o CBasePin sobre alterações de estado do filtro

A **classe CBasePin** é notificada sempre que o estado do filtro de propriedade muda. Para cada transição de estado, o filtro chama um método correspondente no pino, conforme mostrado na tabela a seguir.



| Novo estado de filtro | Método CBasePin                                 |
|------------------|-------------------------------------------------|
| Parado          | [**CBasePin::Inactive**](cbasepin-inactive.md) |
| Em Pausa           | [**CBasePin::Active**](cbasepin-active.md)     |
| Executando          | [**CBasePin::Run**](cbasepin-run.md)           |



 

A classe derivada deve substituir esses métodos para responder à alteração de estado. Dependendo do filtro, o pino pode iniciar um thread de trabalho que fornece exemplos, confirma ou decommite seu alocador de memória e assim por diante.

 

 



