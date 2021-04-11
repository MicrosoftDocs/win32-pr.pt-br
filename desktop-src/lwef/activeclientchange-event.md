---
title: Evento ActiveClientChange
description: Evento ActiveClientChange
ms.assetid: 617b40e6-cafb-463e-8b36-2a12c468d3ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8137edd559d934fd1a478350cd1185885c7dc148
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159808"
---
# <a name="activeclientchange-event"></a><span data-ttu-id="cb59f-103">Evento ActiveClientChange</span><span class="sxs-lookup"><span data-stu-id="cb59f-103">ActiveClientChange Event</span></span>

<span data-ttu-id="cb59f-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="cb59f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="cb59f-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="cb59f-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="cb59f-106">Ocorre quando o cliente ativo do caractere é alterado.</span><span class="sxs-lookup"><span data-stu-id="cb59f-106">Occurs when the active client of the character changes.</span></span>

</dd> <dt>

<span data-ttu-id="cb59f-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="cb59f-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="cb59f-108">**Sub** - *agente.* ActiveClientChange (ByVal *caractereid*, ByVal *ativo* **)**</span><span class="sxs-lookup"><span data-stu-id="cb59f-108">**Sub** *agent.* ActiveClientChange (ByVal *CharacterID*, ByVal *Active* **)**</span></span>



| <span data-ttu-id="cb59f-109">Parte</span><span class="sxs-lookup"><span data-stu-id="cb59f-109">Part</span></span>          | <span data-ttu-id="cb59f-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="cb59f-110">Description</span></span>                                                                                                                                                                                                                                                        |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb59f-111">*Caractere de caracteres*</span><span class="sxs-lookup"><span data-stu-id="cb59f-111">*CharacterID*</span></span> | <span data-ttu-id="cb59f-112">Retorna a ID do caractere para o qual o evento ocorreu.</span><span class="sxs-lookup"><span data-stu-id="cb59f-112">Returns the ID of the character for which the event occurred.</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="cb59f-113">*Ativo*</span><span class="sxs-lookup"><span data-stu-id="cb59f-113">*Active*</span></span>      | <span data-ttu-id="cb59f-114">Um valor booliano que indica se o cliente se tornou ativo ou não ativo.</span><span class="sxs-lookup"><span data-stu-id="cb59f-114">A Boolean value that indicates whether the client became active or not active.</span></span> <span data-ttu-id="cb59f-115">**Verdadeiro** O aplicativo cliente tornou-se o cliente ativo do caractere.</span><span class="sxs-lookup"><span data-stu-id="cb59f-115">**True** The client application became the active client of the character.</span></span> <br/> <span data-ttu-id="cb59f-116">**Falso** O aplicativo cliente não é mais o cliente ativo do caractere.</span><span class="sxs-lookup"><span data-stu-id="cb59f-116">**False** The client application is no longer the active client of the character.</span></span><br/> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="cb59f-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="cb59f-117">Remarks</span></span>

<span data-ttu-id="cb59f-118">Quando vários aplicativos cliente compartilham o mesmo caractere, o cliente ativo do caractere recebe a entrada do mouse (por exemplo, o controle do Microsoft Agent clica ou arrasta eventos).</span><span class="sxs-lookup"><span data-stu-id="cb59f-118">When multiple client applications share the same character, the active client of the character receives mouse input (for example, Microsoft Agent control click or drag events).</span></span> <span data-ttu-id="cb59f-119">Da mesma forma, quando vários caracteres são exibidos, o cliente ativo do caractere superior (também conhecido como o cliente de entrada-ativo) recebe eventos de [comando](command-event.md) .</span><span class="sxs-lookup"><span data-stu-id="cb59f-119">Similarly, when multiple characters are displayed, the active client of the topmost character (also known as the input-active client) receives [Command](command-event.md) events.</span></span>

<span data-ttu-id="cb59f-120">Quando o cliente ativo de um caractere é alterado, esse evento retorna a ID desse caractere e **true** se o aplicativo se tornou o cliente ativo do caractere ou **false** se não for mais o cliente ativo do caractere.</span><span class="sxs-lookup"><span data-stu-id="cb59f-120">When the active client of a character changes, this event passes back the ID of that character and **True** if your application has become the active client of the character or **False** if it is no longer the active client of the character.</span></span>

<span data-ttu-id="cb59f-121">Um aplicativo cliente pode receber esse evento quando o usuário seleciona a entrada de um aplicativo cliente no menu pop-up do caractere ou por comando de voz, quando o aplicativo cliente altera seu status ativo ou quando outro aplicativo cliente sai de sua conexão com o agente.</span><span class="sxs-lookup"><span data-stu-id="cb59f-121">A client application may receive this event when the user selects a client application's entry in character's pop-up menu or by voice command, when the client application changes its active status, or when another client application quits its connection to Agent.</span></span> <span data-ttu-id="cb59f-122">O Agent envia esse evento somente para os aplicativos cliente que são diretamente afetados; que se tornem o cliente ativo ou que parem de ser o cliente ativo.</span><span class="sxs-lookup"><span data-stu-id="cb59f-122">Agent sends this event only to the client applications that are directly affected; that either become the active client or stop being the active client.</span></span>

### <a name="see-also"></a><span data-ttu-id="cb59f-123">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="cb59f-123">See Also</span></span>

<span data-ttu-id="cb59f-124">\* \* \* \* [ActivateInput \* \* evento \*](activateinput-event.md)\*, \* \* \* \* [ativo \* \* Propriedade \* \*](active-property.md), [\* \* \* DeactivateInput \* \* evento \* \*](deactivateinput-event.md), [\* \* \* \* Ativar \* \* método \*](activate-method.md) \*</span><span class="sxs-lookup"><span data-stu-id="cb59f-124">[\*\*\*\*ActivateInput\*\* event\*\*](activateinput-event.md), [\*\*\*\*Active\*\* property\*\*](active-property.md), [\*\*\*\*DeactivateInput\*\* event\*\*](deactivateinput-event.md), [\*\*\*\*Activate\*\* method\*\*](activate-method.md)</span></span>


 

 





