---
title: Propriedade conectada
description: Propriedade conectada
ms.assetid: 61b7f550-d8d6-4719-a0d4-0bf3a8cf096c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bba78358c7c42f0754da017aa0c188d41acd189
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292461"
---
# <a name="connected-property"></a>Propriedade conectada

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Retorna ou define se o controle atual está conectado ao servidor do Microsoft Agent.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*Agent. * * * conectado* *  \[  =  *valor booleano*\]



| Parte      | Descrição                                                                                                     |
|-----------|-----------------------------------------------------------------------------------------------------------------|
| *booleano* | Uma expressão booliana que especifica se o controle está conectado. **Verdadeiro** O controle está conectado.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Em muitas situações, especificar o controle cria automaticamente uma conexão com o servidor do Microsoft Agent. Por exemplo, especificar o CLSID do controle do Microsoft Agent na <OBJECT> marca em uma página da Web abre automaticamente uma conexão de servidor e sair da página fecha a conexão. Da mesma forma, para Visual Basic ou outras linguagens que permitem que você descarte um controle em um formulário, executar o programa abre automaticamente uma conexão e sair do programa fecha a conexão. Se o servidor não estiver em execução no momento, ele será iniciado automaticamente.

No entanto, se você quiser criar um controle de agente em tempo de execução, talvez também seja necessário abrir explicitamente uma nova conexão com o servidor usando a propriedade **Connected** . Por exemplo, no Visual Basic você pode criar um objeto ActiveX em tempo de execução usando a instrução SET com a **nova** palavra-chave (ou função CreateObject). Embora isso crie o objeto, ele não pode criar a conexão com o servidor. Você pode usar a propriedade **Connected** antes de qualquer código que chame a interface de programação do Microsoft Agent, conforme mostrado no exemplo a seguir:


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



Criar um controle usando essa técnica não expõe os eventos do controle do agente. No Visual Basic 5,0 (e posterior), você pode acessar os eventos do controle, incluindo o controle nas referências do seu projeto, e usar a palavra-chave **WithEvents** em sua declaração de variável:


```
   Dim WithEvents MyAgent as Agent

   ' Create an instance of the control using New
   Set MyAgent = New Agent
```



O uso de **WithEvents** para criar uma instância do controle Agent em tempo de execução abre automaticamente a conexão com o servidor do Microsoft Agent. Portanto, você não precisa incluir uma instrução **conectada** .

Você pode fechar a conexão com o servidor liberando todas as referências que você criou para os objetos do Agent, como IAgentCtlCharacterEx e IAgentCtlCommandEx. Você também deve liberar sua referência ao próprio controle Agent. No Visual Basic, você pode liberar uma referência a um objeto definindo sua variável como **Nothing**. Se você tiver carregado caracteres, descarregue-os antes de liberar o objeto de caractere.


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
> Não é possível fechar a conexão com o servidor, liberando referências em que o componente foi adicionado. Por exemplo, você não pode fechar a conexão com o servidor em páginas da Web em que você usa a <OBJECT> marca para declarar o controle ou em um aplicativo Visual Basic onde você solta o controle em um formulário. Embora a liberação de todas as referências de agente reduza o conjunto de trabalho do agente, a conexão permanece até que você navegue para a próxima página ou saia do aplicativo.

 

 

 





