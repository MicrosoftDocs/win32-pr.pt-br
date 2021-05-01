---
title: Como criar uma assinatura raiz
description: As assinaturas raiz são uma estrutura de dados complexa que contém estruturas aninhadas.
ms.assetid: 565B28C1-DBD1-42B6-87F9-70743E4A2E4A
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3705f4e1a0a88841560d67d5904e0f1b5dabd3f8
ms.sourcegitcommit: a0cb986d5694b69d4a65b7d42a22694d02a6e83a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/30/2021
ms.locfileid: "108296331"
---
# <a name="creating-a-root-signature"></a><span data-ttu-id="d5b51-103">Como criar uma assinatura raiz</span><span class="sxs-lookup"><span data-stu-id="d5b51-103">Creating a Root Signature</span></span>

<span data-ttu-id="d5b51-104">As assinaturas raiz são uma estrutura de dados complexa que contém estruturas aninhadas.</span><span class="sxs-lookup"><span data-stu-id="d5b51-104">Root signatures are a complex data structure containing nested structures.</span></span> <span data-ttu-id="d5b51-105">Eles podem ser definidos programaticamente usando a definição de estrutura de dados abaixo (que inclui métodos para ajudar a inicializar Membros).</span><span class="sxs-lookup"><span data-stu-id="d5b51-105">These can be defined programmatically using the data structure definition below (which includes methods to help initialize members).</span></span> <span data-ttu-id="d5b51-106">Como alternativa, eles podem ser criados na HLSL (linguagem de sombreamento de alto nível), dando a vantagem de que o compilador será validado antes que o layout seja compatível com o sombreador.</span><span class="sxs-lookup"><span data-stu-id="d5b51-106">Alternatively, they can be authored in High Level Shading Language (HLSL) – giving the advantage that the compiler will validate early that the layout is compatible with the shader.</span></span>

<span data-ttu-id="d5b51-107">A API para criar uma assinatura raiz usa uma versão serializada (autocontida, ponteiro livre) da descrição do layout descrita abaixo.</span><span class="sxs-lookup"><span data-stu-id="d5b51-107">The API for creating a root signature takes in a serialized (self contained, pointer free) version of the layout description described below.</span></span> <span data-ttu-id="d5b51-108">Um método é fornecido para gerar essa versão serializada da estrutura de dados do C++, mas outra maneira de obter uma definição de assinatura raiz serializada é recuperá-la de um sombreador que foi compilado com uma assinatura raiz.</span><span class="sxs-lookup"><span data-stu-id="d5b51-108">A method is provided for generating this serialized version from the C++ data structure, but another way to obtain a serialized root signature definition is to retrieve it from a shader that has been compiled with a root signature.</span></span>

<span data-ttu-id="d5b51-109">Se você quiser tirar proveito das otimizações de driver para os dados e descritores de assinatura raiz, consulte a [assinatura raiz versão 1,1](root-signature-version-1-1.md)</span><span class="sxs-lookup"><span data-stu-id="d5b51-109">If you wish to take advantage of driver optimizations for root signature descriptors and data, refer to [Root Signature Version 1.1](root-signature-version-1-1.md)</span></span>

-   [<span data-ttu-id="d5b51-110">Tipos de associação de tabela de descritores</span><span class="sxs-lookup"><span data-stu-id="d5b51-110">Descriptor Table Bind Types</span></span>](#descriptor-table-bind-types)
-   [<span data-ttu-id="d5b51-111">Intervalo de descritores</span><span class="sxs-lookup"><span data-stu-id="d5b51-111">Descriptor Range</span></span>](#descriptor-range)
-   [<span data-ttu-id="d5b51-112">Layout da tabela de descritores</span><span class="sxs-lookup"><span data-stu-id="d5b51-112">Descriptor Table Layout</span></span>](#descriptor-table-layout)
-   [<span data-ttu-id="d5b51-113">Constantes raiz</span><span class="sxs-lookup"><span data-stu-id="d5b51-113">Root Constants</span></span>](#root-constants)
-   [<span data-ttu-id="d5b51-114">Descritor raiz</span><span class="sxs-lookup"><span data-stu-id="d5b51-114">Root Descriptor</span></span>](#root-descriptor)
-   [<span data-ttu-id="d5b51-115">Visibilidade do sombreador</span><span class="sxs-lookup"><span data-stu-id="d5b51-115">Shader Visibility</span></span>](#shader-visibility)
-   [<span data-ttu-id="d5b51-116">Definição de assinatura raiz</span><span class="sxs-lookup"><span data-stu-id="d5b51-116">Root Signature Definition</span></span>](#root-signature-definition)
-   [<span data-ttu-id="d5b51-117">Serialização/desserialização da estrutura de dados da assinatura raiz</span><span class="sxs-lookup"><span data-stu-id="d5b51-117">Root Signature Data Structure Serialization / Deserialization</span></span>](/windows)
-   [<span data-ttu-id="d5b51-118">API de criação de assinatura raiz</span><span class="sxs-lookup"><span data-stu-id="d5b51-118">Root Signature Creation API</span></span>](#root-signature-creation-api)
-   [<span data-ttu-id="d5b51-119">Assinatura de raiz em objetos de estado do pipeline</span><span class="sxs-lookup"><span data-stu-id="d5b51-119">Root Signature in Pipeline State Objects</span></span>](#root-signature-in-pipeline-state-objects)
-   [<span data-ttu-id="d5b51-120">Código para definir uma assinatura raiz da versão 1,1</span><span class="sxs-lookup"><span data-stu-id="d5b51-120">Code for Defining a Version 1.1 Root Signature</span></span>](#code-for-defining-a-version-11-root-signature)
-   [<span data-ttu-id="d5b51-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d5b51-121">Related topics</span></span>](#related-topics)

## <a name="descriptor-table-bind-types"></a><span data-ttu-id="d5b51-122">Tipos de associação de tabela de descritores</span><span class="sxs-lookup"><span data-stu-id="d5b51-122">Descriptor Table Bind Types</span></span>

<span data-ttu-id="d5b51-123">O [**tipo de \_ \_ intervalo do \_ descritor**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) de enumeração D3D12 define os tipos de descritores que podem ser referenciados como parte de uma definição de layout de tabela de descritor.</span><span class="sxs-lookup"><span data-stu-id="d5b51-123">The enum [**D3D12\_DESCRIPTOR\_RANGE\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) defines the types of descriptors that can be referenced as part of a descriptor table layout definition.</span></span>

<span data-ttu-id="d5b51-124">É um intervalo para que, por exemplo, se parte de uma tabela de descritor tenha 100 SRVs, esse intervalo possa ser declarado em uma entrada em vez de 100.</span><span class="sxs-lookup"><span data-stu-id="d5b51-124">It is a range so that, for example if part of a descriptor table has 100 SRVs, that range can be declared in one entry rather than 100.</span></span> <span data-ttu-id="d5b51-125">Portanto, uma definição de tabela de descritor é uma coleção de intervalos.</span><span class="sxs-lookup"><span data-stu-id="d5b51-125">So a descriptor table definition is a collection of ranges.</span></span>

``` syntax
typedef enum D3D12_DESCRIPTOR_RANGE_TYPE
{
  D3D12_DESCRIPTOR_RANGE_TYPE_SRV,
  D3D12_DESCRIPTOR_RANGE_TYPE_UAV,
  D3D12_DESCRIPTOR_RANGE_TYPE_CBV,
  D3D12_DESCRIPTOR_RANGE_TYPE_SAMPLER
} D3D12_DESCRIPTOR_RANGE_TYPE;
```

## <a name="descriptor-range"></a><span data-ttu-id="d5b51-126">Intervalo de descritores</span><span class="sxs-lookup"><span data-stu-id="d5b51-126">Descriptor Range</span></span>

<span data-ttu-id="d5b51-127">A estrutura do [**\_ \_ intervalo do descritor D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) define um intervalo de descripdores de um determinado tipo (como SRVs) em uma tabela de descritores.</span><span class="sxs-lookup"><span data-stu-id="d5b51-127">The [**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) structure defines a range of descriptors of a given type (such as SRVs) within a descriptor table.</span></span>

<span data-ttu-id="d5b51-128">A `D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND` macro normalmente pode ser usada para o `OffsetInDescriptorsFromTableStart` parâmetro do [**\_ \_ intervalo do descritor D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range).</span><span class="sxs-lookup"><span data-stu-id="d5b51-128">The `D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND` macro can typically be used for the `OffsetInDescriptorsFromTableStart` parameter of [**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range).</span></span> <span data-ttu-id="d5b51-129">Isso significa acrescentar o intervalo do descritor que está sendo definido após o anterior na tabela de descritores.</span><span class="sxs-lookup"><span data-stu-id="d5b51-129">This means append the descriptor range being defined after the previous one in the descriptor table.</span></span> <span data-ttu-id="d5b51-130">Se o aplicativo quiser descritores de alias ou por algum motivo desejar ignorar os slots, ele poderá ser definido `OffsetInDescriptorsFromTableStart` para qualquer deslocamento desejado.</span><span class="sxs-lookup"><span data-stu-id="d5b51-130">If the application wants to alias descriptors or for some reason wants to skip slots, it can set `OffsetInDescriptorsFromTableStart` to whatever offset is desired.</span></span> <span data-ttu-id="d5b51-131">A definição de intervalos sobrepostos de tipos diferentes é inválida.</span><span class="sxs-lookup"><span data-stu-id="d5b51-131">Defining overlapping ranges of different types is invalid.</span></span>

<span data-ttu-id="d5b51-132">O conjunto de registros de sombreador especificado pela combinação de `RangeType` , `NumDescriptors` , `BaseShaderRegister` e `RegisterSpace` não pode entrar em conflito ou se sobrepor em quaisquer declarações em uma assinatura raiz que tenha [**\_ \_ visibilidade de sombreador D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) comum (consulte a seção de visibilidade do sombreador abaixo).</span><span class="sxs-lookup"><span data-stu-id="d5b51-132">The set of shader registers specified by the combination of `RangeType`, `NumDescriptors`, `BaseShaderRegister`, and `RegisterSpace` cannot conflict or overlap across any declarations in a root signature that have common [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) (refer to the shader visibility section below).</span></span>

## <a name="descriptor-table-layout"></a><span data-ttu-id="d5b51-133">Layout da tabela de descritores</span><span class="sxs-lookup"><span data-stu-id="d5b51-133">Descriptor Table Layout</span></span>

<span data-ttu-id="d5b51-134">A estrutura da [**\_ \_ \_ tabela do descritor raiz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) declara o layout de uma tabela de descritores como uma coleção de intervalos de descritores que aparecem um após o outro em um heap de descritor.</span><span class="sxs-lookup"><span data-stu-id="d5b51-134">The [**D3D12\_ROOT\_DESCRIPTOR\_TABLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) structure declares the layout of a descriptor table as a collection of descriptor ranges that appear one after the other in a descriptor heap.</span></span> <span data-ttu-id="d5b51-135">Os exemplos não são permitidos na mesma tabela de descritores que CBV/UAV/SRVs.</span><span class="sxs-lookup"><span data-stu-id="d5b51-135">Samplers are not allowed in the same descriptor table as CBV/UAV/SRVs.</span></span>

<span data-ttu-id="d5b51-136">Essa estrutura é usada quando o tipo de slot de assinatura raiz é definido como `D3D12_ROOT_PARAMETER_TYPE_DESCRIPTOR_TABLE` .</span><span class="sxs-lookup"><span data-stu-id="d5b51-136">This struct is used when the root signature slot type is set to `D3D12_ROOT_PARAMETER_TYPE_DESCRIPTOR_TABLE`.</span></span>

<span data-ttu-id="d5b51-137">Para definir uma tabela de descritor de gráficos (CBV, SRV, UAV, Sample), use [**ID3D12GraphicsCommandList:: SetGraphicsRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable).</span><span class="sxs-lookup"><span data-stu-id="d5b51-137">To set a graphics (CBV, SRV, UAV, Sampler) descriptor table, use [**ID3D12GraphicsCommandList::SetGraphicsRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable).</span></span>

<span data-ttu-id="d5b51-138">Para definir uma tabela de descritor de computação, use [**ID3D12GraphicsCommandList:: SetComputeRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable).</span><span class="sxs-lookup"><span data-stu-id="d5b51-138">To set a compute descriptor table, use [**ID3D12GraphicsCommandList::SetComputeRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable).</span></span>

## <a name="root-constants"></a><span data-ttu-id="d5b51-139">Constantes raiz</span><span class="sxs-lookup"><span data-stu-id="d5b51-139">Root Constants</span></span>

<span data-ttu-id="d5b51-140">A estrutura de [**\_ \_ constantes raiz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) declara constantes embutidas na assinatura raiz que aparecem em sombreadores como um buffer constante.</span><span class="sxs-lookup"><span data-stu-id="d5b51-140">The [**D3D12\_ROOT\_CONSTANTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) structure declares constants inline in the root signature that appear in shaders as one constant buffer.</span></span>

<span data-ttu-id="d5b51-141">Essa estrutura é usada quando o tipo de slot de assinatura raiz é definido como `D3D12_ROOT_PARAMETER_TYPE_32BIT_CONSTANTS` .</span><span class="sxs-lookup"><span data-stu-id="d5b51-141">This struct is used when the root signature slot type is set to `D3D12_ROOT_PARAMETER_TYPE_32BIT_CONSTANTS`.</span></span>

## <a name="root-descriptor"></a><span data-ttu-id="d5b51-142">Descritor raiz</span><span class="sxs-lookup"><span data-stu-id="d5b51-142">Root Descriptor</span></span>

<span data-ttu-id="d5b51-143">A estrutura do [**\_ \_ descritor raiz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) declara os descritores (que aparecem em sombreadores) embutidos na assinatura raiz.</span><span class="sxs-lookup"><span data-stu-id="d5b51-143">The [**D3D12\_ROOT\_DESCRIPTOR**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) structure declares descriptors (that appear in shaders) inline in the root signature.</span></span>

<span data-ttu-id="d5b51-144">Essa estrutura é usada quando o tipo de slot de assinatura raiz é definido como `D3D12_ROOT_PARAMETER_TYPE_CBV` , `D3D12_ROOT_PARAMETER_TYPE_SRV` ou `D3D12_ROOT_PARAMETER_TYPE_UAV` .</span><span class="sxs-lookup"><span data-stu-id="d5b51-144">This struct is used when the root signature slot type is set to `D3D12_ROOT_PARAMETER_TYPE_CBV`, `D3D12_ROOT_PARAMETER_TYPE_SRV` or `D3D12_ROOT_PARAMETER_TYPE_UAV`.</span></span>

## <a name="shader-visibility"></a><span data-ttu-id="d5b51-145">Visibilidade do sombreador</span><span class="sxs-lookup"><span data-stu-id="d5b51-145">Shader Visibility</span></span>

<span data-ttu-id="d5b51-146">O membro de [**D3D12 \_ de \_ visibilidade do sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) definido no parâmetro de visibilidade do sombreador do [**\_ \_ parâmetro raiz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) determina quais sombreadores veem o conteúdo de um determinado slot de assinatura raiz.</span><span class="sxs-lookup"><span data-stu-id="d5b51-146">The member of [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) enum set into the shader visibility parameter of [**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) determines which shaders see the contents of a given root signature slot.</span></span> <span data-ttu-id="d5b51-147">A computação sempre usa \_ tudo (já que há apenas um estágio ativo).</span><span class="sxs-lookup"><span data-stu-id="d5b51-147">Compute always uses \_ALL (since there is only one active stage).</span></span> <span data-ttu-id="d5b51-148">Os gráficos podem escolher, mas se usar \_ todos, todos os estágios do sombreador verão o que estiver associado ao slot de assinatura raiz.</span><span class="sxs-lookup"><span data-stu-id="d5b51-148">Graphics can choose, but if it uses \_ALL, all shader stages see whatever is bound at the root signature slot.</span></span>

<span data-ttu-id="d5b51-149">Um uso da visibilidade do sombreador é ajudar com os sombreadores que são criados esperando associações diferentes por estágio do sombreador usando um namespace sobreposto.</span><span class="sxs-lookup"><span data-stu-id="d5b51-149">One use of shader visibility is to help with shaders that are authored expecting different bindings per shader stage using an overlapping namespace.</span></span> <span data-ttu-id="d5b51-150">Por exemplo, um sombreador de vértice pode declarar:</span><span class="sxs-lookup"><span data-stu-id="d5b51-150">For example, a vertex shader may declare:</span></span>

```hlsl
Texture2D foo : register(t0);
```

<span data-ttu-id="d5b51-151">e o sombreador de pixel também pode declarar:</span><span class="sxs-lookup"><span data-stu-id="d5b51-151">and the pixel shader may also declare:</span></span>

```hlsl
Texture2D bar : register(t0);
```

<span data-ttu-id="d5b51-152">Se o aplicativo fizer uma associação de assinatura raiz para a visibilidade T0 \_ , ambos os sombreadores verão a mesma textura.</span><span class="sxs-lookup"><span data-stu-id="d5b51-152">If the application makes a root signature binding to t0 VISIBILITY\_ALL, both shaders see the same texture.</span></span> <span data-ttu-id="d5b51-153">Se o sombreador definir realmente deseja que cada sombreador Veja texturas diferentes, ele poderá definir 2 slots de assinatura raiz com \_ vértice de visibilidade e \_ pixel.</span><span class="sxs-lookup"><span data-stu-id="d5b51-153">If the shader defines actually wants each shader to see different textures, it can define 2 root signature slots with VISIBILITY\_VERTEX and \_PIXEL.</span></span> <span data-ttu-id="d5b51-154">Não importa qual a visibilidade está em um slot de assinatura raiz, ela sempre tem o mesmo custo (custo somente dependendo do tipo de Slottype) em relação a um tamanho de assinatura de raiz máximo fixo.</span><span class="sxs-lookup"><span data-stu-id="d5b51-154">No matter what the visibility is on a root signature slot, it always has the same cost (cost only depending on what the SlotType is) towards one fixed maximum root signature size.</span></span>

<span data-ttu-id="d5b51-155">Em hardware D3D11 de baixo nível, \_ a visibilidade do sombreador também é levada em conta usada ao validar os tamanhos das tabelas de descritores em um layout raiz, já que alguns hardwares D3D11 podem dar suporte apenas a uma quantidade máxima de associações por etapa.</span><span class="sxs-lookup"><span data-stu-id="d5b51-155">On low end D3D11 hardware, SHADER\_VISIBILITY is also taken into account used when validating the sizes of descriptor tables in a root layout, since some D3D11 hardware can only support a maximum amount of bindings per-stage.</span></span> <span data-ttu-id="d5b51-156">Essas restrições só são impostas durante a execução em hardware de camada baixa e não limitam um hardware mais moderno.</span><span class="sxs-lookup"><span data-stu-id="d5b51-156">These restrictions are only imposed when running on low tier hardware and do not limit more modern hardware at all.</span></span>

<span data-ttu-id="d5b51-157">Se uma assinatura de raiz tiver várias tabelas de descritores definidas que se sobrepõem em namespace (o registro de associações para o sombreador) e qualquer uma delas especificar \_ tudo para visibilidade, o layout será inválido (a criação falhará).</span><span class="sxs-lookup"><span data-stu-id="d5b51-157">If a root signature has multiple descriptor tables defined that overlap each other in namespace (the register bindings to the shader) and any one of them specifies \_ALL for visibility, the layout is invalid (creation will fail).</span></span>

## <a name="root-signature-definition"></a><span data-ttu-id="d5b51-158">Definição de assinatura raiz</span><span class="sxs-lookup"><span data-stu-id="d5b51-158">Root Signature Definition</span></span>

<span data-ttu-id="d5b51-159">A [**estrutura \_ \_ \_ desc de assinatura raiz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) pode conter tabelas de descritores e constantes embutidas, cada tipo de slot definido pela estrutura de [**\_ \_ parâmetro raiz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) e o tipo de [**\_ parâmetro de raiz \_ \_ D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_parameter_type)de enumeração.</span><span class="sxs-lookup"><span data-stu-id="d5b51-159">The [**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) structure can contain descriptor tables and inline constants, each slot type defined by the [**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) structure and the enum [**D3D12\_ROOT\_PARAMETER\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_parameter_type).</span></span>

<span data-ttu-id="d5b51-160">Para iniciar um slot de assinatura raiz, consulte os **métodos \* \* \* SetComputeRoot** e **SetGraphicsRoot \* \* \*** de [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist).</span><span class="sxs-lookup"><span data-stu-id="d5b51-160">To initiate a root signature slot, refer to the **SetComputeRoot\*\*\*** and **SetGraphicsRoot\*\*\*** methods of [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist).</span></span>

<span data-ttu-id="d5b51-161">Os exemplos estáticos são descritos na assinatura raiz usando a estrutura de [**\_ \_ amostra estática D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) .</span><span class="sxs-lookup"><span data-stu-id="d5b51-161">Static samplers are described in the root signature using the [**D3D12\_STATIC\_SAMPLER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) structure.</span></span>

<span data-ttu-id="d5b51-162">Um número de sinalizadores limita o acesso de determinados sombreadores à assinatura raiz, consulte [**\_ \_ \_ sinalizadores de assinatura raiz D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags).</span><span class="sxs-lookup"><span data-stu-id="d5b51-162">A number of flags limit the access of certain shaders to the root signature, refer to [**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags).</span></span>

## <a name="root-signature-data-structure-serialization--deserialization"></a><span data-ttu-id="d5b51-163">Serialização/desserialização da estrutura de dados da assinatura raiz</span><span class="sxs-lookup"><span data-stu-id="d5b51-163">Root Signature Data Structure Serialization / Deserialization</span></span>

<span data-ttu-id="d5b51-164">Os métodos descritos nesta seção são exportados por D3D12Core.dll e fornecem métodos para serialização e desserialização de uma estrutura de dados de assinatura raiz.</span><span class="sxs-lookup"><span data-stu-id="d5b51-164">The methods described in this section are exported by D3D12Core.dll and provide methods for serializing and deserializing a root signature data structure.</span></span>

<span data-ttu-id="d5b51-165">O formulário serializado é o que é passado para a API ao criar uma assinatura raiz.</span><span class="sxs-lookup"><span data-stu-id="d5b51-165">The serialized form is what is passed into the API when creating a root signature.</span></span> <span data-ttu-id="d5b51-166">Se um sombreador tiver sido criado com uma assinatura de raiz nele (quando esse recurso for adicionado), o sombreador compilado conterá uma assinatura de raiz serializada já.</span><span class="sxs-lookup"><span data-stu-id="d5b51-166">If a shader has been authored with a root signature in it (when that capability is added), then the compiled shader will contain a serialized root signature in it already.</span></span>

<span data-ttu-id="d5b51-167">Se um aplicativo gerar um procedimento de uma estrutura de dados [**\_ \_ \_ desc de assinatura raiz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) , ele deverá tornar o formulário serializado usando [**D3D12SerializeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature).</span><span class="sxs-lookup"><span data-stu-id="d5b51-167">If an application procedurally generates a [**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) data structure, it must make the serialized form using [**D3D12SerializeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature).</span></span> <span data-ttu-id="d5b51-168">A saída de que pode ser passada em [**ID3D12Device:: CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature).</span><span class="sxs-lookup"><span data-stu-id="d5b51-168">The output of that can be passed into [**ID3D12Device::CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature).</span></span>

<span data-ttu-id="d5b51-169">Se um aplicativo já tiver uma assinatura raiz serializada ou tiver um sombreador compilado que contenha uma assinatura raiz e desejar descobrir programaticamente a definição de layout (conhecida como "reflexão"), [**D3D12CreateRootSignatureDeserializer**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createrootsignaturedeserializer) poderá ser chamado.</span><span class="sxs-lookup"><span data-stu-id="d5b51-169">If an application has a serialized root signature already, or has a compiled shader that contains a root signature and wishes to programmatically discover the layout definition (known as "reflection"), [**D3D12CreateRootSignatureDeserializer**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createrootsignaturedeserializer) can be called.</span></span> <span data-ttu-id="d5b51-170">Isso gera uma interface [**ID3D12RootSignatureDeserializer**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignaturedeserializer) , que contém um método para retornar a estrutura de dados [**\_ \_ \_ desc de assinatura raiz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) desserializada.</span><span class="sxs-lookup"><span data-stu-id="d5b51-170">This generates an [**ID3D12RootSignatureDeserializer**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignaturedeserializer) interface, which contains a method to return the deserialized [**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) data structure.</span></span> <span data-ttu-id="d5b51-171">A interface possui o tempo de vida da estrutura de dados desserializada.</span><span class="sxs-lookup"><span data-stu-id="d5b51-171">The interface owns the lifetime of the deserialized data structure.</span></span>

## <a name="root-signature-creation-api"></a><span data-ttu-id="d5b51-172">API de criação de assinatura raiz</span><span class="sxs-lookup"><span data-stu-id="d5b51-172">Root Signature Creation API</span></span>

<span data-ttu-id="d5b51-173">A API [**ID3D12Device:: CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature) usa uma versão serializada de uma assinatura raiz.</span><span class="sxs-lookup"><span data-stu-id="d5b51-173">The [**ID3D12Device::CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature) API takes in a serialized version of a root signature.</span></span>

## <a name="root-signature-in-pipeline-state-objects"></a><span data-ttu-id="d5b51-174">Assinatura de raiz em objetos de estado do pipeline</span><span class="sxs-lookup"><span data-stu-id="d5b51-174">Root Signature in Pipeline State Objects</span></span>

<span data-ttu-id="d5b51-175">Os métodos para criar o estado do pipeline ([**ID3D12Device:: CreateGraphicsPipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) e [**ID3D12Device:: CreateComputePipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate) ) usam uma interface opcional [**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature) como um parâmetro de entrada (armazenado em uma estrutura [**desc de estado de \_ pipeline de elementos gráficos \_ \_ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) ).</span><span class="sxs-lookup"><span data-stu-id="d5b51-175">The methods to create pipeline state ([**ID3D12Device::CreateGraphicsPipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) and [**ID3D12Device::CreateComputePipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate) ) take an optional [**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature) interface as an input parameter (stored in a [**D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) structure).</span></span> <span data-ttu-id="d5b51-176">Isso substituirá qualquer assinatura raiz que já esteja nos sombreadores.</span><span class="sxs-lookup"><span data-stu-id="d5b51-176">This will override any root signature already in the shaders.</span></span>

<span data-ttu-id="d5b51-177">Se uma assinatura de raiz for passada em um dos métodos de criação de estado de pipeline, essa assinatura raiz será validada em relação a todos os sombreadores no PSO para compatibilidade e dada ao driver a ser usado com todos os sombreadores.</span><span class="sxs-lookup"><span data-stu-id="d5b51-177">If a root signature is passed into one of the create pipeline state methods, this root signature is validated against all the shaders in the PSO for compatibility and given to the driver to use with all the shaders.</span></span> <span data-ttu-id="d5b51-178">Se qualquer um dos sombreadores tiver uma assinatura de raiz diferente, ele será substituído pela assinatura raiz passada na API.</span><span class="sxs-lookup"><span data-stu-id="d5b51-178">If any of the shaders has a different root signature in it, it gets replaced by the root signature passed in at the API.</span></span> <span data-ttu-id="d5b51-179">Se uma assinatura raiz não for passada, todos os sombreadores passados deverão ter uma assinatura raiz e deverão corresponder – isso será fornecido ao driver.</span><span class="sxs-lookup"><span data-stu-id="d5b51-179">If a root signature is not passed in, all shaders passed in must have a root signature and they must match – this will be given to the driver.</span></span> <span data-ttu-id="d5b51-180">A definição de um PSO em uma lista de comandos ou pacote não altera a assinatura raiz.</span><span class="sxs-lookup"><span data-stu-id="d5b51-180">Setting a PSO on a command list or bundle does not change the root signature.</span></span> <span data-ttu-id="d5b51-181">Isso é realizado pelos métodos [**SetGraphicsRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootsignature) e [**SetComputeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature).</span><span class="sxs-lookup"><span data-stu-id="d5b51-181">That is accomplished by the methods [**SetGraphicsRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootsignature) and [**SetComputeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature).</span></span> <span data-ttu-id="d5b51-182">No momento em que o empate (Graphics)/dispatch (computação) é invocado, o aplicativo deve garantir que o PSO atual corresponda à assinatura raiz atual; caso contrário, o comportamento será indefinido.</span><span class="sxs-lookup"><span data-stu-id="d5b51-182">By the time draw(graphics)/dispatch(compute) is invoked, the application must ensure that the current PSO matches the current root signature; otherwise, the behavior is undefined.</span></span>

## <a name="code-for-defining-a-version-11-root-signature"></a><span data-ttu-id="d5b51-183">Código para definir uma assinatura raiz da versão 1,1</span><span class="sxs-lookup"><span data-stu-id="d5b51-183">Code for Defining a Version 1.1 Root Signature</span></span>

<span data-ttu-id="d5b51-184">O exemplo a seguir mostra como criar uma assinatura de raiz com o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="d5b51-184">The example below shows how to create a root signature with the following format:</span></span>



|                        |                                                |                                              |
|------------------------|------------------------------------------------|----------------------------------------------|
| <span data-ttu-id="d5b51-185">**RootParameterIndex**</span><span class="sxs-lookup"><span data-stu-id="d5b51-185">**RootParameterIndex**</span></span> | <span data-ttu-id="d5b51-186">**Contents**</span><span class="sxs-lookup"><span data-stu-id="d5b51-186">**Contents**</span></span>                                   |                                              |
| <span data-ttu-id="d5b51-187">\[0\]</span><span class="sxs-lookup"><span data-stu-id="d5b51-187">\[0\]</span></span>                  | <span data-ttu-id="d5b51-188">Constantes raiz: {B2}</span><span class="sxs-lookup"><span data-stu-id="d5b51-188">Root constants: { b2 }</span></span>                         | <span data-ttu-id="d5b51-189">(1 CBV)</span><span class="sxs-lookup"><span data-stu-id="d5b51-189">(1 CBV)</span></span>                                      |
| <span data-ttu-id="d5b51-190">\[1\]</span><span class="sxs-lookup"><span data-stu-id="d5b51-190">\[1\]</span></span>                  | <span data-ttu-id="d5b51-191">Tabela de descritores: {T2-T7, U0-U3}</span><span class="sxs-lookup"><span data-stu-id="d5b51-191">Descriptor table: { t2-t7, u0-u3 }</span></span>             | <span data-ttu-id="d5b51-192">(6 SRVs + 4 UAVs)</span><span class="sxs-lookup"><span data-stu-id="d5b51-192">(6 SRVs + 4 UAVs)</span></span>                            |
| <span data-ttu-id="d5b51-193">\[2\]</span><span class="sxs-lookup"><span data-stu-id="d5b51-193">\[2\]</span></span>                  | <span data-ttu-id="d5b51-194">CBV raiz: {B0}</span><span class="sxs-lookup"><span data-stu-id="d5b51-194">Root CBV: { b0 }</span></span>                               | <span data-ttu-id="d5b51-195">(1 CBV, dados estáticos)</span><span class="sxs-lookup"><span data-stu-id="d5b51-195">(1 CBV, static data)</span></span>                         |
| <span data-ttu-id="d5b51-196">\[3\]</span><span class="sxs-lookup"><span data-stu-id="d5b51-196">\[3\]</span></span>                  | <span data-ttu-id="d5b51-197">Tabela de descritores: {S0-S1}</span><span class="sxs-lookup"><span data-stu-id="d5b51-197">Descriptor table: { s0-s1 }</span></span>                    | <span data-ttu-id="d5b51-198">(2 amostras)</span><span class="sxs-lookup"><span data-stu-id="d5b51-198">(2 Samplers)</span></span>                                 |
| <span data-ttu-id="d5b51-199">\[4\]</span><span class="sxs-lookup"><span data-stu-id="d5b51-199">\[4\]</span></span>                  | <span data-ttu-id="d5b51-200">Tabela de descritores: {T8}</span><span class="sxs-lookup"><span data-stu-id="d5b51-200">Descriptor table: { t8 - unbounded }</span></span>           | <span data-ttu-id="d5b51-201">(não limitado \# de SRVs, descritores voláteis)</span><span class="sxs-lookup"><span data-stu-id="d5b51-201">(unbounded \# of SRVs, volatile descriptors)</span></span> |
| <span data-ttu-id="d5b51-202">\[5\]</span><span class="sxs-lookup"><span data-stu-id="d5b51-202">\[5\]</span></span>                  | <span data-ttu-id="d5b51-203">Tabela de descritores: {(T0, space1) – não associado}</span><span class="sxs-lookup"><span data-stu-id="d5b51-203">Descriptor table: { (t0, space1) - unbounded }</span></span> | <span data-ttu-id="d5b51-204">(não limitado \# de SRVs, descritores voláteis)</span><span class="sxs-lookup"><span data-stu-id="d5b51-204">(unbounded \# of SRVs, volatile descriptors)</span></span> |
| <span data-ttu-id="d5b51-205">\[6\]</span><span class="sxs-lookup"><span data-stu-id="d5b51-205">\[6\]</span></span>                  | <span data-ttu-id="d5b51-206">Tabela de descritores: {B1}</span><span class="sxs-lookup"><span data-stu-id="d5b51-206">Descriptor table: { b1 }</span></span>                       | <span data-ttu-id="d5b51-207">(1 CBV, dados estáticos)</span><span class="sxs-lookup"><span data-stu-id="d5b51-207">(1 CBV, static data)</span></span>                         |



 

<span data-ttu-id="d5b51-208">Se a maioria das partes da assinatura raiz for usada na maior parte do tempo, pode ser melhor ter que mudar a assinatura raiz com muita frequência.</span><span class="sxs-lookup"><span data-stu-id="d5b51-208">If most parts of the root signature get used most of the time it can be better than having to switch the root signature too frequently.</span></span> <span data-ttu-id="d5b51-209">Os aplicativos devem classificar as entradas na assinatura raiz da alteração mais frequente para o mínimo.</span><span class="sxs-lookup"><span data-stu-id="d5b51-209">Applications should sort entries in the root signature from most frequently changing to least.</span></span> <span data-ttu-id="d5b51-210">Quando um aplicativo altera as associações para qualquer parte da assinatura raiz, o driver pode ter que fazer uma cópia de algum ou de todo o estado de assinatura raiz, o que pode se tornar um custo não trivial quando multiplicado por muitas alterações de estado.</span><span class="sxs-lookup"><span data-stu-id="d5b51-210">When an app changes the bindings to any part of the root signature, the driver may have to make a copy of some or all of root signature state, which can become a nontrivial cost when multiplied across many state changes.</span></span>

<span data-ttu-id="d5b51-211">Além disso, a assinatura raiz definirá uma amostra estática que faz a filtragem de textura anisotropic no sombreador de registro S3.</span><span class="sxs-lookup"><span data-stu-id="d5b51-211">In addition, the root signature will define a static sampler that does anisotropic texture filtering at shader register s3.</span></span>

<span data-ttu-id="d5b51-212">Depois que essa assinatura raiz é associada, as tabelas de descritores, CBV e constantes raiz podem ser atribuídas ao \[ espaço de parâmetro 0.. 6 \] .</span><span class="sxs-lookup"><span data-stu-id="d5b51-212">After this root signature is bound, descriptor tables, root CBV and constants can be assigned to the \[0..6\] parameter space.</span></span> <span data-ttu-id="d5b51-213">por exemplo, as tabelas de descritores (intervalos em um heap de descritor) podem ser associadas a cada um dos parâmetros de raiz \[ 1 \] e \[ 3.. 6 \] .</span><span class="sxs-lookup"><span data-stu-id="d5b51-213">e.g. descriptor tables (ranges in a descriptor heap) can be bound at each of root parameters \[1\] and \[3..6\].</span></span>

``` syntax
CD3DX12_DESCRIPTOR_RANGE1 DescRange[6];

DescRange[0].Init(D3D12_DESCRIPTOR_RANGE_SRV,6,2); // t2-t7
DescRange[1].Init(D3D12_DESCRIPTOR_RANGE_UAV,4,0); // u0-u3
DescRange[2].Init(D3D12_DESCRIPTOR_RANGE_SAMPLER,2,0); // s0-s1
DescRange[3].Init(D3D12_DESCRIPTOR_RANGE_SRV,-1,8, 0,
                  D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE); // t8-unbounded
DescRange[4].Init(D3D12_DESCRIPTOR_RANGE_SRV,-1,0,1,
                  D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE); 
                                                            // (t0,space1)-unbounded
DescRange[5].Init(D3D12_DESCRIPTOR_RANGE_CBV,1,1,
                  D3D12_DESCRIPTOR_RANGE_FLAG_DATA_STATIC); // b1

CD3DX12_ROOT_PARAMETER1 RP[7];

RP[0].InitAsConstants(3,2); // 3 constants at b2
RP[1].InitAsDescriptorTable(2,&DescRange[0]); // 2 ranges t2-t7 and u0-u3
RP[2].InitAsConstantBufferView(0, 0, 
                               D3D12_ROOT_DESCRIPTOR_FLAG_DATA_STATIC); // b0
RP[3].InitAsDescriptorTable(1,&DescRange[2]); // s0-s1
RP[4].InitAsDescriptorTable(1,&DescRange[3]); // t8-unbounded
RP[5].InitAsDescriptorTable(1,&DescRange[4]); // (t0,space1)-unbounded
RP[6].InitAsDescriptorTable(1,&DescRange[5]); // b1

CD3DX12_STATIC_SAMPLER StaticSamplers[1];
StaticSamplers[0].Init(3, D3D12_FILTER_ANISOTROPIC); // s3
CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC RootSig(7,RP,1,StaticSamplers);
ID3DBlob* pSerializedRootSig;
CheckHR(D3D12SerializeVersionedRootSignature(&RootSig,pSerializedRootSig)); 

ID3D12RootSignature* pRootSignature;
hr = CheckHR(pDevice->CreateRootSignature(
    pSerializedRootSig->GetBufferPointer(),pSerializedRootSig->GetBufferSize(),
    __uuidof(ID3D12RootSignature),
    &pRootSignature));
```

<span data-ttu-id="d5b51-214">O código a seguir ilustra como a assinatura raiz acima pode ser usada em uma lista de comandos gráficos.</span><span class="sxs-lookup"><span data-stu-id="d5b51-214">The following code illustrates how the above root signature might be used on a graphics command list.</span></span>

``` syntax
InitializeMyDescriptorHeapContentsAheadOfTime(); // for simplicity of the 
                                                 // example
CreatePipelineStatesAhreadOfTime(pRootSignature); // The root signature is passed into 
                                     // shader / pipeline state creation
...

ID3D12DescriptorHeap* pHeaps[2] = {pCommonHeap, pSamplerHeap};
pGraphicsCommandList->SetDescriptorHeaps(pHeaps,2);
pGraphicsCommandList->SetGraphicsRootSignature(pRootSignature);
pGraphicsCommandList->SetGraphicsRootDescriptorTable(
                        6,heapOffsetForMoreData,DescRange[5].NumDescriptors);
pGraphicsCommandList->SetGraphicsRootDescriptorTable(5,heapOffsetForMisc,5000); 
pGraphicsCommandList->SetGraphicsRootDescriptorTable(4,heapOffsetForTerrain,20000);
pGraphicsCommandList->SetGraphicsRootDescriptorTable(
                        3,heapOffsetForSamplers,DescRange[2].NumDescriptors);
pGraphicsCommandList->SetComputeRootConstantBufferView(2,pDynamicCBHeap,&CBVDesc);

MY_PER_DRAW_STUFF stuff;
InitMyPerDrawStuff(&stuff);
pGraphicsCommandList->SetSetGraphicsRoot32BitConstants(
                        0,&stuff,0,RTSlot[0].Constants.Num32BitValues);

SetMyRTVAndOtherMiscBindings();

for(UINT i = 0; i < numObjects; i++)
{
    pGraphicsCommandList->SetPipelineState(PSO[i]);
    pGraphicsCommandList->SetGraphicsRootDescriptorTable(
                    1,heapOffsetForFooAndBar[i],DescRange[1].NumDescriptors);
    pGraphicsCommandList->SetGraphicsRoot32BitConstant(0,&i,1,drawIDOffset);
    SetMyIndexBuffers(i);
    pGraphicsCommandList->DrawIndexedInstanced(...);
}
```

## <a name="related-topics"></a><span data-ttu-id="d5b51-215">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d5b51-215">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5b51-216">Assinaturas raiz</span><span class="sxs-lookup"><span data-stu-id="d5b51-216">Root Signatures</span></span>](root-signatures.md)
</dt> <dt>

[<span data-ttu-id="d5b51-217">Como especificar assinaturas raiz no HLSL</span><span class="sxs-lookup"><span data-stu-id="d5b51-217">Specifying Root Signatures in HLSL</span></span>](specifying-root-signatures-in-hlsl.md)
</dt> <dt>

[<span data-ttu-id="d5b51-218">Como usar uma assinatura raiz</span><span class="sxs-lookup"><span data-stu-id="d5b51-218">Using a Root Signature</span></span>](using-a-root-signature.md)
</dt> </dl>

 

 
