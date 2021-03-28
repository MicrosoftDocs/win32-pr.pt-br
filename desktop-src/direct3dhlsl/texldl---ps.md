---
title: texldl-PS
description: Exemplo de uma textura com uma amostra específica. O nível mipmap específico de detalhes que está sendo amostrado deve ser especificado como o quarto componente da coordenada de textura. | texldl-PS
ms.assetid: f0ca8a1d-ac98-49ef-850a-c534e986c7ac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a6ab8a6f55ce5e069a01edb5d281bfe506c5fee6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968297"
---
# <a name="texldl---ps"></a><span data-ttu-id="3c53a-105">texldl-PS</span><span class="sxs-lookup"><span data-stu-id="3c53a-105">texldl - ps</span></span>

<span data-ttu-id="3c53a-106">Exemplo de uma textura com uma amostra específica.</span><span class="sxs-lookup"><span data-stu-id="3c53a-106">Sample a texture with a particular sampler.</span></span> <span data-ttu-id="3c53a-107">O nível mipmap específico de detalhes que está sendo amostrado deve ser especificado como o quarto componente da coordenada de textura.</span><span class="sxs-lookup"><span data-stu-id="3c53a-107">The particular mipmap level-of-detail being sampled has to be specified as the fourth component of the texture coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c53a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3c53a-108">Syntax</span></span>



| <span data-ttu-id="3c53a-109">texldl DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="3c53a-109">texldl dst, src0, src1</span></span> |
|------------------------|



 

<span data-ttu-id="3c53a-110">Em que:</span><span class="sxs-lookup"><span data-stu-id="3c53a-110">Where:</span></span>

-   <span data-ttu-id="3c53a-111">o DST é um registro de destino.</span><span class="sxs-lookup"><span data-stu-id="3c53a-111">dst is a destination register.</span></span>
-   <span data-ttu-id="3c53a-112">src0 é um registro de origem que fornece as coordenadas de textura para o exemplo de textura.</span><span class="sxs-lookup"><span data-stu-id="3c53a-112">src0 is a source register that provides the texture coordinates for the texture sample.</span></span> <span data-ttu-id="3c53a-113">Consulte [registro de coordenadas de textura](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).</span><span class="sxs-lookup"><span data-stu-id="3c53a-113">See [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).</span></span>
-   <span data-ttu-id="3c53a-114">src1 identifica os registros de amostra de origem \# , em que \# especifica qual número de amostra de textura deve ser amostrado.</span><span class="sxs-lookup"><span data-stu-id="3c53a-114">src1 identifies the source sampler register (s\#), where \# specifies which texture sampler number to sample.</span></span> <span data-ttu-id="3c53a-115">A amostra está associada a ela uma textura e um estado de controle definido pela enumeração [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) (por exemplo, D3DSAMP \_ MINFILTER).</span><span class="sxs-lookup"><span data-stu-id="3c53a-115">The sampler has associated with it a texture and a control state defined by the [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) enumeration (for example, D3DSAMP\_MINFILTER).</span></span>

## <a name="remarks"></a><span data-ttu-id="3c53a-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="3c53a-116">Remarks</span></span>



| <span data-ttu-id="3c53a-117">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="3c53a-117">Pixel shader versions</span></span> | <span data-ttu-id="3c53a-118">1\_1</span><span class="sxs-lookup"><span data-stu-id="3c53a-118">1\_1</span></span> | <span data-ttu-id="3c53a-119">1\_2</span><span class="sxs-lookup"><span data-stu-id="3c53a-119">1\_2</span></span> | <span data-ttu-id="3c53a-120">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="3c53a-120">1\_3</span></span> | <span data-ttu-id="3c53a-121">1\_4</span><span class="sxs-lookup"><span data-stu-id="3c53a-121">1\_4</span></span> | <span data-ttu-id="3c53a-122">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3c53a-122">2\_0</span></span> | <span data-ttu-id="3c53a-123">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="3c53a-123">2\_x</span></span> | <span data-ttu-id="3c53a-124">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3c53a-124">2\_sw</span></span> | <span data-ttu-id="3c53a-125">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3c53a-125">3\_0</span></span> | <span data-ttu-id="3c53a-126">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3c53a-126">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="3c53a-127">texldl</span><span class="sxs-lookup"><span data-stu-id="3c53a-127">texldl</span></span>                |      |      |      |      |      |      |       | <span data-ttu-id="3c53a-128">x</span><span class="sxs-lookup"><span data-stu-id="3c53a-128">x</span></span>    | <span data-ttu-id="3c53a-129">x</span><span class="sxs-lookup"><span data-stu-id="3c53a-129">x</span></span>     |



 

<span data-ttu-id="3c53a-130">texldl pesquisa o conjunto de texturas no estágio de amostra referenciado por src1.</span><span class="sxs-lookup"><span data-stu-id="3c53a-130">texldl looks up the texture set at the sampler stage referenced by src1.</span></span> <span data-ttu-id="3c53a-131">O nível de detalhe é selecionado em src0. w.</span><span class="sxs-lookup"><span data-stu-id="3c53a-131">The level-of-detail is selected from src0.w.</span></span> <span data-ttu-id="3c53a-132">Esse valor pode ser negativo, caso o nível de detalhe selecionado seja o inicial um (maior mapa) com o MAGFILTER.</span><span class="sxs-lookup"><span data-stu-id="3c53a-132">This value can be negative in which case the level-of-detail selected is the zeroth one (biggest map) with the MAGFILTER.</span></span> <span data-ttu-id="3c53a-133">Como src0. w é um valor de ponto flutuante, o valor fracionário é usado para interpolar (se MIPFILTER for LINEAR) entre dois níveis de MIP.</span><span class="sxs-lookup"><span data-stu-id="3c53a-133">Since src0.w is a floating point value, the fractional value is used to interpolate (if MIPFILTER is LINEAR) between two mip levels.</span></span> <span data-ttu-id="3c53a-134">Os Estados de amostra MIPMAPLODBIAS e MAXMIPLEVEL são respeitados.</span><span class="sxs-lookup"><span data-stu-id="3c53a-134">Sampler states MIPMAPLODBIAS and MAXMIPLEVEL are honored.</span></span> <span data-ttu-id="3c53a-135">Para obter mais informações sobre os Estados de amostra, consulte [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span><span class="sxs-lookup"><span data-stu-id="3c53a-135">For more information about sampler states, see [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span></span>

<span data-ttu-id="3c53a-136">Se um programa de sombreador apresentar amostras de uma amostra que não tenha uma textura definida, 0001 será obtido no registro de destino.</span><span class="sxs-lookup"><span data-stu-id="3c53a-136">If a shader program samples from a sampler that does not have a texture set, then 0001 is obtained in the destination register.</span></span>

<span data-ttu-id="3c53a-137">Veja a seguir um algoritmo aproximado que o dispositivo de referência segue:</span><span class="sxs-lookup"><span data-stu-id="3c53a-137">The following is a rough algorithm that the reference device follows:</span></span>


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
   LOD = MAX( MAXMIPLEVEL, LOD );
   tex = Lookup( Floor(LOD), Filter );
   if( MipFilter == LINEAR )
   {
      tex1 = Lookup( Ceil(LOD), Filter );                        
      tex = (1 - frac(src0.w))*tex + frac(src0.w)*tex1;
   }
}
```



<span data-ttu-id="3c53a-138">Restrições:</span><span class="sxs-lookup"><span data-stu-id="3c53a-138">Restrictions:</span></span>

-   <span data-ttu-id="3c53a-139">As coordenadas de textura não devem ser dimensionadas pelo tamanho da textura.</span><span class="sxs-lookup"><span data-stu-id="3c53a-139">The texture coordinates should not be scaled by texture size.</span></span>
-   <span data-ttu-id="3c53a-140">o DST deve ser um [registro temporário](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ).</span><span class="sxs-lookup"><span data-stu-id="3c53a-140">dst must be a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#).</span></span>
-   <span data-ttu-id="3c53a-141">o DST pode aceitar um writemask.</span><span class="sxs-lookup"><span data-stu-id="3c53a-141">dst can accept a writemask.</span></span> <span data-ttu-id="3c53a-142">Consulte [máscara de gravação do registro de destino](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).</span><span class="sxs-lookup"><span data-stu-id="3c53a-142">See [Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).</span></span>
-   <span data-ttu-id="3c53a-143">Os padrões para os componentes ausentes são 0 ou 1 e dependem do formato de textura.</span><span class="sxs-lookup"><span data-stu-id="3c53a-143">Defaults for missing components are either 0 or 1, and depend on the texture format.</span></span>
-   <span data-ttu-id="3c53a-144">src1 deve ser uma [amostra (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s \# ).</span><span class="sxs-lookup"><span data-stu-id="3c53a-144">src1 must be a [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#).</span></span> <span data-ttu-id="3c53a-145">src1 não pode usar um modificador de negação (consulte [máscara de gravação de registro de destino](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md)).</span><span class="sxs-lookup"><span data-stu-id="3c53a-145">src1 may not use a negate modifier (see [Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md)).</span></span> <span data-ttu-id="3c53a-146">src1 pode usar swizzle (consulte [o Swizzling de registro de origem](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md)), que é aplicado após a amostragem, mas antes de a máscara de gravação (consulte máscara de gravação do registro de destino) ser respeitada.</span><span class="sxs-lookup"><span data-stu-id="3c53a-146">src1 may use swizzle (see [Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md)), which is applied after sampling, but before the write mask (see Destination Register Write Mask) is honored.</span></span> <span data-ttu-id="3c53a-147">A amostra deve ter sido declarada (usando o [ \_ SampleType de DCL (SM2, SM3-PS ASM)](dcl-samplertype---ps.md)) no início do sombreador.</span><span class="sxs-lookup"><span data-stu-id="3c53a-147">The sampler must have been declared (using [dcl\_samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md)) at the beginning of the shader.</span></span>
-   <span data-ttu-id="3c53a-148">O número de coordenadas necessárias para executar o exemplo de textura depende de como a amostra foi declarada.</span><span class="sxs-lookup"><span data-stu-id="3c53a-148">The number of coordinates required to perform the texture sample depends on how the sampler was declared.</span></span> <span data-ttu-id="3c53a-149">Se ele foi declarado como um cubo, uma coordenada de textura de três componentes é necessária (. RGB).</span><span class="sxs-lookup"><span data-stu-id="3c53a-149">If it was declared as a cube, a three-component texture coordinate is required (.rgb).</span></span> <span data-ttu-id="3c53a-150">A validação impõe que as coordenadas fornecidas para TeX \_ LDL sejam suficientes para a dimensão de textura declarada para a amostra.</span><span class="sxs-lookup"><span data-stu-id="3c53a-150">Validation enforces that coordinates provided to tex\_ldl Are sufficient for the texture dimension declared for the sampler.</span></span> <span data-ttu-id="3c53a-151">No entanto, não há garantia de que o aplicativo realmente define uma textura (por meio da API) com dimensões iguais à dimensão declarada para a amostra.</span><span class="sxs-lookup"><span data-stu-id="3c53a-151">However, it is not guaranteed that the application actually sets a texture (through the API) with dimensions equal to the dimension declared for the sampler.</span></span> <span data-ttu-id="3c53a-152">Nesse caso, o tempo de execução tentará detectar incompatibilidades (possivelmente em depuração somente).</span><span class="sxs-lookup"><span data-stu-id="3c53a-152">In such a case, the runtime will attempt to detect mismatches (possibly in debug only).</span></span> <span data-ttu-id="3c53a-153">A amostragem de uma textura com menos dimensões do que as presentes na coordenada de textura será permitida e presumida para ignorar os componentes de coordenada de textura extra.</span><span class="sxs-lookup"><span data-stu-id="3c53a-153">Sampling a texture with fewer dimensions than are present in the texture coordinate will be allowed and assumed to ignore the extra texture coordinate components.</span></span> <span data-ttu-id="3c53a-154">Por outro lado, a amostragem de uma textura com mais dimensões do que as presentes na coordenada de textura é inválida.</span><span class="sxs-lookup"><span data-stu-id="3c53a-154">Conversely, sampling a texture with more dimensions than are present in the texture coordinate is illegal.</span></span>
-   <span data-ttu-id="3c53a-155">Se o src0 (coordenada de textura) for um [registro temporário](dx9-graphics-reference-asm-ps-registers-temporary.md), os componentes necessários para a pesquisa (descritos acima) deverão ter sido gravados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="3c53a-155">If the src0 (texture coordinate) is [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md), the components required for the lookup (described above) must have been previously written.</span></span>
-   <span data-ttu-id="3c53a-156">A amostragem de texturas RGB não assinadas resultará em valores flutuantes entre 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="3c53a-156">Sampling unsigned RGB textures will result in float values between 0.0 and 1.0.</span></span>
-   <span data-ttu-id="3c53a-157">As texturas assinadas de amostragem resultarão em valores flutuantes entre-1,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="3c53a-157">Sampling signed textures will result in float values between -1.0 to 1.0.</span></span>
-   <span data-ttu-id="3c53a-158">Durante a amostragem de texturas de ponto flutuante, Float16 significa que os dados serão rangedos no máximo \_ Float16.</span><span class="sxs-lookup"><span data-stu-id="3c53a-158">When sampling floating-point textures, Float16 means that the data will range within MAX\_FLOAT16.</span></span> <span data-ttu-id="3c53a-159">Float32 significa que o intervalo máximo do pipeline será usado.</span><span class="sxs-lookup"><span data-stu-id="3c53a-159">Float32 means the maximum range of the pipeline will be used.</span></span> <span data-ttu-id="3c53a-160">A amostragem fora de um dos intervalos é indefinida.</span><span class="sxs-lookup"><span data-stu-id="3c53a-160">Sampling outside of either range is undefined.</span></span>
-   <span data-ttu-id="3c53a-161">Não há nenhum limite de leitura dependente.</span><span class="sxs-lookup"><span data-stu-id="3c53a-161">There is no dependent read limit.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c53a-162">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3c53a-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c53a-163">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="3c53a-163">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 
