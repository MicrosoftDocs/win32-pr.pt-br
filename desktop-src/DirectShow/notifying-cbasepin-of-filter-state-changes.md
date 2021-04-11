---
description: Notificando CBasePin de alterações de estado de filtro
ms.assetid: 521ba95b-1f2d-4ad0-ab9b-4f1e3343a2d3
title: Notificando CBasePin de alterações de estado de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49dad6fabc162eb2384283ce2fc8914f76707036
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104295999"
---
# <a name="notifying-cbasepin-of-filter-state-changes"></a>Notificando CBasePin de alterações de estado de filtro

A classe **CBasePin** é notificada sempre que o estado do filtro proprietário é alterado. Para cada transição de estado, o filtro chama um método correspondente no PIN, conforme mostrado na tabela a seguir.



| Novo estado de filtro | Método CBasePin                                 |
|------------------|-------------------------------------------------|
| Parado          | [**CBasePin:: inativo**](cbasepin-inactive.md) |
| Em Pausa           | [**CBasePin:: ativo**](cbasepin-active.md)     |
| Executando          | [**CBasePin:: Run**](cbasepin-run.md)           |



 

A classe derivada deve substituir esses métodos para responder à alteração de estado. Dependendo do filtro, o PIN pode iniciar um thread de trabalho que fornece amostras, confirmar ou desconfirmar seu alocador de memória e assim por diante.

 

 



