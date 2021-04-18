---
title: IAgentCommand
description: IAgentCommand
ms.assetid: 70873093-df71-4377-9c39-c7528400052f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53c4ba90f7d355a0baa088a78aa05b7a91e14112
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105813316"
---
# <a name="iagentcommand"></a>IAgentCommand

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

Um objeto de [**comando**](/windows/desktop/lwef/the-command-object) é um item em uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) . O servidor fornece o acesso de usuário aos seus comandos que o aplicativo cliente torna a entrada ativa. Para recuperar um **comando**, chame [**IAgentCommands:: GetCommand**](iagentcommands--getcommand.md).

**IAgentCommand** define uma interface que permite que os aplicativos definam e consultem Propriedades para objetos de [**comando**](/windows/desktop/lwef/the-command-object) que podem aparecer no menu pop-up de um caractere e na janela de comandos de voz. Essas funções também estão disponíveis em [**IAgentCommandEx**](iagentcommandex.md). Um objeto de **comando** é um item em uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) . O servidor fornece ao usuário acesso aos seus comandos quando o aplicativo cliente se torna ativo de entrada.

Um [**comando**](/windows/desktop/lwef/the-command-object) pode aparecer no menu pop-up do caractere e na janela de comandos de voz. Para aparecer no menu pop-up, ele deve ter uma [**legenda**](caption-property.md) e ter a propriedade [**Visible**](visible-property.md) definida como **true**. A propriedade **Visible** para seu objeto de coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) também deve ser definida como **true** para que o comando apareça no menu pop-up quando o aplicativo cliente está em entrada-ativo. Para aparecer na janela de comandos de voz, um **comando** deve ter suas propriedades [**VoiceCaption**](voicecaption-property.md) e [**Voice**](voice-property.md) definidas. (Para compatibilidade com versões anteriores, se não houver nenhum **VoiceCaption**, a configuração de **legenda** será usada.)

As entradas do menu pop-up de um caractere não são alteradas enquanto o menu é exibido. Se você adicionar ou remover comandos ou alterar suas propriedades enquanto o menu popup do caractere for exibido, o menu exibirá essas alterações quando reexibida. No entanto, a janela de comandos de voz exibe alterações à medida que você as faz.

A tabela a seguir resume como as propriedades de um comando afetam sua apresentação.



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



 

¹ se a configuração da propriedade for nula. Em algumas linguagens de programação, uma cadeia de caracteres vazia não pode ser interpretada como a mesma que uma cadeia de caracteres nula.

² o comando ainda é acessível por voz.

Em geral, se você definir um [**comando**](/windows/desktop/lwef/the-command-object) com uma configuração de [**voz**](voice-property.md) , também definirá as configurações de [**legenda**](caption-property.md) e de **voz** para sua coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) associada. Se a coleção de **comandos** para um conjunto de comandos não tiver nenhuma configuração de **voz** ou de **legenda** e estiver ativa no momento, mas os **comandos** tiverem configurações de **legenda** e de **voz** , os **comandos** aparecerão no modo de exibição de árvore da janela de comandos de voz em "(comando indefinido)" quando o aplicativo cliente se tornar entrada-ativo.

Quando o servidor recebe entrada que corresponde a um dos objetos de [**comando**](/windows/desktop/lwef/the-command-object) que você definiu para a coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) , ele envia um evento [**IAgentNotifySink:: Command**](https://www.bing.com/search?q=**IAgentNotifySink::Command**) e retorna a ID do comando como um atributo do objeto [**IAgentUserInput**](https://www.bing.com/search?q=**IAgentUserInput**) . Em seguida, você pode usar instruções condicionais para fazer a correspondência e processar o comando.

**Métodos em ordem vtable**



| Métodos IAgentCommand                                                   | Descrição                                                                                                                         |
|-------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**AutoCaption**](https://www.bing.com/search?q=**SetCaption**)                             | Define o valor da [**legenda**](caption-property.md) de um objeto de [**comando**](/windows/desktop/lwef/the-command-object) .                         |
| [**GetCaption**](https://www.bing.com/search?q=**GetCaption**)                             | Retorna o valor da propriedade [**Caption**](caption-property.md) de um objeto [**Command**](/windows/desktop/lwef/the-command-object) .               |
| [**Setvoice**](iagentcommand--setvoice.md)                             | Define o valor do texto de [**voz**](voice-property.md) para um objeto de [**comando**](/windows/desktop/lwef/the-command-object) .                        |
| [**Getvoice**](iagentcommand--getvoice.md)                             | Retorna o valor da propriedade [**Voice**](voice-property.md) de um objeto [**Command**](/windows/desktop/lwef/the-command-object) .                   |
| [**Sethabilitado**](iagentcommand--setenabled.md)                         | Define o valor da propriedade [**Enabled**](enabled-property.md) para um objeto de [**comando**](/windows/desktop/lwef/the-command-object) .                 |
| [**GetEnabled**](iagentcommand--getenabled.md)                         | Retorna o valor da propriedade [**Enabled**](enabled-property.md) de um objeto [**Command**](/windows/desktop/lwef/the-command-object) .               |
| [**Não visível**](iagentcommand--setvisible.md)                         | Define o valor da propriedade [**Visible**](visible-property.md) para um objeto de [**comando**](/windows/desktop/lwef/the-command-object) .                 |
| [**GetVisible**](iagentcommand--getvisible.md)                         | Retorna o valor da propriedade [**Visible**](visible-property.md) de um objeto [**Command**](/windows/desktop/lwef/the-command-object) .               |
| [**SetConfidenceThreshold**](iagentcommand--setconfidencethreshold.md) | Define o valor da propriedade de [**confiança**](confidence-property.md) para um objeto de [**comando**](/windows/desktop/lwef/the-command-object) .           |
| [**GetConfidenceThreshold**](iagentcommand--getconfidencethreshold.md) | Retorna o valor da propriedade [**int**](confidence-property.md) de um objeto [**Command**](/windows/desktop/lwef/the-command-object) .         |
| [**SetConfidenceText**](iagentcommand--setconfidencetext.md)           | Define o valor da propriedade [**ConfidenceText**](confidencetext-property.md) para um objeto de [**comando**](/windows/desktop/lwef/the-command-object) .   |
| [**getConfidenceText**](iagentcommand--getconfidencetext.md)           | Retorna o valor da propriedade [**ConfidenceText**](confidencetext-property.md) de um objeto de [**comando**](/windows/desktop/lwef/the-command-object) . |
| [**getID**](iagentcommand--getid.md)                                   | Retorna a ID de um objeto de [**comando**](/windows/desktop/lwef/the-command-object) .                                                                      |



 

 

 