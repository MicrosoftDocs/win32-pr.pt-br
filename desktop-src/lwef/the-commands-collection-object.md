---
title: O objeto de coleção commands
description: O objeto de coleção commands
ms.assetid: 8726ce04-77d3-4ae3-bd46-e75f42b36d6f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d30f7933bd973ae500b75abb51c47899fa60322444d49fe0835f6bfa3efab97f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975656"
---
# <a name="the-commands-collection-object"></a>O objeto de coleção commands

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

O servidor do Microsoft Agent mantém uma lista de comandos que estão disponíveis no momento para o usuário. Essa lista inclui comandos que o servidor define para interação geral (como Ocultar e Abrir a Janela comandos de voz), a lista de clientes disponíveis (mas não ativos de entrada) e os comandos definidos pelo cliente ativo atual. Os dois primeiros conjuntos de comandos são comandos globais; ou seja, eles estão disponíveis a qualquer momento, independentemente do cliente ativo de entrada. Os comandos definidos pelo cliente estão disponíveis somente quando esse cliente está ativo de entrada e o caractere está visível.

Cada aplicativo cliente pode definir uma coleção de comandos chamada [**coleção Commands.**](/windows/desktop/lwef/the-commands-collection-object) Para adicionar um comando à coleção, use o [**método Add**](add-method.md) [**ou Insert.**](insert-method.md) Embora você possa especificar as propriedades de um comando com instruções separadas, para um desempenho de código ideal, especifique todas as propriedades de um comando na **instrução Adicionar** ou **Inserir método.** Para cada comando na coleção, você pode determinar se o acesso do usuário ao comando aparece no menu pop-up do caractere, na Janela Comandos de Voz, em ambos ou em nenhum deles. Por exemplo, se você quiser que um comando apareça no menu pop-up do caractere, de definir as propriedades [**Legenda**](caption-property.md) e Visível [**do**](visible-property.md) comando. Para exibir o comando na Janela Comandos de Voz, de definir as propriedades [**VoiceCaption**](voicecaption-property.md) e [**Voice do**](voice-property.md) comando.

Um usuário pode acessar os Comandos e comandos [**de**](/windows/desktop/lwef/the-commands-collection-object)comunicação individuais em sua coleção somente quando o aplicativo cliente estiver ativo de entrada. Portanto, quando você pode estar compartilhando o caractere com outros aplicativos cliente, normalmente você deseja definir as propriedades [**Caption,**](caption-property.md) [**VoiceCaption**](voicecaption-property.md)e [**Voice**](voice-property.md) para o objeto de coleção **Commands,** bem como para os comandos na coleção. Isso coloca uma entrada para a **coleção Comandos** no menu pop-up de um caractere e na Janela Comandos de Voz.

Quando o usuário alterna para [](/windows/desktop/lwef/the-commands-collection-object) seu cliente escolhendo sua entrada Comandos, o servidor torna automaticamente seu cliente de entrada ativo, notificando seu aplicativo cliente usando o evento [**ActivateInput**](activateinput-event.md) e disponibiliza os comandos em sua coleção. O servidor também notifica o cliente de que ele não é mais input-active com [**o evento DeActivateInput.**](deactivateinput-event.md) Isso permite que o servidor apresente e aceite apenas os comandos que se aplicam ao contexto atual do cliente de entrada ativa. Ele também serve para evitar colisões de nome de comando entre clientes.

Um cliente também pode solicitar explicitamente para se tornar o cliente ativo de entrada usando o [**método Activate.**](activate-method.md) Esse método também dá suporte à configuração do aplicativo para não ser o cliente ativo de entrada. Talvez você queira usar esse método ao compartilhar um caractere com outro aplicativo, definindo seu aplicativo como ativo de entrada quando a janela do aplicativo obtém o foco e não a entrada ativa quando ele perde o foco.

Da mesma forma, você pode usar o [**método Activate**](activate-method.md) para definir seu aplicativo como (ou não) o cliente ativo do caractere. O cliente ativo é o cliente que recebe entrada quando seu caractere é o caractere mais alto. Quando esse status muda, o servidor notifica seu aplicativo com o [**evento ActiveClientChange.**](activeclientchange-event.md)

Quando o menu pop-up de um caractere é exibido, as alterações nas propriedades de uma coleção [**de**](/windows/desktop/lwef/the-commands-collection-object) Comandos ou dos comandos em sua coleção não aparecem até que o usuário replay o menu. No entanto, a Janela Comandos exibe alterações conforme elas ocorrem.

-   [Métodos de objeto Commands](commands-object-methods.md)
-   [Propriedades do objeto Commands](commands-object-properties.md)

 

 