---
title: Evento RequestStart
description: Evento RequestStart
ms.assetid: ecfb9691-cbc4-48f5-8e26-a99389e85eed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2be5954636084d3cbc299c718f2b4e6d9330ef90
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103641031"
---
# <a name="requeststart-event"></a>Evento RequestStart

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Ocorre quando o servidor inicia uma solicitação em fila.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

**Sub** *Agent * * * \_ RequestStart* *  **(solicitação ByVal** ** * *)**



| Parte      | Descrição                                            |
|-----------|--------------------------------------------------------|
| *Solicitação* | Retorna o objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) . |



 

</dd> </dl>

### <a name="remarks"></a>Comentários

O evento retorna um objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) . Como as solicitações são processadas de forma assíncrona, você pode usar esse evento para determinar quando o servidor começa a processar uma solicitação (como um método [**Get**](get-method.md), [**Play**](play-method.md)ou [**Speak**](speak-method.md) ) e, assim, sincronizá-la com outras ações geradas pelo seu aplicativo. O evento é enviado somente para o cliente que criou a referência ao objeto de **solicitação** e somente se você definiu uma variável global para a referência de solicitação:


```
   Dim MyRequest 
   Dim Genie 

   Sub window_Onload
   
   Agent1.Characters.Load "Genie", _
      "https://agent.microsoft.com/characters/v2/genie/genie.acf"   

   Set Genie = Agent1.Characters("Genie")

   ' This syntax will generate RequestStart and RequestComplete events.
   Set MyRequest = Genie.Get("state", "Showing")

   ' This syntax will not generate RequestStart and RequestComplete events.
   Genie.Get ("state", "Hiding")

   End Sub

   Sub Agent1_RequestStart(ByVal Request)

   If Request = MyRequest Then
      Status = "Loading the Showing animation"

   End Sub
```



O [**status**](status-property.md) retorna 4 (solicitação em andamento) para o objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) retornado.

Como os objetos de [**solicitação**](/windows/desktop/lwef/the-request-object) de animação não são atribuídos até que o servidor processe a solicitação, verifique se o objeto de **solicitação** existe antes de tentar avaliá-lo. Por exemplo, em Visual Basic, se você usar uma condicional para testar se uma solicitação específica foi concluída, você pode usar a palavra-chave **Nothing** :


```
   Sub Agent1_RequestStart (ByVal Request)

   If Not (MyRequest Is Nothing) Then
      If Request = MyRequest Then
      '-- Do whatever
      End If
   End If

   End Sub
```



> [!Note]  
> No VBScript 1,0, esse evento é acionado mesmo se você não definir referências a um objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) . Isso foi corrigido no VBScript 2,0, que pode ser baixado de <https://microsoft.com/msdownload/vbscript/scripting.asp> .

 

### <a name="see-also"></a>Consulte Também

[**Evento RequestComplete**](requestcomplete-event.md)


 

 