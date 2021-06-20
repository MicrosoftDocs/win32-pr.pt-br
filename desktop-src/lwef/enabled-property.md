---
title: Propriedade Enabled (objeto Balloon)
description: Saiba mais sobre a propriedade de objeto balão habilitada. O Microsoft Agent foi preterido a partir do Windows 7.
ms.assetid: 4d73acda-6fcc-4912-a466-570849aeb807
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 602d39a9bef7713a92707d8a43050f04a3577b6d
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407299"
---
# <a name="enabled-property-balloon-object"></a><span data-ttu-id="7403f-104">Propriedade Enabled (objeto Balloon)</span><span class="sxs-lookup"><span data-stu-id="7403f-104">Enabled Property (Balloon Object)</span></span>

<span data-ttu-id="7403f-105">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7403f-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="7403f-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="7403f-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="7403f-107">Retorna se o balão de palavra está habilitado para o caractere especificado.</span><span class="sxs-lookup"><span data-stu-id="7403f-107">Returns whether the word balloon is enabled for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="7403f-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="7403f-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="7403f-109">\*agente \***. Caracteres ("**_characterid_*_"). Balão. habilitado_*</span><span class="sxs-lookup"><span data-stu-id="7403f-109">*agent\***.Characters ("**_CharacterID_*_").Balloon.Enabled_\*</span></span>



| <span data-ttu-id="7403f-110">Valor</span><span class="sxs-lookup"><span data-stu-id="7403f-110">Value</span></span>     | <span data-ttu-id="7403f-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="7403f-111">Description</span></span>              |
|-----------|--------------------------|
| <span data-ttu-id="7403f-112">**Verdadeiro**</span><span class="sxs-lookup"><span data-stu-id="7403f-112">**True**</span></span>  | <span data-ttu-id="7403f-113">O balão está habilitado.</span><span class="sxs-lookup"><span data-stu-id="7403f-113">The balloon is enabled.</span></span>  |
| <span data-ttu-id="7403f-114">**Falso**</span><span class="sxs-lookup"><span data-stu-id="7403f-114">**False**</span></span> | <span data-ttu-id="7403f-115">O balão está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="7403f-115">The balloon is disabled.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7403f-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="7403f-116">Remarks</span></span>

<span data-ttu-id="7403f-117">A propriedade **Enabled** retorna um valor booliano que especifica se o balão está habilitado.</span><span class="sxs-lookup"><span data-stu-id="7403f-117">The **Enabled** property returns a Boolean value specifying whether the balloon is enabled.</span></span> <span data-ttu-id="7403f-118">O estado padrão do balão de palavras é definido como parte da definição de um caractere quando o caractere é compilado no editor de caracteres do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="7403f-118">The word balloon default state is set as part of a character's definition when the character is compiled in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="7403f-119">Se um caractere for definido para não oferecer suporte à palavra balão, essa propriedade será sempre **falsa** para o caractere.</span><span class="sxs-lookup"><span data-stu-id="7403f-119">If a character is defined to not support the word balloon, this property will always be **False** for the character.</span></span>

 

 




