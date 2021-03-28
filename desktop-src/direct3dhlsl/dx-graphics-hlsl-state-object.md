---
title: Objetos de estado
description: Use HLSL para definir objetos de estado.
ms.assetid: a02432dc-f354-48c0-a7ac-1ff502f3b1d1
ms.topic: article
ms.date: 2/2/2021
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 53bfc903f8bc1be56962e912b1c82f02faaf0c44
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104989134"
---
# <a name="state-objects"></a><span data-ttu-id="ec196-103">Objetos de estado</span><span class="sxs-lookup"><span data-stu-id="ec196-103">State Objects</span></span>

<span data-ttu-id="ec196-104">Com os modelos de sombreador 6,3 e posteriores, os aplicativos têm a conveniência e a flexibilidade de poder definir objetos de estado DXR diretamente no código do sombreador HLSL, além de usar as APIs do Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="ec196-104">With shader models 6.3 and later, applications have the convenience and flexibility of being able to define DXR state objects directly in HLSL shader code in addition to using Direct3D 12 APIs.</span></span>

<span data-ttu-id="ec196-105">No HLSL, os objetos de estado são declarados com essa sintaxe:</span><span class="sxs-lookup"><span data-stu-id="ec196-105">In HLSL, state objects are declared with this syntax:</span></span>

``` syntax
Type Name = 
{ 
    Field1,
    Field2,
    ...
};
```



| <span data-ttu-id="ec196-106">Item</span><span class="sxs-lookup"><span data-stu-id="ec196-106">Item</span></span>                                                                                         | <span data-ttu-id="ec196-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="ec196-107">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec196-108"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Escreva**</span><span class="sxs-lookup"><span data-stu-id="ec196-108"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Type**</span></span><br/>     | <span data-ttu-id="ec196-109">Identifica o tipo de subobjeto.</span><span class="sxs-lookup"><span data-stu-id="ec196-109">Identifies the type of subobject.</span></span> <span data-ttu-id="ec196-110">Deve ser um dos tipos de subobjeto HLSL com suporte.</span><span class="sxs-lookup"><span data-stu-id="ec196-110">Must be one of the supported HLSL subobject types.</span></span><br/>     |
| <span data-ttu-id="ec196-111"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nomes**</span><span class="sxs-lookup"><span data-stu-id="ec196-111"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>     | <span data-ttu-id="ec196-112">Uma cadeia de caracteres ASCII que identifica exclusivamente o nome da variável.</span><span class="sxs-lookup"><span data-stu-id="ec196-112">An ASCII string that uniquely identifies the variable name.</span></span><br/>                 |
| <span data-ttu-id="ec196-113"><span id="Field"></span><span id="field"></span><span id="FIELD"></span>**Campo [1, 2,...]**</span><span class="sxs-lookup"><span data-stu-id="ec196-113"><span id="Field"></span><span id="field"></span><span id="FIELD"></span>**Field[1, 2, ...]**</span></span><br/> | <span data-ttu-id="ec196-114">Campos do subobjeto.</span><span class="sxs-lookup"><span data-stu-id="ec196-114">Fields of the subobject.</span></span> <span data-ttu-id="ec196-115">Os campos específicos para cada tipo de subobjeto são descritos abaixo.</span><span class="sxs-lookup"><span data-stu-id="ec196-115">Specific fields for each type of subobject are described below.</span></span><br/> |




<span data-ttu-id="ec196-116">Lista de tipos de subobjetos:</span><span class="sxs-lookup"><span data-stu-id="ec196-116">List of subobject types:</span></span>
-   [<span data-ttu-id="ec196-117">StateObjectConfig</span><span class="sxs-lookup"><span data-stu-id="ec196-117">StateObjectConfig</span></span>](#stateobjectconfig)
-   [<span data-ttu-id="ec196-118">GlobalRootSignature</span><span class="sxs-lookup"><span data-stu-id="ec196-118">GlobalRootSignature</span></span>](#globalrootsignature)
-   [<span data-ttu-id="ec196-119">LocalRootSignature</span><span class="sxs-lookup"><span data-stu-id="ec196-119">LocalRootSignature</span></span>](#localrootsignature)
-   [<span data-ttu-id="ec196-120">SubobjectToExportsAssocation</span><span class="sxs-lookup"><span data-stu-id="ec196-120">SubobjectToExportsAssocation</span></span>](#subobjecttoexportsassocation)
-   [<span data-ttu-id="ec196-121">RaytracingShaderConfig</span><span class="sxs-lookup"><span data-stu-id="ec196-121">RaytracingShaderConfig</span></span>](#raytracingshaderconfig)
-   [<span data-ttu-id="ec196-122">RaytracingPipelineConfig</span><span class="sxs-lookup"><span data-stu-id="ec196-122">RaytracingPipelineConfig</span></span>](#raytracingpipelineconfig)
-   [<span data-ttu-id="ec196-123">TriangleHitGroup</span><span class="sxs-lookup"><span data-stu-id="ec196-123">TriangleHitGroup</span></span>](#trianglehitgroup)
-   [<span data-ttu-id="ec196-124">ProceduralPrimitiveHitGroup</span><span class="sxs-lookup"><span data-stu-id="ec196-124">ProceduralPrimitiveHitGroup</span></span>](#proceduralprimitivehitgroup)

## <a name="stateobjectconfig"></a><span data-ttu-id="ec196-125">StateObjectConfig</span><span class="sxs-lookup"><span data-stu-id="ec196-125">StateObjectConfig</span></span>

<span data-ttu-id="ec196-126">O tipo de subobjeto StateObjectConfig corresponde a uma estrutura [D3D12_STATE_OBJECT_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_object_config) .</span><span class="sxs-lookup"><span data-stu-id="ec196-126">The StateObjectConfig subobject type corresponds to a [D3D12_STATE_OBJECT_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_object_config) structure.</span></span>

<span data-ttu-id="ec196-127">Ele tem um campo, um sinalizador de bit, que é um ou ambos</span><span class="sxs-lookup"><span data-stu-id="ec196-127">It has one field, a bitwise flag, which is one or both of</span></span>

* <span data-ttu-id="ec196-128">STATE_OBJECT_FLAGS_ALLOW_LOCAL_DEPENDENCIES_ON_EXTERNAL_DEFINITONS</span><span class="sxs-lookup"><span data-stu-id="ec196-128">STATE_OBJECT_FLAGS_ALLOW_LOCAL_DEPENDENCIES_ON_EXTERNAL_DEFINITONS</span></span>
* <span data-ttu-id="ec196-129">STATE_OBJECT_FLAGS_ALLOW_EXTERNAL_DEPENDENCIES_ON_LOCAL_DEFINITIONS</span><span class="sxs-lookup"><span data-stu-id="ec196-129">STATE_OBJECT_FLAGS_ALLOW_EXTERNAL_DEPENDENCIES_ON_LOCAL_DEFINITIONS</span></span>

<span data-ttu-id="ec196-130">ou zero para nenhum deles.</span><span class="sxs-lookup"><span data-stu-id="ec196-130">or, zero for neither of them.</span></span>

<span data-ttu-id="ec196-131">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="ec196-131">Example:</span></span>

```
StateObjectConfig MyStateObjectConfig = 
{ 
    STATE_OBJECT_FLAGS_ALLOW_LOCAL_DEPENDENCIES_ON_EXTERNAL_DEFINITONS
};
```

## <a name="globalrootsignature"></a><span data-ttu-id="ec196-132">GlobalRootSignature</span><span class="sxs-lookup"><span data-stu-id="ec196-132">GlobalRootSignature</span></span>
<span data-ttu-id="ec196-133">Um GlobalRootSignature corresponde a uma estrutura de [D3D12_GLOBAL_ROOT_SIGNATURE](/windows/win32/api/d3d12/ns-d3d12-d3d12_global_root_signature) .</span><span class="sxs-lookup"><span data-stu-id="ec196-133">A GlobalRootSignature corresponds to a [D3D12_GLOBAL_ROOT_SIGNATURE](/windows/win32/api/d3d12/ns-d3d12-d3d12_global_root_signature) structure.</span></span>

<span data-ttu-id="ec196-134">Os campos consistem em um número de cadeias de caracteres que descrevem as partes da assinatura raiz.</span><span class="sxs-lookup"><span data-stu-id="ec196-134">The fields consist of some number of strings describing the parts of the root signature.</span></span> <span data-ttu-id="ec196-135">Para referência sobre isso, consulte [especificando assinaturas raiz no HLSL](../direct3d12/specifying-root-signatures-in-hlsl.md).</span><span class="sxs-lookup"><span data-stu-id="ec196-135">For reference on this, see [Specifying Root Signatures in HLSL](../direct3d12/specifying-root-signatures-in-hlsl.md).</span></span>

<span data-ttu-id="ec196-136">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="ec196-136">Example:</span></span>
```
GlobalRootSignature MyGlobalRootSignature =
{
    "DescriptorTable(UAV(u0)),"                     // Output texture
    "SRV(t0),"                                      // Acceleration structure
    "CBV(b0),"                                      // Scene constants
    "DescriptorTable(SRV(t1, numDescriptors = 2))"  // Static index and vertex buffers.
};
```

## <a name="localrootsignature"></a><span data-ttu-id="ec196-137">LocalRootSignature</span><span class="sxs-lookup"><span data-stu-id="ec196-137">LocalRootSignature</span></span>
<span data-ttu-id="ec196-138">Um LocalRootSignature corresponde a uma estrutura de [D3D12_LOCAL_ROOT_SIGNATURE](/windows/win32/api/d3d12/ns-d3d12-d3d12_local_root_signature) .</span><span class="sxs-lookup"><span data-stu-id="ec196-138">A LocalRootSignature corresponds to a [D3D12_LOCAL_ROOT_SIGNATURE](/windows/win32/api/d3d12/ns-d3d12-d3d12_local_root_signature) structure.</span></span>

<span data-ttu-id="ec196-139">Assim como o subobjeto de assinatura de raiz global, os campos consistem em algum número de cadeias de caracteres que descrevem as partes da assinatura raiz.</span><span class="sxs-lookup"><span data-stu-id="ec196-139">Just like the global root signature subobject, the fields consist of some number of strings describing the parts of the root signature.</span></span> <span data-ttu-id="ec196-140">Para referência sobre isso, consulte [especificando assinaturas raiz no HLSL](../direct3d12/specifying-root-signatures-in-hlsl.md).</span><span class="sxs-lookup"><span data-stu-id="ec196-140">For reference on this, see [Specifying Root Signatures in HLSL](../direct3d12/specifying-root-signatures-in-hlsl.md).</span></span>

<span data-ttu-id="ec196-141">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="ec196-141">Example:</span></span>
```
LocalRootSignature MyLocalRootSignature = 
{
    "RootConstants(num32BitConstants = 4, b1)"  // Cube constants 
};
```

## <a name="subobjecttoexportsassocation"></a><span data-ttu-id="ec196-142">SubobjectToExportsAssocation</span><span class="sxs-lookup"><span data-stu-id="ec196-142">SubobjectToExportsAssocation</span></span>
<span data-ttu-id="ec196-143">Por padrão, um subobjeto meramente declarado na mesma biblioteca como uma exportação é capaz de aplicar a essa exportação.</span><span class="sxs-lookup"><span data-stu-id="ec196-143">By default, a subobject merely declared in the same library as an export is able to apply to that export.</span></span> <span data-ttu-id="ec196-144">No entanto, os aplicativos têm a capacidade de substituí-lo e obter informações específicas sobre qual subobjeto é capaz de exportar.</span><span class="sxs-lookup"><span data-stu-id="ec196-144">However, applications have the ability to override that and get specific about what subobject goes with which export.</span></span> <span data-ttu-id="ec196-145">No HLSL, essa "Associação explícita" é feita usando SubobjectToExportsAssocation.</span><span class="sxs-lookup"><span data-stu-id="ec196-145">In HLSL, this "explicit association" is done using SubobjectToExportsAssocation.</span></span>

<span data-ttu-id="ec196-146">Um SubobjectToExportsAssocation corresponde a uma estrutura de [D3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION ](/windows/win32/api/d3d12/ns-d3d12-d3d12_dxil_subobject_to_exports_association) .</span><span class="sxs-lookup"><span data-stu-id="ec196-146">A SubobjectToExportsAssocation corresponds to a [D3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION ](/windows/win32/api/d3d12/ns-d3d12-d3d12_dxil_subobject_to_exports_association) structure.</span></span>

<span data-ttu-id="ec196-147">Este subobjeto é declarado com a sintaxe</span><span class="sxs-lookup"><span data-stu-id="ec196-147">This subobject is declared with the syntax</span></span>

``` syntax
SubobjectToExportsAssocation Name = 
{ 
    SubobjectName,
    Exports
};
```

| <span data-ttu-id="ec196-148">Item</span><span class="sxs-lookup"><span data-stu-id="ec196-148">Item</span></span>                                                                                         | <span data-ttu-id="ec196-149">Descrição</span><span class="sxs-lookup"><span data-stu-id="ec196-149">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec196-150"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nomes**</span><span class="sxs-lookup"><span data-stu-id="ec196-150"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>     | <span data-ttu-id="ec196-151">Uma cadeia de caracteres ASCII que identifica exclusivamente o nome da variável.</span><span class="sxs-lookup"><span data-stu-id="ec196-151">An ASCII string that uniquely identifies the variable name.</span></span><br/>                 |
| <span data-ttu-id="ec196-152"><span id="SubobjectName"></span><span id="subobjectname"></span><span id="SUBOBJECTNAME"></span>**Subobjectname**</span><span class="sxs-lookup"><span data-stu-id="ec196-152"><span id="SubobjectName"></span><span id="subobjectname"></span><span id="SUBOBJECTNAME"></span>**SubobjectName**</span></span><br/>     | <span data-ttu-id="ec196-153">Cadeia de caracteres que identifica um subobjeto exportado.</span><span class="sxs-lookup"><span data-stu-id="ec196-153">String which identifies an exported subobject.</span></span><br/> |
| <span data-ttu-id="ec196-154"><span id="Exports"></span><span id="exports"></span><span id="EXPORTS"></span>**Port**</span><span class="sxs-lookup"><span data-stu-id="ec196-154"><span id="Exports"></span><span id="exports"></span><span id="EXPORTS"></span>**Exports**</span></span><br/> | <span data-ttu-id="ec196-155">Cadeia de caracteres que contém uma lista delimitada por ponto e vírgula de exportações.</span><span class="sxs-lookup"><span data-stu-id="ec196-155">String containing a semicolon-delimited list of exports.</span></span><br/> |


<span data-ttu-id="ec196-156">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="ec196-156">Example:</span></span>
```
SubobjectToExportsAssociation MyLocalRootSignatureAssociation =
{
    "MyLocalRootSignature",    // Subobject name
    "MyHitGroup;MyMissShader"  // Exports association 
};
```

<span data-ttu-id="ec196-157">Observe que os dois campos usam nomes *exportados* .</span><span class="sxs-lookup"><span data-stu-id="ec196-157">Note that both fields use *exported* names.</span></span> <span data-ttu-id="ec196-158">Um nome exportado pode ser diferente do nome original em HLSL, se o aplicativo optar por fazer a exportação e renomear.</span><span class="sxs-lookup"><span data-stu-id="ec196-158">An exported name may be different from the original name in HLSL, if the application chooses to do export-renaming.</span></span>

## <a name="raytracingshaderconfig"></a><span data-ttu-id="ec196-159">RaytracingShaderConfig</span><span class="sxs-lookup"><span data-stu-id="ec196-159">RaytracingShaderConfig</span></span>

<span data-ttu-id="ec196-160">Um RaytracingShaderConfig corresponde a uma estrutura de [D3D12_RAYTRACING_SHADER_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_shader_config) .</span><span class="sxs-lookup"><span data-stu-id="ec196-160">A RaytracingShaderConfig corresponds to a [D3D12_RAYTRACING_SHADER_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_shader_config) structure.</span></span>

<span data-ttu-id="ec196-161">Este subobjeto é declarado com a sintaxe</span><span class="sxs-lookup"><span data-stu-id="ec196-161">This subobject is declared with the syntax</span></span>

``` syntax
RaytracingShaderConfig Name = 
{ 
    MaxPayloadSize,
    MaxAttributeSize
};
```

| <span data-ttu-id="ec196-162">Item</span><span class="sxs-lookup"><span data-stu-id="ec196-162">Item</span></span>                                                                                         | <span data-ttu-id="ec196-163">Descrição</span><span class="sxs-lookup"><span data-stu-id="ec196-163">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec196-164"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nomes**</span><span class="sxs-lookup"><span data-stu-id="ec196-164"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>     | <span data-ttu-id="ec196-165">Uma cadeia de caracteres ASCII que identifica exclusivamente o nome da variável.</span><span class="sxs-lookup"><span data-stu-id="ec196-165">An ASCII string that uniquely identifies the variable name.</span></span><br/>                 |
| <span data-ttu-id="ec196-166"><span id="MaxPayloadSize"></span><span id="maxpayloadsize"></span><span id="MAXPAYLOADSIZE"></span>**MaxPayloadSize**</span><span class="sxs-lookup"><span data-stu-id="ec196-166"><span id="MaxPayloadSize"></span><span id="maxpayloadsize"></span><span id="MAXPAYLOADSIZE"></span>**MaxPayloadSize**</span></span><br/>     | <span data-ttu-id="ec196-167">Valor numérico para o armazenamento máximo de escalares (contado como 4 bytes cada) em Ray payloads para sombreadores raytracing associados.</span><span class="sxs-lookup"><span data-stu-id="ec196-167">Numerical value for the maximum storage for scalars (counted as 4 bytes each) in ray payloads for associated raytracing shaders.</span></span><br/> |
| <span data-ttu-id="ec196-168"><span id="MaxAttributeSize"></span><span id="maxattributesize"></span><span id="MAXATTRIBUTESIZE"></span>**MaxAttributeSize**</span><span class="sxs-lookup"><span data-stu-id="ec196-168"><span id="MaxAttributeSize"></span><span id="maxattributesize"></span><span id="MAXATTRIBUTESIZE"></span>**MaxAttributeSize**</span></span><br/> | <span data-ttu-id="ec196-169">Valor numérico para o número máximo de escalares (contado como 4 bytes cada) que pode ser usado para atributos em sombreadores raytracing associados.</span><span class="sxs-lookup"><span data-stu-id="ec196-169">Numerical value for the maximum number of scalars (counted as 4 bytes each) that can be used for attributes in associated raytracing shaders.</span></span> <span data-ttu-id="ec196-170">O valor não pode exceder [D3D12_RAYTRACING_MAX_ATTRIBUTE_SIZE_IN_BYTES](../direct3d12/constants.md).</span><span class="sxs-lookup"><span data-stu-id="ec196-170">The value cannot exceed [D3D12_RAYTRACING_MAX_ATTRIBUTE_SIZE_IN_BYTES](../direct3d12/constants.md).</span></span><br/> |


<span data-ttu-id="ec196-171">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="ec196-171">Example:</span></span>
```
RaytracingShaderConfig MyShaderConfig =
{
    16,  // Max payload size
    8    // Max attribute size
};
```

## <a name="raytracingpipelineconfig"></a><span data-ttu-id="ec196-172">RaytracingPipelineConfig</span><span class="sxs-lookup"><span data-stu-id="ec196-172">RaytracingPipelineConfig</span></span>

<span data-ttu-id="ec196-173">Um RaytracingPipelineConfig corresponde a uma estrutura de [D3D12_RAYTRACING_PIPELINE_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_pipeline_config) .</span><span class="sxs-lookup"><span data-stu-id="ec196-173">A RaytracingPipelineConfig corresponds to a [D3D12_RAYTRACING_PIPELINE_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_pipeline_config) structure.</span></span>

<span data-ttu-id="ec196-174">Este subobjeto é declarado com a sintaxe</span><span class="sxs-lookup"><span data-stu-id="ec196-174">This subobject is declared with the syntax</span></span>

``` syntax
RaytracingPipelineConfig Name = 
{ 
    MaxTraceRecursionDepth
};
```

| <span data-ttu-id="ec196-175">Item</span><span class="sxs-lookup"><span data-stu-id="ec196-175">Item</span></span>                                                                                         | <span data-ttu-id="ec196-176">Descrição</span><span class="sxs-lookup"><span data-stu-id="ec196-176">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec196-177"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nomes**</span><span class="sxs-lookup"><span data-stu-id="ec196-177"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>     | <span data-ttu-id="ec196-178">Uma cadeia de caracteres ASCII que identifica exclusivamente o nome da variável.</span><span class="sxs-lookup"><span data-stu-id="ec196-178">An ASCII string that uniquely identifies the variable name.</span></span><br/>                 |
| <span data-ttu-id="ec196-179"><span id="MaxTraceRecursionDepth"></span><span id="maxtracerecursiondepth"></span><span id="MAXTRACERECURSIONDEPTH"></span>**MaxTraceRecursionDepth**</span><span class="sxs-lookup"><span data-stu-id="ec196-179"><span id="MaxTraceRecursionDepth"></span><span id="maxtracerecursiondepth"></span><span id="MAXTRACERECURSIONDEPTH"></span>**MaxTraceRecursionDepth**</span></span><br/>     | <span data-ttu-id="ec196-180">Limite numérico a ser usado para Ray recursão no pipeline raytracing.</span><span class="sxs-lookup"><span data-stu-id="ec196-180">Numerical limit to use for ray recursion in the raytracing pipeline.</span></span> <span data-ttu-id="ec196-181">É um número entre 0 e 31, inclusive.</span><span class="sxs-lookup"><span data-stu-id="ec196-181">It is a number between 0 and 31, inclusive.</span></span> <br/> |


<span data-ttu-id="ec196-182">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="ec196-182">Example:</span></span>
```
RaytracingPipelineConfig MyPipelineConfig =
{
    1  // Max trace recursion depth
};
```
<span data-ttu-id="ec196-183">Como há um custo de desempenho para recursão de raytracing, os aplicativos devem usar a profundidade de recursão mais baixa necessária para os resultados desejados.</span><span class="sxs-lookup"><span data-stu-id="ec196-183">Since there is a performance cost to raytracing recursion, applications should use the lowest recursion depth needed for the desired results.</span></span>

<span data-ttu-id="ec196-184">Se as invocações do sombreador ainda não atingiram a profundidade máxima de recursão, elas poderão chamar [TraceRay](../direct3d12/traceray-function.md) várias vezes.</span><span class="sxs-lookup"><span data-stu-id="ec196-184">If shader invocations haven't yet reached the maximum recursion depth, they can call [TraceRay](../direct3d12/traceray-function.md) any number of times.</span></span> <span data-ttu-id="ec196-185">Mas se eles atingirem ou excederem a profundidade máxima de recursão, chamar TraceRay colocará o dispositivo em estado removido.</span><span class="sxs-lookup"><span data-stu-id="ec196-185">But if they reach or exceed the maximum recursion depth, calling TraceRay puts the device into removed state.</span></span> <span data-ttu-id="ec196-186">Portanto, os sombreadores raytracing devem tomar cuidado para parar de chamar TraceRay se atingiram ou excederam a profundidade máxima de recursão.</span><span class="sxs-lookup"><span data-stu-id="ec196-186">Therefore, raytracing shaders should take care to stop calling TraceRay if they've met or exceeded the maximum recursion depth.</span></span>

## <a name="trianglehitgroup"></a><span data-ttu-id="ec196-187">TriangleHitGroup</span><span class="sxs-lookup"><span data-stu-id="ec196-187">TriangleHitGroup</span></span>

<span data-ttu-id="ec196-188">Um TriangleHitGroup corresponde a uma estrutura de [D3D12_HIT_GROUP_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_hit_group_desc) cujo campo de tipo está definido como [D3D12_HIT_GROUP_TYPE_TRIANGLES](/windows/win32/api/d3d12/ne-d3d12-d3d12_hit_group_type#constants).</span><span class="sxs-lookup"><span data-stu-id="ec196-188">A TriangleHitGroup corresponds to a [D3D12_HIT_GROUP_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_hit_group_desc) structure whose Type field is set to [D3D12_HIT_GROUP_TYPE_TRIANGLES](/windows/win32/api/d3d12/ne-d3d12-d3d12_hit_group_type#constants).</span></span>

<span data-ttu-id="ec196-189">Este subobjeto é declarado com a sintaxe</span><span class="sxs-lookup"><span data-stu-id="ec196-189">This subobject is declared with the syntax</span></span>

``` syntax
TriangleHitGroup Name = 
{ 
    AnyHitShader,
    ClosestHitShader
};
```

| <span data-ttu-id="ec196-190">Item</span><span class="sxs-lookup"><span data-stu-id="ec196-190">Item</span></span>                                                                                         | <span data-ttu-id="ec196-191">Descrição</span><span class="sxs-lookup"><span data-stu-id="ec196-191">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec196-192"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nomes**</span><span class="sxs-lookup"><span data-stu-id="ec196-192"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>     | <span data-ttu-id="ec196-193">Uma cadeia de caracteres ASCII que identifica exclusivamente o nome da variável.</span><span class="sxs-lookup"><span data-stu-id="ec196-193">An ASCII string that uniquely identifies the variable name.</span></span><br/>                 |
| <span data-ttu-id="ec196-194"><span id="AnyHitShader"></span><span id="anyhitshader"></span><span id="ANYHITSHADER"></span>**AnyHitShader**</span><span class="sxs-lookup"><span data-stu-id="ec196-194"><span id="AnyHitShader"></span><span id="anyhitshader"></span><span id="ANYHITSHADER"></span>**AnyHitShader**</span></span><br/>     | <span data-ttu-id="ec196-195">Nome da cadeia de caracteres do sombreador anyhit para o grupo de acesso ou uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="ec196-195">String name of the anyhit shader for the hit group, or an empty string.</span></span><br/> |
| <span data-ttu-id="ec196-196"><span id="ClosestHitShader"></span><span id="closesthitshader"></span><span id="CLOSESTHITSHADER"></span>**ClosestHitShader**</span><span class="sxs-lookup"><span data-stu-id="ec196-196"><span id="ClosestHitShader"></span><span id="closesthitshader"></span><span id="CLOSESTHITSHADER"></span>**ClosestHitShader**</span></span><br/> | <span data-ttu-id="ec196-197">Nome da cadeia de caracteres do sombreador de clique mais próximo para o grupo de acesso ou uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="ec196-197">String name of the closest hit shader for the hit group, or an empty string.</span></span><br/> |


<span data-ttu-id="ec196-198">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="ec196-198">Example:</span></span>
```
TriangleHitGroup MyHitGroup =
{
    "",                    // AnyHit
    "MyClosestHitShader",  // ClosestHit
};
```

<span data-ttu-id="ec196-199">Observe que os dois campos usam nomes *exportados* .</span><span class="sxs-lookup"><span data-stu-id="ec196-199">Note that both fields use *exported* names.</span></span> <span data-ttu-id="ec196-200">Um nome exportado pode ser diferente do nome original em HLSL, se o aplicativo optar por fazer a exportação e renomear.</span><span class="sxs-lookup"><span data-stu-id="ec196-200">An exported name may be different from the original name in HLSL, if the application chooses to do export-renaming.</span></span>

## <a name="proceduralprimitivehitgroup"></a><span data-ttu-id="ec196-201">ProceduralPrimitiveHitGroup</span><span class="sxs-lookup"><span data-stu-id="ec196-201">ProceduralPrimitiveHitGroup</span></span>

<span data-ttu-id="ec196-202">Um ProceduralPrimitiveHitGroup corresponde a uma estrutura de [D3D12_HIT_GROUP_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_hit_group_desc) cujo campo de tipo está definido como [D3D12_HIT_GROUP_TYPE_PROCEDURAL_PRIMITIVE](/windows/win32/api/d3d12/ne-d3d12-d3d12_hit_group_type#constants).</span><span class="sxs-lookup"><span data-stu-id="ec196-202">A ProceduralPrimitiveHitGroup corresponds to a [D3D12_HIT_GROUP_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_hit_group_desc) structure whose Type field is set to [D3D12_HIT_GROUP_TYPE_PROCEDURAL_PRIMITIVE](/windows/win32/api/d3d12/ne-d3d12-d3d12_hit_group_type#constants).</span></span>

<span data-ttu-id="ec196-203">Este subobjeto é declarado com a sintaxe</span><span class="sxs-lookup"><span data-stu-id="ec196-203">This subobject is declared with the syntax</span></span>

``` syntax
ProceduralPrimitiveHitGroup Name = 
{ 
    AnyHitShader,
    ClosestHitShader,
    IntersectionShader
};
```

| <span data-ttu-id="ec196-204">Item</span><span class="sxs-lookup"><span data-stu-id="ec196-204">Item</span></span>                                                                                         | <span data-ttu-id="ec196-205">Descrição</span><span class="sxs-lookup"><span data-stu-id="ec196-205">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec196-206"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nomes**</span><span class="sxs-lookup"><span data-stu-id="ec196-206"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>     | <span data-ttu-id="ec196-207">Uma cadeia de caracteres ASCII que identifica exclusivamente o nome da variável.</span><span class="sxs-lookup"><span data-stu-id="ec196-207">An ASCII string that uniquely identifies the variable name.</span></span><br/>                 |
| <span data-ttu-id="ec196-208"><span id="AnyHitShader"></span><span id="anyhitshader"></span><span id="ANYHITSHADER"></span>**AnyHitShader**</span><span class="sxs-lookup"><span data-stu-id="ec196-208"><span id="AnyHitShader"></span><span id="anyhitshader"></span><span id="ANYHITSHADER"></span>**AnyHitShader**</span></span><br/>     | <span data-ttu-id="ec196-209">Nome da cadeia de caracteres do sombreador anyhit para o grupo de acesso ou uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="ec196-209">String name of the anyhit shader for the hit group, or an empty string.</span></span><br/> |
| <span data-ttu-id="ec196-210"><span id="ClosestHitShader"></span><span id="closesthitshader"></span><span id="CLOSESTHITSHADER"></span>**ClosestHitShader**</span><span class="sxs-lookup"><span data-stu-id="ec196-210"><span id="ClosestHitShader"></span><span id="closesthitshader"></span><span id="CLOSESTHITSHADER"></span>**ClosestHitShader**</span></span><br/> | <span data-ttu-id="ec196-211">Nome da cadeia de caracteres do sombreador de clique mais próximo para o grupo de acesso ou uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="ec196-211">String name of the closest hit shader for the hit group, or an empty string.</span></span><br/> |
| <span data-ttu-id="ec196-212"><span id="IntersectionShader"></span><span id="intersectionshader"></span><span id="INTERSECTIONSHADER"></span>**IntersectionShader**</span><span class="sxs-lookup"><span data-stu-id="ec196-212"><span id="IntersectionShader"></span><span id="intersectionshader"></span><span id="INTERSECTIONSHADER"></span>**IntersectionShader**</span></span><br/> | <span data-ttu-id="ec196-213">Nome da cadeia de caracteres do sombreador de interseção para o grupo de acesso ou uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="ec196-213">String name of the intersection shader for the hit group, or an empty string.</span></span><br/> |


<span data-ttu-id="ec196-214">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="ec196-214">Example:</span></span>
```
ProceduralPrimitiveHitGroup MyProceduralHitGroup
{
    "MyAnyHit",       // AnyHit
    "MyClosestHit",   // ClosestHit
    "MyIntersection"  // Intersection
};

```

<span data-ttu-id="ec196-215">Observe que os três campos usam nomes *exportados* .</span><span class="sxs-lookup"><span data-stu-id="ec196-215">Note that the three fields use *exported* names.</span></span> <span data-ttu-id="ec196-216">Um nome exportado pode ser diferente do nome original em HLSL, se o aplicativo optar por fazer a exportação e renomear.</span><span class="sxs-lookup"><span data-stu-id="ec196-216">An exported name may be different from the original name in HLSL, if the application chooses to do export-renaming.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec196-217">Comentários</span><span class="sxs-lookup"><span data-stu-id="ec196-217">Remarks</span></span>

<span data-ttu-id="ec196-218">Os subobjetos têm a noção de "Associação" ou "qual subobjeto é inserido com o qual exportar".</span><span class="sxs-lookup"><span data-stu-id="ec196-218">Subobjects have the notion of "association", or "which subobject goes with which export".</span></span>

<span data-ttu-id="ec196-219">Ao especificar subobjetos por meio do código do sombreador, a escolha de "qual subobjeto é exibido com o qual exportar" segue as regras, conforme descrito na [especificação DXR](https://microsoft.github.io/DirectX-Specs/d3d/Raytracing.html#subobject-association-behavior).</span><span class="sxs-lookup"><span data-stu-id="ec196-219">When specifying subobjects through shader code, the choice of "which subobject goes with which export" follows the rules as outlined in the [DXR specification](https://microsoft.github.io/DirectX-Specs/d3d/Raytracing.html#subobject-association-behavior).</span></span> <span data-ttu-id="ec196-220">Em particular, suponha que um aplicativo tenha alguma exportação.</span><span class="sxs-lookup"><span data-stu-id="ec196-220">In particular, suppose an application has some export.</span></span> <span data-ttu-id="ec196-221">Se um aplicativo associar essa exportação com a assinatura raiz A por meio do código do sombreador e da assinatura raiz B por meio do código do aplicativo, B será o que é usado.</span><span class="sxs-lookup"><span data-stu-id="ec196-221">If an application associates that export with root signature A through shader-code and root signature B through application code, B is the one that gets used.</span></span> <span data-ttu-id="ec196-222">O design de "uso B" em vez de "produzir um erro" fornece aos aplicativos a capacidade de substituir de forma conveniente as associações de DXIL usando o código do aplicativo, em vez de ser forçado a recompilar os sombreadores para resolver as coisas que não correspondem.</span><span class="sxs-lookup"><span data-stu-id="ec196-222">The design of "use B" instead of "produce an error" gives applications the ability to conveniently override DXIL associations using application code, rather than be forced to recompile shaders to resolve mismatching things.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ec196-223">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ec196-223">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec196-224">A postagem do blog do DirectX Developer "novidade no D3D12 – DirectX raytracing (DXR) agora é compatível com subobjetos de biblioteca"</span><span class="sxs-lookup"><span data-stu-id="ec196-224">DirectX Developer Blog post "New in D3D12 – DirectX Raytracing (DXR) now supports library subobjects"</span></span>](https://devblogs.microsoft.com/directx/dxr-library-subobjects/)

[<span data-ttu-id="ec196-225">Especificação funcional do DirectX raytracing (DXR)</span><span class="sxs-lookup"><span data-stu-id="ec196-225">DirectX Raytracing (DXR) Functional Spec</span></span>](https://microsoft.github.io/DirectX-Specs/d3d/Raytracing.html)

[<span data-ttu-id="ec196-226">Exemplo: D3D12RaytracingLibrarySubobjects</span><span class="sxs-lookup"><span data-stu-id="ec196-226">Sample: D3D12RaytracingLibrarySubobjects</span></span>](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/develop/Samples/Desktop/D3D12Raytracing/src/D3D12RaytracingLibrarySubobjects)

</dt> </dl>