---
title: Evento IdleStart
description: Evento IdleStart
ms.assetid: 3d97c26b-b88a-42e3-9072-0bc65510efc2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 706aafc13cb1639484539e3d08b305df217ecec8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105790332"
---
# <a name="idlestart-event"></a><span data-ttu-id="f23cb-103">Evento IdleStart</span><span class="sxs-lookup"><span data-stu-id="f23cb-103">IdleStart Event</span></span>

<span data-ttu-id="f23cb-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f23cb-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="f23cb-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="f23cb-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="f23cb-106">Ocorre quando o servidor define um caractere para o estado **deixar** .</span><span class="sxs-lookup"><span data-stu-id="f23cb-106">Occurs when the server sets a character to the **Idling** state.</span></span>

</dd> <dt>

<span data-ttu-id="f23cb-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="f23cb-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="f23cb-108">**Sub** *Agent \* \* \* \_ IdleStart* \*  **(ByVal** *characterid \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="f23cb-108">**Sub** *agent\*\*\*\_IdleStart*\* **(ByVal** *CharacterID\*\*\*)*\*</span></span>



| <span data-ttu-id="f23cb-109">Parte</span><span class="sxs-lookup"><span data-stu-id="f23cb-109">Part</span></span>          | <span data-ttu-id="f23cb-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="f23cb-110">Description</span></span>                                         |
|---------------|-----------------------------------------------------|
| <span data-ttu-id="f23cb-111">*Caractere de caracteres*</span><span class="sxs-lookup"><span data-stu-id="f23cb-111">*CharacterID*</span></span> | <span data-ttu-id="f23cb-112">Retorna a ID do caractere deixar como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="f23cb-112">Returns the ID of the idling character as a string.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="f23cb-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="f23cb-113">Remarks</span></span>

<span data-ttu-id="f23cb-114">O servidor envia esse evento para todos os clientes do caractere.</span><span class="sxs-lookup"><span data-stu-id="f23cb-114">The server sends this event to all clients of the character.</span></span>

### <a name="see-also"></a><span data-ttu-id="f23cb-115">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="f23cb-115">See Also</span></span>

[<span data-ttu-id="f23cb-116">**Evento IdleComplete**</span><span class="sxs-lookup"><span data-stu-id="f23cb-116">**IdleComplete event**</span></span>](idlecomplete-event.md)


 

 




