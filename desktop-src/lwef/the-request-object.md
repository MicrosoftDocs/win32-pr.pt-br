---
title: O objeto request
description: O objeto request
ms.assetid: d8b37164-6855-48c0-bcf8-a86c0f8b3a59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d2bc9ecf65403ca6dbb471c81a65b105bcc5b69701760a73f8fbc8a5684a9b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117882389"
---
# <a name="the-request-object"></a>O objeto request

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

O servidor processa alguns métodos de forma assíncrona. Isso permite que o código do aplicativo continue enquanto o método está sendo concluído. Quando um aplicativo cliente chama um desses métodos, o controle cria e retorna um [**objeto Request**](/windows/desktop/lwef/the-request-object) para a solicitação. Você pode usar o **objeto Request** para acompanhar o status do método atribuindo uma variável de objeto ao método . No Visual Basic, primeiro declare uma variável de objeto:


```
   Dim MyRequest as Object
```



No VBScript, você não inclui o tipo de variável em sua declaração:


```
   Dim MyRequest
```



E use Visual Basic instrução Set do usuário para atribuir a variável à chamada de método:


```
   Set MyRequest = <i>agent</i>.Characters("<i>CharacterID</i>").<i>method</i> (<i>parameter</i>[s])
```



Isso adiciona uma referência ao [**objeto Request.**](/windows/desktop/lwef/the-request-object) O **objeto** Request será destruído quando não houver mais referências a ele. Onde você declara o **objeto Request** e como usá-lo determina seu tempo de vida. Se o objeto for declarado local para uma sub-rotina ou função, ele será destruído quando sair do escopo; ou seja, quando a sub-rotina ou a função termina. Se o objeto for declarado globalmente, ele não será destruído até que o programa seja encerrado ou um novo valor (ou um valor definido como "vazio") seja atribuído ao objeto.

O [**objeto Request**](/windows/desktop/lwef/the-request-object) fornece várias propriedades que você pode consultar. Por exemplo, a [**propriedade Status**](status-property.md) retorna o status atual da solicitação. Você pode usar essa propriedade para verificar o status da solicitação:


```
   Dim MyRequest
   
   Set MyRequest = Agent1.Characters.Load ("Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf")

   If (MyRequest.Status = 2) then
      'do something

   Else If (MyRequest.Status = 0) then
      'do something right away

   End If
```



A [**propriedade Status**](status-property.md) retorna o status de um objeto [**Request**](/windows/desktop/lwef/the-request-object) como um valor inteiro Longo.



| Status | Definição                                        |
|--------|---------------------------------------------------|
| 0      | Solicitação concluída com êxito.                   |
| 1      | Falha na solicitação.                                   |
| 2      | Solicitação pendente (na fila, mas não concluída). |
| 3      | Solicitação interrompida.                              |
| 4      | Solicitação em andamento.                              |



 

O [**objeto Request**](/windows/desktop/lwef/the-request-object) também inclui um valor inteiro Longo na propriedade [**Number**](https://www.bing.com/search?q=**Number**) que retorna o erro ou a causa do [**código status.**](status-property.md) Se nenhum, esse valor será zero (0). A [**propriedade Description**](description-property.md) contém um valor de cadeia de caracteres que corresponde ao número de erro. Se a cadeia de caracteres não existir, **Description** conterá "Erro definido pelo aplicativo ou definido pelo objeto".

Para os valores e o significado retornados pela [**propriedade Number,**](https://www.bing.com/search?q=**Number**) consulte [Códigos de erro](microsoft-agent-error-codes.md).

O servidor coloca solicitações de animação na fila do caractere especificado. Isso permite que o servidor reproduza a animação em um thread separado e o código do aplicativo pode continuar durante a reprodução das animações. Se você criar [**uma**](/windows/desktop/lwef/the-request-object) referência de objeto Request, o servidor notifica automaticamente quando uma solicitação de animação é iniciada ou concluída por meio dos eventos [**RequestStart**](https://www.bing.com/search?q=**RequestStart**) e [**RequestComplete.**](https://www.bing.com/search?q=**RequestComplete**) Como os métodos que retornam **objetos Request** são assíncronos e podem não ser concluídos durante o escopo da função de chamada, declare sua referência ao **objeto Request** globalmente.

Os seguintes métodos podem ser usados para retornar [](get-method.md)um objeto [**Request:**](/windows/desktop/lwef/the-request-object) [**GestureAt**](gestureat-method.md), Get , [**Hide**](hide-method.md), [**Interrupt**](interrupt-method.md), [**Load**](load-method.md), [**MoveTo**](moveto-method.md), [**Play**](play-method.md), [**Show**](show-method.md), [**Speak**](speak-method.md)e [**Wait**](https://www.bing.com/search?q=**Wait**).

 

 