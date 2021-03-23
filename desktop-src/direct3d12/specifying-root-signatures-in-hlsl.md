---
title: Especificando assinaturas raiz em HLSL
description: A especificação de assinaturas raiz no modelo do sombreador HLSL 5,1 é uma alternativa para especificá-los no código C++.
ms.assetid: 399F5E91-B017-4F5E-9037-DC055407D96F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 236876e22c3e1e0bb849ec1e1bc7d45692c900d6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548209"
---
# <a name="specifying-root-signatures-in-hlsl"></a><span data-ttu-id="74821-103">Especificando assinaturas raiz em HLSL</span><span class="sxs-lookup"><span data-stu-id="74821-103">Specifying Root Signatures in HLSL</span></span>

<span data-ttu-id="74821-104">A especificação de assinaturas raiz no modelo do sombreador HLSL 5,1 é uma alternativa para especificá-los no código C++.</span><span class="sxs-lookup"><span data-stu-id="74821-104">Specifying root signatures in HLSL Shader Model 5.1 is an alternative to specifying them in C++ code.</span></span>

-   [<span data-ttu-id="74821-105">Um exemplo de assinatura raiz HLSL</span><span class="sxs-lookup"><span data-stu-id="74821-105">An example HLSL Root Signature</span></span>](#an-example-hlsl-root-signature)
    -   [<span data-ttu-id="74821-106">Assinatura de raiz versão 1,0</span><span class="sxs-lookup"><span data-stu-id="74821-106">Root Signature Version 1.0</span></span>](#root-signature-version-10)
    -   [<span data-ttu-id="74821-107">Assinatura de raiz versão 1,1</span><span class="sxs-lookup"><span data-stu-id="74821-107">Root Signature Version 1.1</span></span>](#root-signature-version-11)
-   [<span data-ttu-id="74821-108">RootFlags</span><span class="sxs-lookup"><span data-stu-id="74821-108">RootFlags</span></span>](#rootflags)
-   [<span data-ttu-id="74821-109">Constantes raiz</span><span class="sxs-lookup"><span data-stu-id="74821-109">Root Constants</span></span>](#root-constants)
-   [<span data-ttu-id="74821-110">Visibilidade</span><span class="sxs-lookup"><span data-stu-id="74821-110">Visibility</span></span>](#visibility)
-   [<span data-ttu-id="74821-111">CBV no nível raiz</span><span class="sxs-lookup"><span data-stu-id="74821-111">Root-level CBV</span></span>](#root-level-cbv)
-   [<span data-ttu-id="74821-112">SRV de nível raiz</span><span class="sxs-lookup"><span data-stu-id="74821-112">Root-level SRV</span></span>](#root-level-srv)
-   [<span data-ttu-id="74821-113">UAV no nível raiz</span><span class="sxs-lookup"><span data-stu-id="74821-113">Root-level UAV</span></span>](#root-level-uav)
-   [<span data-ttu-id="74821-114">Tabela de descritores</span><span class="sxs-lookup"><span data-stu-id="74821-114">Descriptor Table</span></span>](#descriptor-table)
-   [<span data-ttu-id="74821-115">Amostra estática</span><span class="sxs-lookup"><span data-stu-id="74821-115">Static Sampler</span></span>](#static-sampler)
-   [<span data-ttu-id="74821-116">Compilando uma assinatura raiz do HLSL</span><span class="sxs-lookup"><span data-stu-id="74821-116">Compiling an HLSL root signature</span></span>](#compiling-an-hlsl-root-signature)
-   [<span data-ttu-id="74821-117">Manipulando assinaturas raiz com o compilador FXC</span><span class="sxs-lookup"><span data-stu-id="74821-117">Manipulating root signatures with the FXC compiler</span></span>](#manipulating-root-signatures-with-the-fxc-compiler)
-   [<span data-ttu-id="74821-118">Observações</span><span class="sxs-lookup"><span data-stu-id="74821-118">Notes</span></span>](#notes)
-   [<span data-ttu-id="74821-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="74821-119">Related topics</span></span>](#related-topics)

## <a name="an-example-hlsl-root-signature"></a><span data-ttu-id="74821-120">Um exemplo de assinatura raiz HLSL</span><span class="sxs-lookup"><span data-stu-id="74821-120">An example HLSL Root Signature</span></span>

<span data-ttu-id="74821-121">Uma assinatura raiz pode ser especificada em HLSL como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="74821-121">A root signature can be specified in HLSL as a string.</span></span> <span data-ttu-id="74821-122">A cadeia de caracteres contém uma coleção de cláusulas separadas por vírgulas que descrevem os componentes constituintes da assinatura raiz.</span><span class="sxs-lookup"><span data-stu-id="74821-122">The string contains a collection of comma-separated clauses that describe root signature constituent components.</span></span> <span data-ttu-id="74821-123">A assinatura raiz deve ser idêntica em sombreadores para qualquer um dos objetos de estado de pipeline (PSO).</span><span class="sxs-lookup"><span data-stu-id="74821-123">The root signature should be identical across shaders for any one pipeline state object (PSO).</span></span> <span data-ttu-id="74821-124">Veja um exemplo:</span><span class="sxs-lookup"><span data-stu-id="74821-124">Here is an example:</span></span>

### <a name="root-signature-version-10"></a><span data-ttu-id="74821-125">Assinatura de raiz versão 1,0</span><span class="sxs-lookup"><span data-stu-id="74821-125">Root Signature Version 1.0</span></span>

``` syntax
#define MyRS1 "RootFlags( ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT | " \
                         "DENY_VERTEX_SHADER_ROOT_ACCESS), " \
              "CBV(b0, space = 1), " \
              "SRV(t0), " \
              "UAV(u0, visibility = SHADER_VISIBILITY_GEOMETRY), " \
              "DescriptorTable( CBV(b0), " \
                               "UAV(u1, numDescriptors = 2), " \
                               "SRV(t1, numDescriptors = unbounded)), " \
              "DescriptorTable(Sampler(s0, numDescriptors = 2)), " \
              "RootConstants(num32BitConstants=1, b9), " \
              "DescriptorTable( UAV(u3), " \
                               "UAV(u4), " \
                               "UAV(u5, offset=1)), " \

              "StaticSampler(s2)," \
              "StaticSampler(s3, " \
                             "addressU = TEXTURE_ADDRESS_CLAMP, " \
                             "filter = FILTER_MIN_MAG_MIP_LINEAR )"
```

### <a name="root-signature-version-11"></a><span data-ttu-id="74821-126">Assinatura de raiz versão 1,1</span><span class="sxs-lookup"><span data-stu-id="74821-126">Root Signature Version 1.1</span></span>

<span data-ttu-id="74821-127">A [assinatura de raiz versão 1,1](root-signature-version-1-1.md) permite otimizações de driver em dados e descritores de assinatura raiz.</span><span class="sxs-lookup"><span data-stu-id="74821-127">[Root Signature Version 1.1](root-signature-version-1-1.md) enables driver optimizations on root signature descriptors and data.</span></span>

``` syntax
#define MyRS1 "RootFlags( ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT | " \
                         "DENY_VERTEX_SHADER_ROOT_ACCESS), " \
              "CBV(b0, space = 1, flags = DATA_STATIC), " \
              "SRV(t0), " \
              "UAV(u0), " \
              "DescriptorTable( CBV(b1), " \
                               "SRV(t1, numDescriptors = 8, " \
                               "        flags = DESCRIPTORS_VOLATILE), " \
                               "UAV(u1, numDescriptors = unbounded, " \
                               "        flags = DESCRIPTORS_VOLATILE)), " \
              "DescriptorTable(Sampler(s0, space=1, numDescriptors = 4)), " \
              "RootConstants(num32BitConstants=3, b10), " \
              "StaticSampler(s1)," \
              "StaticSampler(s2, " \
                             "addressU = TEXTURE_ADDRESS_CLAMP, " \
                             "filter = FILTER_MIN_MAG_MIP_LINEAR )"
```

<span data-ttu-id="74821-128">Essa definição daria a seguinte assinatura de raiz, observando:</span><span class="sxs-lookup"><span data-stu-id="74821-128">This definition would give the following root signature, noting:</span></span>

-   <span data-ttu-id="74821-129">O uso de parâmetros padrão.</span><span class="sxs-lookup"><span data-stu-id="74821-129">The use of default parameters.</span></span>
-   <span data-ttu-id="74821-130">B0 e (B0, espaço = 1) não entram em conflito</span><span class="sxs-lookup"><span data-stu-id="74821-130">b0 and (b0, space=1) do not conflict</span></span>
-   <span data-ttu-id="74821-131">U0 só é visível para o sombreador Geometry</span><span class="sxs-lookup"><span data-stu-id="74821-131">u0 is only visible to the geometry shader</span></span>
-   <span data-ttu-id="74821-132">U4 e U5 são alias para o mesmo descritor em um heap</span><span class="sxs-lookup"><span data-stu-id="74821-132">u4 and u5 are aliased to the same descriptor in a heap</span></span>

![uma assinatura raiz especificada usando o idioma do sombreador de alto nível](images/hlsl-root-signature.png)

<span data-ttu-id="74821-134">A linguagem de assinatura raiz HLSL corresponde de forma mais próxima às APIs de assinatura raiz do C++ e tem uma potência expressiva equivalente.</span><span class="sxs-lookup"><span data-stu-id="74821-134">The HLSL root signature language closely corresponds to the C++ root signature APIs and has equivalent expressive power.</span></span> <span data-ttu-id="74821-135">A assinatura raiz é especificada como uma sequência de cláusulas, separadas por vírgula.</span><span class="sxs-lookup"><span data-stu-id="74821-135">The root signature is specified as a sequence of clauses, separated by comma.</span></span> <span data-ttu-id="74821-136">A ordem das cláusulas é importante, pois a ordem de análise determina a posição do slot na assinatura raiz.</span><span class="sxs-lookup"><span data-stu-id="74821-136">The order of clauses is important, as the order of parsing determines the slot position in the root signature.</span></span> <span data-ttu-id="74821-137">Cada cláusula usa um ou mais parâmetros nomeados.</span><span class="sxs-lookup"><span data-stu-id="74821-137">Each clause takes one or more named parameters.</span></span> <span data-ttu-id="74821-138">No entanto, a ordem dos parâmetros não é importante.</span><span class="sxs-lookup"><span data-stu-id="74821-138">The order of parameters is not important, however.</span></span>

## <a name="rootflags"></a><span data-ttu-id="74821-139">RootFlags</span><span class="sxs-lookup"><span data-stu-id="74821-139">RootFlags</span></span>

<span data-ttu-id="74821-140">A cláusula opcional *RootFlags* usa 0 (o valor padrão para indicar nenhum sinalizador) ou um ou vários valores de sinalizadores de raiz predefinidos, conectados por meio do \| operador ou ' '.</span><span class="sxs-lookup"><span data-stu-id="74821-140">The optional *RootFlags* clause takes either 0 (the default value to indicate no flags), or one or several of predefined root flags values, connected via the OR ‘\|’ operator.</span></span> <span data-ttu-id="74821-141">Os valores de sinalizador raiz permitidos são definidos [**por \_ \_ \_ sinalizadores de assinatura raiz D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags).</span><span class="sxs-lookup"><span data-stu-id="74821-141">The allowed root flag values are defined by [**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags).</span></span>

<span data-ttu-id="74821-142">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="74821-142">For example:</span></span>

``` syntax
RootFlags(0) // default value – no flags
RootFlags(ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT)
RootFlags(ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT | DENY_VERTEX_SHADER_ROOT_ACCESS)
```

## <a name="root-constants"></a><span data-ttu-id="74821-143">Constantes raiz</span><span class="sxs-lookup"><span data-stu-id="74821-143">Root Constants</span></span>

<span data-ttu-id="74821-144">A cláusula *RootConstants* Especifica constantes raiz na assinatura raiz.</span><span class="sxs-lookup"><span data-stu-id="74821-144">The *RootConstants* clause specifies root constants in the root signature.</span></span> <span data-ttu-id="74821-145">Dois parâmetros obrigatórios são: *num32BitConstants* e *bReg* (o registro correspondente ao *BaseShaderRegister* em APIs do C++) do *CBuffer*.</span><span class="sxs-lookup"><span data-stu-id="74821-145">Two mandatory parameters are: *num32BitConstants* and *bReg* (the register corresponding to *BaseShaderRegister* in C++ APIs) of the *cbuffer*.</span></span> <span data-ttu-id="74821-146">Os parâmetros Space (*RegisterSpace* em c++ APIs) e Visibility (*ShaderVisibility* em c++) são opcionais e os valores padrão são:</span><span class="sxs-lookup"><span data-stu-id="74821-146">The space (*RegisterSpace* in C++ APIs) and visibility (*ShaderVisibility* in C++) parameters are optional, and the default values are:</span></span>

``` syntax
RootConstants(num32BitConstants=N, bReg [, space=0, 
              visibility=SHADER_VISIBILITY_ALL ])
```

<span data-ttu-id="74821-147">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="74821-147">For example:</span></span>

``` syntax
RootConstants(num32BitConstants=3, b3)
```

## <a name="visibility"></a><span data-ttu-id="74821-148">Visibilidade</span><span class="sxs-lookup"><span data-stu-id="74821-148">Visibility</span></span>

<span data-ttu-id="74821-149">Visibility é um parâmetro opcional que pode ter um dos valores da [**\_ \_ visibilidade do sombreador D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility).</span><span class="sxs-lookup"><span data-stu-id="74821-149">Visibility is an optional parameter that can have one of the values from [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility).</span></span>

<span data-ttu-id="74821-150">\_A visibilidade \_ do sombreador todos transmite os argumentos raiz para todos os sombreadores.</span><span class="sxs-lookup"><span data-stu-id="74821-150">SHADER\_VISIBILITY\_ALL broadcasts the root arguments to all shaders.</span></span> <span data-ttu-id="74821-151">Em algum hardware, isso não tem nenhum custo, mas em outro hardware há um custo para bifurcar os dados para todos os estágios do sombreador.</span><span class="sxs-lookup"><span data-stu-id="74821-151">On some hardware this has no cost, but on other hardware there is a cost to fork the data to all the shader stages.</span></span> <span data-ttu-id="74821-152">Definir uma das opções, como \_ vértice de visibilidade do sombreador \_ , limita o argumento raiz a um único estágio de sombreador.</span><span class="sxs-lookup"><span data-stu-id="74821-152">Setting one of the options, such as SHADER\_VISIBILITY\_VERTEX, limits the root argument to a single shader stage.</span></span>

<span data-ttu-id="74821-153">A configuração de argumentos raiz para estágios de sombreador único permite que o mesmo nome de associação seja usado em diferentes estágios.</span><span class="sxs-lookup"><span data-stu-id="74821-153">Setting root arguments to single shader stages allows the same bind name to be used at different stages.</span></span> <span data-ttu-id="74821-154">Por exemplo, uma associação SRV de `t0,SHADER_VISIBILITY_VERTEX` e a associação SRV de `t0,SHADER_VISIBILITY_PIXEL` seriam válidas.</span><span class="sxs-lookup"><span data-stu-id="74821-154">For example, an SRV binding of `t0,SHADER_VISIBILITY_VERTEX` and SRV binding of `t0,SHADER_VISIBILITY_PIXEL` would be valid.</span></span> <span data-ttu-id="74821-155">Mas se a configuração de visibilidade era `t0,SHADER_VISIBILITY_ALL` para uma das associações, a assinatura raiz seria inválida.</span><span class="sxs-lookup"><span data-stu-id="74821-155">But if the visibility setting was `t0,SHADER_VISIBILITY_ALL` for one of the bindings, the root signature would be invalid.</span></span>

## <a name="root-level-cbv"></a><span data-ttu-id="74821-156">CBV no nível raiz</span><span class="sxs-lookup"><span data-stu-id="74821-156">Root-level CBV</span></span>

<span data-ttu-id="74821-157">A `CBV` cláusula (exibição de buffer de constante) especifica uma entrada reg de buffer constante de nível de raiz b.</span><span class="sxs-lookup"><span data-stu-id="74821-157">The `CBV` (constant buffer view) clause specifies a root-level constant buffer b-register Reg entry.</span></span> <span data-ttu-id="74821-158">Observe que esta é uma entrada escalar; Não é possível especificar um intervalo para o nível raiz.</span><span class="sxs-lookup"><span data-stu-id="74821-158">Note that this is a scalar entry; it is not possible to specify a range for the root level.</span></span>

``` syntax
CBV(bReg [, space=0, visibility=SHADER_VISIBILITY_ALL ])    //   Version 1.0
CBV(bReg [, space=0, visibility=SHADER_VISIBILITY_ALL,      // Version 1.1
            flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

## <a name="root-level-srv"></a><span data-ttu-id="74821-159">SRV de nível raiz</span><span class="sxs-lookup"><span data-stu-id="74821-159">Root-level SRV</span></span>

<span data-ttu-id="74821-160">A `SRV` cláusula (exibição de recurso do sombreador) especifica uma entrada reg t-Register do registro no nível raiz.</span><span class="sxs-lookup"><span data-stu-id="74821-160">The `SRV` (shader resource view) clause specifies a root-level SRV t-register Reg entry.</span></span> <span data-ttu-id="74821-161">Observe que esta é uma entrada escalar; Não é possível especificar um intervalo para o nível raiz.</span><span class="sxs-lookup"><span data-stu-id="74821-161">Note that this is a scalar entry; it is not possible to specify a range for the root level.</span></span>

``` syntax
SRV(tReg [, space=0, visibility=SHADER_VISIBILITY_ALL ])    //   Version 1.0
SRV(tReg [, space=0, visibility=SHADER_VISIBILITY_ALL,      // Version 1.1
            flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

## <a name="root-level-uav"></a><span data-ttu-id="74821-162">UAV no nível raiz</span><span class="sxs-lookup"><span data-stu-id="74821-162">Root-level UAV</span></span>

<span data-ttu-id="74821-163">A `UAV` cláusula (exibição de acesso não ordenado) especifica uma entrada reg do UAV no nível da raiz.</span><span class="sxs-lookup"><span data-stu-id="74821-163">The `UAV` (unordered access view) clause specifies a root-level UAV u-register Reg entry.</span></span> <span data-ttu-id="74821-164">Observe que esta é uma entrada escalar; Não é possível especificar um intervalo para o nível raiz.</span><span class="sxs-lookup"><span data-stu-id="74821-164">Note that this is a scalar entry; it is not possible to specify a range for the root level.</span></span>

``` syntax
UAV(uReg [, space=0, visibility=SHADER_VISIBILITY_ALL ])    //   Version 1.0
UAV(uReg [, space=0, visibility=SHADER_VISIBILITY_ALL,      // Version 1.1
            flags=DATA_VOLATILE ])
```

<span data-ttu-id="74821-165">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="74821-165">For example:</span></span>

``` syntax
UAV(u3)
```

## <a name="descriptor-table"></a><span data-ttu-id="74821-166">Tabela de descritores</span><span class="sxs-lookup"><span data-stu-id="74821-166">Descriptor Table</span></span>

<span data-ttu-id="74821-167">A `DescriptorTable` cláusula é, em si, uma lista de cláusulas de tabela de descritores separados por vírgulas, bem como um parâmetro de visibilidade opcional.</span><span class="sxs-lookup"><span data-stu-id="74821-167">The `DescriptorTable` clause is itself a list of comma-separated descriptor table clauses, as well as an optional visibility parameter.</span></span> <span data-ttu-id="74821-168">As cláusulas de *descriptortable* incluem cbv, SRV, UAV e amostra.</span><span class="sxs-lookup"><span data-stu-id="74821-168">The *DescriptorTable* clauses include CBV, SRV, UAV, and Sampler.</span></span> <span data-ttu-id="74821-169">Observe que seus parâmetros diferem das cláusulas de nível raiz.</span><span class="sxs-lookup"><span data-stu-id="74821-169">Note that their parameters differ from those of the root-level clauses.</span></span>

``` syntax
DescriptorTable( DTClause1, [ DTClause2, … DTClauseN,
                 visibility=SHADER_VISIBILITY_ALL ] )
```

<span data-ttu-id="74821-170">A tabela de descritores `CBV` tem a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="74821-170">The Descriptor Table `CBV` has the following syntax:</span></span>

``` syntax
CBV(bReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])   // Version 1.0
CBV(bReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND      // Version 1.1
          , flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

<span data-ttu-id="74821-171">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="74821-171">For example:</span></span>

``` syntax
DescriptorTable(CBV(b0),SRV(t3, numDescriptors=unbounded))
```

<span data-ttu-id="74821-172">O parâmetro obrigatório *bReg* especifica o Reg de início do intervalo de CBuffer.</span><span class="sxs-lookup"><span data-stu-id="74821-172">The mandatory parameter *bReg* specifies the start Reg of the cbuffer range.</span></span> <span data-ttu-id="74821-173">O parâmetro *numDescriptors* especifica o número de descritores no intervalo CBuffer contíguo; o valor padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="74821-173">The *numDescriptors* parameter specifies the number of descriptors in the contiguous cbuffer range; the default value being 1.</span></span> <span data-ttu-id="74821-174">A entrada declara um intervalo de CBuffer ` [Reg, Reg + numDescriptors - 1]` quando *numDescriptors* é um número.</span><span class="sxs-lookup"><span data-stu-id="74821-174">The entry declares a cbuffer range` [Reg, Reg + numDescriptors - 1]`, when *numDescriptors* is a number.</span></span> <span data-ttu-id="74821-175">Se *numDescriptors* for igual a "unbounded", o intervalo será `[Reg, UINT_MAX]` , o que significa que o aplicativo deve garantir que ele não faz referência a uma área fora de limites.</span><span class="sxs-lookup"><span data-stu-id="74821-175">If *numDescriptors* is equal to "unbounded", the range is `[Reg, UINT_MAX]`, which means the app must ensure it is not referencing an out-of-bounds area.</span></span> <span data-ttu-id="74821-176">O campo de *deslocamento* representa o parâmetro *OffsetInDescriptorsFromTableStart* nas APIs do C++, ou seja, o deslocamento (em descritores) do início da tabela.</span><span class="sxs-lookup"><span data-stu-id="74821-176">The *offset* field represents the *OffsetInDescriptorsFromTableStart* parameter in the C++ APIs, that is, the offset (in descriptors) from the start of the table.</span></span> <span data-ttu-id="74821-177">Se o deslocamento for definido como DESCRITOr de deslocamento de intervalo de descrição \_ \_ \_ (o padrão), significa que o intervalo é diretamente após o intervalo anterior.</span><span class="sxs-lookup"><span data-stu-id="74821-177">If the offset is set to DESCRIPTOR\_RANGE\_OFFSET\_APPEND (the default), it means the range is directly after the previous range.</span></span> <span data-ttu-id="74821-178">No entanto, a inserção de deslocamentos específicos permite que os intervalos se sobreponham, permitindo o registro de alias.</span><span class="sxs-lookup"><span data-stu-id="74821-178">However, entering specific offsets does allow for ranges to overlap each other, allowing register aliasing.</span></span>

<span data-ttu-id="74821-179">A tabela de descritores `SRV` tem a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="74821-179">The Descriptor Table `SRV` has the following syntax:</span></span>

``` syntax
SRV(tReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])    // Version 1.0
SRV(tReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND,      // Version 1.1
            flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

<span data-ttu-id="74821-180">Isso é semelhante à entrada da tabela de descritores `CBV` , exceto pelo intervalo especificado para exibições de recursos do sombreador.</span><span class="sxs-lookup"><span data-stu-id="74821-180">This is similar to the descriptor table `CBV` entry, except the specified range is for shader resource views.</span></span>

<span data-ttu-id="74821-181">A tabela de descritores `UAV` tem a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="74821-181">The Descriptor Table `UAV` has the following syntax:</span></span>

``` syntax
UAV(uReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])    // Version 1.0
UAV(uReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND,      // Version 1.1
            flags=DATA_VOLATILE ])
```

<span data-ttu-id="74821-182">Isso é semelhante à entrada da tabela de descritores `CBV` , exceto pelo intervalo especificado para exibições de acesso não ordenado.</span><span class="sxs-lookup"><span data-stu-id="74821-182">This is similar to the descriptor table `CBV` entry, except the specified range is for unordered access views.</span></span>

<span data-ttu-id="74821-183">A tabela de descritores `Sampler` tem a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="74821-183">The Descriptor Table `Sampler` has the following syntax:</span></span>

``` syntax
Sampler(sReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])  // Version 1.0
Sampler(sReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND,    // Version 1.1
                flags=0 ])
```

<span data-ttu-id="74821-184">Isso é semelhante à entrada da tabela de descritores `CBV` , exceto pelo intervalo especificado para os exemplos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="74821-184">This is similar to the descriptor table `CBV` entry, except the specified range is for shader samplers.</span></span> <span data-ttu-id="74821-185">Observe que os exemplos não podem ser misturados com outros tipos de descritores na mesma tabela de descrição (já que estão em um heap de descritor separado).</span><span class="sxs-lookup"><span data-stu-id="74821-185">Note that Samplers can’t be mixed with other types of descriptors in the same descriptor table (since they are in a separate descriptor heap).</span></span>

## <a name="static-sampler"></a><span data-ttu-id="74821-186">Amostra estática</span><span class="sxs-lookup"><span data-stu-id="74821-186">Static Sampler</span></span>

<span data-ttu-id="74821-187">A amostra estática representa a [**estrutura \_ \_ \_ desc de amostra estática D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) .</span><span class="sxs-lookup"><span data-stu-id="74821-187">The static sampler represents the [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) structure.</span></span> <span data-ttu-id="74821-188">O parâmetro obrigatório para *StaticSampler* é um Reg de amostras de s-Register. Outros parâmetros são opcionais com valores padrão mostrados abaixo.</span><span class="sxs-lookup"><span data-stu-id="74821-188">The mandatory parameter for *StaticSampler* is a scalar, sampler s-register Reg. Other parameters are optional with default values shown below.</span></span> <span data-ttu-id="74821-189">A maioria dos campos aceita um conjunto de enums predefinidos.</span><span class="sxs-lookup"><span data-stu-id="74821-189">Most fields accept a set of predefined enums.</span></span>

``` syntax
StaticSampler( sReg,
              [ filter = FILTER_ANISOTROPIC, 
                addressU = TEXTURE_ADDRESS_WRAP,
                addressV = TEXTURE_ADDRESS_WRAP,
                addressW = TEXTURE_ADDRESS_WRAP,
                mipLODBias = 0.f,
                maxAnisotropy = 16,
                comparisonFunc = COMPARISON_LESS_EQUAL,
                borderColor = STATIC_BORDER_COLOR_OPAQUE_WHITE,
                minLOD = 0.f,         
                maxLOD = 3.402823466e+38f,
                space = 0, 
                visibility = SHADER_VISIBILITY_ALL ])
```

<span data-ttu-id="74821-190">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="74821-190">For example:</span></span>

``` syntax
StaticSampler(s4, filter=FILTER_MIN_MAG_MIP_LINEAR)
```

<span data-ttu-id="74821-191">As opções de parâmetro são muito semelhantes às chamadas da API do C++, exceto a *BorderColor*, que é restrita a uma enumeração em HLSL.</span><span class="sxs-lookup"><span data-stu-id="74821-191">The parameter options are very similar to the C++ API calls, except for *borderColor*, which is restricted to an enum in HLSL.</span></span>

<span data-ttu-id="74821-192">O campo de filtro pode ser um [**dos \_ filtros D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter).</span><span class="sxs-lookup"><span data-stu-id="74821-192">The filter field can be one of [**D3D12\_FILTER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter).</span></span>

<span data-ttu-id="74821-193">Os campos de endereço podem ser um dos [**\_ modos de \_ endereço \_ de textura D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode).</span><span class="sxs-lookup"><span data-stu-id="74821-193">The address fields can each be one of [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode).</span></span>

<span data-ttu-id="74821-194">A função de comparação pode ser uma das [**D3D12 de \_ comparação \_ Func**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func).</span><span class="sxs-lookup"><span data-stu-id="74821-194">The comparison function can be one of [**D3D12\_COMPARISON\_FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func).</span></span>

<span data-ttu-id="74821-195">O campo de cor da borda pode ser uma das [**\_ \_ \_ cores de borda estática D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color).</span><span class="sxs-lookup"><span data-stu-id="74821-195">The border color field can be one of [**D3D12\_STATIC\_BORDER\_COLOR**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color).</span></span>

<span data-ttu-id="74821-196">A visibilidade pode ser uma das [**D3D12 do \_ sombreador \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility).</span><span class="sxs-lookup"><span data-stu-id="74821-196">Visibility can be one of [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility).</span></span>

## <a name="compiling-an-hlsl-root-signature"></a><span data-ttu-id="74821-197">Compilando uma assinatura raiz do HLSL</span><span class="sxs-lookup"><span data-stu-id="74821-197">Compiling an HLSL root signature</span></span>

<span data-ttu-id="74821-198">Há dois mecanismos para compilar uma assinatura raiz HLSL.</span><span class="sxs-lookup"><span data-stu-id="74821-198">There are two mechanisms to compile an HLSL root signature.</span></span> <span data-ttu-id="74821-199">Primeiro, é possível anexar uma cadeia de caracteres de assinatura raiz a um sombreador específico por meio do atributo *RootSignature* (no exemplo a seguir, usando o ponto de entrada **MyRS1** ):</span><span class="sxs-lookup"><span data-stu-id="74821-199">First, it is possible to attach a root signature string to a particular shader via the *RootSignature* attribute (in the following example, using the **MyRS1** entry point):</span></span>

``` syntax
[RootSignature(MyRS1)]
float4 main(float4 coord : COORD) : SV_Target
{
…
}
```

<span data-ttu-id="74821-200">O compilador criará e verificará o blob de assinatura raiz para o sombreador e o inserirá junto com o código de byte do sombreador no blob do sombreador.</span><span class="sxs-lookup"><span data-stu-id="74821-200">The compiler will create and verify the root signature blob for the shader and embed it alongside the shader byte code into the shader blob.</span></span> <span data-ttu-id="74821-201">O compilador dá suporte à sintaxe de assinatura raiz para o modelo de sombreador 5,0 e superior.</span><span class="sxs-lookup"><span data-stu-id="74821-201">The compiler supports root signature syntax for shader model 5.0 and higher.</span></span> <span data-ttu-id="74821-202">Se uma assinatura raiz for inserida em um sombreador do modelo do sombreador 5,0 e esse sombreador for enviado para o tempo de execução D3D11, em oposição ao D3D12, a parte da assinatura raiz será silenciosamente ignorada pelo D3D11.</span><span class="sxs-lookup"><span data-stu-id="74821-202">If a root signature is embedded in a shader model 5.0 shader and that shader is sent to the D3D11 runtime, as opposed to D3D12, the root signature portion will get silently ignored by D3D11.</span></span>

<span data-ttu-id="74821-203">O outro mecanismo é criar um blob de assinatura de raiz autônoma, talvez reutilizá-lo com um grande conjunto de sombreadores, economizando espaço.</span><span class="sxs-lookup"><span data-stu-id="74821-203">The other mechanism is to create a standalone root signature blob, perhaps to reuse it with a large set of shaders, saving space.</span></span> <span data-ttu-id="74821-204">A [ferramenta de compilador de efeito](/windows/desktop/direct3dtools/fxc) (FXC) dá suporte aos modelos de sombreador **rootsig \_ 1 \_ 0** e **rootsig \_ 1 \_ 1** .</span><span class="sxs-lookup"><span data-stu-id="74821-204">The [Effect-Compiler Tool](/windows/desktop/direct3dtools/fxc) (FXC) supports both **rootsig\_1\_0** and **rootsig\_1\_1** shader models.</span></span> <span data-ttu-id="74821-205">O nome da cadeia de caracteres de definição é especificado por meio do argumento/E usual.</span><span class="sxs-lookup"><span data-stu-id="74821-205">The name of the define string is specified via the usual /E argument.</span></span> <span data-ttu-id="74821-206">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="74821-206">For example:</span></span>

``` syntax
fxc.exe /T rootsig_1_1 MyRS1.hlsl /E MyRS1 /Fo MyRS1.fxo
```

<span data-ttu-id="74821-207">Observe que a cadeia de caracteres de assinatura de raiz também pode ser passada na linha de comando, por exemplo,/D MyRS1 = "...".</span><span class="sxs-lookup"><span data-stu-id="74821-207">Note that the root signature string define can also be passed on the command line, e.g, /D MyRS1=”…”.</span></span>

## <a name="manipulating-root-signatures-with-the-fxc-compiler"></a><span data-ttu-id="74821-208">Manipulando assinaturas raiz com o compilador FXC</span><span class="sxs-lookup"><span data-stu-id="74821-208">Manipulating root signatures with the FXC compiler</span></span>

<span data-ttu-id="74821-209">O compilador FXC cria o código de byte de sombreador de arquivos de origem HLSL.</span><span class="sxs-lookup"><span data-stu-id="74821-209">The FXC compiler creates shader byte-code from HLSL source files.</span></span> <span data-ttu-id="74821-210">Há muitos parâmetros opcionais para esse compilador, consulte a [ferramenta de compilador de efeito](/windows/desktop/direct3dtools/fxc).</span><span class="sxs-lookup"><span data-stu-id="74821-210">There are a lot of optional parameters for this compiler, refer to the [Effect-Compiler Tool](/windows/desktop/direct3dtools/fxc).</span></span>

<span data-ttu-id="74821-211">Para gerenciar assinaturas raiz criadas pelo HLSL, a tabela a seguir fornece alguns exemplos de como usar o FXC.</span><span class="sxs-lookup"><span data-stu-id="74821-211">For managing HLSL authored root signatures, the following table gives some examples of using FXC.</span></span>



| <span data-ttu-id="74821-212">Linha</span><span class="sxs-lookup"><span data-stu-id="74821-212">Line</span></span> | <span data-ttu-id="74821-213">Linha de comando</span><span class="sxs-lookup"><span data-stu-id="74821-213">Command line</span></span>                                                                 | <span data-ttu-id="74821-214">Descrição</span><span class="sxs-lookup"><span data-stu-id="74821-214">Description</span></span>                                                                                                                                                                                                                              |
|------|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74821-215">1</span><span class="sxs-lookup"><span data-stu-id="74821-215">1</span></span>    | `fxc /T ps_5_1 shaderWithRootSig.hlsl /Fo rs1.fxo`                           | <span data-ttu-id="74821-216">Compila um sombreador para o destino do pixel shader 5,1, a origem do sombreador está no arquivo shaderWithRootSig. HLSL, que inclui uma assinatura raiz.</span><span class="sxs-lookup"><span data-stu-id="74821-216">Compiles a shader for the pixel shader 5.1 target, the shader source is in the shaderWithRootSig.hlsl file, which includes a root signature.</span></span> <span data-ttu-id="74821-217">O sombreador e a assinatura raiz são compilados como BLOBs separados no arquivo binário RS1. FXO.</span><span class="sxs-lookup"><span data-stu-id="74821-217">The shader and root signature are compiled as separate blobs in the rs1.fxo binary file.</span></span>    |
| <span data-ttu-id="74821-218">2</span><span class="sxs-lookup"><span data-stu-id="74821-218">2</span></span>    | `fxc /dumpbin rs1.fxo /extractrootsignature /Fo rs1.rs.fxo`                  | <span data-ttu-id="74821-219">Extrai a assinatura raiz do arquivo criado pela linha 1, portanto, o arquivo RS1. RS. FXO contém apenas uma assinatura raiz.</span><span class="sxs-lookup"><span data-stu-id="74821-219">Extracts the root signature from the file created by line 1, so the rs1.rs.fxo file contains just a root signature.</span></span>                                                                                                                      |
| <span data-ttu-id="74821-220">3</span><span class="sxs-lookup"><span data-stu-id="74821-220">3</span></span>    | `fxc /dumpbin rs1.fxo /Qstrip_rootsignature /Fo rs1.stripped.fxo`            | <span data-ttu-id="74821-221">Remove a assinatura raiz do arquivo criado pela linha 1, de modo que o arquivo RS1.. FXO contém um sombreador sem assinatura raiz.</span><span class="sxs-lookup"><span data-stu-id="74821-221">Removes the root signature from the file created by line 1, so the rs1.stripped.fxo file contains a shader with no root signature.</span></span>                                                                                                       |
| <span data-ttu-id="74821-222">4</span><span class="sxs-lookup"><span data-stu-id="74821-222">4</span></span>    | `fxc /dumpbin rs1.stripped.fxo /setrootsignature rs1.rs.fxo /Fo rs1.new.fxo` | <span data-ttu-id="74821-223">Combina um sombreador e uma assinatura raiz que estão em arquivos separados em um arquivo binário que contém os dois BLOBs.</span><span class="sxs-lookup"><span data-stu-id="74821-223">Combines a shader and root signature that are in separate files into a binary file containing both blobs.</span></span> <span data-ttu-id="74821-224">Neste exemplo, RS1. New. fx0 seria idêntico a RS1. fx0 na linha 1.</span><span class="sxs-lookup"><span data-stu-id="74821-224">In this example rs1.new.fx0 would be identical to rs1.fx0 in line 1.</span></span>                                                           |
| <span data-ttu-id="74821-225">5</span><span class="sxs-lookup"><span data-stu-id="74821-225">5</span></span>    | `fxc /T rootsig_1_0 rootSigAndMaybeShaderInHereToo.hlsl /E RS1 /Fo rs2.fxo`  | <span data-ttu-id="74821-226">Cria um arquivo binário de assinatura de raiz autônoma de uma fonte que pode conter mais do que apenas uma assinatura raiz.</span><span class="sxs-lookup"><span data-stu-id="74821-226">Creates a stand-alone root signature binary file from a source that may contain more than just a root signature.</span></span> <span data-ttu-id="74821-227">Observe o \_ destino rootsig 1 \_ 0 e que RS1 é o nome da cadeia de caracteres de macro da assinatura raiz ( \# definir) no arquivo HLSL.</span><span class="sxs-lookup"><span data-stu-id="74821-227">Note the rootsig\_1\_0 target, and that RS1 is the name of the root signature (\#define) macro string in the HLSL file.</span></span> |



 

<span data-ttu-id="74821-228">A funcionalidade disponível por meio do FXC também está disponível programaticamente usando a função [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) .</span><span class="sxs-lookup"><span data-stu-id="74821-228">The functionality available through FXC is also available programmatically using the [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) function.</span></span> <span data-ttu-id="74821-229">Essa chamada compila um sombreador com uma assinatura raiz ou uma assinatura raiz autônoma (definindo o \_ destino rootsig 1 \_ 0).</span><span class="sxs-lookup"><span data-stu-id="74821-229">This call compiles a shader with a root signature, or stand-alone root signature (setting the rootsig\_1\_0 target).</span></span> <span data-ttu-id="74821-230">[**D3DGetBlobPart**](/windows/desktop/direct3dhlsl/d3dgetblobpart) e [**D3DSetBlobPart**](/windows/desktop/direct3dhlsl/d3dsetblobpart) podem extrair e anexar assinaturas raiz a um blob existente.</span><span class="sxs-lookup"><span data-stu-id="74821-230">[**D3DGetBlobPart**](/windows/desktop/direct3dhlsl/d3dgetblobpart) and [**D3DSetBlobPart**](/windows/desktop/direct3dhlsl/d3dsetblobpart) can extract and attach root signatures to an existing blob.</span></span><span data-ttu-id="74821-231">\_ \_ A assinatura raiz do blob do D3D \_ é usada para especificar o tipo de parte do blob de assinatura raiz.</span><span class="sxs-lookup"><span data-stu-id="74821-231">  D3D\_BLOB\_ROOT\_SIGNATURE is used to specify the root signature blob part type.</span></span> <span data-ttu-id="74821-232">[**D3DStripShader**](/windows/desktop/direct3dhlsl/d3dstripshader) remove a assinatura raiz (usando o \_ sinalizador de \_ assinatura raiz da faixa D3DCOMPILER \_ ) do blob.</span><span class="sxs-lookup"><span data-stu-id="74821-232">[**D3DStripShader**](/windows/desktop/direct3dhlsl/d3dstripshader) removes the root signature (using the D3DCOMPILER\_STRIP\_ROOT\_SIGNATURE flag) from the blob.</span></span>

## <a name="notes"></a><span data-ttu-id="74821-233">Observações</span><span class="sxs-lookup"><span data-stu-id="74821-233">Notes</span></span>

> [!Note]  
> <span data-ttu-id="74821-234">Enquanto a compilação offline de sombreadores é altamente recomendável, se os sombreadores precisarem ser compilados em tempo de execução, consulte os comentários para [**D3DCompile2**](/windows/desktop/direct3dhlsl/d3dcompile2).</span><span class="sxs-lookup"><span data-stu-id="74821-234">Whereas the offline compilation of shaders is strongly recommended, if shaders have to be compiled at runtime, refer to the remarks for [**D3DCompile2**](/windows/desktop/direct3dhlsl/d3dcompile2).</span></span>

 

> [!Note]  
> <span data-ttu-id="74821-235">Os ativos HLSL existentes não precisam ser alterados para lidar com as assinaturas raiz a serem usadas com eles.</span><span class="sxs-lookup"><span data-stu-id="74821-235">Existing HLSL assets do not need to be changed to handle root signatures to be used with them.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="74821-236">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="74821-236">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74821-237">Indexação dinâmica usando HLSL 5.1</span><span class="sxs-lookup"><span data-stu-id="74821-237">Dynamic Indexing using HLSL 5.1</span></span>](dynamic-indexing-using-hlsl-5-1.md)
</dt> <dt>

[<span data-ttu-id="74821-238">Recursos do HLSL Shader Model 5,1 para Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="74821-238">HLSL Shader Model 5.1 Features for Direct3D 12</span></span>](/windows/desktop/direct3dhlsl/hlsl-shader-model-5-1-features-for-direct3d-12)
</dt> <dt>

[<span data-ttu-id="74821-239">Associação de recursos</span><span class="sxs-lookup"><span data-stu-id="74821-239">Resource Binding</span></span>](resource-binding.md)
</dt> <dt>

[<span data-ttu-id="74821-240">Associação de recursos em HLSL</span><span class="sxs-lookup"><span data-stu-id="74821-240">Resource Binding in HLSL</span></span>](resource-binding-in-hlsl.md)
</dt> <dt>

[<span data-ttu-id="74821-241">Assinaturas raiz</span><span class="sxs-lookup"><span data-stu-id="74821-241">Root Signatures</span></span>](root-signatures.md)
</dt> <dt>

[<span data-ttu-id="74821-242">Modelo do sombreador 5,1</span><span class="sxs-lookup"><span data-stu-id="74821-242">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[<span data-ttu-id="74821-243">Valor de referência de estêncil especificado do sombreador</span><span class="sxs-lookup"><span data-stu-id="74821-243">Shader Specified Stencil Reference Value</span></span>](shader-specified-stencil-reference-value.md)
</dt> <dt>

[<span data-ttu-id="74821-244">Cargas de exibição de acesso não ordenado digitado</span><span class="sxs-lookup"><span data-stu-id="74821-244">Typed Unordered Access View Loads</span></span>](typed-unordered-access-view-loads.md)
</dt> </dl>

 

 