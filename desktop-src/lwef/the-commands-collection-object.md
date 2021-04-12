---
title: O objeto da coleção de comandos
description: O objeto da coleção de comandos
ms.assetid: 8726ce04-77d3-4ae3-bd46-e75f42b36d6f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2367035d86f92d57dc459564943b9e7797ecb04
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365851"
---
# <a name="the-commands-collection-object"></a>O objeto da coleção de comandos

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

O servidor do Microsoft Agent mantém uma lista de comandos que estão disponíveis atualmente para o usuário. Essa lista inclui comandos que o servidor define para interação geral (como ocultar e abrir a janela de comandos de voz), a lista de clientes disponíveis (mas que não são de entrada ativa) e os comandos definidos pelo cliente ativo atual. Os dois primeiros conjuntos de comandos são comandos globais; ou seja, eles estão disponíveis a qualquer momento, independentemente do cliente de entrada-ativo. Comandos definidos pelo cliente estão disponíveis somente quando esse cliente está em entrada-ativo e o caractere é visível.

Cada aplicativo cliente pode definir uma coleção de comandos chamada coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) . Para adicionar um comando à coleção, use o método [**Add**](add-method.md) ou [**Insert**](insert-method.md) . Embora você possa especificar as propriedades de um comando com instruções separadas, para o desempenho de código ideal, especifique todas as propriedades de um comando na instrução **Add** ou **Insert** do método. Para cada comando na coleção, você pode determinar se o acesso do usuário ao comando é exibido no menu pop-up do caractere, na janela comandos de voz, em ambos ou em nenhum. Por exemplo, se você quiser que um comando apareça no menu pop-up para o caractere, defina a [**legenda**](caption-property.md) do comando e as propriedades [**visíveis**](visible-property.md) . Para exibir o comando na janela comandos de voz, defina as propriedades [**VoiceCaption**](voicecaption-property.md) e [**Voice**](voice-property.md) do comando.

Um usuário pode acessar os [**comandos**](/windows/desktop/lwef/the-commands-collection-object)de comunicação individuais ands em sua coleção somente quando o aplicativo cliente é de entrada-ativo. Portanto, quando você pode estar compartilhando o caractere com outros aplicativos cliente, normalmente você desejará definir as propriedades [**Caption**](caption-property.md), [**VoiceCaption**](voicecaption-property.md)e [**Voice**](voice-property.md) para o objeto de coleção de **comandos** , bem como para os comandos na coleção. Isso coloca uma entrada para a coleção de **comandos** no menu pop-up de um caractere e na janela de comandos de voz.

Quando o usuário alterna para o cliente escolhendo sua entrada de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) , o servidor automaticamente torna o cliente de entrada-ativo, notificando o aplicativo cliente usando o evento [**ActivateInput**](activateinput-event.md) e disponibiliza os comandos em sua coleção. O servidor também notifica o cliente de que ele não está mais em entrada-ativo com o evento [**DeActivateInput**](deactivateinput-event.md) . Isso permite que o servidor apresente e aceite somente os comandos que se aplicam ao contexto atual do cliente de entrada-ativo. Ele também serve para evitar colisões de nome de comando entre clientes.

Um cliente também pode solicitar explicitamente para se tornar o cliente de entrada-ativo usando o método [**Activate**](activate-method.md) . Esse método também dá suporte à configuração de seu aplicativo para não ser o cliente de entrada-ativo. Talvez você queira usar esse método quando estiver compartilhando um caractere com outro aplicativo, definindo seu aplicativo como entrada-ativo quando a janela do aplicativo obtém o foco e não a entrada-ativa quando ele perde o foco.

Da mesma forma, você pode usar o método [**Activate**](activate-method.md) para definir seu aplicativo como (ou não) o cliente ativo do caractere. O cliente ativo é o cliente que recebe a entrada quando seu caractere é o caractere mais alto. Quando esse status é alterado, o servidor notifica seu aplicativo com o evento [**ActiveClientChange**](activeclientchange-event.md) .

Quando o menu pop-up de um caractere é exibido, as alterações nas propriedades de uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) ou os comandos em sua coleção não aparecem até que o usuário reexiba o menu. No entanto, a janela comandos exibe as alterações conforme elas acontecem.

-   [Métodos de objeto Commands](commands-object-methods.md)
-   [Propriedades do objeto Commands](commands-object-properties.md)

 

 