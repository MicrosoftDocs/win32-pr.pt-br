---
title: Evento BalloonShow
description: Evento BalloonShow
ms.assetid: 8a73e883-c003-480b-8a0a-e699caffe54c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de67318b02775619332fe60ea47fb27edb893c8b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364264"
---
# <a name="balloonshow-event"></a><span data-ttu-id="43fa6-103">Evento BalloonShow</span><span class="sxs-lookup"><span data-stu-id="43fa6-103">BalloonShow Event</span></span>

<span data-ttu-id="43fa6-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="43fa6-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="43fa6-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="43fa6-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="43fa6-106">Ocorre quando o balão de palavra de um caractere é mostrado.</span><span class="sxs-lookup"><span data-stu-id="43fa6-106">Occurs when a character's word balloon is shown.</span></span>

</dd> <dt>

<span data-ttu-id="43fa6-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="43fa6-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="43fa6-108">**Sub** *Agent* \_ **BalloonShow** **(ByVal** *characterid \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="43fa6-108">**Sub** *agent*\_**BalloonShow** **(ByVal** *CharacterID\*\*\*)*\*</span></span>



| <span data-ttu-id="43fa6-109">Parte</span><span class="sxs-lookup"><span data-stu-id="43fa6-109">Part</span></span>          | <span data-ttu-id="43fa6-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="43fa6-110">Description</span></span>                                                       |
|---------------|-------------------------------------------------------------------|
| <span data-ttu-id="43fa6-111">*Caractere de caracteres*</span><span class="sxs-lookup"><span data-stu-id="43fa6-111">*CharacterID*</span></span> | <span data-ttu-id="43fa6-112">Retorna a ID do caractere associado à palavra balão.</span><span class="sxs-lookup"><span data-stu-id="43fa6-112">Returns the ID of the character associated with the word balloon.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="43fa6-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="43fa6-113">Remarks</span></span>

<span data-ttu-id="43fa6-114">O servidor envia esse evento somente para os clientes do caractere (aplicativos que carregaram o caractere) que usa o balão de palavra.</span><span class="sxs-lookup"><span data-stu-id="43fa6-114">The server sends this event only to the clients of the character (applications that have loaded the character) that uses the word balloon.</span></span>

### <a name="see-also"></a><span data-ttu-id="43fa6-115">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="43fa6-115">See Also</span></span>

[<span data-ttu-id="43fa6-116">**Evento BalloonHide**</span><span class="sxs-lookup"><span data-stu-id="43fa6-116">**BalloonHide event**</span></span>](balloonhide-event.md)


 

 




