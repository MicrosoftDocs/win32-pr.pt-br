---
title: sincronização (SM5-ASM)
description: A sincronização do grupo de threads ou a barreira de memória.
ms.assetid: DCA637FE-8F5C-41D0-8B5E-F913463BA387
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be072b51b4a18d9f1408df0907ec0a55131c18d2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104988629"
---
# <a name="sync-sm5---asm"></a><span data-ttu-id="77065-103">sincronização (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="77065-103">sync (sm5 - asm)</span></span>

<span data-ttu-id="77065-104">A sincronização do grupo de threads ou a barreira de memória.</span><span class="sxs-lookup"><span data-stu-id="77065-104">Thread group sync or memory barrier.</span></span>



| <span data-ttu-id="77065-105">sincronizar \[ \_ uglobal </span><span class="sxs-lookup"><span data-stu-id="77065-105">sync\[\_uglobal</span></span>\|<span data-ttu-id="77065-106">\_ugroup \] \[ \_ g \] \[ \_ t\]</span><span class="sxs-lookup"><span data-stu-id="77065-106">\_ugroup\]\[\_g\]\[\_t\]</span></span> |
|-------------------------------------------|



 

## <a name="remarks"></a><span data-ttu-id="77065-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="77065-107">Remarks</span></span>

<span data-ttu-id="77065-108">A **sincronização** tem opções \_ uglobal, \_ ugroup, \_ g e \_ t.</span><span class="sxs-lookup"><span data-stu-id="77065-108">**Sync** has options \_uglobal, \_ugroup, \_g and \_t.</span></span>

<span data-ttu-id="77065-109">No sombreador de pixel, somente a **\_ uglobal de sincronização** é permitida.</span><span class="sxs-lookup"><span data-stu-id="77065-109">In the pixel shader, only **sync\_uglobal** is allowed.</span></span>

<span data-ttu-id="77065-110">No sombreador de computação, ( \_ uglobal ou \_ ugroup \* ) e/ou \_ g devem ser especificados.</span><span class="sxs-lookup"><span data-stu-id="77065-110">In the compute shader, (\_uglobal or \_ugroup\*) and/or \_g must be specified.</span></span> <span data-ttu-id="77065-111">\_t é opcional também.</span><span class="sxs-lookup"><span data-stu-id="77065-111">\_t is optional in addition.</span></span>

### <a name="_uglobal"></a><span data-ttu-id="77065-112">\_uglobal</span><span class="sxs-lookup"><span data-stu-id="77065-112">\_uglobal</span></span>

<span data-ttu-id="77065-113">\#Limite de memória global u (UAV).</span><span class="sxs-lookup"><span data-stu-id="77065-113">Global u\# (UAV) memory fence.</span></span>

<span data-ttu-id="77065-114">Todas as \# leituras/gravações da memória anterior de u por este thread na ordem do programa são tornadas visíveis para todos os threads em toda a GPU antes de qualquer \# acesso à memória u subsequente por esse thread.</span><span class="sxs-lookup"><span data-stu-id="77065-114">All prior u\# memory reads/writes by this thread in program order are made visible to all threads on the entire GPU before any subsequent u\# memory accesses by this thread.</span></span> <span data-ttu-id="77065-115">A parte inteira da GPU da definição é substituída por um escopo menor que global em um caso, descrito abaixo.</span><span class="sxs-lookup"><span data-stu-id="77065-115">The entire GPU part of the definition is replaced by a less-than-global scope in one case, described below.</span></span>

<span data-ttu-id="77065-116">Isso se aplica a toda a memória UAV associada no estágio atual do sombreador.</span><span class="sxs-lookup"><span data-stu-id="77065-116">This applies to all UAV memory bound at the current shader stage.</span></span>

<span data-ttu-id="77065-117">\_uglobal está disponível no sombreador de computação ou sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="77065-117">\_uglobal is available in the compute shader or pixel shader.</span></span>

<span data-ttu-id="77065-118">Para qualquer UAV associado que não tenha sido declarado pelo sombreador como coerente globalmente, o \_ limite de memória de u uglobal \# só tem visibilidade no grupo de threads do sombreador de computação atual para esse UAV, como se fosse \_ ugroup em vez de \_ uglobal.</span><span class="sxs-lookup"><span data-stu-id="77065-118">For any bound UAV that has not been declared by the shader as Globally Coherent, the \_uglobal u\# memory fence only has visibility within the current compute shader thread-group for that UAV, as if it is \_ugroup instead of \_uglobal.</span></span> <span data-ttu-id="77065-119">Esse problema se aplica somente ao sombreador de computação, pois o sombreador de pixel deve declarar todos os UAVs como coerentes globalmente.</span><span class="sxs-lookup"><span data-stu-id="77065-119">This issue only applies to the compute shader, since the pixel shader must declare all UAVs as Globally Coherent.</span></span>

### <a name="_ugroup"></a><span data-ttu-id="77065-120">\_ugroup</span><span class="sxs-lookup"><span data-stu-id="77065-120">\_ugroup</span></span>

<span data-ttu-id="77065-121">\#Limite de memória u (UAV) do escopo do grupo de threads.</span><span class="sxs-lookup"><span data-stu-id="77065-121">Thread group scope u\# (UAV) memory fence.</span></span>

<span data-ttu-id="77065-122">Todas as \# leituras ou gravações anteriores da memória de u por este thread na ordem do programa são tornadas visíveis para todos os threads no grupo de threads antes de qualquer \# acesso à memória u subsequente por esse thread.</span><span class="sxs-lookup"><span data-stu-id="77065-122">All prior u\# memory reads or writes by this thread in program order are made visible to all threads in the thread group before any subsequent u\# memory accesses by this thread.</span></span>

<span data-ttu-id="77065-123">Isso se aplica a toda a memória UAV associada no estágio atual do sombreador.</span><span class="sxs-lookup"><span data-stu-id="77065-123">This applies to all UAV memory bound at the current shader stage.</span></span>

<span data-ttu-id="77065-124">\_ugroup está disponível somente no sombreador de computação.</span><span class="sxs-lookup"><span data-stu-id="77065-124">\_ugroup is available in the compute shader only.</span></span>

<span data-ttu-id="77065-125">Se \_ ugroup for exposto, para algumas implementações.</span><span class="sxs-lookup"><span data-stu-id="77065-125">If \_ugroup is exposed, for some implementations.</span></span> <span data-ttu-id="77065-126">A vantagem de especificar \_ ugroup em vez de \_ uglobal é que a operação de **sincronização** pode ser concluída mais rapidamente.</span><span class="sxs-lookup"><span data-stu-id="77065-126">The advantage of specifying \_ugroup instead of \_uglobal is that the **sync** operation can complete more quickly.</span></span>

<span data-ttu-id="77065-127">Outras implementações não distinguem \_ ugroup de \_ uglobal, portanto ambas as operações são equivalentes e se comportam como \_ uglobal.</span><span class="sxs-lookup"><span data-stu-id="77065-127">Other implementations do not distinguish \_ugroup from \_uglobal, so both operations are equivalent and behave like \_uglobal.</span></span> <span data-ttu-id="77065-128">Os aplicativos podem especificar sua intenção solicitando o escopo mais estreito de **sincronização** necessário.</span><span class="sxs-lookup"><span data-stu-id="77065-128">Applications can specify their intent by requesting the narrowest scope of **sync** necessary.</span></span>

<span data-ttu-id="77065-129">Mesmo que um determinado UAV seja declarado como coerente globalmente, uma \_ operação de **sincronização** ugroup funcionará com mais eficiência no UAV se uma barreira global não for necessária.</span><span class="sxs-lookup"><span data-stu-id="77065-129">Even if a particular UAV is declared as Globally Coherent, a \_ugroup **sync** operation will function more efficiently on that UAV if a global barrier is not required.</span></span>

### <a name="_g"></a><span data-ttu-id="77065-130">\_m</span><span class="sxs-lookup"><span data-stu-id="77065-130">\_g</span></span>

<span data-ttu-id="77065-131">\#limite de g (memória compartilhada do grupo de threads).</span><span class="sxs-lookup"><span data-stu-id="77065-131">g\# (thread group shared memory) fence.</span></span>

<span data-ttu-id="77065-132">Todas as \# leituras ou gravações anteriores da memória por este thread na ordem do programa são tornadas visíveis para todos os threads no grupo de threads antes de qualquer \# acesso à memória de g subsequente por esse thread.</span><span class="sxs-lookup"><span data-stu-id="77065-132">All prior g\# memory reads or writes by this thread in program order are made visible to all threads in the thread group before any subsequent g\# memory accesses by this thread.</span></span>

<span data-ttu-id="77065-133">Isso se aplica a toda a memória compartilhada g do grupo de threads atual \# .</span><span class="sxs-lookup"><span data-stu-id="77065-133">This applies to all of the current thread group's g\# shared memory.</span></span>

<span data-ttu-id="77065-134">\_g está disponível somente no sombreador de computação.</span><span class="sxs-lookup"><span data-stu-id="77065-134">\_g is available in the compute shader only.</span></span>

### <a name="_t"></a><span data-ttu-id="77065-135">\_t</span><span class="sxs-lookup"><span data-stu-id="77065-135">\_t</span></span>

<span data-ttu-id="77065-136">Sincronização de grupo de threads. Todos os threads dentro de um único grupo de threads (aqueles que podem compartilhar o acesso a um conjunto comum de espaço de registro compartilhado) serão executados até o ponto em que atingem essa instrução antes que qualquer thread possa continuar.</span><span class="sxs-lookup"><span data-stu-id="77065-136">Thread group sync. All threads within a single thread group (those that can share access to a common set of shared register space) will be executed up to the point where they reach this instruction before any thread can continue.</span></span>

<span data-ttu-id="77065-137">\_t não pode ser colocado no controle de fluxo dinâmico, (branches que poderiam variar dentro de um grupo de threads), mas podem estar presentes no controle de fluxo uniforme, onde todos os threads no grupo selecionam o mesmo caminho.</span><span class="sxs-lookup"><span data-stu-id="77065-137">\_t cannot be placed in dynamic flow control, (branches which could vary within a thread group), but can be present in uniform flow control, where all threads in the group pick the same path.</span></span>

<span data-ttu-id="77065-138">\_t está disponível somente no sombreador de computação.</span><span class="sxs-lookup"><span data-stu-id="77065-138">\_t is available in the compute shader only.</span></span>

<span data-ttu-id="77065-139">Veja a seguir uma lista de variantes ' Sync ' do sombreador de cálculo.</span><span class="sxs-lookup"><span data-stu-id="77065-139">The following is a listing of compute shader ‘sync’ variants.</span></span>

-   <span data-ttu-id="77065-140">sincronizar \_ g</span><span class="sxs-lookup"><span data-stu-id="77065-140">sync\_g</span></span>
-   <span data-ttu-id="77065-141">sincronizar \_ ugroup\*</span><span class="sxs-lookup"><span data-stu-id="77065-141">sync\_ugroup\*</span></span>
-   <span data-ttu-id="77065-142">sincronizar \_ uglobal</span><span class="sxs-lookup"><span data-stu-id="77065-142">sync\_uglobal</span></span>
-   <span data-ttu-id="77065-143">sincronização \_ g \_ t</span><span class="sxs-lookup"><span data-stu-id="77065-143">sync\_g\_t</span></span>
-   <span data-ttu-id="77065-144">sincronizar \_ ugroup \_ t\*</span><span class="sxs-lookup"><span data-stu-id="77065-144">sync\_ugroup\_t\*</span></span>
-   <span data-ttu-id="77065-145">sincronizar \_ uglobal \_ t</span><span class="sxs-lookup"><span data-stu-id="77065-145">sync\_uglobal\_t</span></span>
-   <span data-ttu-id="77065-146">sincronizar \_ ugroup \_ g\*</span><span class="sxs-lookup"><span data-stu-id="77065-146">sync\_ugroup\_g\*</span></span>
-   <span data-ttu-id="77065-147">sincronizar \_ uglobal \_ g</span><span class="sxs-lookup"><span data-stu-id="77065-147">sync\_uglobal\_g</span></span>
-   <span data-ttu-id="77065-148">sincronizar \_ ugroup \_ g \_ t\*</span><span class="sxs-lookup"><span data-stu-id="77065-148">sync\_ugroup\_g\_t\*</span></span>
-   <span data-ttu-id="77065-149">sincronizar \_ uglobal \_ g \_ t</span><span class="sxs-lookup"><span data-stu-id="77065-149">sync\_uglobal\_g\_t</span></span>

<span data-ttu-id="77065-150">\*Variantes com \_ ugroup podem não ser direcionadas pelo compilador HLSL, de acordo com a discussão anterior na \_ seção ugroup acima.</span><span class="sxs-lookup"><span data-stu-id="77065-150">\*Variants with \_ugroup may not be targeted by the HLSL compiler, per the earlier discussion in the \_ugroup section above.</span></span>

<span data-ttu-id="77065-151">A listagem de variantes de sincronização de sombreador de pixel inclui \_ somente uglobal de sincronização.</span><span class="sxs-lookup"><span data-stu-id="77065-151">Listing of pixel shader sync variants include sync\_uglobal only.</span></span>

<span data-ttu-id="77065-152">Os limites de memória impedem que as instruções afetadas sejam reordenadas pelos compiladores ou pelo hardware ao longo do limite.</span><span class="sxs-lookup"><span data-stu-id="77065-152">Memory fences prevent affected instructions from being reordered by compilers or hardware across the fence.</span></span>

<span data-ttu-id="77065-153">Várias leituras do mesmo endereço por uma invocação de sombreador que não são separadas por barreiras de memória ou gravações no endereço podem ser recolhidas juntas.</span><span class="sxs-lookup"><span data-stu-id="77065-153">Multiple reads from the same address by a shader invocation that are not separated by memory barriers or writes to the address can be collapsed together.</span></span> <span data-ttu-id="77065-154">O mesmo se aplica às gravações.</span><span class="sxs-lookup"><span data-stu-id="77065-154">The same applies to writes.</span></span> <span data-ttu-id="77065-155">Os acessos separados por uma barreira não podem ser mesclados ou movidos pela barreira.</span><span class="sxs-lookup"><span data-stu-id="77065-155">Accesses separated by a barrier cannot be merged or moved across the barrier.</span></span>

<span data-ttu-id="77065-156">Os limites de memória não são necessários para operações atômicas para um determinado endereço por threads diferentes para funcionar corretamente.</span><span class="sxs-lookup"><span data-stu-id="77065-156">Memory fences are not necessary for atomic operations to a given address by different threads to function correctly.</span></span> <span data-ttu-id="77065-157">Os limites são necessários quando as operações Atomic e/ou Load/Store precisam ser sincronizadas em relação uma à outra, pois aparecem em threads individuais do ponto de vista de outros threads.</span><span class="sxs-lookup"><span data-stu-id="77065-157">Fences are needed when atomics and/or load/store operations need to be synchronized with respect to each other as they appear in individual threads from the point of view of other threads.</span></span>

<span data-ttu-id="77065-158">No sombreador de pixel, as instruções de [descarte](discard--sm4---asm-.md) implicam uma cerca de uglobal de sincronização \_ , nas instruções que não podem ser reordenadas pelo **descarte**.</span><span class="sxs-lookup"><span data-stu-id="77065-158">In the pixel shader, [discard](discard--sm4---asm-.md) instructions imply a sync\_uglobal fence, in that instructions cannot be reordered across the **discard**.</span></span> <span data-ttu-id="77065-159">\_os uglobal de sincronização em pixels auxiliares (que são executados apenas para dar suporte a derivações) ou pixels descartados podem ou não ter nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="77065-159">sync\_uglobal in helper pixels (which run only to support derivatives) or discarded pixels may or may not have any affect.</span></span> <span data-ttu-id="77065-160">Não é permitido que os pixels auxiliares ou descartados gravem em UAVs se, no caso de descarte, as gravações são emitidas após o descarte.</span><span class="sxs-lookup"><span data-stu-id="77065-160">It is not allowed for helper or discarded pixels to write to UAVs if, in the case of discard, the writes are issued after the discard.</span></span> <span data-ttu-id="77065-161">Os valores retornados de UAVs não têm permissão para contribuir com cálculos derivados.</span><span class="sxs-lookup"><span data-stu-id="77065-161">Returned values from UAVs are not allowed to contribute to derivative calculations.</span></span> <span data-ttu-id="77065-162">Portanto, se a sincronização \_ u será atendida ou não por pixels auxiliares ou quando for emitido depois que um descarte for sentido.</span><span class="sxs-lookup"><span data-stu-id="77065-162">Therefore whether or not sync\_u is honored for helper pixels or when issued after a discard is moot.</span></span>

<span data-ttu-id="77065-163">cs \_ 4 \_ 0 e cs \_ 4 \_ 1 dão suporte a essa instrução.</span><span class="sxs-lookup"><span data-stu-id="77065-163">cs\_4\_0 and cs\_4\_1 support this instruction.</span></span>

<span data-ttu-id="77065-164">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="77065-164">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="77065-165">Vértice</span><span class="sxs-lookup"><span data-stu-id="77065-165">Vertex</span></span> | <span data-ttu-id="77065-166">Envoltória</span><span class="sxs-lookup"><span data-stu-id="77065-166">Hull</span></span> | <span data-ttu-id="77065-167">Domínio</span><span class="sxs-lookup"><span data-stu-id="77065-167">Domain</span></span> | <span data-ttu-id="77065-168">Geometria</span><span class="sxs-lookup"><span data-stu-id="77065-168">Geometry</span></span> | <span data-ttu-id="77065-169">16x16</span><span class="sxs-lookup"><span data-stu-id="77065-169">Pixel</span></span> | <span data-ttu-id="77065-170">Computação</span><span class="sxs-lookup"><span data-stu-id="77065-170">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="77065-171">X</span><span class="sxs-lookup"><span data-stu-id="77065-171">X</span></span>     | <span data-ttu-id="77065-172">X</span><span class="sxs-lookup"><span data-stu-id="77065-172">X</span></span>       |



 

<span data-ttu-id="77065-173">Como UAVs estão disponíveis em todos os estágios de sombreador para o Direct3D 11,1, a variante de **sincronização \_ uglobal** desta instrução aplica-se a todos os estágios de sombreador para o tempo de execução do Direct3D 11,1, que está disponível a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="77065-173">Because UAVs are available at all shader stages for Direct3D 11.1, the **sync\_uglobal** variant of this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="77065-174">Vértice</span><span class="sxs-lookup"><span data-stu-id="77065-174">Vertex</span></span> | <span data-ttu-id="77065-175">Envoltória</span><span class="sxs-lookup"><span data-stu-id="77065-175">Hull</span></span> | <span data-ttu-id="77065-176">Domínio</span><span class="sxs-lookup"><span data-stu-id="77065-176">Domain</span></span> | <span data-ttu-id="77065-177">Geometria</span><span class="sxs-lookup"><span data-stu-id="77065-177">Geometry</span></span> | <span data-ttu-id="77065-178">16x16</span><span class="sxs-lookup"><span data-stu-id="77065-178">Pixel</span></span> | <span data-ttu-id="77065-179">Computação</span><span class="sxs-lookup"><span data-stu-id="77065-179">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="77065-180">X</span><span class="sxs-lookup"><span data-stu-id="77065-180">X</span></span>      | <span data-ttu-id="77065-181">X</span><span class="sxs-lookup"><span data-stu-id="77065-181">X</span></span>    | <span data-ttu-id="77065-182">X</span><span class="sxs-lookup"><span data-stu-id="77065-182">X</span></span>      | <span data-ttu-id="77065-183">X</span><span class="sxs-lookup"><span data-stu-id="77065-183">X</span></span>        | <span data-ttu-id="77065-184">X</span><span class="sxs-lookup"><span data-stu-id="77065-184">X</span></span>     | <span data-ttu-id="77065-185">X</span><span class="sxs-lookup"><span data-stu-id="77065-185">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="77065-186">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="77065-186">Minimum Shader Model</span></span>

<span data-ttu-id="77065-187">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="77065-187">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="77065-188">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="77065-188">Shader Model</span></span>                                              | <span data-ttu-id="77065-189">Com suporte</span><span class="sxs-lookup"><span data-stu-id="77065-189">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="77065-190">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="77065-190">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="77065-191">sim</span><span class="sxs-lookup"><span data-stu-id="77065-191">yes</span></span>       |
| [<span data-ttu-id="77065-192">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="77065-192">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="77065-193">não</span><span class="sxs-lookup"><span data-stu-id="77065-193">no</span></span>        |
| [<span data-ttu-id="77065-194">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="77065-194">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="77065-195">não</span><span class="sxs-lookup"><span data-stu-id="77065-195">no</span></span>        |
| [<span data-ttu-id="77065-196">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="77065-196">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="77065-197">não</span><span class="sxs-lookup"><span data-stu-id="77065-197">no</span></span>        |
| [<span data-ttu-id="77065-198">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="77065-198">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="77065-199">não</span><span class="sxs-lookup"><span data-stu-id="77065-199">no</span></span>        |
| [<span data-ttu-id="77065-200">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="77065-200">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="77065-201">não</span><span class="sxs-lookup"><span data-stu-id="77065-201">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="77065-202">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="77065-202">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77065-203">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="77065-203">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 




