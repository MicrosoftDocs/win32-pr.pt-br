---
title: Propriedade Top (objeto characters)
description: Saiba mais sobre a propriedade Top (objeto characters). O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.
ms.assetid: d5758a77-2d9a-44b8-bbbb-57ddf96c7fe4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a5e26d2ef578a98447d47eb2a3fae3613760a9
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396341"
---
# <a name="top-property-characters-object"></a><span data-ttu-id="081b2-104">Propriedade Top (objeto characters)</span><span class="sxs-lookup"><span data-stu-id="081b2-104">Top Property (Characters Object)</span></span>

<span data-ttu-id="081b2-105">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="081b2-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="081b2-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="081b2-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="081b2-107">Retorna ou define a borda superior do quadro do caractere especificado.</span><span class="sxs-lookup"><span data-stu-id="081b2-107">Returns or sets the top edge of the specified character's frame.</span></span>

</dd> <dt>

<span data-ttu-id="081b2-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="081b2-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="081b2-109">\*Agente \***. Caracteres ("**_characterid_\*_")._ \*  \[  =  *Valor* superior\]</span><span class="sxs-lookup"><span data-stu-id="081b2-109">*agent\***.Characters ("**_CharacterID_*_").Top_\* \[ = *value*\]</span></span>



| <span data-ttu-id="081b2-110">Parte</span><span class="sxs-lookup"><span data-stu-id="081b2-110">Part</span></span>    | <span data-ttu-id="081b2-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="081b2-111">Description</span></span>                                             |
|---------|---------------------------------------------------------|
| <span data-ttu-id="081b2-112">*value*</span><span class="sxs-lookup"><span data-stu-id="081b2-112">*value*</span></span> | <span data-ttu-id="081b2-113">Um inteiro longo que especifica a borda superior do caractere.</span><span class="sxs-lookup"><span data-stu-id="081b2-113">A Long integer that specifies the character's top edge.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="081b2-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="081b2-114">Remarks</span></span>

<span data-ttu-id="081b2-115">A propriedade **Top** é sempre expressa em pixels, em relação à origem da tela (superior esquerda).</span><span class="sxs-lookup"><span data-stu-id="081b2-115">The **Top** property is always expressed in pixels, relative to screen origin (upper left).</span></span> <span data-ttu-id="081b2-116">A configuração dessa propriedade se aplica a todos os clientes do caractere.</span><span class="sxs-lookup"><span data-stu-id="081b2-116">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="081b2-117">Embora o caractere apareça em uma janela de região com formato irregular, o local do caractere é baseado nas dimensões externas do quadro de animação retangular usado quando o caractere foi compilado com o editor de caracteres do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="081b2-117">Even though the character appears in an irregularly shaped region window, the location of the character is based on the external dimensions of the rectangular animation frame used when the character was compiled with the Microsoft Agent Character Editor.</span></span>

<span data-ttu-id="081b2-118">Use o método [**MoveTo**](moveto-method.md) para alterar o local do caractere.</span><span class="sxs-lookup"><span data-stu-id="081b2-118">Use the [**MoveTo**](moveto-method.md) method to change the character's location.</span></span>

## <a name="see-also"></a><span data-ttu-id="081b2-119">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="081b2-119">See Also</span></span>

<span data-ttu-id="081b2-120">[**Propriedade Left**](left-property.md), [ **método MoveTo**](moveto-method.md)</span><span class="sxs-lookup"><span data-stu-id="081b2-120">[**Left property**](left-property.md), [**MoveTo method**](moveto-method.md)</span></span>


 

 




