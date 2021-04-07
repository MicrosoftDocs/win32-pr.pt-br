---
title: Evento IdleComplete
description: Evento IdleComplete
ms.assetid: 1d684f75-f23e-4ed8-a60a-5e6792332103
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01782825dc880dc4d214a8d0e682d69a9f842e22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004779"
---
# <a name="idlecomplete-event"></a><span data-ttu-id="d586d-103">Evento IdleComplete</span><span class="sxs-lookup"><span data-stu-id="d586d-103">IdleComplete Event</span></span>

<span data-ttu-id="d586d-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d586d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="d586d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="d586d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="d586d-106">Ocorre quando o servidor termina o estado **deixar** de um caractere.</span><span class="sxs-lookup"><span data-stu-id="d586d-106">Occurs when the server ends the **Idling** state of a character.</span></span>

</dd> <dt>

<span data-ttu-id="d586d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="d586d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="d586d-108">**Sub** *Agent \* \* \* \_ IdleComplete* \*  **(ByVal** *characterid \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="d586d-108">**Sub** *agent\*\*\*\_IdleComplete*\* **(ByVal** *CharacterID\*\*\*)*\*</span></span>



| <span data-ttu-id="d586d-109">Parte</span><span class="sxs-lookup"><span data-stu-id="d586d-109">Part</span></span>          | <span data-ttu-id="d586d-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="d586d-110">Description</span></span>                                         |
|---------------|-----------------------------------------------------|
| <span data-ttu-id="d586d-111">*Caractere de caracteres*</span><span class="sxs-lookup"><span data-stu-id="d586d-111">*CharacterID*</span></span> | <span data-ttu-id="d586d-112">Retorna a ID do caractere deixar como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d586d-112">Returns the ID of the idling character as a string.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="d586d-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="d586d-113">Remarks</span></span>

<span data-ttu-id="d586d-114">O servidor envia esse evento para todos os clientes do caractere.</span><span class="sxs-lookup"><span data-stu-id="d586d-114">The server sends this event to all clients of the character.</span></span>

### <a name="see-also"></a><span data-ttu-id="d586d-115">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="d586d-115">See Also</span></span>

[<span data-ttu-id="d586d-116">**Evento IdleStart**</span><span class="sxs-lookup"><span data-stu-id="d586d-116">**IdleStart event**</span></span>](idlestart-event.md)


 

 




