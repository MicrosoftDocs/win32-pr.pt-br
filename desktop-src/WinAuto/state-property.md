---
title: Propriedade State
description: A propriedade State descreve o status de um objeto em um momento no tempo. Todos os objetos dão suporte à propriedade State.
ms.assetid: 6a56070f-7913-45b2-b693-3c0a8b7fa2f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d151f09fca6c31abaaa98a19139d3e22eb28ec90
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822990"
---
# <a name="state-property"></a>Propriedade State

A propriedade **State** descreve o status de um objeto em um momento no tempo. Todos os objetos dão suporte à propriedade **State** .

A propriedade **State** é recuperada chamando [**IAccessible:: get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate).

O Microsoft Acessibilidade Ativa fornece [constantes de estado de objeto](object-state-constants.md), definidas em OleAcc. h, que são combinadas para identificar o estado de um objeto. É recomendável que os desenvolvedores de servidor usem esses valores de estado predefinidos. Se valores de estado predefinidos forem retornados, os clientes usarão [**GetStateText**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta) para recuperar uma cadeia de caracteres localizada que descreve o estado.

Os gráficos que, ocasionalmente, são animados devem ter a propriedade **State** definida como [**estado do \_ sistema \_ animado**](object-state-constants.md) e a propriedade [**role**](role-property.md) definida como [**\_ \_ elemento gráfico do sistema de funções**](object-roles.md).

 

 




