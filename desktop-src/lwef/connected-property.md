---
title: Propriedade Connected
description: Propriedade Connected
ms.assetid: 61b7f550-d8d6-4719-a0d4-0bf3a8cf096c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6af3a44e97236060733adc55ec6e44eddd0b1d8879250b2a28b54c0bca384cac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726086"
---
# <a name="connected-property"></a>Propriedade Connected

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**
</dt> <dd>

Retorna ou define se o controle atual está conectado ao servidor do Microsoft Agent.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agent.***Connected* *  \[  =  *booliana*\]



| Parte      | Descrição                                                                                                     |
|-----------|-----------------------------------------------------------------------------------------------------------------|
| *booleano* | Uma expressão booliana que especifica se o controle está conectado. **True** O controle está conectado.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Em muitas situações, especificar o controle cria automaticamente uma conexão com o servidor do Microsoft Agent. Por exemplo, especificar o CLSID do controle do Microsoft Agent na marca em uma página da Web abre automaticamente uma conexão de servidor e sair da página <OBJECT> fecha a conexão. Da mesma forma, para Visual Basic ou outros idiomas que permitem que você solte um controle em um formulário, a execução do programa abre automaticamente uma conexão e a saída do programa fecha a conexão. Se o servidor não estiver em execução no momento, ele será iniciado automaticamente.

No entanto, se você quiser criar um controle do Agent em tempo de executar, talvez também seja necessário abrir explicitamente uma nova conexão com o servidor usando a **propriedade Connected.** Por exemplo, no Visual Basic você pode criar um objeto ActiveX em tempo de executar usando a instrução Set com a palavra-chave **New** (ou função CreateObject). Embora isso crie o objeto , ele pode não criar a conexão com o servidor. Você pode usar a **propriedade Connected** antes de qualquer código que chama a interface de programação do Microsoft Agent, conforme mostrado no exemplo a seguir:


```
   ' Declare a global variable for the control
   Dim MyAgent as Agent

   ' Create an instance of the control using New
   Set MyAgent = New Agent

   ' Open a connection to the server
   MyAgent.Connected = True

   ' Load a character
   MyAgent.Characters.Load "Genie", " Genie.acs"

   ' Display the character
   MyAgent.Characters("Genie").Show
```



A criação de um controle usando essa técnica não expõe os eventos do controle Agent. No Visual Basic 5.0 (e posterior), você pode acessar os eventos do controle incluindo o controle nas referências do projeto e usar a palavra-chave **WithEvents** em sua declaração de variável:


```
   Dim WithEvents MyAgent as Agent

   ' Create an instance of the control using New
   Set MyAgent = New Agent
```



Usar **WithEvents para** criar uma instância do controle Agent em tempo de executar abre automaticamente a conexão com o servidor do Microsoft Agent. Portanto, você não precisa incluir uma **instrução Connected.**

Você pode fechar sua conexão com o servidor liberando todas as referências criadas para objetos do Agent, como IAgentCtlCharacterEx e IAgentCtlCommandEx. Você também deve liberar sua referência para o próprio controle do Agent. No Visual Basic, você pode liberar uma referência a um objeto definindo sua variável como **Nothing.** Se você tiver carregado caracteres, descarregue-os antes de liberar o objeto de caractere.


```
   Dim WithEvents MyAgent as Agent
   Dim Genie as IAgentCtlCharacterEx
   
   Sub Form_Load

   ' Create an instance of the control using New
   Set MyAgent = New Agent

   ' Open a connection to the server
   MyAgent.Connected = True

   ' Load the character into the Characters collection
   MyAgent.Characters.Load "Genie", " Genie.acs"

   ' Create a reference to the character
   Set Genie = MyAgent.Characters("Genie")

   End Sub

   Sub CloseConnection

   ' Unload the character
   MyAgent.Characters.Unload "Genie"

   ' Release the reference to the character object
   Set Genie = Nothing

   ' Release the reference to the Agent control
   Set MyAgent = Nothing
   End Sub
```



> [!Note]  
> Não é possível fechar sua conexão com o servidor liberando referências em que o componente foi adicionado. Por exemplo, você não pode fechar sua conexão com o servidor em páginas da Web em que você usa a marca para declarar o controle ou em um aplicativo Visual Basic em que você solta o controle em <OBJECT> um formulário. Ao liberar todas as referências do Agent reduzirá o conjunto de trabalho do Agent, a conexão permanecerá até que você navegue até a próxima página ou saia do aplicativo.

 

 

 





