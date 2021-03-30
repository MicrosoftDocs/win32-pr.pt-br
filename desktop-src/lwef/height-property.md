---
title: Propriedade Height (objeto characters)
description: Propriedade Height
ms.assetid: 2c8dc333-e3c1-4f25-833b-9a4262c75b9f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e504dcbbfd470c62b4102d86f25a1d2b3c4c25e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103644105"
---
# <a name="height-property-characters-object"></a><span data-ttu-id="a6b1f-103">Propriedade Height (objeto characters)</span><span class="sxs-lookup"><span data-stu-id="a6b1f-103">Height Property (Characters Object)</span></span>

<span data-ttu-id="a6b1f-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a6b1f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="a6b1f-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="a6b1f-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="a6b1f-106">Retorna ou define a altura do quadro do caractere especificado.</span><span class="sxs-lookup"><span data-stu-id="a6b1f-106">Returns or sets the height of the specified character's frame.</span></span>

</dd> <dt>

<span data-ttu-id="a6b1f-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="a6b1f-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="a6b1f-108">\*Agente \***. Caracteres ("**_characterid_\*_")._ \*  \[ =  *Valor* da altura\]</span><span class="sxs-lookup"><span data-stu-id="a6b1f-108">*agent\***.Characters ("**_CharacterID_*_").Height_\* \[= *value*\]</span></span>



| <span data-ttu-id="a6b1f-109">Parte</span><span class="sxs-lookup"><span data-stu-id="a6b1f-109">Part</span></span>    | <span data-ttu-id="a6b1f-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="a6b1f-110">Description</span></span>                                                 |
|---------|-------------------------------------------------------------|
| <span data-ttu-id="a6b1f-111">*value*</span><span class="sxs-lookup"><span data-stu-id="a6b1f-111">*value*</span></span> | <span data-ttu-id="a6b1f-112">Um inteiro longo que especifica a altura do quadro do caractere.</span><span class="sxs-lookup"><span data-stu-id="a6b1f-112">A Long integer that specifies the character's frame height.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a6b1f-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="a6b1f-113">Remarks</span></span>

<span data-ttu-id="a6b1f-114">A propriedade **Height** é sempre expressa em pixels, em relação às coordenadas da tela (superior esquerda).</span><span class="sxs-lookup"><span data-stu-id="a6b1f-114">The **Height** property is always expressed in pixels, relative to screen coordinates (upper left).</span></span> <span data-ttu-id="a6b1f-115">A configuração dessa propriedade se aplica a todos os clientes do caractere.</span><span class="sxs-lookup"><span data-stu-id="a6b1f-115">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="a6b1f-116">Embora o caractere apareça em uma janela de região com formato irregular, a altura do caractere é baseada nas dimensões externas do quadro de animação retangular usado quando o caractere foi compilado com o editor de caracteres do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="a6b1f-116">Even though the character appears in an irregularly shaped region window, the height of the character is based on the external dimensions of the rectangular animation frame used when the character was compiled with the Microsoft Agent Character Editor.</span></span>

 

 




