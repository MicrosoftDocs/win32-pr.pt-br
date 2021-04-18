---
title: Método Activate
description: Método Activate
ms.assetid: 8111139d-1453-416e-8f08-38c06669ff4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21df1965abaeed35e9e440a0f559f5e12d68d6fe
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105796065"
---
# <a name="activate-method"></a><span data-ttu-id="8be98-103">Método Activate</span><span class="sxs-lookup"><span data-stu-id="8be98-103">Activate Method</span></span>

<span data-ttu-id="8be98-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8be98-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="8be98-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>[**Ndescrição**](../wmformat/description.md)</span><span class="sxs-lookup"><span data-stu-id="8be98-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>[**Description**](../wmformat/description.md)</span></span>
</dt> <dd>

<span data-ttu-id="8be98-106">Define o caractere ou o cliente ativo.</span><span class="sxs-lookup"><span data-stu-id="8be98-106">Sets the active client or character.</span></span>

</dd> <dt>

<span data-ttu-id="8be98-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="8be98-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="8be98-108">\*agente do ***. Caracteres ("*** characterid \* \* *"). Ativar* \*  \[ *estado*\]</span><span class="sxs-lookup"><span data-stu-id="8be98-108">*agent ***.Characters ("*** CharacterID\*\*\*").Activate*\* \[*State*\]</span></span>



| <span data-ttu-id="8be98-109">Parte</span><span class="sxs-lookup"><span data-stu-id="8be98-109">Part</span></span>    | <span data-ttu-id="8be98-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="8be98-110">Description</span></span>                                                                                                                                                                           |
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8be98-111">*State*</span><span class="sxs-lookup"><span data-stu-id="8be98-111">*State*</span></span> | <span data-ttu-id="8be98-112">Opcional.</span><span class="sxs-lookup"><span data-stu-id="8be98-112">Optional.</span></span> <span data-ttu-id="8be98-113">Você pode especificar os seguintes valores para este parâmetro: 0 não é o cliente ativo.</span><span class="sxs-lookup"><span data-stu-id="8be98-113">You can specify the following values for this parameter: 0 Not the active client.</span></span><br/> <span data-ttu-id="8be98-114">1 o cliente ativo.</span><span class="sxs-lookup"><span data-stu-id="8be98-114">1 The active client.</span></span> <br/> <span data-ttu-id="8be98-115">2 (padrão) o caractere superior.</span><span class="sxs-lookup"><span data-stu-id="8be98-115">2 (Default) The topmost character.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8be98-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="8be98-116">Remarks</span></span>

<span data-ttu-id="8be98-117">Quando vários caracteres são visíveis, apenas um dos caracteres recebe a entrada de fala de cada vez.</span><span class="sxs-lookup"><span data-stu-id="8be98-117">When multiple characters are visible, only one of the characters receives speech input at a time.</span></span> <span data-ttu-id="8be98-118">Da mesma forma, quando vários aplicativos cliente compartilham o mesmo caractere, apenas um dos clientes recebe a entrada do mouse (por exemplo, o controle do Microsoft Agent clica ou arrasta eventos).</span><span class="sxs-lookup"><span data-stu-id="8be98-118">Similarly, when multiple client applications share the same character, only one of the clients receives mouse input (for example, Microsoft Agent control click or drag events).</span></span> <span data-ttu-id="8be98-119">O conjunto de caracteres para receber o mouse e a entrada de fala é o caractere superior e o cliente que recebe a entrada é o cliente ativo desse caractere.</span><span class="sxs-lookup"><span data-stu-id="8be98-119">The character set to receive mouse and speech input is the topmost character and the client that receives the input is the active client of that character.</span></span> <span data-ttu-id="8be98-120">(A janela do caractere superior também aparece na parte superior da ordem z da janela de caractere.) Normalmente, o usuário determina o caractere superior selecionando explicitamente o caractere.</span><span class="sxs-lookup"><span data-stu-id="8be98-120">(The topmost character's window also appears at the top of the character window's z-order.) Typically, the user determines the topmost character by explicitly selecting the character.</span></span> <span data-ttu-id="8be98-121">No entanto, a ativação na extremidade superior também é alterada quando um caractere é mostrado ou oculto (o caractere se torna ou não é mais o mais alto, respectivamente.)</span><span class="sxs-lookup"><span data-stu-id="8be98-121">However, topmost activation also changes when a character is shown or hidden (the character becomes or is no longer topmost, respectively.)</span></span>

<span data-ttu-id="8be98-122">Você também pode usar esse método para gerenciar explicitamente quando o cliente recebe a entrada direcionada para o caractere, como quando o próprio aplicativo se torna ativo.</span><span class="sxs-lookup"><span data-stu-id="8be98-122">You can also use this method to explicitly manage when your client receives input directed to the character such as when your application itself becomes active.</span></span> <span data-ttu-id="8be98-123">Por exemplo, definir *State* como 2 torna o caractere mais alto e o cliente recebe todos os eventos de entrada de mouse e fala gerados da interação do usuário com o caractere.</span><span class="sxs-lookup"><span data-stu-id="8be98-123">For example, setting *State* to 2 makes the character topmost and your client receives all mouse and speech input events generated from user interaction with the character.</span></span> <span data-ttu-id="8be98-124">Portanto, ele também torna o cliente o cliente de entrada-ativo do caractere.</span><span class="sxs-lookup"><span data-stu-id="8be98-124">Therefore, it also makes your client the input-active client of the character.</span></span>

<span data-ttu-id="8be98-125">No entanto, você também pode definir a si mesmo como o cliente ativo para um caractere sem tornar o caractere mais alto, definindo o *estado* como 1.</span><span class="sxs-lookup"><span data-stu-id="8be98-125">However, you can also set yourself to be the active client for a character without making the character topmost, by setting *State* to 1.</span></span> <span data-ttu-id="8be98-126">Isso permite que o cliente receba entrada direcionada para esse caractere quando o caractere se tornar mais alto.</span><span class="sxs-lookup"><span data-stu-id="8be98-126">This enables your client to receive input directed to that character when the character becomes topmost.</span></span> <span data-ttu-id="8be98-127">Da mesma forma, você pode definir que o cliente não seja o cliente ativo (não para receber a entrada) quando o caractere se tornar mais alto, definindo *State* como 0.</span><span class="sxs-lookup"><span data-stu-id="8be98-127">Similarly, you can set your client to not be the active client (not to receive input) when the character becomes topmost, by setting *State* to 0.</span></span>

<span data-ttu-id="8be98-128">Evite chamar esse método diretamente após um método [**show**](/previous-versions/visualstudio/foxpro/d79z7xxa(v=vs.71)) .</span><span class="sxs-lookup"><span data-stu-id="8be98-128">Avoid calling this method directly after a [**Show**](/previous-versions/visualstudio/foxpro/d79z7xxa(v=vs.71)) method.</span></span> <span data-ttu-id="8be98-129">**Mostrar** define automaticamente o cliente de entrada-ativo.</span><span class="sxs-lookup"><span data-stu-id="8be98-129">**Show** automatically sets the input-active client.</span></span> <span data-ttu-id="8be98-130">Quando o caractere estiver oculto, a chamada de [**ativação**](/previous-versions/visualstudio/foxpro/01ayxx68(v=vs.71)) poderá falhar se for processada antes de o método **show** ser concluído.</span><span class="sxs-lookup"><span data-stu-id="8be98-130">When the character is hidden, the [**Activate**](/previous-versions/visualstudio/foxpro/01ayxx68(v=vs.71)) call may fail if it gets processed before the **Show** method completes.</span></span>

<span data-ttu-id="8be98-131">Se você chamar esse método para uma função, ele retornará um valor booliano que indica se o método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="8be98-131">If you call this method to a function, it returns a Boolean value that indicates whether the method succeeded.</span></span> <span data-ttu-id="8be98-132">A tentativa de chamar esse método com o parâmetro de *estado* definido como 2 quando o caractere especificado for oculta falhará.</span><span class="sxs-lookup"><span data-stu-id="8be98-132">Attempting to call this method with the *State* parameter set to 2 when the specified character is hidden will fail.</span></span> <span data-ttu-id="8be98-133">Da mesma forma, se você definir o *estado* como 0 e seu aplicativo for o único cliente, essa chamada falhará porque um caractere sempre deve ter um cliente de nível superior.</span><span class="sxs-lookup"><span data-stu-id="8be98-133">Similarly, if you set *State* to 0 and your application is the only client, this call fails because a character must always have a topmost client.</span></span>


```
   Dim Genie as Object

   Sub FormLoad()

   Agent1.Characters.Load "Genie", "Genie.acs"

   Set Genie = Agent1.Characters ("Genie")

   If (Genie. Activate = True) Then
      'I'm active

   Else
      'I must be hidden or something

   End If 
   
   End Sub
```



> [!Note]  
> <span data-ttu-id="8be98-134">Chamar esse método com o *estado* definido como 1 normalmente não gera um evento [**ActivateInput**](https://www.bing.com/search?q=**ActivateInput**) , a menos que não haja nenhum outro caractere carregado ou seu aplicativo já está em entrada-ativo.</span><span class="sxs-lookup"><span data-stu-id="8be98-134">Calling this method with *State* set to 1 does not typically generate an [**ActivateInput**](https://www.bing.com/search?q=**ActivateInput**) event unless there are no other characters loaded or your application is already input-active.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="8be98-135">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="8be98-135">See Also</span></span>

<span data-ttu-id="8be98-136">[**Evento ActivateInput**](activateinput-event.md), [ **evento DeactivateInput**](deactivateinput-event.md)</span><span class="sxs-lookup"><span data-stu-id="8be98-136">[**ActivateInput event**](activateinput-event.md), [**DeactivateInput event**](deactivateinput-event.md)</span></span>


 

