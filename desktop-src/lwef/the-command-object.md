---
title: O objeto Command
description: O objeto Command
ms.assetid: a757846a-c2d0-4239-9533-babf5dc8399f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 242a90022431b826cf877edd862cd89a39d193865ed31afc1e4ff911f4189756
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118245612"
---
# <a name="the-command-object"></a>O objeto Command

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

Um [**objeto Command**](/windows/desktop/lwef/the-command-object) é um item em uma coleção [**De**](/windows/desktop/lwef/the-commands-collection-object) comandos. O servidor fornece ao usuário acesso aos seus **objetos Command** quando o aplicativo cliente se torna ativo de entrada.

-   [Propriedades do objeto Command](command-object-properties.md)

Para acessar a propriedade de um [**objeto Command,**](/windows/desktop/lwef/the-command-object) você a referencia em sua coleção usando sua [**propriedade**](name-property.md) Name. No VBScript e Visual Basic você pode usar a **propriedade Name** diretamente:


```
   <i>agent</i>.Characters("<i>CharacterID</i>").Commands("<i>Name</i>").<i>property</i> [= <i>value</i>]
```



Para linguagens de programação que não são suportadas por coleções, use o [**método Command:**](command-method.md)


```
   <i>agent</i>.Characters("<i>CharacterID</i>").Commands.Command("<i>Name</i>").<i>property</i> [= <i>value</i>]
```



Você também pode referenciar um objeto Command criando uma referência a ele. Em Visual Basic, declare uma variável de objeto e use a instrução Set para criar a referência:


```
   Dim Cmd1 as Object
   ...
   Set Cmd1 = Agent.Characters("MyCharacterID").Commands("SampleCommand")
   ...
   Cmd1.Enabled = True
```



No Visual Basic 5.0, você também pode declarar o objeto como tipo [**IAgentCtlCommandEx**](https://www.bing.com/search?q=**IAgentCtlCommandEx**) e criar a referência. Essa convenção permite a associação antecipada, o que resulta em um melhor desempenho:


```
   Dim Cmd1 as IAgentCtlCommandEx
   ...
   Set Cmd1 = Agent.Characters("MyCharacterID").Commands("SampleCommand")
   ...
   Cmd1.Enabled = True
```



No VBScript, você pode declarar uma referência como um tipo específico, mas ainda pode declarar a variável e defini-la como o [**Comando**](/windows/desktop/lwef/the-command-object) na coleção:


```
   Dim Cmd1
   ...
   Set Cmd1 = Agent.Characters("MyCharacterID").Commands("SampleCommand")
   ...
   Cmd1.Enabled = True
```



Um comando pode aparecer no menu pop-up do caractere e na Janela Comandos ou em ambos. Para aparecer no menu pop-up, ele deve ter uma legenda e ter a propriedade [**Visible**](visible-property.md) definida como **True.** Além disso, sua propriedade Visible do objeto de coleção **Commands** também deve ser definida como **True.** Para aparecer na janela Comandos, um [**comando**](/windows/desktop/lwef/the-command-object) deve ter suas propriedades [**Caption**](caption-property.md) e [**Voice**](voice-property.md) definidas. Observe que as entradas do menu pop-up de um caractere não são mudadas enquanto o menu é exibido. Se você adicionar ou remover comandos ou alterar suas propriedades enquanto o menu pop-up do caractere é exibido, o menu exibirá essas alterações sempre que o usuário a exibir em seguida. No entanto, a janela Comandos reflete dinamicamente as alterações feitas.

A tabela a seguir resume como as propriedades de um [**comando afetam**](/windows/desktop/lwef/the-command-object) sua apresentação:



Propriedade Caption

Voice-Caption propriedade

Propriedade Voice

Propriedade Visible

Propriedade Enabled

Aparece no menu pop-up do caractere

Aparece na janela Comandos

Sim

Sim

Sim

True

True

Normal, usando [ **Legenda**](caption-property.md)

Sim, usando [ **VoiceCaption**](voicecaption-property.md)

Sim

Sim

Sim

True

Falso

Desabilitado, usando [ **Legenda**](caption-property.md)

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

Normal, usando [ **Legenda**](caption-property.md)

Não

Sim

Sim

Não 

True

Falso

Desabilitado, usando [ **Legenda**](caption-property.md)

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

 Se a configuração de propriedade for nula. Em algumas linguagens de programação, uma cadeia de caracteres vazia pode não ser interpretada da mesma forma que uma cadeia de caracteres nula.  O comando ainda é acessível por voz.<br/>



 

Quando o servidor recebe a entrada de um de seus comandos, ele envia um evento [**Command**](/windows/desktop/lwef/the-command-object) e passa o nome do **Comando** como um atributo do [**objeto UserInput.**](/windows/desktop/lwef/iagentuserinput) Em seguida, você pode usar instruções condicionais para corresponder e processar o **Comando**.

 

