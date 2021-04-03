---
title: Mostrar evento
description: Mostrar evento
ms.assetid: vs|msagent|~\pacontrol_7wrw.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6964164e14c759a971e5ceeda542a5c27131663
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822445"
---
# <a name="show-event"></a><span data-ttu-id="32a38-103">Mostrar evento</span><span class="sxs-lookup"><span data-stu-id="32a38-103">Show Event</span></span>

<span data-ttu-id="32a38-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="32a38-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="32a38-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="32a38-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="32a38-106">Ocorre quando um caractere é exibido.</span><span class="sxs-lookup"><span data-stu-id="32a38-106">Occurs when a character is displayed.</span></span>

</dd> <dt>

<span data-ttu-id="32a38-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="32a38-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="32a38-108">**Sub** *agente \* \* \* \_ Mostrar (ByVal* \*  *characterid*, **ByVal** *causa \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="32a38-108">**Sub** *agent\*\*\*\_Show (ByVal*\* *CharacterID*, **ByVal** *Cause\*\*\*)*\*</span></span>



| <span data-ttu-id="32a38-109">Parte</span><span class="sxs-lookup"><span data-stu-id="32a38-109">Part</span></span>          | <span data-ttu-id="32a38-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="32a38-110">Description</span></span>                                                                                                                                                                                                                                                                 |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32a38-111">*Caractere de caracteres*</span><span class="sxs-lookup"><span data-stu-id="32a38-111">*CharacterID*</span></span> | <span data-ttu-id="32a38-112">Retorna a ID do caractere mostrado como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="32a38-112">Returns the ID of the character shown as a string.</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="32a38-113">*Causa*</span><span class="sxs-lookup"><span data-stu-id="32a38-113">*Cause*</span></span>       | <span data-ttu-id="32a38-114">Retorna um valor que indica o que causou o caractere a ser exibido.</span><span class="sxs-lookup"><span data-stu-id="32a38-114">Returns a value that indicates what caused the character to display.</span></span> <span data-ttu-id="32a38-115">2 o usuário mostrou o caractere (usando o menu ou comando de voz).</span><span class="sxs-lookup"><span data-stu-id="32a38-115">2 The user showed the character (using the menu or voice command).</span></span><br/> <span data-ttu-id="32a38-116">4 seu aplicativo cliente mostrou o caractere.</span><span class="sxs-lookup"><span data-stu-id="32a38-116">4 Your client application showed the character.</span></span><br/> <span data-ttu-id="32a38-117">6 outro aplicativo cliente mostrou o caractere.</span><span class="sxs-lookup"><span data-stu-id="32a38-117">6 Another client application showed the character.</span></span><br/> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="32a38-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="32a38-118">Remarks</span></span>

<span data-ttu-id="32a38-119">O servidor envia esse evento para todos os clientes do caractere.</span><span class="sxs-lookup"><span data-stu-id="32a38-119">The server sends this event to all clients of the character.</span></span> <span data-ttu-id="32a38-120">Para consultar o estado atual do caractere, use a propriedade [**Visible**](visible-property.md) .</span><span class="sxs-lookup"><span data-stu-id="32a38-120">To query the current state of the character, use the [**Visible**](visible-property.md) property.</span></span>

### <a name="see-also"></a><span data-ttu-id="32a38-121">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="32a38-121">See Also</span></span>

<span data-ttu-id="32a38-122">[**Ocultar evento**](hide-event.md), [ **VisibilityCause**](visibilitycause-property.md)</span><span class="sxs-lookup"><span data-stu-id="32a38-122">[**Hide event**](hide-event.md), [**VisibilityCause**](visibilitycause-property.md)</span></span>


 

 





