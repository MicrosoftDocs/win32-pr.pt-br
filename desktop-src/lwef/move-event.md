---
title: Mover evento
description: Mover evento
ms.assetid: 973e9e68-edbb-4741-b50e-57db96712df8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31facb1d57b807fb0322783a291b77ef5a7c1487
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822664"
---
# <a name="move-event"></a><span data-ttu-id="33296-103">Mover evento</span><span class="sxs-lookup"><span data-stu-id="33296-103">Move Event</span></span>

<span data-ttu-id="33296-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="33296-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="33296-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="33296-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="33296-106">Ocorre quando um caractere é movido.</span><span class="sxs-lookup"><span data-stu-id="33296-106">Occurs when a character is moved.</span></span>

</dd> <dt>

<span data-ttu-id="33296-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="33296-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="33296-108"> Movimentação de *subagente* \_ **(ByVal** *caractereid*, **ByVal** *X*, **ByVal** *Y*, **ByVal** *causa\ *\ * *)**</span><span class="sxs-lookup"><span data-stu-id="33296-108">**Sub** *agent*\_**Move (ByVal** *CharacterID*, **ByVal** *X*, **ByVal** *Y*, **ByVal** *Cause\*\*\*)*\*</span></span>



| <span data-ttu-id="33296-109">Parte</span><span class="sxs-lookup"><span data-stu-id="33296-109">Part</span></span>          | <span data-ttu-id="33296-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="33296-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                   |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33296-111">*Caractere de caracteres*</span><span class="sxs-lookup"><span data-stu-id="33296-111">*CharacterID*</span></span> | <span data-ttu-id="33296-112">Retorna a ID do caractere movido.</span><span class="sxs-lookup"><span data-stu-id="33296-112">Returns the ID of the character that moved.</span></span>                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="33296-113">*X*</span><span class="sxs-lookup"><span data-stu-id="33296-113">*X*</span></span>           | <span data-ttu-id="33296-114">Retorna a coordenada x (em pixels) da borda superior do novo local do quadro de caracteres como um inteiro.</span><span class="sxs-lookup"><span data-stu-id="33296-114">Returns the x-coordinate (in pixels) of the top edge of character frame's new location as an integer.</span></span>                                                                                                                                                                                                                                         |
| <span data-ttu-id="33296-115">*S*</span><span class="sxs-lookup"><span data-stu-id="33296-115">*Y*</span></span>           | <span data-ttu-id="33296-116">Retorna a coordenada y (em pixels) da borda esquerda do novo local do quadro de caracteres como um inteiro.</span><span class="sxs-lookup"><span data-stu-id="33296-116">Returns the y-coordinate (in pixels) of the left edge of character frame's new location as an integer.</span></span>                                                                                                                                                                                                                                        |
| <span data-ttu-id="33296-117">*Causa*</span><span class="sxs-lookup"><span data-stu-id="33296-117">*Cause*</span></span>       | <span data-ttu-id="33296-118">Retorna um valor que indica o que causou a movimentação do caractere.</span><span class="sxs-lookup"><span data-stu-id="33296-118">Returns a value that indicates what caused the character to move.</span></span> <span data-ttu-id="33296-119">1 o usuário arrastou o caractere.</span><span class="sxs-lookup"><span data-stu-id="33296-119">1 The user dragged the character.</span></span><br/> <span data-ttu-id="33296-120">2 o aplicativo cliente moveu o caractere.</span><span class="sxs-lookup"><span data-stu-id="33296-120">2 Your client application moved the character.</span></span><br/> <span data-ttu-id="33296-121">3 outro aplicativo cliente moveu o caractere.</span><span class="sxs-lookup"><span data-stu-id="33296-121">3 Another client application moved the character.</span></span><br/> <span data-ttu-id="33296-122">4 o servidor do agente moveu o caractere para mantê-lo na tela após a alteração da resolução da tela.</span><span class="sxs-lookup"><span data-stu-id="33296-122">4 The Agent server moved the character to keep it onscreen after a screen resolution change.</span></span><br/> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="33296-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="33296-123">Remarks</span></span>

<span data-ttu-id="33296-124">Esse evento ocorre quando o usuário ou um aplicativo altera a posição do caractere.</span><span class="sxs-lookup"><span data-stu-id="33296-124">This event occurs when the user or an application changes the character's position.</span></span> <span data-ttu-id="33296-125">As coordenadas são relevantes para o canto superior esquerdo da tela.</span><span class="sxs-lookup"><span data-stu-id="33296-125">Coordinates are relevant to the upper left corner of the screen.</span></span> <span data-ttu-id="33296-126">Esse evento é enviado somente para os clientes do caractere (aplicativos que carregaram o caractere).</span><span class="sxs-lookup"><span data-stu-id="33296-126">This event is sent only to the clients of the character (applications that have loaded the character).</span></span>

<span data-ttu-id="33296-127">**Consulte também**</span><span class="sxs-lookup"><span data-stu-id="33296-127">**See Also**</span></span>

<span data-ttu-id="33296-128">[**Propriedade MoveCause**](movecause-property.md), [ **evento size**](size-event.md)</span><span class="sxs-lookup"><span data-stu-id="33296-128">[**MoveCause property**](movecause-property.md), [**Size event**](size-event.md)</span></span>

 

 





