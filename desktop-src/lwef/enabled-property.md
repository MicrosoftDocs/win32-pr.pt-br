---
title: Propriedade Enabled (objeto Balloon)
description: Propriedade Enabled
ms.assetid: 4d73acda-6fcc-4912-a466-570849aeb807
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07179390b183e98a5eaccb2dfdb4405525d7d26e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105781163"
---
# <a name="enabled-property-balloon-object"></a><span data-ttu-id="802c3-103">Propriedade Enabled (objeto Balloon)</span><span class="sxs-lookup"><span data-stu-id="802c3-103">Enabled Property (Balloon Object)</span></span>

<span data-ttu-id="802c3-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="802c3-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="802c3-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="802c3-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="802c3-106">Retorna se o balão de palavra está habilitado para o caractere especificado.</span><span class="sxs-lookup"><span data-stu-id="802c3-106">Returns whether the word balloon is enabled for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="802c3-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="802c3-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="802c3-108">\*agente \***. Caracteres ("**_characterid_*_"). Balão. habilitado_*</span><span class="sxs-lookup"><span data-stu-id="802c3-108">*agent\***.Characters ("**_CharacterID_*_").Balloon.Enabled_\*</span></span>



| <span data-ttu-id="802c3-109">Valor</span><span class="sxs-lookup"><span data-stu-id="802c3-109">Value</span></span>     | <span data-ttu-id="802c3-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="802c3-110">Description</span></span>              |
|-----------|--------------------------|
| <span data-ttu-id="802c3-111">**Verdadeiro**</span><span class="sxs-lookup"><span data-stu-id="802c3-111">**True**</span></span>  | <span data-ttu-id="802c3-112">O balão está habilitado.</span><span class="sxs-lookup"><span data-stu-id="802c3-112">The balloon is enabled.</span></span>  |
| <span data-ttu-id="802c3-113">**Falso**</span><span class="sxs-lookup"><span data-stu-id="802c3-113">**False**</span></span> | <span data-ttu-id="802c3-114">O balão está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="802c3-114">The balloon is disabled.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="802c3-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="802c3-115">Remarks</span></span>

<span data-ttu-id="802c3-116">A propriedade **Enabled** retorna um valor booliano que especifica se o balão está habilitado.</span><span class="sxs-lookup"><span data-stu-id="802c3-116">The **Enabled** property returns a Boolean value specifying whether the balloon is enabled.</span></span> <span data-ttu-id="802c3-117">O estado padrão do balão de palavras é definido como parte da definição de um caractere quando o caractere é compilado no editor de caracteres do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="802c3-117">The word balloon default state is set as part of a character's definition when the character is compiled in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="802c3-118">Se um caractere for definido para não oferecer suporte à palavra balão, essa propriedade será sempre **falsa** para o caractere.</span><span class="sxs-lookup"><span data-stu-id="802c3-118">If a character is defined to not support the word balloon, this property will always be **False** for the character.</span></span>

 

 




