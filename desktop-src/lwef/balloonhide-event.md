---
title: Evento BalloonHide
description: Evento BalloonHide
ms.assetid: dd1f3e83-f3d9-496e-9a54-b3a23b2403da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 062a82afcabb3597ca8c254e039c231b52033657
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160338"
---
# <a name="balloonhide-event"></a><span data-ttu-id="df9be-103">Evento BalloonHide</span><span class="sxs-lookup"><span data-stu-id="df9be-103">BalloonHide Event</span></span>

<span data-ttu-id="df9be-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="df9be-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="df9be-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="df9be-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="df9be-106">Ocorre quando o balão de palavra de um caractere é ocultado.</span><span class="sxs-lookup"><span data-stu-id="df9be-106">Occurs when a character's word balloon is hidden.</span></span>

</dd> <dt>

<span data-ttu-id="df9be-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="df9be-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="df9be-108">**Sub** *Agent* \_ **BalloonHide** **(ByVal** *characterid \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="df9be-108">**Sub** *agent*\_**BalloonHide** **(ByVal** *CharacterID\*\*\*)*\*</span></span>



| <span data-ttu-id="df9be-109">Parte</span><span class="sxs-lookup"><span data-stu-id="df9be-109">Part</span></span>          | <span data-ttu-id="df9be-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="df9be-110">Description</span></span>                                                       |
|---------------|-------------------------------------------------------------------|
| <span data-ttu-id="df9be-111">*Caractere de caracteres*</span><span class="sxs-lookup"><span data-stu-id="df9be-111">*CharacterID*</span></span> | <span data-ttu-id="df9be-112">Retorna a ID do caractere associado à palavra balão.</span><span class="sxs-lookup"><span data-stu-id="df9be-112">Returns the ID of the character associated with the word balloon.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="df9be-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="df9be-113">Remarks</span></span>

<span data-ttu-id="df9be-114">O servidor envia esse evento somente para os clientes do caractere (aplicativos que carregaram o caractere) que usa o balão de palavra.</span><span class="sxs-lookup"><span data-stu-id="df9be-114">The server sends this event only to the clients of the character (applications that have loaded the character) that uses the word balloon.</span></span>

### <a name="see-also"></a><span data-ttu-id="df9be-115">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="df9be-115">See Also</span></span>

[<span data-ttu-id="df9be-116">**Evento BalloonShow**</span><span class="sxs-lookup"><span data-stu-id="df9be-116">**BalloonShow event**</span></span>](balloonshow-event.md)


 

 




