---
title: IAgentCommands
description: IAgentCommands
ms.assetid: a171a2f0-7c1c-440f-9b19-28447cc68b95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1fc57b7e2e5f628708f46ace98700605f1eb5d7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104499036"
---
# <a name="iagentcommands"></a>IAgentCommands

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

O servidor do Microsoft Agent mantém uma lista de comandos que estão disponíveis atualmente para o usuário. Essa lista inclui comandos que o servidor define para interação geral, como ocultar e propriedades do Microsoft Agent, a lista de clientes disponíveis (mas que não são de entrada ativa) e os comandos definidos pelo cliente ativo atual. Os dois primeiros conjuntos de comandos são comandos globais; ou seja, eles estão disponíveis a qualquer momento, independentemente do cliente de entrada-ativo. Comandos definidos pelo cliente estão disponíveis somente quando esse cliente está em entrada-ativo.

Recupere uma interface **IAgentCommands** consultando a interface [**IAgentCharacter**](https://www.bing.com/search?q=**IAgentCharacter**) para **IAgentCommands**. Cada aplicativo cliente do Microsoft Agent pode definir uma coleção de comandos chamada coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) . Para adicionar um [**comando**](/windows/desktop/lwef/the-command-object) à coleção, use o método [**Add**](add-method.md) ou [**Insert**](insert-method.md) . Embora você possa especificar as propriedades de um **comando** usando métodos [**IAgentCommand**](iagentcommand.md) , para o desempenho de código ideal, especifique todas as propriedades de um **comando** nos métodos [**IAgentCommands:: Add**](iagentcommands--add.md) ou [**IAgentCommands:: Insert**](iagentcommands--insert.md) ao definir inicialmente as propriedades para um novo **comando**. Você pode usar os métodos **IAgentCommand** para consultar ou alterar as configurações de propriedade.

Para cada [**comando**](/windows/desktop/lwef/the-command-object) na coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) , você pode determinar se o comando aparece no menu pop-up do caractere, na janela comandos de voz, em ambos ou em nenhum deles. Por exemplo, se você quiser que um comando apareça no menu pop-up para o caractere, defina a [**legenda**](caption-property.md) do comando e as propriedades [**visíveis**](visible-property.md) . Para exibir o comando na **janela comandos de voz**, defina a **legenda** do comando e as propriedades de [**voz**](voice-property.md) .

Um usuário pode acessar os comandos individuais em sua coleção de comandos somente quando o aplicativo cliente é de entrada-ativo e o caractere é visível. Portanto, normalmente você desejará definir as propriedades [**Caption**](caption-property.md), [**VoiceCaption**](voicecaption-property.md)e [**Voice**](voice-property.md) para o objeto da coleção [**Commands**](/windows/desktop/lwef/the-commands-collection-object) , bem como para os comandos na coleção, porque isso coloca uma entrada para a coleção de **comandos** no menu pop-up de um caractere e na janela de comandos de voz. Quando o usuário alterna para o cliente escolhendo sua entrada de **comandos** , o servidor automaticamente torna o cliente de entrada-ativo, notificando o aplicativo cliente usando o [**IAgentNotifySink:: ActivateInputState**](https://www.bing.com/search?q=**IAgentNotifySink::ActivateInputState**) e disponibiliza os **comandos** em sua coleção. O servidor também notifica o cliente que não está mais em entrada-ativo com o evento **IAgentNotifySink:: ActivateInputState** . Isso permite que o servidor apresente e aceite somente os **comandos** que se aplicam ao contexto atual do cliente de entrada-ativo. Ele também serve para evitar colisões de nome de [**comando**](/windows/desktop/lwef/the-command-object)entre clientes.

Um cliente também pode solicitar explicitamente para se tornar o cliente de entrada-ativo usando o método [**IAgentCharacter:: Activate**](iagentcharacter--activate.md) . Esse método também dá suporte à configuração de seu aplicativo para não ser o cliente de entrada-ativo. Talvez você queira usar esse método ao compartilhar um caractere com outro aplicativo, definindo seu aplicativo como entrada-ativo quando a janela do aplicativo fica em foco e não entrada-ativa quando perde o foco.

Da mesma forma, você pode usar [**IAgentCharacter:: Activate**](iagentcharacter--activate.md) para definir seu aplicativo como (ou não) o cliente ativo do caractere. O cliente ativo é o cliente que recebe a entrada quando seu caractere é o caractere mais alto. Quando esse status é alterado, o servidor notifica seu aplicativo com o evento [**IAgentNotifySinkEx:: ActiveClientChange**](iagentnotifysinkex--activeclientchange.md) .

Quando o menu pop-up de um caractere é exibido, as alterações nas propriedades de uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) ou os comandos em sua coleção não aparecem até que o usuário reexiba o menu. No entanto, quando aberto, a janela de comandos de voz exibe as alterações conforme elas acontecem.

**IAgentCommands** define uma interface que permite que os aplicativos adicionem, removam, definam e consultem Propriedades para uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) . Essas funções também estão disponíveis em [**IAgentCommandsEx**](iagentcommandsex.md).

Uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) pode aparecer como um comando no menu pop-up e na janela de comandos de voz para um caractere. Para fazer a coleção de **comandos** aparecer, você deve definir sua propriedade [**Caption**](caption-property.md) . A tabela a seguir resume como as propriedades de uma coleção de **comandos** afetam sua apresentação.



| Propriedade Caption | Propriedade Voice-Caption | Propriedade de voz | Propriedade Visible | Aparece no menu pop-up do caractere             | Aparece na janela de comandos de voz                         |
|------------------|------------------------|----------------|------------------|------------------------------------------------|----------------------------------------------------------|
| Sim              | Sim                    | Sim            | True             | Sim, usando [ **legenda**](caption-property.md) | Sim, usando [ **VoiceCaption**](voicecaption-property.md) |
| Sim              | Sim                    | Sem ¹            | True             | Sim, usando [ **legenda**](caption-property.md) | Não                                                       |
| Sim              | Sim                    | Sim            | Falso            | Não                                             | Sim, usando [ **VoiceCaption**](voicecaption-property.md) |
| Sim              | Sim                    | Sem ¹            | Falso            | Não                                             | Não                                                       |
| Sem ¹              | Sim                    | Sim            | True             | Não                                             | Sim, usando [ **VoiceCaption**](voicecaption-property.md) |
| Sem ¹              | Sim                    | Sim            | Falso            | Não                                             | Sim, usando [ **VoiceCaption**](voicecaption-property.md) |
| Sem ¹              | Sim                    | Sem ¹            | True             | Não                                             | Não                                                       |
| Sem ¹              | Sim                    | Sem ¹            | Falso            | Não                                             | Não                                                       |
| Sim              | Sem ¹                    | Sim            | True             | Sim, usando [ **legenda**](caption-property.md) | Sim, usando [ **legenda**](caption-property.md)           |
| Sim              | Sem ¹                    | Sem ¹            | True             | Sim                                            | Não                                                       |
| Sim              | Sem ¹                    | Sim            | Falso            | Não                                             | Sim, usando [ **legenda**](caption-property.md)           |
| Sim              | Sem ¹                    | Sem ¹            | Falso            | Não                                             | Não                                                       |
| Sem ¹              | Sem ¹                    | Sim            | True             | Não                                             | Sem ²                                                      |
| Sem ¹              | Sem ¹                    | Sim            | Falso            | Não                                             | Sem ²                                                      |
| Sem ¹              | Sem ¹                    | Sem ¹            | True             | Não                                             | Não                                                       |
| Sem ¹              | Sem ¹                    | Sem ¹            | Falso            | Não                                             | Não                                                       |



 

¹ se a configuração da propriedade for nula. Em algumas linguagens de programação, uma cadeia de caracteres vazia não pode ser interpretada da mesma forma que uma cadeia de caracteres nula.

² o comando ainda é acessível por voz.

**Métodos em ordem vtable**



| Métodos IAgentCommands                           | Descrição                                                                                                                      |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**GetCommand**](iagentcommands--getcommand.md) | Recupera um objeto de [**comando**](/windows/desktop/lwef/the-command-object) da coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .              |
| [**GetCount**](iagentcommands--getcount.md)     | Retorna o valor do número de [**comandos**](/windows/desktop/lwef/the-command-object) em uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) . |
| [**AutoCaption**](iagentcommands--setcaption.md) | Define o valor da propriedade [**Caption**](caption-property.md) para uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .    |
| [**GetCaption**](iagentcommands--getcaption.md) | Retorna o valor da propriedade [**Caption**](caption-property.md) de uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .  |
| [**Setvoice**](iagentcommands--setvoice.md)     | Define o valor da propriedade de [**voz**](voice-property.md) para uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .        |
| [**Getvoice**](iagentcommands--getvoice.md)     | Retorna o valor da propriedade [**Voice**](voice-property.md) de uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .      |
| [**Não visível**](iagentcommands--setvisible.md) | Define o valor da propriedade [**Visible**](visible-property.md) para uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .    |
| [**GetVisible**](iagentcommands--getvisible.md) | Retorna o valor da propriedade [**Visible**](visible-property.md) de uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .  |
| [**Adicionar**](iagentcommands--add.md)               | Adiciona um objeto de [**comando**](/windows/desktop/lwef/the-command-object) a uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .                       |
| [**Inserido**](iagentcommands--insert.md)         | Insere um objeto de [**comando**](/windows/desktop/lwef/the-command-object) em uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .                    |
| [**Remover**](iagentcommands--remove.md)         | Remove um objeto de [**comando**](/windows/desktop/lwef/the-command-object) em uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .                    |
| [**RemoveAll**](iagentcommands--removeall.md)   | Remove todos os objetos de [**comando**](/windows/desktop/lwef/the-command-object) de uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .               |



 

 

 