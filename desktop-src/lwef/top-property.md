---
title: Propriedade Top (objeto characters)
description: Propriedade Top
ms.assetid: d5758a77-2d9a-44b8-bbbb-57ddf96c7fe4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef724c7052ad1d9ba5cb51ea46ccd7647723ed32
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105766482"
---
# <a name="top-property-characters-object"></a><span data-ttu-id="65c8d-103">Propriedade Top (objeto characters)</span><span class="sxs-lookup"><span data-stu-id="65c8d-103">Top Property (Characters Object)</span></span>

<span data-ttu-id="65c8d-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="65c8d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="65c8d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="65c8d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="65c8d-106">Retorna ou define a borda superior do quadro do caractere especificado.</span><span class="sxs-lookup"><span data-stu-id="65c8d-106">Returns or sets the top edge of the specified character's frame.</span></span>

</dd> <dt>

<span data-ttu-id="65c8d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="65c8d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="65c8d-108">\*Agente \***. Caracteres ("**_characterid_\*_")._ \*  \[  =  *Valor* superior\]</span><span class="sxs-lookup"><span data-stu-id="65c8d-108">*agent\***.Characters ("**_CharacterID_*_").Top_\* \[ = *value*\]</span></span>



| <span data-ttu-id="65c8d-109">Parte</span><span class="sxs-lookup"><span data-stu-id="65c8d-109">Part</span></span>    | <span data-ttu-id="65c8d-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="65c8d-110">Description</span></span>                                             |
|---------|---------------------------------------------------------|
| <span data-ttu-id="65c8d-111">*value*</span><span class="sxs-lookup"><span data-stu-id="65c8d-111">*value*</span></span> | <span data-ttu-id="65c8d-112">Um inteiro longo que especifica a borda superior do caractere.</span><span class="sxs-lookup"><span data-stu-id="65c8d-112">A Long integer that specifies the character's top edge.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="65c8d-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="65c8d-113">Remarks</span></span>

<span data-ttu-id="65c8d-114">A propriedade **Top** é sempre expressa em pixels, em relação à origem da tela (superior esquerda).</span><span class="sxs-lookup"><span data-stu-id="65c8d-114">The **Top** property is always expressed in pixels, relative to screen origin (upper left).</span></span> <span data-ttu-id="65c8d-115">A configuração dessa propriedade se aplica a todos os clientes do caractere.</span><span class="sxs-lookup"><span data-stu-id="65c8d-115">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="65c8d-116">Embora o caractere apareça em uma janela de região com formato irregular, o local do caractere é baseado nas dimensões externas do quadro de animação retangular usado quando o caractere foi compilado com o editor de caracteres do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="65c8d-116">Even though the character appears in an irregularly shaped region window, the location of the character is based on the external dimensions of the rectangular animation frame used when the character was compiled with the Microsoft Agent Character Editor.</span></span>

<span data-ttu-id="65c8d-117">Use o método [**MoveTo**](moveto-method.md) para alterar o local do caractere.</span><span class="sxs-lookup"><span data-stu-id="65c8d-117">Use the [**MoveTo**](moveto-method.md) method to change the character's location.</span></span>

## <a name="see-also"></a><span data-ttu-id="65c8d-118">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="65c8d-118">See Also</span></span>

<span data-ttu-id="65c8d-119">[**Propriedade Left**](left-property.md), [ **método MoveTo**](moveto-method.md)</span><span class="sxs-lookup"><span data-stu-id="65c8d-119">[**Left property**](left-property.md), [**MoveTo method**](moveto-method.md)</span></span>


 

 




