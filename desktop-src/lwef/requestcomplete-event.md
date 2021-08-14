---
title: Evento RequestComplete
description: Evento RequestComplete
ms.assetid: 543b79d1-f09d-4061-a1a8-8c8ab496bceb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcf5202cc6aee6e8727651279fd216d5f0e5676025584c9cb66c4c6ad958da54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118746553"
---
# <a name="requestcomplete-event"></a>Evento RequestComplete

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**
</dt> <dd>

Ocorre quando o servidor conclui uma solicitação na fila.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

**Sub** *agente*** \_ RequestComplete* *  **(Solicitação ByVal***)** *



| Parte      | Descrição                                            |
|-----------|--------------------------------------------------------|
| *Solicitação* | Retorna o [**objeto Request.**](/windows/desktop/lwef/the-request-object) |



 

</dd> </dl>

### <a name="remarks"></a>Comentários

Esse evento retorna um [**objeto Request.**](/windows/desktop/lwef/the-request-object) Como as solicitações são processadas de forma assíncrona, você pode usar esse evento para determinar quando o servidor conclui o processamento de uma solicitação (como um método [**Get,**](get-method.md) [**Play**](play-method.md)ou [**Speak)**](speak-method.md) para sincronizar esse evento com outras ações geradas pelo seu aplicativo. O servidor envia o evento somente para o cliente que criou a referência ao objeto **Request** e somente se você definiu uma variável global para a referência de solicitação:


```
   Dim MyRequest 
   Dim Genie 

   Sub window_Onload
   
   Agent1.Characters.Load "Genie","https://agent.microsoft.com/characters/v2/genie/genie.acf"

   Set Genie = Agent.Characters("Genie")

   ' This syntax will generate RequestStart and RequestComplete events.
   Set MyRequest = Genie.Get("state", "Showing")
   ' This syntax will not generate RequestStart and RequestComplete events.
   Genie.Get "state", "Hiding"
   
   End Sub

   Sub Agent1_RequestComplete(ByVal Request)

   If Request = MyRequest Then
      Status = "Showing animation is now loaded"

   End Sub
```



Como os [**objetos de**](/windows/desktop/lwef/the-request-object) solicitação de animação não são atribuídos até que o servidor processe a solicitação, certifique-se de que o objeto **Request** exista antes de tentar avaliá-lo. Por exemplo, no Visual Basic, se você usar uma condicional para testar se uma solicitação específica foi concluída, poderá usar a palavra-chave **Nothing:**


```
   Sub Agent1_RequestComplete (ByVal Request)

   If Not (MyRequest Is Nothing) Then
      If Request = MyRequest Then
      '-- Do whatever
      End If
   End If

   End Sub
```



> [!Note]  
> No VBScript 1.0, esse evento é a disparo mesmo que você não defina referências a um [**objeto Request.**](/windows/desktop/lwef/the-request-object) Isso foi corrigido no VBScript 2.0, que pode ser baixado do <https://microsoft.com/msdownload/vbscript/scripting.asp> .

 

### <a name="see-also"></a>Consulte Também

[**Evento RequestStart**](requeststart-event.md)


 

 