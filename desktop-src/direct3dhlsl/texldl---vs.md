---
title: texldl-vs
description: Exemplo de uma textura com uma amostra específica. O nível mipmap específico de detalhes que está sendo amostrado deve ser especificado como o quarto componente da coordenada de textura. | texldl-vs
ms.assetid: 774c058d-7b3e-46a9-adce-c9a44efefd78
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: be9240f5307bb1e70b1f10cc1e392b92e5833fd8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104012008"
---
# <a name="texldl---vs"></a><span data-ttu-id="05158-105">texldl-vs</span><span class="sxs-lookup"><span data-stu-id="05158-105">texldl - vs</span></span>

<span data-ttu-id="05158-106">Exemplo de uma textura com uma amostra específica.</span><span class="sxs-lookup"><span data-stu-id="05158-106">Sample a texture with a particular sampler.</span></span> <span data-ttu-id="05158-107">O nível mipmap específico de detalhes que está sendo amostrado deve ser especificado como o quarto componente da coordenada de textura.</span><span class="sxs-lookup"><span data-stu-id="05158-107">The particular mipmap level-of-detail being sampled has to be specified as the fourth component of the texture coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="05158-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="05158-108">Syntax</span></span>



| <span data-ttu-id="05158-109">texldl DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="05158-109">texldl dst, src0, src1</span></span> |
|------------------------|



 

<span data-ttu-id="05158-110">Em que:</span><span class="sxs-lookup"><span data-stu-id="05158-110">Where:</span></span>

-   <span data-ttu-id="05158-111">o DST é um registro de destino.</span><span class="sxs-lookup"><span data-stu-id="05158-111">dst is a destination register.</span></span>
-   <span data-ttu-id="05158-112">src0 é um registro de origem que fornece as coordenadas de textura para o exemplo de textura.</span><span class="sxs-lookup"><span data-stu-id="05158-112">src0 is a source register that provides the texture coordinates for the texture sample.</span></span>
-   <span data-ttu-id="05158-113">src1 identifica os registros de amostra de origem \# , em que \# especifica qual número de amostra de textura deve ser amostrado.</span><span class="sxs-lookup"><span data-stu-id="05158-113">src1 identifies the source sampler register (s\#), where \# specifies which texture sampler number to sample.</span></span> <span data-ttu-id="05158-114">A amostra está associada a ela uma textura e um estado de controle definido pela enumeração [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) (por exemplo, D3DSAMP \_ MINFILTER).</span><span class="sxs-lookup"><span data-stu-id="05158-114">The sampler has associated with it a texture and a control state defined by the [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) enumeration (for example, D3DSAMP\_MINFILTER).</span></span>

## <a name="remarks"></a><span data-ttu-id="05158-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="05158-115">Remarks</span></span>



| <span data-ttu-id="05158-116">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="05158-116">Vertex shader versions</span></span> | <span data-ttu-id="05158-117">1\_1</span><span class="sxs-lookup"><span data-stu-id="05158-117">1\_1</span></span> | <span data-ttu-id="05158-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="05158-118">2\_0</span></span> | <span data-ttu-id="05158-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="05158-119">2\_x</span></span> | <span data-ttu-id="05158-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="05158-120">2\_sw</span></span> | <span data-ttu-id="05158-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="05158-121">3\_0</span></span> | <span data-ttu-id="05158-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="05158-122">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="05158-123">texldl</span><span class="sxs-lookup"><span data-stu-id="05158-123">texldl</span></span>                 |      |      |      |       | <span data-ttu-id="05158-124">x</span><span class="sxs-lookup"><span data-stu-id="05158-124">x</span></span>    | <span data-ttu-id="05158-125">x</span><span class="sxs-lookup"><span data-stu-id="05158-125">x</span></span>     |



 

<span data-ttu-id="05158-126">texldl pesquisa o conjunto de texturas no estágio de amostra referenciado por src1.</span><span class="sxs-lookup"><span data-stu-id="05158-126">texldl looks up the texture set at the sampler stage referenced by src1.</span></span> <span data-ttu-id="05158-127">O nível de detalhe é selecionado em src0. w.</span><span class="sxs-lookup"><span data-stu-id="05158-127">The level-of-detail is selected from src0.w.</span></span> <span data-ttu-id="05158-128">Esse valor pode ser negativo; nesse caso, o nível de detalhe selecionado é o "inicial One" (maior mapa) com o MAGFILTER.</span><span class="sxs-lookup"><span data-stu-id="05158-128">This value can be negative, in which case the level-of-detail selected is the "zeroth one" (biggest map) with the MAGFILTER.</span></span> <span data-ttu-id="05158-129">Como src0. w é um valor de ponto flutuante, o valor fracionário é usado para interpolar (se MIPFILTER for LINEAR) entre dois níveis de MIP.</span><span class="sxs-lookup"><span data-stu-id="05158-129">Because src0.w is a floating point value, the fractional value is used to interpolate (if MIPFILTER is LINEAR) between two mip levels.</span></span> <span data-ttu-id="05158-130">Os Estados de amostra MIPMAPLODBIAS e MAXMIPLEVEL são respeitados.</span><span class="sxs-lookup"><span data-stu-id="05158-130">Sampler states MIPMAPLODBIAS and MAXMIPLEVEL are honored.</span></span> <span data-ttu-id="05158-131">Para obter mais informações sobre os Estados de amostra, consulte [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span><span class="sxs-lookup"><span data-stu-id="05158-131">For more information about sampler states, see [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span></span>

<span data-ttu-id="05158-132">Se um programa de sombreador apresentar amostras de uma amostra que não tenha uma textura definida, 0001 será obtido no registro de destino.</span><span class="sxs-lookup"><span data-stu-id="05158-132">If a shader program samples from a sampler that does not have a texture set, 0001 is obtained in the destination register.</span></span>

<span data-ttu-id="05158-133">Essa é uma aproximação para o algoritmo do dispositivo de referência.</span><span class="sxs-lookup"><span data-stu-id="05158-133">This is an approximation to the reference device algorithm.</span></span>


```
LOD = src0.w + LODBIAS;
if (LOD <= 0 )
{
   LOD = 0;
   Filter = MagFilter;
   tex = Lookup( MAX(MAXMIPLEVEL, LOD), Filter );
}
else
{
   Filter = MinFilter;
   LOD = MAX( MAXMIPLEVEL, LOD);
   tex = Lookup( Floor(LOD), Filter );
   if( MipFilter == LINEAR )
   {
      tex1 = Lookup( Ceil(LOD), Filter );                        
      tex = (1 - frac(src0.w))*tex + frac(src0.w)*tex1;
   }
}
```



<span data-ttu-id="05158-134">Restrições:</span><span class="sxs-lookup"><span data-stu-id="05158-134">Restrictions:</span></span>

-   <span data-ttu-id="05158-135">As coordenadas de textura não devem ser dimensionadas pelo tamanho da textura.</span><span class="sxs-lookup"><span data-stu-id="05158-135">The texture coordinates should not be scaled by texture size.</span></span>
-   <span data-ttu-id="05158-136">o DST deve ser um [registro temporário](dx9-graphics-reference-asm-vs-registers-temporary.md) (r \# ).</span><span class="sxs-lookup"><span data-stu-id="05158-136">dst must be a [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md) (r\#).</span></span>
-   <span data-ttu-id="05158-137">o DST pode aceitar uma máscara de gravação.</span><span class="sxs-lookup"><span data-stu-id="05158-137">dst can accept a write mask.</span></span> <span data-ttu-id="05158-138">Consulte [máscara de registro de destino](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md).</span><span class="sxs-lookup"><span data-stu-id="05158-138">See [Destination Register Masking](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md).</span></span>
-   <span data-ttu-id="05158-139">Os padrões para os componentes ausentes são 0 ou 1 e dependem do formato de textura.</span><span class="sxs-lookup"><span data-stu-id="05158-139">Defaults for missing components are either 0 or 1, and depend on the texture format.</span></span>
-   <span data-ttu-id="05158-140">src1 deve ser uma [amostra (Direct3D 9 ASM-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md) (s \# ).</span><span class="sxs-lookup"><span data-stu-id="05158-140">src1 must be a [Sampler (Direct3D 9 asm-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md) (s\#).</span></span> <span data-ttu-id="05158-141">src1 não pode usar um modificador de negação.</span><span class="sxs-lookup"><span data-stu-id="05158-141">src1 may not use a negate modifier.</span></span> <span data-ttu-id="05158-142">src1 pode usar swizzle, que é aplicado após a amostragem antes que a máscara de gravação seja respeitada.</span><span class="sxs-lookup"><span data-stu-id="05158-142">src1 may use swizzle, which is applied after sampling before the write mask is honored.</span></span> <span data-ttu-id="05158-143">A amostra deve ter sido declarada (usando o [ \_ SampleType de DCL (SM3-vs ASM)](dcl-samplertype---vs.md)) no início do sombreador.</span><span class="sxs-lookup"><span data-stu-id="05158-143">The sampler must have been declared (using [dcl\_samplerType (sm3 - vs asm)](dcl-samplertype---vs.md)) at the beginning of the shader.</span></span>
-   <span data-ttu-id="05158-144">O número de coordenadas necessárias para executar o exemplo de textura depende de como a amostra foi declarada.</span><span class="sxs-lookup"><span data-stu-id="05158-144">The number of coordinates required to perform the texture sample depends on how the sampler was declared.</span></span> <span data-ttu-id="05158-145">Se ele foi declarado como um cubo, uma coordenada de textura de três componentes é necessária (. RGB).</span><span class="sxs-lookup"><span data-stu-id="05158-145">If it was declared as a cube, a three-component texture coordinate is required (.rgb).</span></span> <span data-ttu-id="05158-146">A validação impõe que as coordenadas fornecidas para texldl sejam suficientes para a dimensão de textura declarada para a amostra.</span><span class="sxs-lookup"><span data-stu-id="05158-146">Validation enforces that coordinates provided to texldl Are sufficient for the texture dimension declared for the sampler.</span></span> <span data-ttu-id="05158-147">No entanto, não é garantido que o aplicativo realmente defina uma textura (por meio da API) com dimensões iguais à dimensão declarada para a amostra.</span><span class="sxs-lookup"><span data-stu-id="05158-147">However, it is not guaranteed that the application actually set a texture (through the API) with dimensions equal to the dimension declared for the sampler.</span></span> <span data-ttu-id="05158-148">Nesse caso, o tempo de execução tentará detectar incompatibilidades (possivelmente em depuração somente).</span><span class="sxs-lookup"><span data-stu-id="05158-148">In such a case, the runtime will attempt to detect mismatches (possibly in debug only).</span></span> <span data-ttu-id="05158-149">A amostragem de uma textura com menos dimensões do que as presentes na coordenada de textura será permitida e será considerada para ignorar os componentes de coordenadas de textura extras.</span><span class="sxs-lookup"><span data-stu-id="05158-149">Sampling a texture with fewer dimensions than are present in the texture coordinate will be allowed, and will be assumed to ignore the extra texture coordinate components.</span></span> <span data-ttu-id="05158-150">Por outro lado, a amostragem de uma textura com mais dimensões do que as presentes na coordenada de textura não é permitida.</span><span class="sxs-lookup"><span data-stu-id="05158-150">Conversely, sampling a texture with more dimensions than are present in the texture coordinate is not allowed.</span></span>
-   <span data-ttu-id="05158-151">Se o src0 (coordenada de textura) for um [registro temporário](dx9-graphics-reference-asm-vs-registers-temporary.md) (r \# ), os componentes necessários para a pesquisa (descritos acima) deverão ter sido gravados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="05158-151">If the src0 (texture coordinate) is a [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md) (r\#), the components required for the lookup (described above) must have been previously written.</span></span>
-   <span data-ttu-id="05158-152">A amostragem de texturas RGB não assinadas resultará em valores flutuantes entre 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="05158-152">Sampling unsigned RGB textures will result in float values between 0.0 and 1.0.</span></span>
-   <span data-ttu-id="05158-153">As texturas assinadas de amostragem resultarão em valores flutuantes entre-1,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="05158-153">Sampling signed textures will result in float values between -1.0 to 1.0.</span></span>
-   <span data-ttu-id="05158-154">Quando texturas de ponto flutuante de amostragem, Float16 significa que os dados serão rangedos no máximo \_ Float16.</span><span class="sxs-lookup"><span data-stu-id="05158-154">When sampling floating point textures, Float16 means that the data will range within MAX\_FLOAT16.</span></span> <span data-ttu-id="05158-155">Float32 significa que o intervalo máximo do pipeline será usado.</span><span class="sxs-lookup"><span data-stu-id="05158-155">Float32 means the maximum range of the pipeline will be used.</span></span> <span data-ttu-id="05158-156">A amostragem fora de um dos intervalos é indefinida.</span><span class="sxs-lookup"><span data-stu-id="05158-156">Sampling outside of either range is undefined.</span></span>
-   <span data-ttu-id="05158-157">Não há nenhum limite de leitura dependente.</span><span class="sxs-lookup"><span data-stu-id="05158-157">There is no dependent read limit.</span></span>

## <a name="related-topics"></a><span data-ttu-id="05158-158">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="05158-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05158-159">Instruções do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="05158-159">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
