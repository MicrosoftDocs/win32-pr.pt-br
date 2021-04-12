---
title: Evento DefaultCharacterChange
description: Evento DefaultCharacterChange
ms.assetid: 14b86a44-8fd2-4719-b7b5-cdcc618d27cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab92fe04f9c42466d559e9b4610eafc8490556d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364194"
---
# <a name="defaultcharacterchange-event"></a><span data-ttu-id="0628f-103">Evento DefaultCharacterChange</span><span class="sxs-lookup"><span data-stu-id="0628f-103">DefaultCharacterChange Event</span></span>

<span data-ttu-id="0628f-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0628f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="0628f-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="0628f-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="0628f-106">Ocorre quando o usuário altera o caractere padrão.</span><span class="sxs-lookup"><span data-stu-id="0628f-106">Occurs when the user changes the default character.</span></span>

</dd> <dt>

<span data-ttu-id="0628f-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="0628f-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="0628f-108">**Sub** *Agent. \* \* \* DefaultCharacterChange* \*  **(ByVal** *GUID \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="0628f-108">**Sub** *agent.\*\*\*DefaultCharacterChange*\* **(ByVal** *GUID\*\*\*)*\*</span></span>



| <span data-ttu-id="0628f-109">Parte</span><span class="sxs-lookup"><span data-stu-id="0628f-109">Part</span></span>   | <span data-ttu-id="0628f-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="0628f-110">Description</span></span>                                      |
|--------|--------------------------------------------------|
| <span data-ttu-id="0628f-111">*GUID*</span><span class="sxs-lookup"><span data-stu-id="0628f-111">*GUID*</span></span> | <span data-ttu-id="0628f-112">Retorna o identificador exclusivo do caractere.</span><span class="sxs-lookup"><span data-stu-id="0628f-112">Returns the unique identifier for the character.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="0628f-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="0628f-113">Remarks</span></span>

<span data-ttu-id="0628f-114">Esse evento indica quando o usuário alterou o caractere atribuído como o caractere padrão do usuário.</span><span class="sxs-lookup"><span data-stu-id="0628f-114">This event indicates when the user has changed the character assigned as the user's default character.</span></span> <span data-ttu-id="0628f-115">O servidor envia isso somente para clientes que carregaram o caractere padrão.</span><span class="sxs-lookup"><span data-stu-id="0628f-115">The server sends this only to clients that have loaded the default character.</span></span>

<span data-ttu-id="0628f-116">Quando o novo caractere é exibido, ele assume o mesmo tamanho que qualquer instância já carregada do caractere ou o caractere padrão anterior (nessa ordem).</span><span class="sxs-lookup"><span data-stu-id="0628f-116">When the new character appears, it assumes the same size as any already loaded instance of the character or the previous default character (in that order).</span></span>

### <a name="see-also"></a><span data-ttu-id="0628f-117">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="0628f-117">See Also</span></span>

<span data-ttu-id="0628f-118">[**Método ShowDefaultCharacterProperties**](showdefaultcharacterproperties-method.md), [ **método Load**](load-method.md)</span><span class="sxs-lookup"><span data-stu-id="0628f-118">[**ShowDefaultCharacterProperties method**](showdefaultcharacterproperties-method.md), [**Load method**](load-method.md)</span></span>


 

 




