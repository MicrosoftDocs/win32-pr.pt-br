---
title: Evento de tamanho
description: Evento de tamanho
ms.assetid: 06089f84-8e75-475f-a492-536c83fa6730
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d9a896d2dcbf8b925c0ca13fa429f6dfd95bc21
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822551"
---
# <a name="size-event"></a><span data-ttu-id="458cc-103">Evento de tamanho</span><span class="sxs-lookup"><span data-stu-id="458cc-103">Size Event</span></span>

<span data-ttu-id="458cc-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="458cc-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="458cc-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="458cc-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="458cc-106">Ocorre quando o tamanho de um caractere é alterado.</span><span class="sxs-lookup"><span data-stu-id="458cc-106">Occurs when a character's size changes.</span></span>

</dd> <dt>

<span data-ttu-id="458cc-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="458cc-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="458cc-108"> Tamanho do *subagente* \_ **(ByVal** *caractereid*, **ByVal** *largura*, **ByVal** *Height*)</span><span class="sxs-lookup"><span data-stu-id="458cc-108">**Sub** *agent*\_**Size (ByVal** *CharacterID*, **ByVal** *Width*, **ByVal** *Height*)</span></span>



| <span data-ttu-id="458cc-109">Parte</span><span class="sxs-lookup"><span data-stu-id="458cc-109">Part</span></span>          | <span data-ttu-id="458cc-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="458cc-110">Description</span></span>                                                         |
|---------------|---------------------------------------------------------------------|
| <span data-ttu-id="458cc-111">*Caractere de caracteres*</span><span class="sxs-lookup"><span data-stu-id="458cc-111">*CharacterID*</span></span> | <span data-ttu-id="458cc-112">Retorna a ID do caractere movido.</span><span class="sxs-lookup"><span data-stu-id="458cc-112">Returns the ID of the character that moved.</span></span>                         |
| <span data-ttu-id="458cc-113">*Largura*</span><span class="sxs-lookup"><span data-stu-id="458cc-113">*Width*</span></span>       | <span data-ttu-id="458cc-114">Retorna a nova largura do quadro de caracteres (em pixels) como um inteiro.</span><span class="sxs-lookup"><span data-stu-id="458cc-114">Returns the character frame's new width (in pixels) as an integer.</span></span>  |
| <span data-ttu-id="458cc-115">*Altura*</span><span class="sxs-lookup"><span data-stu-id="458cc-115">*Height*</span></span>      | <span data-ttu-id="458cc-116">Retorna a nova altura do quadro de caracteres (em pixels) como um inteiro.</span><span class="sxs-lookup"><span data-stu-id="458cc-116">Returns the character frame's new height (in pixels) as an integer.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="458cc-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="458cc-117">Remarks</span></span>

<span data-ttu-id="458cc-118">Esse evento ocorre quando um aplicativo altera o tamanho de um caractere.</span><span class="sxs-lookup"><span data-stu-id="458cc-118">This event occurs when an application changes the size of a character.</span></span> <span data-ttu-id="458cc-119">Esse evento é enviado somente para os clientes do caractere (aplicativos que carregaram o caractere).</span><span class="sxs-lookup"><span data-stu-id="458cc-119">This event is sent only to the clients of the character (applications that have loaded the character).</span></span>

### <a name="see-also"></a><span data-ttu-id="458cc-120">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="458cc-120">See Also</span></span>

[<span data-ttu-id="458cc-121">**Mover evento**</span><span class="sxs-lookup"><span data-stu-id="458cc-121">**Move event**</span></span>](move-event.md)


 

 




