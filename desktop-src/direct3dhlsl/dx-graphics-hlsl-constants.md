---
title: Constantes de sombreador (HLSL)
description: No sombreador modelo 4, as constantes de sombreador são armazenadas em um ou mais recursos de buffer na memória.
ms.assetid: 89fe874a-8009-4901-bebe-2d9e45f894bb
keywords:
- cbuffer
- tbuffers
- buffer de constantes
- buffer de textura
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a1b78da747a248bf4bb5774add1bf97f14f048c4
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103644132"
---
# <a name="shader-constants-hlsl"></a><span data-ttu-id="c0322-107">Constantes de sombreador (HLSL)</span><span class="sxs-lookup"><span data-stu-id="c0322-107">Shader Constants (HLSL)</span></span>

<span data-ttu-id="c0322-108">No sombreador modelo 4, as constantes de sombreador são armazenadas em um ou mais recursos de buffer na memória.</span><span class="sxs-lookup"><span data-stu-id="c0322-108">In Shader Model 4, shader constants are stored in one or more buffer resources in memory.</span></span> <span data-ttu-id="c0322-109">Eles podem ser organizados em dois tipos de buffers: buffers de constantes (cbuffers) e buffers de textura (tbuffers).</span><span class="sxs-lookup"><span data-stu-id="c0322-109">They can be organized into two types of buffers: constant buffers (cbuffers) and texture buffers (tbuffers).</span></span> <span data-ttu-id="c0322-110">Buffers de constantes são otimizados para uso de variável constante, que é caracterizado por acesso de menor latência e atualização mais frequente da CPU.</span><span class="sxs-lookup"><span data-stu-id="c0322-110">Constant buffers are optimized for constant-variable usage, which is characterized by lower-latency access and more frequent update from the CPU.</span></span> <span data-ttu-id="c0322-111">Por esse motivo, o tamanho adicional, o layout e as restrições de acesso se aplicam a esses recursos.</span><span class="sxs-lookup"><span data-stu-id="c0322-111">For this reason, additional size, layout, and access restrictions apply to these resources.</span></span> <span data-ttu-id="c0322-112">Os buffers de textura são acessados como texturas e têm melhor desempenho para dados indexados arbitrariamente.</span><span class="sxs-lookup"><span data-stu-id="c0322-112">Texture buffers are accessed like textures and perform better for arbitrarily indexed data.</span></span> <span data-ttu-id="c0322-113">Independentemente do tipo de recurso usado, não há nenhum limite para o número de buffers de constantes ou buffers de textura que um aplicativo pode criar.</span><span class="sxs-lookup"><span data-stu-id="c0322-113">Regardless of which type of resource you use, there is no limit to the number of constant buffers or texture buffers an application can create.</span></span>

<span data-ttu-id="c0322-114">A declaração de um buffer de constantes ou de um buffer de textura parece muito parecida com uma declaração de estrutura em C, com a adição das palavras-chave **Register** e **packoffset** para atribuir manualmente registros ou dados de empacotamento.</span><span class="sxs-lookup"><span data-stu-id="c0322-114">Declaring a constant buffer or a texture buffer looks very much like a structure declaration in C, with the addition of the **register** and **packoffset** keywords for manually assigning registers or packing data.</span></span>



|                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0322-115">*BufferType* \[ *Nome* \] do \[: **Register**(b \# ) \] { *VariableDeclaration* \[ : **packoffset**(c \# . xyzw) \] ;      ... };</span><span class="sxs-lookup"><span data-stu-id="c0322-115">*BufferType* \[*Name*\] \[: **register**(b\#)\] {     *VariableDeclaration* \[: **packoffset**(c\#.xyzw)\];      ... };</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="c0322-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c0322-116">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0322-117"><span id="BufferType"></span><span id="buffertype"></span><span id="BUFFERTYPE"></span>*BufferType*</span><span class="sxs-lookup"><span data-stu-id="c0322-117"><span id="BufferType"></span><span id="buffertype"></span><span id="BUFFERTYPE"></span>*BufferType*</span></span>
</dt> <dd>

<span data-ttu-id="c0322-118">\[no \] tipo de buffer.</span><span class="sxs-lookup"><span data-stu-id="c0322-118">\[in\] The buffer type.</span></span>



| <span data-ttu-id="c0322-119">BufferType</span><span class="sxs-lookup"><span data-stu-id="c0322-119">BufferType</span></span> | <span data-ttu-id="c0322-120">Description</span><span class="sxs-lookup"><span data-stu-id="c0322-120">Description</span></span>     |
|------------|-----------------|
| <span data-ttu-id="c0322-121">cbuffer</span><span class="sxs-lookup"><span data-stu-id="c0322-121">cbuffer</span></span>    | <span data-ttu-id="c0322-122">buffer de constantes</span><span class="sxs-lookup"><span data-stu-id="c0322-122">constant buffer</span></span> |
| <span data-ttu-id="c0322-123">tbuffers</span><span class="sxs-lookup"><span data-stu-id="c0322-123">tbuffer</span></span>    | <span data-ttu-id="c0322-124">buffer de textura</span><span class="sxs-lookup"><span data-stu-id="c0322-124">texture buffer</span></span>  |



 

</dd> <dt>

<span data-ttu-id="c0322-125"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nomes*</span><span class="sxs-lookup"><span data-stu-id="c0322-125"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span></span>
</dt> <dd>

<span data-ttu-id="c0322-126">\[em \] opcional, a cadeia de caracteres ASCII contendo um nome de buffer exclusivo.</span><span class="sxs-lookup"><span data-stu-id="c0322-126">\[in\] Optional, ASCII string containing a unique buffer name.</span></span>

</dd> <dt>

<span data-ttu-id="c0322-127"><span id="register_b__"></span><span id="REGISTER_B__"></span>**registrar**(b \# )</span><span class="sxs-lookup"><span data-stu-id="c0322-127"><span id="register_b__"></span><span id="REGISTER_B__"></span>**register**(b\#)</span></span>
</dt> <dd>

<span data-ttu-id="c0322-128">\[na \] palavra-chave opcional, usada para empacotar manualmente os dados constantes.</span><span class="sxs-lookup"><span data-stu-id="c0322-128">\[in\] Optional keyword, used to manually pack constant data.</span></span> <span data-ttu-id="c0322-129">As constantes podem ser empacotadas em um registro somente em um buffer de constantes, em que o registro inicial é fornecido pelo número de registro ( *\#* ).</span><span class="sxs-lookup"><span data-stu-id="c0322-129">Constants can be packed in a register only in a constant buffer, where the starting register is given by the register number (*\#*).</span></span>

</dd> <dt>

<span data-ttu-id="c0322-130"><span id="VariableDeclaration"></span><span id="variabledeclaration"></span><span id="VARIABLEDECLARATION"></span>*VariableDeclaration*</span><span class="sxs-lookup"><span data-stu-id="c0322-130"><span id="VariableDeclaration"></span><span id="variabledeclaration"></span><span id="VARIABLEDECLARATION"></span>*VariableDeclaration*</span></span>
</dt> <dd>

<span data-ttu-id="c0322-131">\[em \] declaração de variável, semelhante a uma declaração de membro de estrutura.</span><span class="sxs-lookup"><span data-stu-id="c0322-131">\[in\] Variable declaration, similar to a structure member declaration.</span></span> <span data-ttu-id="c0322-132">Pode ser qualquer tipo de HLSL ou objeto de efeito (exceto um objeto de textura ou de amostra).</span><span class="sxs-lookup"><span data-stu-id="c0322-132">This can be any HLSL type or effect object (except a texture or a sampler object).</span></span>

</dd> <dt>

<span data-ttu-id="c0322-133"><span id="packoffset_c_.xyzw_"></span><span id="PACKOFFSET_C_.XYZW_"></span>**packoffset**(c \# . xyzw)</span><span class="sxs-lookup"><span data-stu-id="c0322-133"><span id="packoffset_c_.xyzw_"></span><span id="PACKOFFSET_C_.XYZW_"></span>**packoffset**(c\#.xyzw)</span></span>
</dt> <dd>

<span data-ttu-id="c0322-134">\[na \] palavra-chave opcional, usada para empacotar manualmente os dados constantes.</span><span class="sxs-lookup"><span data-stu-id="c0322-134">\[in\] Optional keyword, used to manually pack constant data.</span></span> <span data-ttu-id="c0322-135">As constantes podem ser empacotadas em qualquer buffer constante, onde o número de registro é fornecido pelo ( *\#* ).</span><span class="sxs-lookup"><span data-stu-id="c0322-135">Constants can be packed in any constant buffer, where the register number is given by (*\#*).</span></span> <span data-ttu-id="c0322-136">A embalagem de subcomponente (usando xyzw swizzling) está disponível para constantes cujo tamanho se ajusta em um único registro (não cruzar um limite de registro).</span><span class="sxs-lookup"><span data-stu-id="c0322-136">Sub-component packing (using xyzw swizzling) is available for constants whose size fit within a single register (do not cross a register boundary).</span></span> <span data-ttu-id="c0322-137">Por exemplo, um FLOAT4 não pôde ser empacotado em um único registro, começando com o componente y, porque ele não caberia em um registro de quatro componentes.</span><span class="sxs-lookup"><span data-stu-id="c0322-137">For instance, a float4 could not be packed in a single register starting with the y-component because it would not fit in a four-component register.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c0322-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="c0322-138">Remarks</span></span>

<span data-ttu-id="c0322-139">Buffers constantes reduzem a largura de banda necessária para atualizar constantes de sombreador, permitindo que as constantes de sombreador sejam agrupadas e confirmadas ao mesmo tempo em vez de fazer chamadas individuais para confirmar cada constante separadamente.</span><span class="sxs-lookup"><span data-stu-id="c0322-139">Constant buffers reduce the bandwidth required to update shader constants by allowing shader constants to be grouped together and committed at the same time rather than making individual calls to commit each constant separately.</span></span>

<span data-ttu-id="c0322-140">Um buffer de constantes é um recurso de buffer especializado que é acessado como um buffer.</span><span class="sxs-lookup"><span data-stu-id="c0322-140">A constant buffer is a specialized buffer resource that is accessed like a buffer.</span></span> <span data-ttu-id="c0322-141">Cada buffer de constantes pode conter até 4096 [vetores](dx-graphics-hlsl-vector.md); cada vetor contém até valores de 4 32 bits.</span><span class="sxs-lookup"><span data-stu-id="c0322-141">Each constant buffer can hold up to 4096 [vectors](dx-graphics-hlsl-vector.md); each vector contains up to four 32-bit values.</span></span> <span data-ttu-id="c0322-142">Você pode associar até 14 buffers de constante por estágio de pipeline (2 slots adicionais são reservados para uso interno).</span><span class="sxs-lookup"><span data-stu-id="c0322-142">You can bind up to 14 constant buffers per pipeline stage (2 additional slots are reserved for internal use).</span></span>

<span data-ttu-id="c0322-143">Um buffer de textura é um recurso de buffer especializado que é acessado como uma textura.</span><span class="sxs-lookup"><span data-stu-id="c0322-143">A texture buffer is a specialized buffer resource that is accessed like a texture.</span></span> <span data-ttu-id="c0322-144">O acesso à textura (em comparação com o acesso ao buffer) pode ter um desempenho melhor para dados indexados arbitrariamente.</span><span class="sxs-lookup"><span data-stu-id="c0322-144">Texture access (as compared with buffer access) can have better performance for arbitrarily indexed data.</span></span> <span data-ttu-id="c0322-145">Você pode associar até 128 buffers de textura por estágio de pipeline.</span><span class="sxs-lookup"><span data-stu-id="c0322-145">You can bind up to 128 texture buffers per pipeline stage.</span></span>

<span data-ttu-id="c0322-146">Um recurso de buffer foi projetado para minimizar a sobrecarga de definir constantes de sombreador.</span><span class="sxs-lookup"><span data-stu-id="c0322-146">A buffer resource is designed to minimize the overhead of setting shader constants.</span></span> <span data-ttu-id="c0322-147">A estrutura de efeito (consulte a [**interface ID3D10Effect**](/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effect)) gerenciará os buffers de textura e constante de atualização, ou você poderá usar a API do Direct3D para atualizar os buffers (consulte [copiando e acessando dados de recurso (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-mapping) para obter informações).</span><span class="sxs-lookup"><span data-stu-id="c0322-147">The effect framework (see [**ID3D10Effect Interface**](/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effect)) will manage updating constant and texture buffers, or you can use the Direct3D API to update buffers (see [Copying and Accessing Resource Data (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-mapping) for information).</span></span> <span data-ttu-id="c0322-148">Um aplicativo também pode copiar dados de outro buffer (como um destino de renderização ou um destino de saída de fluxo) em um buffer de constantes.</span><span class="sxs-lookup"><span data-stu-id="c0322-148">An application can also copy data from another buffer (such as a render target or a stream-output target) into a constant buffer.</span></span>

<span data-ttu-id="c0322-149">Para obter mais informações sobre como usar buffers de constantes em um aplicativo D3D10, consulte [tipos de recursos (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) e [criando recursos de buffer (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating).</span><span class="sxs-lookup"><span data-stu-id="c0322-149">For more info on using constant buffers in a D3D10 application, see [Resource Types (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) and [Creating Buffer Resources (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating).</span></span>

<span data-ttu-id="c0322-150">Para obter informações de Morel sobre como usar buffers de constantes em um aplicativo D3D11, consulte [introdução aos buffers no Direct3D 11](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-intro) e [como criar um buffer de constantes](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to).</span><span class="sxs-lookup"><span data-stu-id="c0322-150">For morel info on using constant buffers in a D3D11 application, see [Introduction to Buffers in Direct3D 11](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-intro) and [How to: Create a Constant Buffer](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to).</span></span>

<span data-ttu-id="c0322-151">Um buffer de constantes não requer uma [exibição](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-access-views) para ser associado ao pipeline.</span><span class="sxs-lookup"><span data-stu-id="c0322-151">A constant buffer does not require a [view](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-access-views) to be bound to the pipeline.</span></span> <span data-ttu-id="c0322-152">Um buffer de textura, no entanto, requer uma exibição e deve estar associado a um slot de textura (ou deve ser associado a [**SetTextureBuffer**](/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectconstantbuffer-settexturebuffer) ao usar um efeito).</span><span class="sxs-lookup"><span data-stu-id="c0322-152">A texture buffer, however, requires a view and must be bound to a texture slot (or must be bound with [**SetTextureBuffer**](/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectconstantbuffer-settexturebuffer) when using an effect).</span></span>

<span data-ttu-id="c0322-153">Há duas maneiras de empacotar dados constantes: usando as palavras-chave [Register (DirectX HLSL)](dx-graphics-hlsl-variable-register.md) e [PACKOFFSET (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md) .</span><span class="sxs-lookup"><span data-stu-id="c0322-153">There are two ways to pack constants data: using the [register (DirectX HLSL)](dx-graphics-hlsl-variable-register.md) and [packoffset (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md) keywords.</span></span>



|                                                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0322-154">Diferenças entre o Direct3D 9 e o Direct3D 10 e 11:</span><span class="sxs-lookup"><span data-stu-id="c0322-154">Differences between Direct3D 9 and Direct3D 10 and 11:</span></span><br/> <span data-ttu-id="c0322-155">Ao contrário da alocação automática de constantes no Direct3D 9, que não executou a embalagem e, em vez disso, atribuiu cada variável a um conjunto de registros FLOAT4, as variáveis constantes HLSL seguem regras de empacotamento no Direct3D 10 e 11.</span><span class="sxs-lookup"><span data-stu-id="c0322-155">Unlike the auto-allocation of constants in Direct3D 9, which did not perform packing and instead assigned each variable to a set of float4 registers, HLSL constant variables follow packing rules in Direct3D 10 and 11.</span></span><br/> |



 

### <a name="organizing-constant-buffers"></a><span data-ttu-id="c0322-156">Organizando buffers de constantes</span><span class="sxs-lookup"><span data-stu-id="c0322-156">Organizing constant buffers</span></span>

<span data-ttu-id="c0322-157">Buffers constantes reduzem a largura de banda necessária para atualizar constantes de sombreador, permitindo que as constantes de sombreador sejam agrupadas e confirmadas ao mesmo tempo em vez de fazer chamadas individuais para confirmar cada constante separadamente.</span><span class="sxs-lookup"><span data-stu-id="c0322-157">Constant buffers reduce the bandwidth required to update shader constants by allowing shader constants to be grouped together and committed at the same time rather than making individual calls to commit each constant separately.</span></span>

<span data-ttu-id="c0322-158">O melhor modo de usar buffers constantes de modo eficiente é organizar as variáveis de sombreador em buffers constantes com base na frequência de atualização.</span><span class="sxs-lookup"><span data-stu-id="c0322-158">The best way to efficiently use constant buffers is to organize shader variables into constant buffers based on their frequency of update.</span></span> <span data-ttu-id="c0322-159">Isso permite que um aplicativo Minimize a largura de banda necessária para atualizar constantes de sombreador.</span><span class="sxs-lookup"><span data-stu-id="c0322-159">This allows an application to minimize the bandwidth required for updating shader constants.</span></span> <span data-ttu-id="c0322-160">Por exemplo, um sombreador pode declarar dois buffers constantes e organizar os dados em cada um com base em sua frequência de atualização: os dados que precisam ser atualizados por objeto (como uma matriz mundial) são agrupados em um buffer constante que pode ser atualizado para cada objeto.</span><span class="sxs-lookup"><span data-stu-id="c0322-160">For example, a shader might declare two constant buffers and organize the data in each based on their frequency of update: data that needs to be updated on a per-object basis (like a world matrix) is grouped into a constant buffer which could be updated for each object.</span></span> <span data-ttu-id="c0322-161">Isso é separado dos dados que caracterizam uma cena e, portanto, provavelmente serão atualizados com muito menos frequência (quando a cena for alterada).</span><span class="sxs-lookup"><span data-stu-id="c0322-161">This is separate from data that characterizes a scene and is therefore likely to be updated much less often (when the scene changes).</span></span>


```
cbuffer myObject
{       
    float4x4 matWorld;
    float3   vObjectPosition;
    int      arrayIndex;
}
 
cbuffer myScene
{
    float3   vSunPosition;
    float4x4 matView;
}
        
```



### <a name="default-constant-buffers"></a><span data-ttu-id="c0322-162">Buffers de constantes padrão</span><span class="sxs-lookup"><span data-stu-id="c0322-162">Default constant buffers</span></span>

<span data-ttu-id="c0322-163">Há dois buffers de constante padrão disponíveis, $Global e $Param.</span><span class="sxs-lookup"><span data-stu-id="c0322-163">There are two default constant buffers available, $Global and $Param.</span></span> <span data-ttu-id="c0322-164">Variáveis que são colocadas no escopo global são adicionadas implicitamente ao $Global CBuffer, usando o mesmo método de empacotamento usado para cbuffers.</span><span class="sxs-lookup"><span data-stu-id="c0322-164">Variables that are placed in the global scope are added implicitly to the $Global cbuffer, using the same packing method that is used for cbuffers.</span></span> <span data-ttu-id="c0322-165">Os parâmetros uniformes na lista de parâmetros de uma função aparecem no buffer de constantes $Param quando um sombreador é compilado fora da estrutura de efeitos.</span><span class="sxs-lookup"><span data-stu-id="c0322-165">Uniform parameters in the parameter list of a function appear in the $Param constant buffer when a shader is compiled outside of the effects framework.</span></span> <span data-ttu-id="c0322-166">Quando compilado dentro da estrutura de efeitos, todos os uniforms devem ser resolvidos para as variáveis definidas no escopo global.</span><span class="sxs-lookup"><span data-stu-id="c0322-166">When compiled inside the effects framework, all uniforms must resolve to variables defined in the global scope.</span></span>

## <a name="examples"></a><span data-ttu-id="c0322-167">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c0322-167">Examples</span></span>

<span data-ttu-id="c0322-168">Aqui está um exemplo de exemplo de [Skinning10](https://msdn.microsoft.com/library/Ee416429(v=VS.85).aspx) que é um buffer de textura composto por uma matriz de matrizes.</span><span class="sxs-lookup"><span data-stu-id="c0322-168">Here is an example from [Skinning10 Sample](https://msdn.microsoft.com/library/Ee416429(v=VS.85).aspx) that is a texture buffer made up of an array of matrices.</span></span>


```
tbuffer tbAnimMatrices
{
    matrix g_mTexBoneWorld[MAX_BONE_MATRICES];
};
      
```



<span data-ttu-id="c0322-169">Essa declaração de exemplo atribui manualmente um buffer de constantes para iniciar em um registro específico e também empacota elementos específicos por subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="c0322-169">This example declaration manually assigns a constant buffer to start at a particular register, and also packs particular elements by subcomponents.</span></span>


```
cbuffer MyBuffer : register(b3)
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c1);
    float1 Element3 : packoffset(c1.y);
}
      
```



## <a name="related-topics"></a><span data-ttu-id="c0322-170">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c0322-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0322-171">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="c0322-171">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

