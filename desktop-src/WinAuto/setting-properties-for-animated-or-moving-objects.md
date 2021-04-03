---
title: Definindo propriedades para objetos animados ou movendo
description: Para controles de animação, como o controle de animação exibido ao copiar arquivos, use a \_ função de objeto de animação do sistema de funções \_ .
ms.assetid: 8c5ebbc3-4066-452b-8f37-2fb595adea53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1551899305968471bf1425b5cc043be8329c2bd4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005979"
---
# <a name="setting-properties-for-animated-or-moving-objects"></a>Definindo propriedades para objetos animados ou movendo

Para controles de animação, como o controle de animação exibido ao copiar arquivos, use a função de objeto de [**\_ \_ animação do sistema de funções**](object-roles.md) . Para gráficos que são, ocasionalmente, animados, use a função de objeto [**\_ \_ gráfico do sistema de funções**](object-roles.md) com o [**estado**](state-property.md) definido como [**sistema de estado \_ \_ animado**](object-state-constants.md).

Use o [**sinalizador \_ \_ animado do sistema de estado**](object-state-constants.md) para marcar um objeto cuja aparência é alterada rapidamente. Os clientes usam esse sinalizador para evitar notificar os usuários repetidamente pelo que realmente é uma única série de alterações visuais.

Um exemplo disso é o texto de letreiro, que é divulgado progressivamente à medida que rola pela tela. Esses objetos recebem o atributo de [**sistema de \_ estado \_ animado**](object-state-constants.md). Na maioria dos casos, a cadeia de caracteres de [**valor**](value-property.md) do objeto reflete todo o texto, até mesmo a parte que não está visível no momento. A alteração da cadeia de caracteres de **valor** com frequência para corresponder ao texto atualmente visível não é recomendável porque resulta em um número muito grande de eventos [**VALUECHANGE de \_ objeto \_ de evento**](event-constants.md) que não transmitem informações úteis.

Por exemplo, em uma janela que contém uma região retangular que mostra a palavra "Sim!" movendo um padrão Figure-oito, a [**função**](role-property.md) é o [**\_ \_ gráfico do sistema de funções**](object-roles.md), a propriedade [**Value**](value-property.md) é a cadeia de caracteres exibida, a propriedade [**Location**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) é o retângulo delimitador em volta do texto e o sinalizador de atributo [**\_ \_ animado do sistema de estado**](object-state-constants.md) é definido. A [**Descrição**](description-property.md) é "a palavra ' Yes! ' está se movendo pela tela em um padrão Figure-oito. " O servidor gera apenas [**eventos \_ \_ STATECHANGE de objeto de evento**](event-constants.md) quando o objeto inicia ou deixa a animação.

 

 




