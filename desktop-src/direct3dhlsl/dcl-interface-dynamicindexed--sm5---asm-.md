---
title: dcl_interface_dynamicindexed (SM5-ASM)
description: Declare ponteiros de tabela de função (interfaces). | dcl_interface_dynamicindexed (SM5-ASM)
ms.assetid: 5C77EBB6-7AEC-4471-AA6E-0F6D3E215156
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f78bb0152b44f7e29b9e76221db13da0c465a434
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989236"
---
# <a name="dcl_interface_dynamicindexed-sm5---asm"></a><span data-ttu-id="f13b6-104">\_interface DCL \_ dynamicindexed (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="f13b6-104">dcl\_interface\_dynamicindexed (sm5 - asm)</span></span>

<span data-ttu-id="f13b6-105">Declare ponteiros de tabela de função (interfaces).</span><span class="sxs-lookup"><span data-stu-id="f13b6-105">Declare function table pointers (interfaces).</span></span>



| <span data-ttu-id="f13b6-106">\_interface DCL \_ dynamicindexed FP \# \[ \] \[ numCallSites \] = {ft \# , ft \# ,...}</span><span class="sxs-lookup"><span data-stu-id="f13b6-106">dcl\_interface\_dynamicindexed fp\#\[arraySize\]\[numCallSites\] = {ft\#, ft\#, ...}</span></span> |
|--------------------------------------------------------------------------------------|



 



| <span data-ttu-id="f13b6-107">Item</span><span class="sxs-lookup"><span data-stu-id="f13b6-107">Item</span></span>                                                          | <span data-ttu-id="f13b6-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="f13b6-108">Description</span></span>                                    |
|---------------------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="f13b6-109"><span id="fp_"></span><span id="FP_"></span>*FP\#*</span><span class="sxs-lookup"><span data-stu-id="f13b6-109"><span id="fp_"></span><span id="FP_"></span>*fp\#*</span></span><br/> | <span data-ttu-id="f13b6-110">\[nos \] ponteiros de tabela de função.</span><span class="sxs-lookup"><span data-stu-id="f13b6-110">\[in\] The function table pointers.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f13b6-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="f13b6-111">Remarks</span></span>

<span data-ttu-id="f13b6-112">Cada interface precisa ser associada da API para que o sombreador possa ser usado.</span><span class="sxs-lookup"><span data-stu-id="f13b6-112">Each interface needs to be bound from the API before the shader is usable.</span></span> <span data-ttu-id="f13b6-113">A associação fornece uma referência a uma das tabelas de função para que os slots de método possam ser preenchidos.</span><span class="sxs-lookup"><span data-stu-id="f13b6-113">Binding gives a reference to one of the function tables so that the method slots can be filled in.</span></span> <span data-ttu-id="f13b6-114">O compilador não gerará ponteiros para objetos não referenciados.</span><span class="sxs-lookup"><span data-stu-id="f13b6-114">The compiler will not generate pointers for unreferenced objects.</span></span>

<span data-ttu-id="f13b6-115">Um ponteiro de tabela de função tem um conjunto completo de Slots de método para evitar o nível extra de indireção que uma representação de ponteiro para vtable de C++ exigiria.</span><span class="sxs-lookup"><span data-stu-id="f13b6-115">A function table pointer has a full set of method slots to avoid the extra level of indirection that a C++ pointer-to- pointer-to-vtable representation would require.</span></span> <span data-ttu-id="f13b6-116">Isso também exigiria que esses ponteiros fossem cinco tuplas.</span><span class="sxs-lookup"><span data-stu-id="f13b6-116">That would also require that this pointers be 5-tuples.</span></span> <span data-ttu-id="f13b6-117">No modelo de inalinhamento virtual do HLSL, sempre é conhecido qual variável/entrada global é usada para uma chamada para que possamos configurar tabelas por objeto raiz.</span><span class="sxs-lookup"><span data-stu-id="f13b6-117">In the HLSL virtual inlining model it's always known what global variable/input is used for a call so we can set up tables per root object.</span></span>

<span data-ttu-id="f13b6-118">Declarações de ponteiro de função indicam quais tabelas de função são legais para usar com elas.</span><span class="sxs-lookup"><span data-stu-id="f13b6-118">Function pointer declarations indicate which function tables are legal to use with them.</span></span> <span data-ttu-id="f13b6-119">Isso também permite a derivação de informações de correlação de método.</span><span class="sxs-lookup"><span data-stu-id="f13b6-119">This also allows derivation of method correlation information.</span></span>

<span data-ttu-id="f13b6-120">O primeiro \[ \] de uma declaração de interface é o tamanho da matriz.</span><span class="sxs-lookup"><span data-stu-id="f13b6-120">The first \[\] of an interface declaration is the array size.</span></span> <span data-ttu-id="f13b6-121">Se a indexação dinâmica for usada, a declaração indicará que, conforme mostrado.</span><span class="sxs-lookup"><span data-stu-id="f13b6-121">If dynamic indexing is used the declaration will indicate that as shown.</span></span> <span data-ttu-id="f13b6-122">Uma matriz de ponteiros de interface também pode ser indexada estaticamente, não é necessário que as matrizes de ponteiros de interface significam indexação dinâmica.</span><span class="sxs-lookup"><span data-stu-id="f13b6-122">An array of interface pointers can be indexed statically also, it is not required that arrays of interface pointers mean dynamic indexing.</span></span>

<span data-ttu-id="f13b6-123">A numeração de ponteiros de interface começa em 0 para a primeira declaração e, subsequentemente, usa o tamanho da matriz em conta, portanto, o primeiro ponteiro após uma matriz de quatro entradas FP0 \[ 4 \] \[ 1 \] seria FP4 \[ \] \[ \] .</span><span class="sxs-lookup"><span data-stu-id="f13b6-123">Numbering of interface pointers starts at 0 for the first declaration and subsequently takes array size into account, so the first pointer after a four entry array fp0\[4\]\[1\] would be fp4\[\]\[\].</span></span>

<span data-ttu-id="f13b6-124">O segundo \[ \] de uma declaração de interface é o número de sites de chamada, que deve corresponder ao número de corpos em cada tabela referenciada na declaração.</span><span class="sxs-lookup"><span data-stu-id="f13b6-124">The second \[\] of an interface declaration is the number of call sites, which must match the number of bodies in each table referenced in the declaration.</span></span>

<span data-ttu-id="f13b6-125">Não há limites para quantas opções de tabela de função (ft \# ) podem ser listadas em uma declaração de interface.</span><span class="sxs-lookup"><span data-stu-id="f13b6-125">There are no bounds to how many function table (ft\#) choices can be listed in an interface declaration.</span></span>

<span data-ttu-id="f13b6-126">Uma determinada tabela de função (ft \# ) pode aparecer mais de uma vez em uma ou mais declarações de interface.</span><span class="sxs-lookup"><span data-stu-id="f13b6-126">A given function table (ft\#) can appear more than once in one or more interface declarations.</span></span>

### <a name="restrictions"></a><span data-ttu-id="f13b6-127">Restrições</span><span class="sxs-lookup"><span data-stu-id="f13b6-127">Restrictions</span></span>

-   <span data-ttu-id="f13b6-128">O número de sites de objeto em um sombreador, que é a soma em todas as declarações de *FP \#* de suas \[ declarações de matrizes \] , não deve ser maior que 253.</span><span class="sxs-lookup"><span data-stu-id="f13b6-128">The number of object sites in a shader, which is the sum across all *fp\#* declarations of their \[arraySize\] declarations, must be no more than 253.</span></span> <span data-ttu-id="f13b6-129">Esse número corresponde a **quantos desses** ponteiros podem estar presentes.</span><span class="sxs-lookup"><span data-stu-id="f13b6-129">This number corresponds to how many **this** pointers can be present.</span></span> <span data-ttu-id="f13b6-130">O tempo de execução impõe esse limite de 253 para manter-se ligado ao tamanho da DDI para comunicar esses dados de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="f13b6-130">The runtime enforces this 253 limit to keep a bound on the size of the DDI for communicating this pointer data.</span></span>
-   <span data-ttu-id="f13b6-131">O número de sites de chamada em um sombreador, que é a soma em todas as instruções fcall do número de possíveis destinos de ramificação, não deve ser maior que 4096.</span><span class="sxs-lookup"><span data-stu-id="f13b6-131">The number of call sites in a shader, which is the sum across all fcall statements of the number of potential branch targets, must be no more than 4096.</span></span>

    <span data-ttu-id="f13b6-132">Por exemplo, um [fcall](fcall--sm5---asm-.md) que usa um índice estático para a primeira *dimensão \[ \] \[ \] FP* conta como um:</span><span class="sxs-lookup"><span data-stu-id="f13b6-132">For example, an [fcall](fcall--sm5---asm-.md) that uses a static index for the first *fp\[\]\[\]* dimension counts as one:</span></span>

    `                       fcall fp0[0][0]         // +1`

    <span data-ttu-id="f13b6-133">Um **fcall** que usa um índice dinâmico conta como o número de elementos na matriz (primeiro \[ \] da **\_ interface DCL**):</span><span class="sxs-lookup"><span data-stu-id="f13b6-133">An **fcall** that uses a dynamic index counts as the number of elements in the array (first \[\] of **dcl\_interface**):</span></span>

    `                    dcl_interface_dynamicindexed fp1[2][1] = {ft2, ft3, ft4}                      ...                     `

    `fcall fp1[r0.z + 0][1]  // +2`

    <span data-ttu-id="f13b6-134">Esse limite ajuda algumas implementações que se ajustam facilmente a tabelas das seleções do corpo da função em armazenamento constante, como o de buffer.</span><span class="sxs-lookup"><span data-stu-id="f13b6-134">This limit helps some implementations easily fit tables of function body selections in constant buffer-like storage.</span></span>

<span data-ttu-id="f13b6-135">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="f13b6-135">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f13b6-136">Vértice</span><span class="sxs-lookup"><span data-stu-id="f13b6-136">Vertex</span></span> | <span data-ttu-id="f13b6-137">Envoltória</span><span class="sxs-lookup"><span data-stu-id="f13b6-137">Hull</span></span> | <span data-ttu-id="f13b6-138">Domínio</span><span class="sxs-lookup"><span data-stu-id="f13b6-138">Domain</span></span> | <span data-ttu-id="f13b6-139">Geometria</span><span class="sxs-lookup"><span data-stu-id="f13b6-139">Geometry</span></span> | <span data-ttu-id="f13b6-140">16x16</span><span class="sxs-lookup"><span data-stu-id="f13b6-140">Pixel</span></span> | <span data-ttu-id="f13b6-141">Computação</span><span class="sxs-lookup"><span data-stu-id="f13b6-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="f13b6-142">X</span><span class="sxs-lookup"><span data-stu-id="f13b6-142">X</span></span>      | <span data-ttu-id="f13b6-143">X</span><span class="sxs-lookup"><span data-stu-id="f13b6-143">X</span></span>    | <span data-ttu-id="f13b6-144">X</span><span class="sxs-lookup"><span data-stu-id="f13b6-144">X</span></span>      | <span data-ttu-id="f13b6-145">X</span><span class="sxs-lookup"><span data-stu-id="f13b6-145">X</span></span>        | <span data-ttu-id="f13b6-146">X</span><span class="sxs-lookup"><span data-stu-id="f13b6-146">X</span></span>     | <span data-ttu-id="f13b6-147">X</span><span class="sxs-lookup"><span data-stu-id="f13b6-147">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f13b6-148">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="f13b6-148">Minimum Shader Model</span></span>

<span data-ttu-id="f13b6-149">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="f13b6-149">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="f13b6-150">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="f13b6-150">Shader Model</span></span>                                              | <span data-ttu-id="f13b6-151">Com suporte</span><span class="sxs-lookup"><span data-stu-id="f13b6-151">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f13b6-152">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="f13b6-152">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f13b6-153">sim</span><span class="sxs-lookup"><span data-stu-id="f13b6-153">yes</span></span>       |
| [<span data-ttu-id="f13b6-154">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="f13b6-154">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f13b6-155">não</span><span class="sxs-lookup"><span data-stu-id="f13b6-155">no</span></span>        |
| [<span data-ttu-id="f13b6-156">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="f13b6-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f13b6-157">não</span><span class="sxs-lookup"><span data-stu-id="f13b6-157">no</span></span>        |
| [<span data-ttu-id="f13b6-158">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f13b6-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f13b6-159">não</span><span class="sxs-lookup"><span data-stu-id="f13b6-159">no</span></span>        |
| [<span data-ttu-id="f13b6-160">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f13b6-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f13b6-161">não</span><span class="sxs-lookup"><span data-stu-id="f13b6-161">no</span></span>        |
| [<span data-ttu-id="f13b6-162">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f13b6-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f13b6-163">não</span><span class="sxs-lookup"><span data-stu-id="f13b6-163">no</span></span>        |



 

<span data-ttu-id="f13b6-164">cs \_ 4 \_ 0 e cs \_ 4 \_ 1 dão suporte a essa instrução para UAV e SRV.</span><span class="sxs-lookup"><span data-stu-id="f13b6-164">cs\_4\_0 and cs\_4\_1 support this instruction for UAV and SRV.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f13b6-165">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f13b6-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f13b6-166">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f13b6-166">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





