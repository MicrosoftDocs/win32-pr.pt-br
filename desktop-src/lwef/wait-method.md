---
title: Método Wait
description: Método Wait
ms.assetid: 968a3f19-6953-473b-ba98-0dc93696e703
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f2e94b0f765a9861c30b254761fbc4dc2e72763
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105788607"
---
# <a name="wait-method"></a>Método Wait

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Faz com que a fila de animação para o caractere especificado aguarde até que a solicitação de animação especificada seja concluída.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agente do ***. Caracteres ("*** characterid ***"). Aguardar*** solicitação*



| Parte      | Descrição                                                                     |
|-----------|---------------------------------------------------------------------------------|
| *Solicitação* | Um objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) que especifica uma determinada animação.. |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Use esse método somente quando você der suporte a vários caracteres (simultâneos) e estiver tentando sequenciar a interação de caracteres. (Para um único caractere, cada solicitação de animação é executada sequencialmente--após a conclusão da solicitação anterior.) Se você tiver dois caracteres e quiser que a solicitação de animação de um caractere aguarde até que a animação do outro caractere seja concluída, defina o método **Wait** como o objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) de animação do outro caractere. Para especificar o parâmetro de solicitação, você deve criar uma variável e atribuir a solicitação de animação que deseja interromper:


```
   Dim GenieRequest 
   Dim RobbyRequest 
   Dim Genie 
   Dim Robby 

   Sub window_Onload

   Agent1.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"
   Agent1.Characters.Load "Robby", "https://agent.microsoft.com/characters/v2/robby/robby.acf"

   Set Genie = Agent1.Characters("Genie")
   Set Robby = Agent1.Characters("Robby")

   Genie.Get "State", "Showing"
   Robby.Get "State", "Showing"

   Genie.Get "Animation", "Announce, AnnounceReturn, Pleased, _ 
      PleasedReturn"
   
   Robby.Get "Animation", "Confused, ConfusedReturn, Sad, SadReturn"

   Set Genie = Agent1.Characters ("Genie")
   Set Robby = Agent1.Characters ("Robby")

   Genie.MoveTo 100,100
   Genie.Show

   Robby.MoveTo 250,100
   Robby.Show

   Genie.Play "Announce"
   Set GenieRequest = Genie.Speak ("Why did the chicken cross the road?")
   
   Robby.Wait GenieRequest
   Robby.Play "Confused"
   Set RobbyRequest = Robby.Speak ("I don't know. Why did the chicken _
      cross the road?")
   
   Genie.Wait RobbyRequest
   Genie.Play "Pleased"
   Set GenieRequest = Genie.Speak ("To get to the other side.")
   
   Robby.Wait GenieRequest
   Robby.Play "Sad"
   Robby.Speak "I never should have asked."

   End Sub
```



Você também pode simplificar seu código simplesmente chamando **Wait** diretamente, usando uma solicitação de animação específica.


```
   Robby.Wait Genie.Play "GestureRight"
```



Isso evita que você precise declarar explicitamente um objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) .

 

 