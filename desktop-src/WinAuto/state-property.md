---
title: Propriedade State
description: A propriedade State descreve o status de um objeto em um momento no tempo. Todos os objetos dão suporte à propriedade State.
ms.assetid: 6a56070f-7913-45b2-b693-3c0a8b7fa2f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e174e938dd6252852ded6de957a54f6f94264aa811bd5bb76094af7bbba61f48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118564414"
---
# <a name="state-property"></a>Propriedade State

A propriedade **State** descreve o status de um objeto em um momento no tempo. Todos os objetos dão suporte à propriedade **State** .

A propriedade **State** é recuperada chamando [**IAccessible:: get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate).

O Microsoft Acessibilidade Ativa fornece [constantes de estado de objeto](object-state-constants.md), definidas em OleAcc. h, que são combinadas para identificar o estado de um objeto. É recomendável que os desenvolvedores de servidor usem esses valores de estado predefinidos. Se valores de estado predefinidos forem retornados, os clientes usarão [**GetStateText**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta) para recuperar uma cadeia de caracteres localizada que descreve o estado.

Os gráficos que, ocasionalmente, são animados devem ter a propriedade **State** definida como [**estado do \_ sistema \_ animado**](object-state-constants.md) e a propriedade [**role**](role-property.md) definida como [**\_ \_ elemento gráfico do sistema de funções**](object-roles.md).

 

 




