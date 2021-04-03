---
title: Evento ActivateInput
description: Evento ActivateInput
ms.assetid: bc395750-5da0-4379-8eca-3195e936052c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e0b4fdf83256d58dd247dee85b639f5499f013e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006037"
---
# <a name="activateinput-event"></a><span data-ttu-id="7453c-103">Evento ActivateInput</span><span class="sxs-lookup"><span data-stu-id="7453c-103">ActivateInput Event</span></span>

<span data-ttu-id="7453c-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7453c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="7453c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="7453c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="7453c-106">Ocorre quando um cliente torna-se entrada-ativo.</span><span class="sxs-lookup"><span data-stu-id="7453c-106">Occurs when a client becomes input-active.</span></span>

</dd> <dt>

<span data-ttu-id="7453c-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="7453c-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="7453c-108">**Sub** *Agent* \_ ActivateInput **(ByVal** *characterid \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="7453c-108">**Sub** *agent*\_ActivateInput **(ByVal** *CharacterID\*\*\*)*\*</span></span>



| <span data-ttu-id="7453c-109">Parte</span><span class="sxs-lookup"><span data-stu-id="7453c-109">Part</span></span>          | <span data-ttu-id="7453c-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="7453c-110">Description</span></span>                                                                    |
|---------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="7453c-111">*Caractere de caracteres*</span><span class="sxs-lookup"><span data-stu-id="7453c-111">*CharacterID*</span></span> | <span data-ttu-id="7453c-112">Retorna a ID do caractere por meio do qual o cliente se torna ativo.</span><span class="sxs-lookup"><span data-stu-id="7453c-112">Returns the ID of the character through which the client becomes input-active.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="7453c-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="7453c-113">Remarks</span></span>

<span data-ttu-id="7453c-114">O cliente de entrada-ativo recebe eventos de entrada de mouse e fala fornecidos pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="7453c-114">The input-active client receives mouse and speech input events supplied by the server.</span></span> <span data-ttu-id="7453c-115">O servidor envia esse evento somente para o cliente que se torna de entrada-ativo.</span><span class="sxs-lookup"><span data-stu-id="7453c-115">The server sends this event only to the client that becomes input-active.</span></span>

<span data-ttu-id="7453c-116">Esse evento pode ocorrer quando o usuário alterna para o objeto de [comando](the-command-object.md) , por exemplo, escolhendo a entrada do objeto de comando na janela comandos ou no menu pop-up de um caractere.</span><span class="sxs-lookup"><span data-stu-id="7453c-116">This event can occur when the user switches to your [Command](the-command-object.md) object, for example, by choosing your Command object entry in the Commands Window or in the pop-up menu for a character.</span></span> <span data-ttu-id="7453c-117">Isso também pode ocorrer quando o usuário seleciona um caractere (clicando ou falando com seu nome), quando um caractere se torna visível e quando o caractere de outro aplicativo cliente se torna oculto.</span><span class="sxs-lookup"><span data-stu-id="7453c-117">It can also occur when the user selects a character (by clicking or speaking its name), when a character becomes visible, and when the character of another client application becomes hidden.</span></span> <span data-ttu-id="7453c-118">Você também pode chamar o [método Activate](activate-method.md) (com o **estado** definido como 2) para tornar explicitamente o caractere mais alto, o que faz com que o aplicativo cliente torne-se entrada-ativo e dispare esse evento.</span><span class="sxs-lookup"><span data-stu-id="7453c-118">You can also call the [Activate Method](activate-method.md) (with **State** set to 2) to explicitly make the character topmost, which results in your client application becoming input-active and triggers this event.</span></span> <span data-ttu-id="7453c-119">No entanto, esse evento não ocorrerá se você usar o método Activate do método somente para especificar se o cliente é o cliente ativo do caractere.</span><span class="sxs-lookup"><span data-stu-id="7453c-119">However, this event does not occur if you use the Activate Method method only to specify whether your client is the active client of the character.</span></span>

### <a name="see-also"></a><span data-ttu-id="7453c-120">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="7453c-120">See Also</span></span>

<span data-ttu-id="7453c-121">[Evento **DeactivateInput**](deactivateinput-event.md), [método **Activate**](activate-method.md)</span><span class="sxs-lookup"><span data-stu-id="7453c-121">[**DeactivateInput** event](deactivateinput-event.md), [**Activate** method](activate-method.md)</span></span>


 

 




