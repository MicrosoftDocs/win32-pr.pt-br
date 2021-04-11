---
title: Método de interrupção
description: Método de interrupção
ms.assetid: b8442e25-a629-47c7-acdd-1d28e74d78a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d58050e181525cc4a4b9f35ec169e92d91ab28e7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104366020"
---
# <a name="interrupt-method"></a><span data-ttu-id="988a7-103">Método de interrupção</span><span class="sxs-lookup"><span data-stu-id="988a7-103">Interrupt Method</span></span>

<span data-ttu-id="988a7-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="988a7-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="988a7-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="988a7-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="988a7-106">Interrompe a animação para o caractere especificado.</span><span class="sxs-lookup"><span data-stu-id="988a7-106">Interrupts the animation for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="988a7-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="988a7-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="988a7-108">\*agente do ***. Caracteres ("*** characterid \* \* *").* \*  *Solicitação* de interrupção</span><span class="sxs-lookup"><span data-stu-id="988a7-108">*agent ***.Characters ("*** CharacterID\*\*\*").Interrupt*\* *Request*</span></span>



| <span data-ttu-id="988a7-109">Parte</span><span class="sxs-lookup"><span data-stu-id="988a7-109">Part</span></span>      | <span data-ttu-id="988a7-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="988a7-110">Description</span></span>                                                                  |
|-----------|------------------------------------------------------------------------------|
| <span data-ttu-id="988a7-111">*Solicitação*</span><span class="sxs-lookup"><span data-stu-id="988a7-111">*Request*</span></span> | <span data-ttu-id="988a7-112">Um objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) para uma chamada de animação específica.</span><span class="sxs-lookup"><span data-stu-id="988a7-112">A [**Request**](/windows/desktop/lwef/the-request-object) object for a particular animation call.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="988a7-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="988a7-113">Remarks</span></span>

<span data-ttu-id="988a7-114">Você pode usar isso para sincronizar a animação entre os caracteres.</span><span class="sxs-lookup"><span data-stu-id="988a7-114">You can use this to sync up animation between characters.</span></span> <span data-ttu-id="988a7-115">Por exemplo, se outro caractere estiver em uma animação de looping, esse método irá parar o loop e passar para a próxima animação na fila do caractere.</span><span class="sxs-lookup"><span data-stu-id="988a7-115">For example, if another character is in a looping animation, this method will stop the loop and move to the next animation in the character's queue.</span></span> <span data-ttu-id="988a7-116">Não é possível interromper uma animação de caracteres que você não está usando (que você não carregou).</span><span class="sxs-lookup"><span data-stu-id="988a7-116">You cannot interrupt a character animation that you are not using (that you have not loaded).</span></span>

<span data-ttu-id="988a7-117">Para especificar o parâmetro de solicitação, você deve criar uma variável e atribuir a solicitação de animação que deseja interromper:</span><span class="sxs-lookup"><span data-stu-id="988a7-117">To specify the request parameter, you must create a variable and assign the animation request you want to interrupt:</span></span>


```
   Dim GenieRequest as Object
   Dim RobbyRequest as Object
   Dim Genie as Object
   Dim Robby as Object

   Sub FormLoad()

      MyAgent1.Characters.Load "Genie", "Genie.acs"

      MyAgent1.Characters.Load "Robby", "Robby.acs"

      Set Genie = MyAgent1.Characters ("Genie")
      Set Robby = MyAgent1.Characters ("Robby")

      Genie.Show

      Genie.Speak "Just a moment"

      Set GenieRequest = Genie.Play ("Processing")

      Robby.Show
      Robby.Play "confused"
      Robby.Speak "Hey, Genie. What are you doing?"
      Robby.Interrupt GenieRequest

      Genie.Speak "I was just checking on something."

   End Sub
```



<span data-ttu-id="988a7-118">Não é possível interromper a animação do mesmo caractere que você especifica nesse método, pois o servidor enfileira o método de **interrupção** na fila de animação desse caractere.</span><span class="sxs-lookup"><span data-stu-id="988a7-118">You cannot interrupt the animation of the same character you specify in this method because the server queues the **Interrupt** method in that character's animation queue.</span></span> <span data-ttu-id="988a7-119">Portanto, você só pode usar a **interrupção** para interromper a animação de outro caractere que você carregou.</span><span class="sxs-lookup"><span data-stu-id="988a7-119">Therefore, you can only use **Interrupt** to halt the animation of another character you have loaded.</span></span>

<span data-ttu-id="988a7-120">Se você declarar uma referência de objeto e defini-la para esse método, ela retornará um objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="988a7-120">If you declare an object reference and set it to this method, it returns a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span>

> [!Note]  
> <span data-ttu-id="988a7-121">A **interrupção** não libera a fila do caractere; Ele interrompe a animação existente e passa para a próxima animação na fila do caractere.</span><span class="sxs-lookup"><span data-stu-id="988a7-121">**Interrupt** does not flush the character's queue; it halts the existing animation and moves on to the next animation in the character's queue.</span></span> <span data-ttu-id="988a7-122">Para interromper e liberar a fila de um caractere, use o método [**Stop**](stop-method.md) .</span><span class="sxs-lookup"><span data-stu-id="988a7-122">To halt and flush a character's queue, use the [**Stop**](stop-method.md) method.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="988a7-123">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="988a7-123">See Also</span></span>

[<span data-ttu-id="988a7-124">**Método Stop**</span><span class="sxs-lookup"><span data-stu-id="988a7-124">**Stop method**</span></span>](stop-method.md)


 

 