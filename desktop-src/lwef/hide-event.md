---
title: Ocultar evento
description: Ocultar evento
ms.assetid: vs|msagent|~\pacontrol_9yuk.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87d396fb0985cd4c3c2e9647dfe0e7c9126ad9c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822674"
---
# <a name="hide-event"></a><span data-ttu-id="6f66d-103">Ocultar evento</span><span class="sxs-lookup"><span data-stu-id="6f66d-103">Hide Event</span></span>

<span data-ttu-id="6f66d-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6f66d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="6f66d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="6f66d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="6f66d-106">Ocorre quando um caractere é ocultado.</span><span class="sxs-lookup"><span data-stu-id="6f66d-106">Occurs when a character is hidden.</span></span>

</dd> <dt>

<span data-ttu-id="6f66d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="6f66d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="6f66d-108">**Sub** *Agent \* \* \* \_ ocultar (* \*  **ByVal** *characterid*, **ByVal** *causa \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="6f66d-108">**Sub** *agent\*\*\*\_Hide(*\* **ByVal** *CharacterID*, **ByVal** *Cause\*\*\*)*\*</span></span>



| <span data-ttu-id="6f66d-109">Parte</span><span class="sxs-lookup"><span data-stu-id="6f66d-109">Part</span></span>          | <span data-ttu-id="6f66d-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="6f66d-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f66d-111">*Caractere de caracteres*</span><span class="sxs-lookup"><span data-stu-id="6f66d-111">*CharacterID*</span></span> | <span data-ttu-id="6f66d-112">Retorna a ID do caractere oculto como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="6f66d-112">Returns the ID of the hidden character as a string.</span></span>                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="6f66d-113">*Causa*</span><span class="sxs-lookup"><span data-stu-id="6f66d-113">*Cause*</span></span>       | <span data-ttu-id="6f66d-114">Retorna um valor que indica o que causou a ocultação do caractere.</span><span class="sxs-lookup"><span data-stu-id="6f66d-114">Returns a value that indicates what caused the character to hide.</span></span> <span data-ttu-id="6f66d-115">1 usuário ocultou o caractere selecionando o comando no menu pop-up do ícone da barra de tarefas do caractere ou usando a entrada de fala.</span><span class="sxs-lookup"><span data-stu-id="6f66d-115">1 User hid the character by selecting the command on the character's taskbar icon pop-up menu or using speech input.</span></span><br/> <span data-ttu-id="6f66d-116">3 o aplicativo cliente ocultou o caractere.</span><span class="sxs-lookup"><span data-stu-id="6f66d-116">3 Your client application hid the character.</span></span><br/> <span data-ttu-id="6f66d-117">5 outro aplicativo cliente ocultou o caractere.</span><span class="sxs-lookup"><span data-stu-id="6f66d-117">5 Another client application hid the character.</span></span><br/> <span data-ttu-id="6f66d-118">7 o usuário ocultou o caractere selecionando o comando no menu pop-up do caractere.</span><span class="sxs-lookup"><span data-stu-id="6f66d-118">7 User hid the character by selecting the command on the character's pop-up menu.</span></span><br/> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="6f66d-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="6f66d-119">Remarks</span></span>

<span data-ttu-id="6f66d-120">O servidor envia esse evento para todos os clientes do caractere.</span><span class="sxs-lookup"><span data-stu-id="6f66d-120">The server sends this event to all clients of the character.</span></span> <span data-ttu-id="6f66d-121">Para consultar o estado atual do caractere, use a propriedade [**Visible**](visible-property.md) .</span><span class="sxs-lookup"><span data-stu-id="6f66d-121">To query the current state of the character, use the [**Visible**](visible-property.md) property.</span></span>

### <a name="see-also"></a><span data-ttu-id="6f66d-122">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="6f66d-122">See Also</span></span>

<span data-ttu-id="6f66d-123">[**Mostrar evento**](show-event.md), [ **VisibilityCause**](visibilitycause-property.md)</span><span class="sxs-lookup"><span data-stu-id="6f66d-123">[**Show event**](show-event.md), [**VisibilityCause**](visibilitycause-property.md)</span></span>


 

 





