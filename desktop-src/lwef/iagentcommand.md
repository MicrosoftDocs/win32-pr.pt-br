---
title: IAgentCommand
description: IAgentCommand
ms.assetid: 70873093-df71-4377-9c39-c7528400052f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42e2288a7b913becc54e2c0baa43eb14903e65fb7eddf6620d5cefbd78968026
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665476"
---
# <a name="iagentcommand"></a>IAgentCommand

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

Um [**objeto Command**](/windows/desktop/lwef/the-command-object) é um item em uma coleção [**De**](/windows/desktop/lwef/the-commands-collection-object) comandos. O servidor fornece ao usuário acesso aos comandos em que seu aplicativo cliente se torna ativo de entrada. Para recuperar um **Comando**, chame [**IAgentCommands::GetCommand.**](iagentcommands--getcommand.md)

**IAgentCommand** define uma interface que permite que os aplicativos definam e consultem propriedades para objetos [**Command**](/windows/desktop/lwef/the-command-object) que podem aparecer no menu pop-up de um caractere e na Janela comandos de voz. Essas funções também estão disponíveis em [**IAgentCommandEx.**](iagentcommandex.md) Um **objeto Command** é um item em uma coleção [**De**](/windows/desktop/lwef/the-commands-collection-object) comandos. O servidor fornece ao usuário acesso aos seus comandos quando seu aplicativo cliente se torna ativo de entrada.

Um [**Comando**](/windows/desktop/lwef/the-command-object) pode aparecer no menu pop-up do caractere e na Janela comandos de voz. Para aparecer no menu pop-up, ele deve ter uma [**Legenda**](caption-property.md) e ter a propriedade [**Visible**](visible-property.md) definida como **True.** A **propriedade Visible** para seu objeto de coleção [**Commands**](/windows/desktop/lwef/the-commands-collection-object) também deve ser definida como **True** para que o comando apareça no menu pop-up quando o aplicativo cliente estiver ativo de entrada. Para aparecer na janela Comandos de Voz, um **comando** deve ter suas [**propriedades VoiceCaption**](voicecaption-property.md) e [**Voice**](voice-property.md) definidas. (Para compatibilidade com backward, se não houver **VoiceCaption**, a **configuração Legenda** será usada.)

As entradas do menu pop-up de um caractere não são alteradas enquanto o menu é exibido. Se você adicionar ou remover Comandos ou alterar suas propriedades enquanto o menu pop-up do caractere for exibido, o menu exibirá essas alterações quando for exibido. No entanto, a Janela Comandos de Voz exibe alterações conforme você as faz.

A tabela a seguir resume como as propriedades de um comando afetam sua apresentação.



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
| Sim              | Não;                    | Sim            | Falso            | Não                                             | Sim, usando [ **Legenda**](caption-property.md)           |
| Sim              | Não;                    | Não;            | Falso            | Não                                             | Não                                                       |
| Não;              | Não;                    | Sim            | True             | Não                                             | Sem ²                                                      |
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



 

 

 