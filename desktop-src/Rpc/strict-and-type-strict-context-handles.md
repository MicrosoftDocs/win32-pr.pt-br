---
title: Identificador de contexto estrito e de tipo estrito
description: Use o atributo de \_ alça \_ de contexto estrito para todos os alças de contexto.
ms.assetid: 2483aa76-0814-4f63-9c38-0aa050d73772
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91c266fb70b540e08d066e51f61a921b8f88819456e83b909e3be31bb1f518c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120017506"
---
# <a name="strict-and-type-strict-context-handles"></a>Identificador de contexto estrito e de tipo estrito

Use o atributo [**de alça de contexto \_ \_ estrito**](/windows/desktop/Midl/strict-context-handle) para todos os alças de contexto. Por padrão, um alça de contexto não está associado a uma interface, o que significa que um alça de contexto pode ser criado em uma interface e passado para outra. Esse é um ataque fácil e muitos servidores RPC falham ao impedi-lo.

Se duas interfaces coexistissem no mesmo processo, um invasor poderia abrir um alçamento de contexto em uma interface e passá-lo para outra, o que pode passar sobre os dados inesperados. Muitos desenvolvedores acredita que seu software é a única interface em um processo, mas muitas vezes esse não é o caso, porque o sistema e muitos componentes de terceiros usam RPC internamente e essas interfaces podem criar alças de contexto. Quando o atributo de alça [**\_ \_ de**](/windows/desktop/Midl/strict-context-handle) contexto estrito é usado, o tempo de executar RPC garante que um contexto criado em uma interface possa ser passado como um argumento somente para métodos dessa interface.

Em situações em que um aplicativo é desenvolvido para Windows Vista, o uso do identificador de contexto estrito de tipo está disponível e recomendado. [**\_ \_ \_**](/windows/desktop/Midl/type-strict-context-handle) Identificador de contexto não estão associados a um tipo específico por padrão. Quando vários tipos de alças de contexto são usados no mesmo processo, é possível que um cliente mal-intencionado passe um handle de contexto no lugar de outro para produzir resultados indesejáveis. O uso do **identificador \_ de contexto \_ \_ estrito** de tipo permite que os aplicativos imigram a consistência do tipo de identificador de contexto e impeçam qualquer uso de tipo de identificador de contexto incompatibilidade.

 

 