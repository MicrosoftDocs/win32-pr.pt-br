---
title: Propriedade Width (objeto Characters)
description: Saiba mais sobre a Propriedade width do objeto Characters, que retorna ou define a largura do quadro para o caractere especificado.
ms.assetid: ebada4cc-dbe6-4540-be1f-1f61e176765b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e17f11412774fcf34e887a2f00479ab7d96369de
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395122"
---
# <a name="width-property-characters-object"></a><span data-ttu-id="2fadb-103">Propriedade Width (objeto Characters)</span><span class="sxs-lookup"><span data-stu-id="2fadb-103">Width Property (Characters Object)</span></span>

<span data-ttu-id="2fadb-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2fadb-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="2fadb-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2fadb-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="2fadb-106">Retorna ou define a largura do quadro para o caractere especificado.</span><span class="sxs-lookup"><span data-stu-id="2fadb-106">Returns or sets the width of the frame for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="2fadb-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="2fadb-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="2fadb-108">*agent\***. Caracteres ("**_CharacterID_*_"). Valor_ \*  \[ =  *de largura*\]</span><span class="sxs-lookup"><span data-stu-id="2fadb-108">*agent\***.Characters ("**_CharacterID_*_").Width_\* \[= *value*\]</span></span>



| <span data-ttu-id="2fadb-109">Parte</span><span class="sxs-lookup"><span data-stu-id="2fadb-109">Part</span></span>    | <span data-ttu-id="2fadb-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="2fadb-110">Description</span></span>                                                |
|---------|------------------------------------------------------------|
| <span data-ttu-id="2fadb-111">*value*</span><span class="sxs-lookup"><span data-stu-id="2fadb-111">*value*</span></span> | <span data-ttu-id="2fadb-112">Um inteiro Longo que especifica a largura do quadro do caractere.</span><span class="sxs-lookup"><span data-stu-id="2fadb-112">A Long integer that specifies the character's frame width.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2fadb-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="2fadb-113">Remarks</span></span>

<span data-ttu-id="2fadb-114">A [**propriedade Width**](width-property.md) é sempre expressa em pixels.</span><span class="sxs-lookup"><span data-stu-id="2fadb-114">The [**Width**](width-property.md) property is always expressed in pixels.</span></span> <span data-ttu-id="2fadb-115">A configuração dessa propriedade se aplica a todos os clientes do caractere.</span><span class="sxs-lookup"><span data-stu-id="2fadb-115">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="2fadb-116">Embora o caractere apareça em uma janela de região com forma irregular, o local do caractere é baseado nas dimensões externas do quadro de animação retangular usado quando o caractere foi compilado com o Editor de Caracteres do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="2fadb-116">Even though the character appears in an irregularly shaped region window, the location of the character is based on the external dimensions of the rectangular animation frame used when the character was compiled with the Microsoft Agent Character Editor.</span></span>

 

 




