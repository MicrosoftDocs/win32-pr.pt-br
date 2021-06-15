---
title: Propriedade Height (objeto characters)
description: Saiba mais sobre a propriedade altura do objeto de caracteres. O Microsoft Agent foi preterido a partir do Windows 7.
ms.assetid: 2c8dc333-e3c1-4f25-833b-9a4262c75b9f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d93d288276bd9717378c9a1ab0d9b00489959c00
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068502"
---
# <a name="height-property-characters-object"></a><span data-ttu-id="dde1b-104">Propriedade Height (objeto characters)</span><span class="sxs-lookup"><span data-stu-id="dde1b-104">Height Property (Characters Object)</span></span>

<span data-ttu-id="dde1b-105">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="dde1b-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="dde1b-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="dde1b-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="dde1b-107">Retorna ou define a altura do quadro do caractere especificado.</span><span class="sxs-lookup"><span data-stu-id="dde1b-107">Returns or sets the height of the specified character's frame.</span></span>

</dd> <dt>

<span data-ttu-id="dde1b-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="dde1b-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="dde1b-109">\*Agente \***. Caracteres ("**_characterid_\*_")._ \*  \[ =  *Valor* da altura\]</span><span class="sxs-lookup"><span data-stu-id="dde1b-109">*agent\***.Characters ("**_CharacterID_*_").Height_\* \[= *value*\]</span></span>



| <span data-ttu-id="dde1b-110">Parte</span><span class="sxs-lookup"><span data-stu-id="dde1b-110">Part</span></span>    | <span data-ttu-id="dde1b-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="dde1b-111">Description</span></span>                                                 |
|---------|-------------------------------------------------------------|
| <span data-ttu-id="dde1b-112">*value*</span><span class="sxs-lookup"><span data-stu-id="dde1b-112">*value*</span></span> | <span data-ttu-id="dde1b-113">Um inteiro longo que especifica a altura do quadro do caractere.</span><span class="sxs-lookup"><span data-stu-id="dde1b-113">A Long integer that specifies the character's frame height.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dde1b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="dde1b-114">Remarks</span></span>

<span data-ttu-id="dde1b-115">A propriedade **Height** é sempre expressa em pixels, em relação às coordenadas da tela (superior esquerda).</span><span class="sxs-lookup"><span data-stu-id="dde1b-115">The **Height** property is always expressed in pixels, relative to screen coordinates (upper left).</span></span> <span data-ttu-id="dde1b-116">A configuração dessa propriedade se aplica a todos os clientes do caractere.</span><span class="sxs-lookup"><span data-stu-id="dde1b-116">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="dde1b-117">Embora o caractere apareça em uma janela de região com formato irregular, a altura do caractere é baseada nas dimensões externas do quadro de animação retangular usado quando o caractere foi compilado com o editor de caracteres do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="dde1b-117">Even though the character appears in an irregularly shaped region window, the height of the character is based on the external dimensions of the rectangular animation frame used when the character was compiled with the Microsoft Agent Character Editor.</span></span>

 

 




