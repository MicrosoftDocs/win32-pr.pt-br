---
title: Propriedade Width (objeto characters)
description: Propriedade Width
ms.assetid: ebada4cc-dbe6-4540-be1f-1f61e176765b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a37a29bd8f50231bd44b6529a0c1ce13c0256d3
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104008718"
---
# <a name="width-property-characters-object"></a><span data-ttu-id="74968-103">Propriedade Width (objeto characters)</span><span class="sxs-lookup"><span data-stu-id="74968-103">Width Property (Characters Object)</span></span>

<span data-ttu-id="74968-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="74968-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="74968-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="74968-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="74968-106">Retorna ou define a largura do quadro para o caractere especificado.</span><span class="sxs-lookup"><span data-stu-id="74968-106">Returns or sets the width of the frame for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="74968-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="74968-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="74968-108">\*Agente \***. Caracteres ("**_characterid_\*_")._ \*  \[ =  *Valor* de largura\]</span><span class="sxs-lookup"><span data-stu-id="74968-108">*agent\***.Characters ("**_CharacterID_*_").Width_\* \[= *value*\]</span></span>



| <span data-ttu-id="74968-109">Parte</span><span class="sxs-lookup"><span data-stu-id="74968-109">Part</span></span>    | <span data-ttu-id="74968-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="74968-110">Description</span></span>                                                |
|---------|------------------------------------------------------------|
| <span data-ttu-id="74968-111">*value*</span><span class="sxs-lookup"><span data-stu-id="74968-111">*value*</span></span> | <span data-ttu-id="74968-112">Um inteiro longo que especifica a largura do quadro do caractere.</span><span class="sxs-lookup"><span data-stu-id="74968-112">A Long integer that specifies the character's frame width.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="74968-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="74968-113">Remarks</span></span>

<span data-ttu-id="74968-114">A propriedade [**Width**](width-property.md) é sempre expressa em pixels.</span><span class="sxs-lookup"><span data-stu-id="74968-114">The [**Width**](width-property.md) property is always expressed in pixels.</span></span> <span data-ttu-id="74968-115">A configuração dessa propriedade se aplica a todos os clientes do caractere.</span><span class="sxs-lookup"><span data-stu-id="74968-115">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="74968-116">Embora o caractere apareça em uma janela de região com formato irregular, o local do caractere é baseado nas dimensões externas do quadro de animação retangular usado quando o caractere foi compilado com o editor de caracteres do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="74968-116">Even though the character appears in an irregularly shaped region window, the location of the character is based on the external dimensions of the rectangular animation frame used when the character was compiled with the Microsoft Agent Character Editor.</span></span>

 

 




