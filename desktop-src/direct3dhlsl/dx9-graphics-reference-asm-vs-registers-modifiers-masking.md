---
title: Máscara de registro de destino
description: O mascaramento especifica quais componentes do registro de destino serão atualizados com o resultado de uma instrução. Os registros de textura têm um conjunto de regras e os registros de não-textura têm outro conjunto de regras.
ms.assetid: 989ebe55-1f80-4063-b116-4284520f52cc
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7ce15f75f424cb7796ef7db7a8b89bd5bcbfa9cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364211"
---
# <a name="destination-register-masking"></a><span data-ttu-id="5a55c-104">Máscara de registro de destino</span><span class="sxs-lookup"><span data-stu-id="5a55c-104">Destination Register Masking</span></span>

<span data-ttu-id="5a55c-105">O mascaramento especifica quais componentes do registro de destino serão atualizados com o resultado de uma instrução.</span><span class="sxs-lookup"><span data-stu-id="5a55c-105">Masking specifies which components of the destination register will be updated with the result of an instruction.</span></span> <span data-ttu-id="5a55c-106">Os registros de textura têm um conjunto de regras e os registros de não-textura têm outro conjunto de regras.</span><span class="sxs-lookup"><span data-stu-id="5a55c-106">Texture registers have one set of rules and nontexture registers have another set of rules.</span></span>

-   <span data-ttu-id="5a55c-107">referência de gráficos do DX9 \_ \_ \_ ASM \_ vs \_ registra \_ \_ mascaramento de modificadores – esta seção contém regras para aplicar máscaras aos registros de destino.</span><span class="sxs-lookup"><span data-stu-id="5a55c-107">dx9\_graphics\_reference\_asm\_vs\_registers\_modifiers\_masking - This section contains rules for applying masks to destination registers.</span></span>
-   <span data-ttu-id="5a55c-108">\_ \_ Máscaras de registro de textura – os registros de textura têm algumas regras exclusivas.</span><span class="sxs-lookup"><span data-stu-id="5a55c-108">Texture\_Register\_Masks - Texture registers have some unique rules.</span></span>

## <a name="destination-register-masking"></a><span data-ttu-id="5a55c-109">Máscara de registro de destino</span><span class="sxs-lookup"><span data-stu-id="5a55c-109">Destination Register Masking</span></span>

<span data-ttu-id="5a55c-110">Conforme mostrado na tabela a seguir, o mascaramento (em que é um dos registros válidos do [sombreador](dx9-graphics-reference-asm-vs-registers.md)de vértices do sombreador de vértice) pode ser aplicado aos componentes individuais dos dados de vetor.</span><span class="sxs-lookup"><span data-stu-id="5a55c-110">As shown in the following table, masking (where r is one of the valid vertex shader [Vertex Shader Registers](dx9-graphics-reference-asm-vs-registers.md)) can be applied to the individual components of the vector data.</span></span>



| <span data-ttu-id="5a55c-111">Modificador de componente</span><span class="sxs-lookup"><span data-stu-id="5a55c-111">Component modifier</span></span> | <span data-ttu-id="5a55c-112">Description</span><span class="sxs-lookup"><span data-stu-id="5a55c-112">Description</span></span>      |
|--------------------|------------------|
| <span data-ttu-id="5a55c-113">r. {x} {y} {z} {w}</span><span class="sxs-lookup"><span data-stu-id="5a55c-113">r.{x}{y}{z}{w}</span></span>     | <span data-ttu-id="5a55c-114">Máscara de destino</span><span class="sxs-lookup"><span data-stu-id="5a55c-114">Destination mask</span></span> |



 

-   <span data-ttu-id="5a55c-115">Em geral, especificar máscaras de gravação de registro de destino é um bom estilo de codificação.</span><span class="sxs-lookup"><span data-stu-id="5a55c-115">In general, specifying destination register write masks is good coding style.</span></span> <span data-ttu-id="5a55c-116">Torna o código mais fácil de ler e manter.</span><span class="sxs-lookup"><span data-stu-id="5a55c-116">It makes code easier to read and maintain.</span></span>
-   <span data-ttu-id="5a55c-117">Qualquer combinação de componentes pode ser especificada (incluindo nenhum), desde que x preceda y, y preceda z e z preceda w.</span><span class="sxs-lookup"><span data-stu-id="5a55c-117">Any combination of components may be specified (including none) as long as x precedes y, y precedes z, and z precedes w.</span></span>
-   <span data-ttu-id="5a55c-118">Os registros de saída de oFog e de entrada devem usar apenas uma máscara.</span><span class="sxs-lookup"><span data-stu-id="5a55c-118">The oPts and oFog output registers must use only one mask.</span></span>
-   <span data-ttu-id="5a55c-119">Algumas instruções exigem que o registro de destino use uma única máscara de gravação: exp, expp, log, LogP, pow, RCP e RSQ.</span><span class="sxs-lookup"><span data-stu-id="5a55c-119">Certain instructions require the destination register to use a single write mask: exp, expp, log, logp, pow, rcp, and rsq.</span></span>
-   <span data-ttu-id="5a55c-120">Na versão 1,0, a instrução FRC exigia uma das seguintes combinações de máscara:. x ou. y ou. XY.</span><span class="sxs-lookup"><span data-stu-id="5a55c-120">In version 1.0, the frc instruction required one of the following mask combinations: .x or .y or .xy.</span></span> <span data-ttu-id="5a55c-121">A versão 2,0 não tem restrição de máscara.</span><span class="sxs-lookup"><span data-stu-id="5a55c-121">Version 2.0 has no mask restriction.</span></span>
-   <span data-ttu-id="5a55c-122">Sincos requer uma das seguintes combinações de máscara:. x ou. y ou. xyz.</span><span class="sxs-lookup"><span data-stu-id="5a55c-122">sincos requires one of the following mask combinations: .x or .y or .xyz.</span></span>
-   <span data-ttu-id="5a55c-123">M3X2 requer a máscara de gravação. XY.</span><span class="sxs-lookup"><span data-stu-id="5a55c-123">m3x2 requires the .xy write mask.</span></span>
-   <span data-ttu-id="5a55c-124">m3x3 e m4x3 exigem a máscara de gravação. xyz.</span><span class="sxs-lookup"><span data-stu-id="5a55c-124">m3x3 and m4x3 require the .xyz write mask.</span></span>
-   <span data-ttu-id="5a55c-125">M3x4 e m4x4 exigem a máscara de gravação. xyz ou a xyzw (máscara de gravação padrão).</span><span class="sxs-lookup"><span data-stu-id="5a55c-125">m3x4 and m4x4 require either the .xyz write mask or the default write mask (xyzw).</span></span>

## <a name="texture-register-masks"></a><span data-ttu-id="5a55c-126">Máscaras de registro de textura</span><span class="sxs-lookup"><span data-stu-id="5a55c-126">Texture Register Masks</span></span>

<span data-ttu-id="5a55c-127">As regras de validação para usar modificadores em registros de coordenadas de textura são mais rígidas do que as regras de validação para outros registros.</span><span class="sxs-lookup"><span data-stu-id="5a55c-127">The validation rules for using modifiers on texture coordinate registers are tighter than the validation rules for other registers.</span></span>

-   <span data-ttu-id="5a55c-128">Se oTn for gravado, todos os registros anteriores (oTn-1 ~ oT0) também precisarão ser escritos.</span><span class="sxs-lookup"><span data-stu-id="5a55c-128">If oTn is written, all previous registers (oTn-1 ~ oT0) have to be written as well.</span></span>
-   <span data-ttu-id="5a55c-129">A máscara de gravação "combinada" para qualquer \# registro de OT deve ser exatamente uma das seguintes:</span><span class="sxs-lookup"><span data-stu-id="5a55c-129">The "combined" write mask for any oT\# register must be exactly one of the following:</span></span>
    -   <span data-ttu-id="5a55c-130">. x</span><span class="sxs-lookup"><span data-stu-id="5a55c-130">.x</span></span>
    -   <span data-ttu-id="5a55c-131">. XY</span><span class="sxs-lookup"><span data-stu-id="5a55c-131">.xy</span></span>
    -   <span data-ttu-id="5a55c-132">. xyz</span><span class="sxs-lookup"><span data-stu-id="5a55c-132">.xyz</span></span>
    -   <span data-ttu-id="5a55c-133">. xyzw (que é equivalente a não usar nenhum modificador de componente)</span><span class="sxs-lookup"><span data-stu-id="5a55c-133">.xyzw (which is equivalent to not using any component modifiers)</span></span>

<span data-ttu-id="5a55c-134">Por exemplo, um sombreador de vértice pode gerar uma saída para os registros de textura em instruções separadas.</span><span class="sxs-lookup"><span data-stu-id="5a55c-134">For example, a vertex shader can output to texture registers in separate instructions.</span></span>


```
    oT1.y  
    oT0.y  
    oT2  
    oT0.xz  
    oT1.x
```



<span data-ttu-id="5a55c-135">Ou, as instruções podem ser combinadas.</span><span class="sxs-lookup"><span data-stu-id="5a55c-135">Or, the instructions can be combined.</span></span>


```
    oT0.xyz  
    oT1.xy  
    oT2.xyzw    
```



<span data-ttu-id="5a55c-136">Essas restrições se aplicam somente aos registros de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="5a55c-136">These restrictions apply only to the texture coordinate registers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5a55c-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5a55c-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a55c-138">Modificadores de registro do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="5a55c-138">Vertex Shader Register Modifiers</span></span>](dx9-graphics-reference-asm-vs-registers-modifiers.md)
</dt> </dl>

 

 




