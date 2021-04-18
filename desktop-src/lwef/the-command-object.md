---
title: O objeto Command
description: O objeto Command
ms.assetid: a757846a-c2d0-4239-9533-babf5dc8399f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e9e9ce22b3a1c0c2286232b5e2204e158501332
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105785266"
---
# <a name="the-command-object"></a>O objeto Command

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

Um objeto de [**comando**](/windows/desktop/lwef/the-command-object) é um item em uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) . O servidor fornece ao usuário acesso aos objetos de **comando** quando o aplicativo cliente se torna ativo.

-   [Propriedades do objeto de comando](command-object-properties.md)

Para acessar a propriedade de um objeto de [**comando**](/windows/desktop/lwef/the-command-object) , você faz referência a ela em sua coleção usando sua propriedade [**Name**](name-property.md) . No VBScript e Visual Basic você pode usar a propriedade **Name** diretamente:


```
   <i>agent</i>.Characters("<i>CharacterID</i>").Commands("<i>Name</i>").<i>property</i> [= <i>value</i>]
```



Para linguagens de programação que não dão suporte a coleções, use o método de [**comando**](command-method.md) :


```
   <i>agent</i>.Characters("<i>CharacterID</i>").Commands.Command("<i>Name</i>").<i>property</i> [= <i>value</i>]
```



Você também pode fazer referência a um objeto de comando criando uma referência a ele. Em Visual Basic, declare uma variável de objeto e use a instrução SET para criar a referência:


```
   Dim Cmd1 as Object
   ...
   Set Cmd1 = Agent.Characters("MyCharacterID").Commands("SampleCommand")
   ...
   Cmd1.Enabled = True
```



No Visual Basic 5,0, você também pode declarar o objeto como o tipo [**IAgentCtlCommandEx**](https://www.bing.com/search?q=**IAgentCtlCommandEx**) e criar a referência. Essa convenção habilita a ligação antecipada, o que resulta em um melhor desempenho:


```
   Dim Cmd1 as IAgentCtlCommandEx
   ...
   Set Cmd1 = Agent.Characters("MyCharacterID").Commands("SampleCommand")
   ...
   Cmd1.Enabled = True
```



No VBScript, você pode declarar uma referência como um tipo específico, mas ainda pode declarar a variável e defini-la para o [**comando**](/windows/desktop/lwef/the-command-object) na coleção:


```
   Dim Cmd1
   ...
   Set Cmd1 = Agent.Characters("MyCharacterID").Commands("SampleCommand")
   ...
   Cmd1.Enabled = True
```



Um comando pode aparecer no menu pop-up do caractere e na janela comandos ou em ambos. Para aparecer no menu pop-up, ele deve ter uma legenda e ter a propriedade [**Visible**](visible-property.md) definida como **true**. Além disso, sua propriedade **Visible** do objeto de coleção de comandos também deve ser definida como **true**. Para aparecer na janela comandos, um [**comando**](/windows/desktop/lwef/the-command-object) deve ter suas propriedades [**Caption**](caption-property.md) e [**Voice**](voice-property.md) definidas. Observe que as entradas de menu pop-up de um caractere não são alteradas enquanto o menu é exibido. Se você adicionar ou remover comandos ou alterar suas propriedades enquanto o menu pop-up do caractere for exibido, o menu exibirá essas alterações sempre que o usuário o exibir. No entanto, a janela comandos reflete dinamicamente todas as alterações feitas.

A tabela a seguir resume como as propriedades de um [**comando**](/windows/desktop/lwef/the-command-object) afetam sua apresentação:



Propriedade Caption

Propriedade Voice-Caption

Propriedade de voz

Propriedade Visible

Propriedade Enabled

Aparece no menu pop-up do caractere

Aparece na janela de comandos

Sim

Sim

Sim

True

True

Normal, usando [ **legenda**](caption-property.md)

Sim, usando [ **VoiceCaption**](voicecaption-property.md)

Sim

Sim

Sim

True

Falso

Desabilitado, usando [ **legenda**](caption-property.md)

Não

Sim

Sim

Sim

Falso

True

Não aparece

Sim, usando [ **VoiceCaption**](voicecaption-property.md)

Sim

Sim

Sim

Falso

Falso

Não aparece

Não

Sim

Sim

Não 

True

True

Normal, usando [ **legenda**](caption-property.md)

Não

Sim

Sim

Não 

True

Falso

Desabilitado, usando [ **legenda**](caption-property.md)

Não

Sim

Sim

Não 

Falso

True

Não aparece

Não

Sim

Sim

Não 

Falso

Falso

Não aparece

Não

Não 

Sim

Sim

True

True

Não aparece

Sim, usando [ **VoiceCaption**](voicecaption-property.md)

Não 

Sim

Sim

True

Falso

Não aparece

Não

Não 

Sim

Sim

Falso

True

Não aparece

Sim, usando [ **VoiceCaption**](voicecaption-property.md)

Não 

Sim

Sim

Falso

Falso

Não aparece

Não

Não 

Sim

Não 

True

True

Não aparece

Não

Não 

Sim

Não 

True

Falso

Não aparece

Não

Não 

Sim

Não 

Falso

True

Não aparece

Não

Não 

Sim

Não 

Falso

Falso

Não aparece

Não

Sim

Não 

Sim

True

True

Normal, usando [ **legenda**](caption-property.md)

Sim, usando [ **legenda**](caption-property.md)

Sim

Não 

Sim

True

Falso

Desabilitado, usando [ **legenda**](caption-property.md)

Não

Sim

Não 

Sim

Falso

True

Não aparece

Sim, usando [ **legenda**](caption-property.md)

Sim

Não 

Sim

Falso

Falso

Não aparece

Não

Sim

Não 

Não 

True

True

Normal, usando [ **legenda**](caption-property.md)

Não

Sim

Não 

Não 

True

Falso

Desabilitado, usando [ **legenda**](caption-property.md)

Não

Sim

Não 

Não 

Falso

True

Não aparece

Não

Sim

Não 

Não 

Falso

Falso

Não aparece

Não

Não 

Não 

Sim

True

True

Não aparece

Não 

Não 

Não 

Sim

True

Falso

Não aparece

Não

Não 

Não 

Sim

Falso

True

Não aparece

Não 

Não 

Não 

Sim

Falso

Falso

Não aparece

Não

Não 

Não 

Não 

True

True

Não aparece

Não

Não 

Não 

Não 

True

Falso

Não aparece

Não

Não 

Não 

Não 

Falso

True

Não aparece

Não

Não 

Não 

Não 

Falso

Falso

Não aparece

Não

 Se a configuração da propriedade for nula. Em algumas linguagens de programação, uma cadeia de caracteres vazia não pode ser interpretada da mesma forma que uma cadeia de caracteres nula.  O comando ainda é acessível por voz.<br/>



 

Quando o servidor recebe entrada para um de seus comandos, ele envia um evento de [**comando**](/windows/desktop/lwef/the-command-object) e retorna o nome do **comando** como um atributo do objeto [**userinput**](/windows/desktop/lwef/iagentuserinput) . Em seguida, você pode usar instruções condicionais para fazer a correspondência e processar o **comando**.

 

