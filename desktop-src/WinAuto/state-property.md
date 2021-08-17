---
title: Propriedade State
description: A propriedade State descreve o status de um objeto em um momento no tempo. Todos os objetos suportam a propriedade State.
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

A **propriedade State** descreve o status de um objeto em um momento no tempo. Todos os objetos suportam a **propriedade** State.

A **propriedade State** é recuperada chamando [**IAccessible::get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate).

Microsoft Active Accessibility fornece constantes de estado do objeto , definidas em oleacc.h, que são [combinadas](object-state-constants.md)para identificar o estado de um objeto. É recomendável que os desenvolvedores de servidores usem esses valores de estado predefinidos. Se valores de estado predefinidos são retornados, os clientes [**usam GetStateText**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta) para recuperar uma cadeia de caracteres localizada que descreve o estado.

Gráficos ocasionalmente animados devem ter a propriedade **State** definida como [**STATE SYSTEM \_ \_ ANIMATED**](object-state-constants.md) e a propriedade [**Role**](role-property.md) definida como ROLE [**SYSTEM \_ \_ GRAPHIC**](object-roles.md).

 

 




