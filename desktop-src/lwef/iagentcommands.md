---
title: IAgentCommands
description: IAgentCommands
ms.assetid: a171a2f0-7c1c-440f-9b19-28447cc68b95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a1bcc40f80e9a10301ec305fdc3e8f3e83984ceb0de5d36121e13c3d823b8a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961886"
---
# <a name="iagentcommands"></a>IAgentCommands

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

O servidor do Microsoft Agent mantém uma lista de comandos que estão disponíveis no momento para o usuário. Essa lista inclui comandos que o servidor define para interação geral, como Ocultar e Propriedades do Microsoft Agent, a lista de clientes disponíveis (mas não ativos de entrada) e os comandos definidos pelo cliente ativo atual. Os dois primeiros conjuntos de comandos são comandos globais; ou seja, eles estão disponíveis a qualquer momento, independentemente do cliente ativo de entrada. Comandos definidos pelo cliente estão disponíveis somente quando esse cliente está ativo de entrada.

Recupere uma interface **IAgentCommands** consultando a interface [**IAgentCharacter**](https://www.bing.com/search?q=**IAgentCharacter**) para **IAgentCommands.** Cada aplicativo cliente do Microsoft Agent pode definir uma coleção de comandos chamada coleção [**Commands.**](/windows/desktop/lwef/the-commands-collection-object) Para adicionar um [**Comando**](/windows/desktop/lwef/the-command-object) à coleção, use o [**método Add**](add-method.md) [**ou Insert.**](insert-method.md) Embora você possa  especificar as propriedades de um comando usando métodos [**IAgentCommand,**](iagentcommand.md) para um desempenho de código ideal, especifique todas as propriedades de um comando nos métodos [**IAgentCommands::Add**](iagentcommands--add.md) ou [**IAgentCommands::Insert**](iagentcommands--insert.md) ao definir inicialmente as propriedades para um novo **Comando**.  Você pode usar os **métodos IAgentCommand** para consultar ou alterar as configurações de propriedade.

Para cada [**Comando**](/windows/desktop/lwef/the-command-object) na coleção [**Comandos,**](/windows/desktop/lwef/the-commands-collection-object) você pode determinar se o comando aparece no menu pop-up do caractere, na Janela Comandos de Voz, em ambos ou em nenhum deles. Por exemplo, se você quiser que um comando apareça no menu pop-up do caractere, de definir as propriedades [**Legenda**](caption-property.md) e Visível [**do**](visible-property.md) comando. Para exibir o comando na Janela **Comandos de Voz**, de definido as propriedades **Legenda** e [**Voz do**](voice-property.md) comando.

Um usuário pode acessar os comandos individuais em sua coleção De comandos somente quando o aplicativo cliente estiver ativo de entrada e o caractere estiver visível. Portanto, normalmente, você deseja definir as propriedades [**Caption**](caption-property.md), [**VoiceCaption**](voicecaption-property.md)e [**Voice**](voice-property.md) para o objeto de coleção [**Commands,**](/windows/desktop/lwef/the-commands-collection-object) bem como para os comandos na coleção, porque isso coloca uma entrada para sua coleção **de** Comandos no menu pop-up de um caractere e na Janela comandos de voz. Quando o usuário alterna para  seu cliente escolhendo sua entrada Comandos, o servidor torna automaticamente o cliente ativo de entrada, notificando seu aplicativo cliente usando [**IAgentNotifySink::ActivateInputState**](https://www.bing.com/search?q=**IAgentNotifySink::ActivateInputState**) e disponibiliza os Comandos em sua coleção.  O servidor também notifica o cliente que não é mais input-active com o **evento IAgentNotifySink::ActivateInputState.** Isso permite que o servidor apresente e aceite apenas os **Comandos** que se aplicam ao contexto atual do cliente de entrada ativa. Ele também serve para evitar [**colisões de nome**](/windows/desktop/lwef/the-command-object)de comando entre clientes.

Um cliente também pode solicitar explicitamente para se tornar o cliente ativo de entrada usando o [**método IAgentCharacter::Activate.**](iagentcharacter--activate.md) Esse método também dá suporte à configuração do aplicativo para não ser o cliente ativo de entrada. Talvez você queira usar esse método ao compartilhar um caractere com outro aplicativo, definindo seu aplicativo como input-active quando a janela do aplicativo obtém o foco e não a entrada ativa quando ele perde o foco.

Da mesma forma, você pode usar [**IAgentCharacter::Activate**](iagentcharacter--activate.md) para definir seu aplicativo como (ou não) o cliente ativo do caractere. O cliente ativo é o cliente que recebe entrada quando seu caractere é o caractere mais alto. Quando esse status muda, o servidor notifica seu aplicativo com o [**evento IAgentNotifySinkEx::ActiveClientChange.**](iagentnotifysinkex--activeclientchange.md)

Quando o menu pop-up de um caractere é exibido, as alterações nas propriedades de uma coleção [**de**](/windows/desktop/lwef/the-commands-collection-object) Comandos ou dos comandos em sua coleção não aparecem até que o usuário replay o menu. No entanto, quando aberta, a Janela Comandos de Voz exibe alterações conforme elas ocorrem.

**IAgentCommands** define uma interface que permite que os aplicativos adicionem, removam, definam e consultem propriedades para uma coleção [**de Comandos.**](/windows/desktop/lwef/the-commands-collection-object) Essas funções também estão disponíveis em [**IAgentCommandsEx.**](iagentcommandsex.md)

Uma [**coleção**](/windows/desktop/lwef/the-commands-collection-object) comandos pode aparecer como um comando no menu pop-up e na Janela comandos de voz para um caractere. Para fazer com **que a coleção Comandos** apareça, você deve definir sua propriedade [**Caption.**](caption-property.md) A tabela a seguir resume como as propriedades de uma coleção **de Comandos** afetam sua apresentação.



| Propriedade Caption | Voice-Caption propriedade | Propriedade Voice | Propriedade Visible | Aparece no menu pop-up do caractere             | Aparece na janela Comandos de Voz                         |
|------------------|------------------------|----------------|------------------|------------------------------------------------|----------------------------------------------------------|
| Sim              | Sim                    | Sim            | Verdadeiro             | Sim, usando [ **Legenda**](caption-property.md) | Sim, usando [ **VoiceCaption**](voicecaption-property.md) |
| Sim              | Sim                    | Não;            | Verdadeiro             | Sim, usando [ **Legenda**](caption-property.md) | Não                                                       |
| Sim              | Sim                    | Sim            | Falso            | Não                                             | Sim, usando [ **VoiceCaption**](voicecaption-property.md) |
| Sim              | Sim                    | Não;            | Falso            | Não                                             | Não                                                       |
| Não;              | Sim                    | Sim            | True             | Não                                             | Sim, usando [ **VoiceCaption**](voicecaption-property.md) |
| Não;              | Sim                    | Sim            | Falso            | Não                                             | Sim, usando [ **VoiceCaption**](voicecaption-property.md) |
| Não;              | Sim                    | Não;            | True             | Não                                             | Não                                                       |
| Não;              | Sim                    | Não;            | Falso            | Não                                             | Não                                                       |
| Sim              | Não;                    | Sim            | Verdadeiro             | Sim, usando [ **Legenda**](caption-property.md) | Sim, usando [ **Legenda**](caption-property.md)           |
| Sim              | Não;                    | Não;            | True             | Sim                                            | Não                                                       |
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



 

 

 