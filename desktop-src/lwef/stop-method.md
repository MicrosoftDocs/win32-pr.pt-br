---
title: Método Stop (recursos de ambiente herdado do Windows)
description: Método Stop
ms.assetid: 68372f72-db9c-447c-a3e4-488940c730d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20192634c197559ca54bb8af3d8a29f37beb53e2
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105771601"
---
# <a name="stop-method-legacy-windows-environment-features"></a><span data-ttu-id="90822-103">Método Stop (recursos de ambiente herdado do Windows)</span><span class="sxs-lookup"><span data-stu-id="90822-103">Stop Method (Legacy Windows Environment Features)</span></span>

<span data-ttu-id="90822-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="90822-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="90822-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="90822-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="90822-106">Interrompe a animação para o caractere especificado.</span><span class="sxs-lookup"><span data-stu-id="90822-106">Stops the animation for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="90822-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="90822-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="90822-108">\*Agente \***. Caracteres ("**_characterid_\*_"). Parar_ \*  \[ *solicitação*\]</span><span class="sxs-lookup"><span data-stu-id="90822-108">*agent\***.Characters ("**_CharacterID_*_").Stop_\* \[*Request*\]</span></span>



| <span data-ttu-id="90822-109">Parte</span><span class="sxs-lookup"><span data-stu-id="90822-109">Part</span></span>      | <span data-ttu-id="90822-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="90822-110">Description</span></span>                                                                                   |
|-----------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="90822-111">*Solicitação*</span><span class="sxs-lookup"><span data-stu-id="90822-111">*Request*</span></span> | <span data-ttu-id="90822-112">Opcional.</span><span class="sxs-lookup"><span data-stu-id="90822-112">Optional.</span></span> <span data-ttu-id="90822-113">Um objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) que especifica uma chamada de animação específica.</span><span class="sxs-lookup"><span data-stu-id="90822-113">A [**Request**](/windows/desktop/lwef/the-request-object) object specifying a particular animation call.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="90822-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="90822-114">Remarks</span></span>

<span data-ttu-id="90822-115">Para especificar o parâmetro de solicitação, você deve criar uma variável e atribuir a solicitação de animação que deseja parar.</span><span class="sxs-lookup"><span data-stu-id="90822-115">To specify the request parameter, you must create a variable and assign the animation request you want to stop.</span></span> <span data-ttu-id="90822-116">Se você não definir o parâmetro de **solicitação** , o servidor interromperá todas as animações para o caractere, incluindo chamadas [**Get**](get-method.md) em fila e desmarcará sua fila de animação, a menos que o caractere esteja atualmente reproduzindo sua animação de **ocultação** ou **exibição** .</span><span class="sxs-lookup"><span data-stu-id="90822-116">If you don't set the **Request** parameter, the server stops all animations for the character, including queued [**Get**](get-method.md) calls, and clears its animation queue unless the character is currently playing its **Hiding** or **Showing** animation.</span></span> <span data-ttu-id="90822-117">Esse método não interrompe chamadas **Get** não enfileiradas.</span><span class="sxs-lookup"><span data-stu-id="90822-117">This method does not stop non-queued **Get** calls.</span></span>

<span data-ttu-id="90822-118">Para interromper uma animação específica ou [**obter**](get-method.md) uma chamada, declare uma variável de objeto e atribua sua solicitação de animação a essa variável:</span><span class="sxs-lookup"><span data-stu-id="90822-118">To stop a specific animation or [**Get**](get-method.md) call, declare an object variable and assign your animation request to that variable:</span></span>


```
   Dim MyRequest
   Dim Genie

   Agent1.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"

   Set Genie = Agent1.Characters ("Genie")

   Genie.Get "state", "Showing"
   Genie.Get "animation", "Greet, GreetReturn"

   Genie.Show
   
   'This animation will never play
   Set MyRequest = Genie.Play ("Greet")
   
   Genie.Stop MyRequest
```



<span data-ttu-id="90822-119">Esse método não gerará um objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="90822-119">This method will not generate a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span>

## <a name="see-also"></a><span data-ttu-id="90822-120">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="90822-120">See Also</span></span>

[<span data-ttu-id="90822-121">**Método do opAll**</span><span class="sxs-lookup"><span data-stu-id="90822-121">**StopAll method**</span></span>](stopall-method.md)


 

 
