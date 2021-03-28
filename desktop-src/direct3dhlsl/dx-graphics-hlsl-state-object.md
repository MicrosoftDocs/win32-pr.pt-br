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
# <a name="state-objects"></a>Objetos de estado

Com os modelos de sombreador 6,3 e posteriores, os aplicativos têm a conveniência e a flexibilidade de poder definir objetos de estado DXR diretamente no código do sombreador HLSL, além de usar as APIs do Direct3D 12.

No HLSL, os objetos de estado são declarados com essa sintaxe:

``` syntax
Type Name = 
{ 
    Field1,
    Field2,
    ...
};
```



| Item                                                                                         | Descrição                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Escreva**<br/>     | Identifica o tipo de subobjeto. Deve ser um dos tipos de subobjeto HLSL com suporte.<br/>     |
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nomes**<br/>     | Uma cadeia de caracteres ASCII que identifica exclusivamente o nome da variável.<br/>                 |
| <span id="Field"></span><span id="field"></span><span id="FIELD"></span>**Campo [1, 2,...]**<br/> | Campos do subobjeto. Os campos específicos para cada tipo de subobjeto são descritos abaixo.<br/> |




Lista de tipos de subobjetos:
-   [StateObjectConfig](#stateobjectconfig)
-   [GlobalRootSignature](#globalrootsignature)
-   [LocalRootSignature](#localrootsignature)
-   [SubobjectToExportsAssocation](#subobjecttoexportsassocation)
-   [RaytracingShaderConfig](#raytracingshaderconfig)
-   [RaytracingPipelineConfig](#raytracingpipelineconfig)
-   [TriangleHitGroup](#trianglehitgroup)
-   [ProceduralPrimitiveHitGroup](#proceduralprimitivehitgroup)

## <a name="stateobjectconfig"></a>StateObjectConfig

O tipo de subobjeto StateObjectConfig corresponde a uma estrutura [D3D12_STATE_OBJECT_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_object_config) .

Ele tem um campo, um sinalizador de bit, que é um ou ambos

* STATE_OBJECT_FLAGS_ALLOW_LOCAL_DEPENDENCIES_ON_EXTERNAL_DEFINITONS
* STATE_OBJECT_FLAGS_ALLOW_EXTERNAL_DEPENDENCIES_ON_LOCAL_DEFINITIONS

ou zero para nenhum deles.

Exemplo:

```
StateObjectConfig MyStateObjectConfig = 
{ 
    STATE_OBJECT_FLAGS_ALLOW_LOCAL_DEPENDENCIES_ON_EXTERNAL_DEFINITONS
};
```

## <a name="globalrootsignature"></a>GlobalRootSignature
Um GlobalRootSignature corresponde a uma estrutura de [D3D12_GLOBAL_ROOT_SIGNATURE](/windows/win32/api/d3d12/ns-d3d12-d3d12_global_root_signature) .

Os campos consistem em um número de cadeias de caracteres que descrevem as partes da assinatura raiz. Para referência sobre isso, consulte [especificando assinaturas raiz no HLSL](../direct3d12/specifying-root-signatures-in-hlsl.md).

Exemplo:
```
GlobalRootSignature MyGlobalRootSignature =
{
    "DescriptorTable(UAV(u0)),"                     // Output texture
    "SRV(t0),"                                      // Acceleration structure
    "CBV(b0),"                                      // Scene constants
    "DescriptorTable(SRV(t1, numDescriptors = 2))"  // Static index and vertex buffers.
};
```

## <a name="localrootsignature"></a>LocalRootSignature
Um LocalRootSignature corresponde a uma estrutura de [D3D12_LOCAL_ROOT_SIGNATURE](/windows/win32/api/d3d12/ns-d3d12-d3d12_local_root_signature) .

Assim como o subobjeto de assinatura de raiz global, os campos consistem em algum número de cadeias de caracteres que descrevem as partes da assinatura raiz. Para referência sobre isso, consulte [especificando assinaturas raiz no HLSL](../direct3d12/specifying-root-signatures-in-hlsl.md).

Exemplo:
```
LocalRootSignature MyLocalRootSignature = 
{
    "RootConstants(num32BitConstants = 4, b1)"  // Cube constants 
};
```

## <a name="subobjecttoexportsassocation"></a>SubobjectToExportsAssocation
Por padrão, um subobjeto meramente declarado na mesma biblioteca como uma exportação é capaz de aplicar a essa exportação. No entanto, os aplicativos têm a capacidade de substituí-lo e obter informações específicas sobre qual subobjeto é capaz de exportar. No HLSL, essa "Associação explícita" é feita usando SubobjectToExportsAssocation.

Um SubobjectToExportsAssocation corresponde a uma estrutura de [D3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION ](/windows/win32/api/d3d12/ns-d3d12-d3d12_dxil_subobject_to_exports_association) .

Este subobjeto é declarado com a sintaxe

``` syntax
SubobjectToExportsAssocation Name = 
{ 
    SubobjectName,
    Exports
};
```

| Item                                                                                         | Descrição                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nomes**<br/>     | Uma cadeia de caracteres ASCII que identifica exclusivamente o nome da variável.<br/>                 |
| <span id="SubobjectName"></span><span id="subobjectname"></span><span id="SUBOBJECTNAME"></span>**Subobjectname**<br/>     | Cadeia de caracteres que identifica um subobjeto exportado.<br/> |
| <span id="Exports"></span><span id="exports"></span><span id="EXPORTS"></span>**Port**<br/> | Cadeia de caracteres que contém uma lista delimitada por ponto e vírgula de exportações.<br/> |


Exemplo:
```
SubobjectToExportsAssociation MyLocalRootSignatureAssociation =
{
    "MyLocalRootSignature",    // Subobject name
    "MyHitGroup;MyMissShader"  // Exports association 
};
```

Observe que os dois campos usam nomes *exportados* . Um nome exportado pode ser diferente do nome original em HLSL, se o aplicativo optar por fazer a exportação e renomear.

## <a name="raytracingshaderconfig"></a>RaytracingShaderConfig

Um RaytracingShaderConfig corresponde a uma estrutura de [D3D12_RAYTRACING_SHADER_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_shader_config) .

Este subobjeto é declarado com a sintaxe

``` syntax
RaytracingShaderConfig Name = 
{ 
    MaxPayloadSize,
    MaxAttributeSize
};
```

| Item                                                                                         | Descrição                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nomes**<br/>     | Uma cadeia de caracteres ASCII que identifica exclusivamente o nome da variável.<br/>                 |
| <span id="MaxPayloadSize"></span><span id="maxpayloadsize"></span><span id="MAXPAYLOADSIZE"></span>**MaxPayloadSize**<br/>     | Valor numérico para o armazenamento máximo de escalares (contado como 4 bytes cada) em Ray payloads para sombreadores raytracing associados.<br/> |
| <span id="MaxAttributeSize"></span><span id="maxattributesize"></span><span id="MAXATTRIBUTESIZE"></span>**MaxAttributeSize**<br/> | Valor numérico para o número máximo de escalares (contado como 4 bytes cada) que pode ser usado para atributos em sombreadores raytracing associados. O valor não pode exceder [D3D12_RAYTRACING_MAX_ATTRIBUTE_SIZE_IN_BYTES](../direct3d12/constants.md).<br/> |


Exemplo:
```
RaytracingShaderConfig MyShaderConfig =
{
    16,  // Max payload size
    8    // Max attribute size
};
```

## <a name="raytracingpipelineconfig"></a>RaytracingPipelineConfig

Um RaytracingPipelineConfig corresponde a uma estrutura de [D3D12_RAYTRACING_PIPELINE_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_pipeline_config) .

Este subobjeto é declarado com a sintaxe

``` syntax
RaytracingPipelineConfig Name = 
{ 
    MaxTraceRecursionDepth
};
```

| Item                                                                                         | Descrição                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nomes**<br/>     | Uma cadeia de caracteres ASCII que identifica exclusivamente o nome da variável.<br/>                 |
| <span id="MaxTraceRecursionDepth"></span><span id="maxtracerecursiondepth"></span><span id="MAXTRACERECURSIONDEPTH"></span>**MaxTraceRecursionDepth**<br/>     | Limite numérico a ser usado para Ray recursão no pipeline raytracing. É um número entre 0 e 31, inclusive. <br/> |


Exemplo:
```
RaytracingPipelineConfig MyPipelineConfig =
{
    1  // Max trace recursion depth
};
```
Como há um custo de desempenho para recursão de raytracing, os aplicativos devem usar a profundidade de recursão mais baixa necessária para os resultados desejados.

Se as invocações do sombreador ainda não atingiram a profundidade máxima de recursão, elas poderão chamar [TraceRay](../direct3d12/traceray-function.md) várias vezes. Mas se eles atingirem ou excederem a profundidade máxima de recursão, chamar TraceRay colocará o dispositivo em estado removido. Portanto, os sombreadores raytracing devem tomar cuidado para parar de chamar TraceRay se atingiram ou excederam a profundidade máxima de recursão.

## <a name="trianglehitgroup"></a>TriangleHitGroup

Um TriangleHitGroup corresponde a uma estrutura de [D3D12_HIT_GROUP_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_hit_group_desc) cujo campo de tipo está definido como [D3D12_HIT_GROUP_TYPE_TRIANGLES](/windows/win32/api/d3d12/ne-d3d12-d3d12_hit_group_type#constants).

Este subobjeto é declarado com a sintaxe

``` syntax
TriangleHitGroup Name = 
{ 
    AnyHitShader,
    ClosestHitShader
};
```

| Item                                                                                         | Descrição                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nomes**<br/>     | Uma cadeia de caracteres ASCII que identifica exclusivamente o nome da variável.<br/>                 |
| <span id="AnyHitShader"></span><span id="anyhitshader"></span><span id="ANYHITSHADER"></span>**AnyHitShader**<br/>     | Nome da cadeia de caracteres do sombreador anyhit para o grupo de acesso ou uma cadeia de caracteres vazia.<br/> |
| <span id="ClosestHitShader"></span><span id="closesthitshader"></span><span id="CLOSESTHITSHADER"></span>**ClosestHitShader**<br/> | Nome da cadeia de caracteres do sombreador de clique mais próximo para o grupo de acesso ou uma cadeia de caracteres vazia.<br/> |


Exemplo:
```
TriangleHitGroup MyHitGroup =
{
    "",                    // AnyHit
    "MyClosestHitShader",  // ClosestHit
};
```

Observe que os dois campos usam nomes *exportados* . Um nome exportado pode ser diferente do nome original em HLSL, se o aplicativo optar por fazer a exportação e renomear.

## <a name="proceduralprimitivehitgroup"></a>ProceduralPrimitiveHitGroup

Um ProceduralPrimitiveHitGroup corresponde a uma estrutura de [D3D12_HIT_GROUP_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_hit_group_desc) cujo campo de tipo está definido como [D3D12_HIT_GROUP_TYPE_PROCEDURAL_PRIMITIVE](/windows/win32/api/d3d12/ne-d3d12-d3d12_hit_group_type#constants).

Este subobjeto é declarado com a sintaxe

``` syntax
ProceduralPrimitiveHitGroup Name = 
{ 
    AnyHitShader,
    ClosestHitShader,
    IntersectionShader
};
```

| Item                                                                                         | Descrição                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nomes**<br/>     | Uma cadeia de caracteres ASCII que identifica exclusivamente o nome da variável.<br/>                 |
| <span id="AnyHitShader"></span><span id="anyhitshader"></span><span id="ANYHITSHADER"></span>**AnyHitShader**<br/>     | Nome da cadeia de caracteres do sombreador anyhit para o grupo de acesso ou uma cadeia de caracteres vazia.<br/> |
| <span id="ClosestHitShader"></span><span id="closesthitshader"></span><span id="CLOSESTHITSHADER"></span>**ClosestHitShader**<br/> | Nome da cadeia de caracteres do sombreador de clique mais próximo para o grupo de acesso ou uma cadeia de caracteres vazia.<br/> |
| <span id="IntersectionShader"></span><span id="intersectionshader"></span><span id="INTERSECTIONSHADER"></span>**IntersectionShader**<br/> | Nome da cadeia de caracteres do sombreador de interseção para o grupo de acesso ou uma cadeia de caracteres vazia.<br/> |


Exemplo:
```
ProceduralPrimitiveHitGroup MyProceduralHitGroup
{
    "MyAnyHit",       // AnyHit
    "MyClosestHit",   // ClosestHit
    "MyIntersection"  // Intersection
};

```

Observe que os três campos usam nomes *exportados* . Um nome exportado pode ser diferente do nome original em HLSL, se o aplicativo optar por fazer a exportação e renomear.

## <a name="remarks"></a>Comentários

Os subobjetos têm a noção de "Associação" ou "qual subobjeto é inserido com o qual exportar".

Ao especificar subobjetos por meio do código do sombreador, a escolha de "qual subobjeto é exibido com o qual exportar" segue as regras, conforme descrito na [especificação DXR](https://microsoft.github.io/DirectX-Specs/d3d/Raytracing.html#subobject-association-behavior). Em particular, suponha que um aplicativo tenha alguma exportação. Se um aplicativo associar essa exportação com a assinatura raiz A por meio do código do sombreador e da assinatura raiz B por meio do código do aplicativo, B será o que é usado. O design de "uso B" em vez de "produzir um erro" fornece aos aplicativos a capacidade de substituir de forma conveniente as associações de DXIL usando o código do aplicativo, em vez de ser forçado a recompilar os sombreadores para resolver as coisas que não correspondem.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[A postagem do blog do DirectX Developer "novidade no D3D12 – DirectX raytracing (DXR) agora é compatível com subobjetos de biblioteca"](https://devblogs.microsoft.com/directx/dxr-library-subobjects/)

[Especificação funcional do DirectX raytracing (DXR)](https://microsoft.github.io/DirectX-Specs/d3d/Raytracing.html)

[Exemplo: D3D12RaytracingLibrarySubobjects](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/develop/Samples/Desktop/D3D12Raytracing/src/D3D12RaytracingLibrarySubobjects)

</dt> </dl>