---
title: O objeto de solicitação
description: O objeto de solicitação
ms.assetid: d8b37164-6855-48c0-bcf8-a86c0f8b3a59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a50d554a5799af9a434b456113d7c826d2a0aa2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105763044"
---
# <a name="the-request-object"></a>O objeto de solicitação

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

O servidor processa alguns métodos de forma assíncrona. Isso permite que o código do aplicativo continue enquanto o método está sendo concluído. Quando um aplicativo cliente chama um desses métodos, o controle cria e retorna um objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) para a solicitação. Você pode usar o objeto de **solicitação** para acompanhar o status do método atribuindo uma variável de objeto ao método. Em Visual Basic, primeiro declare uma variável de objeto:


```
   Dim MyRequest as Object
```



No VBScript, você não inclui o tipo de variável em sua declaração:


```
   Dim MyRequest
```



E use a instrução SET do Visual Basic para atribuir a variável à chamada do método:


```
   Set MyRequest = <i>agent</i>.Characters("<i>CharacterID</i>").<i>method</i> (<i>parameter</i>[s])
```



Isso adiciona uma referência ao objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) . O objeto de **solicitação** será destruído quando não houver mais referências a ele. Onde você declara o objeto de **solicitação** e como usá-lo determina seu tempo de vida. Se o objeto for declarado local para uma sub-rotina ou função, ele será destruído quando sair do escopo; ou seja, quando a sub-rotina ou a função termina. Se o objeto for declarado globalmente, ele não será destruído até que o programa seja encerrado ou um novo valor (ou um valor definido como "Empty") seja atribuído ao objeto.

O objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) fornece várias propriedades que você pode consultar. Por exemplo, a propriedade [**status**](status-property.md) retorna o status atual da solicitação. Você pode usar essa propriedade para verificar o status da sua solicitação:


```
   Dim MyRequest
   
   Set MyRequest = Agent1.Characters.Load ("Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf")

   If (MyRequest.Status = 2) then
      'do something

   Else If (MyRequest.Status = 0) then
      'do something right away

   End If
```



A propriedade [**status**](status-property.md) retorna o status de um objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) como um valor inteiro longo.



| Status | Definição                                        |
|--------|---------------------------------------------------|
| 0      | Solicitação concluída com êxito.                   |
| 1      | Falha na solicitação.                                   |
| 2      | Solicitação pendente (na fila, mas não concluída). |
| 3      | Solicitação interrompida.                              |
| 4      | Solicitação em andamento.                              |



 

O objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) também inclui um valor inteiro longo na propriedade [**Number**](https://www.bing.com/search?q=**Number**) que retorna o erro ou a causa do código de [**status**](status-property.md) . Se nenhum, esse valor será zero (0). A propriedade [**Description**](description-property.md) contém um valor de cadeia de caracteres que corresponde ao número do erro. Se a cadeia de caracteres não existir, a **Descrição** conterá "erro definido pelo aplicativo ou definido pelo objeto".

Para obter os valores e o significado retornados pela propriedade [**Number**](https://www.bing.com/search?q=**Number**) , consulte [códigos de erro](microsoft-agent-error-codes.md).

O servidor coloca as solicitações de animação na fila do caractere especificado. Isso permite que o servidor reproduza a animação em um thread separado, e o código do aplicativo pode continuar enquanto as animações são reproduzidas. Se você criar uma referência de objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) , o servidor o notificará automaticamente quando uma solicitação de animação for iniciada ou concluída por meio dos eventos [**RequestStart**](https://www.bing.com/search?q=**RequestStart**) e [**RequestComplete**](https://www.bing.com/search?q=**RequestComplete**) . Como os métodos que retornam objetos de **solicitação** são assíncronos e podem não ser concluídos durante o escopo da função de chamada, declare sua referência ao objeto de **solicitação** globalmente.

Os métodos a seguir podem ser usados para retornar um objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) : [**GestureAt**](gestureat-method.md), [**obter**](get-method.md), [**ocultar**](hide-method.md), [**interromper**](interrupt-method.md), [**carregar**](load-method.md), [**MoveTo**](moveto-method.md), [**reproduzir**](play-method.md), [**Mostrar**](show-method.md), [**falar**](speak-method.md)e [**aguardar**](https://www.bing.com/search?q=**Wait**).

 

 