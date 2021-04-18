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
# <a name="wait-method"></a><span data-ttu-id="2a1b8-103">Método Wait</span><span class="sxs-lookup"><span data-stu-id="2a1b8-103">Wait Method</span></span>

<span data-ttu-id="2a1b8-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2a1b8-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="2a1b8-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="2a1b8-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="2a1b8-106">Faz com que a fila de animação para o caractere especificado aguarde até que a solicitação de animação especificada seja concluída.</span><span class="sxs-lookup"><span data-stu-id="2a1b8-106">Causes the animation queue for the specified character to wait until the specified animation request completes.</span></span>

</dd> <dt>

<span data-ttu-id="2a1b8-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="2a1b8-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="2a1b8-108">*agente do ***. Caracteres ("*** characterid ***"). Aguardar*** solicitação*</span><span class="sxs-lookup"><span data-stu-id="2a1b8-108">*agent ***.Characters ("*** CharacterID ***").Wait*** Request*</span></span>



| <span data-ttu-id="2a1b8-109">Parte</span><span class="sxs-lookup"><span data-stu-id="2a1b8-109">Part</span></span>      | <span data-ttu-id="2a1b8-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="2a1b8-110">Description</span></span>                                                                     |
|-----------|---------------------------------------------------------------------------------|
| <span data-ttu-id="2a1b8-111">*Solicitação*</span><span class="sxs-lookup"><span data-stu-id="2a1b8-111">*Request*</span></span> | <span data-ttu-id="2a1b8-112">Um objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) que especifica uma determinada animação..</span><span class="sxs-lookup"><span data-stu-id="2a1b8-112">A [**Request**](/windows/desktop/lwef/the-request-object) object specifying a particular animation..</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2a1b8-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="2a1b8-113">Remarks</span></span>

<span data-ttu-id="2a1b8-114">Use esse método somente quando você der suporte a vários caracteres (simultâneos) e estiver tentando sequenciar a interação de caracteres.</span><span class="sxs-lookup"><span data-stu-id="2a1b8-114">Use this method only when you support multiple (simultaneous) characters and are trying to sequence the interaction of characters.</span></span> <span data-ttu-id="2a1b8-115">(Para um único caractere, cada solicitação de animação é executada sequencialmente--após a conclusão da solicitação anterior.) Se você tiver dois caracteres e quiser que a solicitação de animação de um caractere aguarde até que a animação do outro caractere seja concluída, defina o método **Wait** como o objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) de animação do outro caractere.</span><span class="sxs-lookup"><span data-stu-id="2a1b8-115">(For a single character, each animation request is played sequentially--after the previous request completes.) If you have two characters and you want a character's animation request to wait until the other character's animation completes, set the **Wait** method to the other character's animation [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="2a1b8-116">Para especificar o parâmetro de solicitação, você deve criar uma variável e atribuir a solicitação de animação que deseja interromper:</span><span class="sxs-lookup"><span data-stu-id="2a1b8-116">To specify the request parameter, you must create a variable and assign the animation request you want to interrupt:</span></span>


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



<span data-ttu-id="2a1b8-117">Você também pode simplificar seu código simplesmente chamando **Wait** diretamente, usando uma solicitação de animação específica.</span><span class="sxs-lookup"><span data-stu-id="2a1b8-117">You can also streamline your code by just calling **Wait** directly, using a specific animation request.</span></span>


```
   Robby.Wait Genie.Play "GestureRight"
```



<span data-ttu-id="2a1b8-118">Isso evita que você precise declarar explicitamente um objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="2a1b8-118">This avoids having to explicitly declare a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span>

 

 