---
title: Como criar uma assinatura raiz
description: As assinaturas raiz são uma estrutura de dados complexa que contém estruturas aninhadas.
ms.assetid: 565B28C1-DBD1-42B6-87F9-70743E4A2E4A
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87209dfc324b950a74d2b31e5f1a1f6326792b9f
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826432"
---
# <a name="creating-a-root-signature"></a><span data-ttu-id="44889-103">Como criar uma assinatura raiz</span><span class="sxs-lookup"><span data-stu-id="44889-103">Creating a Root Signature</span></span>

<span data-ttu-id="44889-104">As assinaturas raiz são uma estrutura de dados complexa que contém estruturas aninhadas.</span><span class="sxs-lookup"><span data-stu-id="44889-104">Root signatures are a complex data structure containing nested structures.</span></span> <span data-ttu-id="44889-105">Eles podem ser definidos programaticamente usando a definição de estrutura de dados abaixo (que inclui métodos para ajudar a inicializar membros).</span><span class="sxs-lookup"><span data-stu-id="44889-105">These can be defined programmatically using the data structure definition below (which includes methods to help initialize members).</span></span> <span data-ttu-id="44889-106">Como alternativa, elas podem ser escritas em HLSL (Linguagem de Sombreamento de Alto Nível) – dando a vantagem de que o compilador validará no início que o layout é compatível com o sombreador.</span><span class="sxs-lookup"><span data-stu-id="44889-106">Alternatively, they can be authored in High Level Shading Language (HLSL) – giving the advantage that the compiler will validate early that the layout is compatible with the shader.</span></span>

<span data-ttu-id="44889-107">A API para criar uma assinatura raiz leva em uma versão serializada (autossunte, sem ponteiro) da descrição de layout descrita abaixo.</span><span class="sxs-lookup"><span data-stu-id="44889-107">The API for creating a root signature takes in a serialized (self contained, pointer free) version of the layout description described below.</span></span> <span data-ttu-id="44889-108">Um método é fornecido para gerar essa versão serializada da estrutura de dados do C++, mas outra maneira de obter uma definição de assinatura raiz serializada é recuperá-la de um sombreador que foi compilado com uma assinatura raiz.</span><span class="sxs-lookup"><span data-stu-id="44889-108">A method is provided for generating this serialized version from the C++ data structure, but another way to obtain a serialized root signature definition is to retrieve it from a shader that has been compiled with a root signature.</span></span>

<span data-ttu-id="44889-109">Se você quiser aproveitar as otimizações de driver para descritores de assinatura raiz e dados, consulte [Root Signature Versão 1.1](root-signature-version-1-1.md)</span><span class="sxs-lookup"><span data-stu-id="44889-109">If you wish to take advantage of driver optimizations for root signature descriptors and data, refer to [Root Signature Version 1.1](root-signature-version-1-1.md)</span></span>

-   [<span data-ttu-id="44889-110">Tipos de vinculação de tabela do descritor</span><span class="sxs-lookup"><span data-stu-id="44889-110">Descriptor Table Bind Types</span></span>](#descriptor-table-bind-types)
-   [<span data-ttu-id="44889-111">Intervalo do descritor</span><span class="sxs-lookup"><span data-stu-id="44889-111">Descriptor Range</span></span>](#descriptor-range)
-   [<span data-ttu-id="44889-112">Layout da tabela do descritor</span><span class="sxs-lookup"><span data-stu-id="44889-112">Descriptor Table Layout</span></span>](#descriptor-table-layout)
-   [<span data-ttu-id="44889-113">Constantes raiz</span><span class="sxs-lookup"><span data-stu-id="44889-113">Root Constants</span></span>](#root-constants)
-   [<span data-ttu-id="44889-114">Descritor raiz</span><span class="sxs-lookup"><span data-stu-id="44889-114">Root Descriptor</span></span>](#root-descriptor)
-   [<span data-ttu-id="44889-115">Visibilidade do sombreador</span><span class="sxs-lookup"><span data-stu-id="44889-115">Shader Visibility</span></span>](#shader-visibility)
-   [<span data-ttu-id="44889-116">Definição de assinatura raiz</span><span class="sxs-lookup"><span data-stu-id="44889-116">Root Signature Definition</span></span>](#root-signature-definition)
-   [<span data-ttu-id="44889-117">Serialização/deserialização da estrutura de dados de assinatura raiz</span><span class="sxs-lookup"><span data-stu-id="44889-117">Root Signature Data Structure Serialization / Deserialization</span></span>](/windows)
-   [<span data-ttu-id="44889-118">API de Criação de Assinatura Raiz</span><span class="sxs-lookup"><span data-stu-id="44889-118">Root Signature Creation API</span></span>](#root-signature-creation-api)
-   [<span data-ttu-id="44889-119">Assinatura raiz em objetos de estado do pipeline</span><span class="sxs-lookup"><span data-stu-id="44889-119">Root Signature in Pipeline State Objects</span></span>](#root-signature-in-pipeline-state-objects)
-   [<span data-ttu-id="44889-120">Código para definir uma assinatura raiz da versão 1.1</span><span class="sxs-lookup"><span data-stu-id="44889-120">Code for Defining a Version 1.1 Root Signature</span></span>](#code-for-defining-a-version-11-root-signature)
-   [<span data-ttu-id="44889-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="44889-121">Related topics</span></span>](#related-topics)

## <a name="descriptor-table-bind-types"></a><span data-ttu-id="44889-122">Tipos de vinculação de tabela do descritor</span><span class="sxs-lookup"><span data-stu-id="44889-122">Descriptor Table Bind Types</span></span>

<span data-ttu-id="44889-123">A enum [**D3D12 \_ DESCRIPTOR \_ RANGE \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) define os tipos de descritores que podem ser referenciados como parte de uma definição de layout de tabela de descritor.</span><span class="sxs-lookup"><span data-stu-id="44889-123">The enum [**D3D12\_DESCRIPTOR\_RANGE\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) defines the types of descriptors that can be referenced as part of a descriptor table layout definition.</span></span>

<span data-ttu-id="44889-124">É um intervalo para que, por exemplo, se parte de uma tabela de descritor tiver 100 SRVs, esse intervalo poderá ser declarado em uma entrada em vez de 100.</span><span class="sxs-lookup"><span data-stu-id="44889-124">It is a range so that, for example if part of a descriptor table has 100 SRVs, that range can be declared in one entry rather than 100.</span></span> <span data-ttu-id="44889-125">Portanto, uma definição de tabela de descritor é uma coleção de intervalos.</span><span class="sxs-lookup"><span data-stu-id="44889-125">So a descriptor table definition is a collection of ranges.</span></span>

``` syntax
typedef enum D3D12_DESCRIPTOR_RANGE_TYPE
{
  D3D12_DESCRIPTOR_RANGE_TYPE_SRV,
  D3D12_DESCRIPTOR_RANGE_TYPE_UAV,
  D3D12_DESCRIPTOR_RANGE_TYPE_CBV,
  D3D12_DESCRIPTOR_RANGE_TYPE_SAMPLER
} D3D12_DESCRIPTOR_RANGE_TYPE;
```

## <a name="descriptor-range"></a><span data-ttu-id="44889-126">Intervalo do descritor</span><span class="sxs-lookup"><span data-stu-id="44889-126">Descriptor Range</span></span>

<span data-ttu-id="44889-127">A [**estrutura D3D12 \_ DESCRIPTOR \_ RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) define um intervalo de descritores de um determinado tipo (como SRVs) dentro de uma tabela de descritor.</span><span class="sxs-lookup"><span data-stu-id="44889-127">The [**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) structure defines a range of descriptors of a given type (such as SRVs) within a descriptor table.</span></span>

<span data-ttu-id="44889-128">A `D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND` macro normalmente pode ser usada para o parâmetro de `OffsetInDescriptorsFromTableStart` [**D3D12 \_ DESCRIPTOR \_ RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range).</span><span class="sxs-lookup"><span data-stu-id="44889-128">The `D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND` macro can typically be used for the `OffsetInDescriptorsFromTableStart` parameter of [**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range).</span></span> <span data-ttu-id="44889-129">Isso significa anexar o intervalo de descritor que está sendo definido após o anterior na tabela do descritor.</span><span class="sxs-lookup"><span data-stu-id="44889-129">This means append the descriptor range being defined after the previous one in the descriptor table.</span></span> <span data-ttu-id="44889-130">Se o aplicativo quiser alias de descritores ou por algum motivo desejar ignorar slots, ele poderá definir como qualquer `OffsetInDescriptorsFromTableStart` deslocamento desejado.</span><span class="sxs-lookup"><span data-stu-id="44889-130">If the application wants to alias descriptors or for some reason wants to skip slots, it can set `OffsetInDescriptorsFromTableStart` to whatever offset is desired.</span></span> <span data-ttu-id="44889-131">Definir intervalos sobrepostos de tipos diferentes é inválido.</span><span class="sxs-lookup"><span data-stu-id="44889-131">Defining overlapping ranges of different types is invalid.</span></span>

<span data-ttu-id="44889-132">O conjunto de registros de sombreador especificado pela combinação de , , e não pode entrar em conflito ou se sobrepor a qualquer declaração em uma assinatura raiz que tenha VISIBILIDADE DO SOMBREADOR `RangeType` `NumDescriptors` `BaseShaderRegister` `RegisterSpace` [**D3D12 \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) comum (consulte a seção visibilidade do sombreador abaixo).</span><span class="sxs-lookup"><span data-stu-id="44889-132">The set of shader registers specified by the combination of `RangeType`, `NumDescriptors`, `BaseShaderRegister`, and `RegisterSpace` cannot conflict or overlap across any declarations in a root signature that have common [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) (refer to the shader visibility section below).</span></span>

## <a name="descriptor-table-layout"></a><span data-ttu-id="44889-133">Layout da tabela do descritor</span><span class="sxs-lookup"><span data-stu-id="44889-133">Descriptor Table Layout</span></span>

<span data-ttu-id="44889-134">A [**estrutura D3D12 \_ ROOT \_ DESCRIPTOR \_ TABLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) declara o layout de uma tabela de descritor como uma coleção de intervalos de descritores que aparecem um após o outro em um heap de descritor.</span><span class="sxs-lookup"><span data-stu-id="44889-134">The [**D3D12\_ROOT\_DESCRIPTOR\_TABLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) structure declares the layout of a descriptor table as a collection of descriptor ranges that appear one after the other in a descriptor heap.</span></span> <span data-ttu-id="44889-135">Os exemplos não são permitidos na mesma tabela de descritor que CBV/UAV/SRVs.</span><span class="sxs-lookup"><span data-stu-id="44889-135">Samplers are not allowed in the same descriptor table as CBV/UAV/SRVs.</span></span>

<span data-ttu-id="44889-136">Esse struct é usado quando o tipo de slot de assinatura raiz é definido como `D3D12_ROOT_PARAMETER_TYPE_DESCRIPTOR_TABLE` .</span><span class="sxs-lookup"><span data-stu-id="44889-136">This struct is used when the root signature slot type is set to `D3D12_ROOT_PARAMETER_TYPE_DESCRIPTOR_TABLE`.</span></span>

<span data-ttu-id="44889-137">Para definir uma tabela de descritor de gráficos (CBV, SRV, UAV, Sampler), use [**ID3D12GraphicsCommandList::SetGraphicsRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable).</span><span class="sxs-lookup"><span data-stu-id="44889-137">To set a graphics (CBV, SRV, UAV, Sampler) descriptor table, use [**ID3D12GraphicsCommandList::SetGraphicsRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable).</span></span>

<span data-ttu-id="44889-138">Para definir uma tabela de descritor de computação, use [**ID3D12GraphicsCommandList::SetComputeRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable).</span><span class="sxs-lookup"><span data-stu-id="44889-138">To set a compute descriptor table, use [**ID3D12GraphicsCommandList::SetComputeRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable).</span></span>

## <a name="root-constants"></a><span data-ttu-id="44889-139">Constantes raiz</span><span class="sxs-lookup"><span data-stu-id="44889-139">Root Constants</span></span>

<span data-ttu-id="44889-140">A [**estrutura \_ \_ CONSTANTS RAIZ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) declara constantes em linha na assinatura raiz que aparecem em sombreadores como um buffer constante.</span><span class="sxs-lookup"><span data-stu-id="44889-140">The [**D3D12\_ROOT\_CONSTANTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) structure declares constants inline in the root signature that appear in shaders as one constant buffer.</span></span>

<span data-ttu-id="44889-141">Esse struct é usado quando o tipo de slot de assinatura raiz é definido como `D3D12_ROOT_PARAMETER_TYPE_32BIT_CONSTANTS` .</span><span class="sxs-lookup"><span data-stu-id="44889-141">This struct is used when the root signature slot type is set to `D3D12_ROOT_PARAMETER_TYPE_32BIT_CONSTANTS`.</span></span>

## <a name="root-descriptor"></a><span data-ttu-id="44889-142">Descritor raiz</span><span class="sxs-lookup"><span data-stu-id="44889-142">Root Descriptor</span></span>

<span data-ttu-id="44889-143">A [**estrutura D3D12 \_ ROOT \_ DESCRIPTOR**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) declara descritores (que aparecem em sombreadores) em linha na assinatura raiz.</span><span class="sxs-lookup"><span data-stu-id="44889-143">The [**D3D12\_ROOT\_DESCRIPTOR**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) structure declares descriptors (that appear in shaders) inline in the root signature.</span></span>

<span data-ttu-id="44889-144">Esse struct é usado quando o tipo de slot de assinatura raiz é definido como `D3D12_ROOT_PARAMETER_TYPE_CBV` ou `D3D12_ROOT_PARAMETER_TYPE_SRV` `D3D12_ROOT_PARAMETER_TYPE_UAV` .</span><span class="sxs-lookup"><span data-stu-id="44889-144">This struct is used when the root signature slot type is set to `D3D12_ROOT_PARAMETER_TYPE_CBV`, `D3D12_ROOT_PARAMETER_TYPE_SRV` or `D3D12_ROOT_PARAMETER_TYPE_UAV`.</span></span>

## <a name="shader-visibility"></a><span data-ttu-id="44889-145">Visibilidade do sombreador</span><span class="sxs-lookup"><span data-stu-id="44889-145">Shader Visibility</span></span>

<span data-ttu-id="44889-146">O membro de [**D3D12 \_ SHADER \_ VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) enum definido no parâmetro de visibilidade do sombreador [**de D3D12 \_ ROOT \_ PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) determina quais sombreadores veem o conteúdo de um determinado slot de assinatura raiz.</span><span class="sxs-lookup"><span data-stu-id="44889-146">The member of [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) enum set into the shader visibility parameter of [**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) determines which shaders see the contents of a given root signature slot.</span></span> <span data-ttu-id="44889-147">A computação sempre \_ usa ALL (já que há apenas um estágio ativo).</span><span class="sxs-lookup"><span data-stu-id="44889-147">Compute always uses \_ALL (since there is only one active stage).</span></span> <span data-ttu-id="44889-148">Os gráficos podem escolher, mas se usar ALL, todos os estágios do sombreador verão o que \_ está vinculado no slot de assinatura raiz.</span><span class="sxs-lookup"><span data-stu-id="44889-148">Graphics can choose, but if it uses \_ALL, all shader stages see whatever is bound at the root signature slot.</span></span>

<span data-ttu-id="44889-149">Um uso da visibilidade do sombreador é ajudar com sombreadores que são destinados à espera de diferentes vinculações por estágio do sombreador usando um namespace sobreposto.</span><span class="sxs-lookup"><span data-stu-id="44889-149">One use of shader visibility is to help with shaders that are authored expecting different bindings per shader stage using an overlapping namespace.</span></span> <span data-ttu-id="44889-150">Por exemplo, um sombreador de vértice pode declarar:</span><span class="sxs-lookup"><span data-stu-id="44889-150">For example, a vertex shader may declare:</span></span>

```hlsl
Texture2D foo : register(t0);
```

<span data-ttu-id="44889-151">e o sombreador de pixel também pode declarar:</span><span class="sxs-lookup"><span data-stu-id="44889-151">and the pixel shader may also declare:</span></span>

```hlsl
Texture2D bar : register(t0);
```

<span data-ttu-id="44889-152">Se o aplicativo fizer uma associação de assinatura raiz para t0 VISIBILITY \_ ALL, ambos os sombreadores verão a mesma textura.</span><span class="sxs-lookup"><span data-stu-id="44889-152">If the application makes a root signature binding to t0 VISIBILITY\_ALL, both shaders see the same texture.</span></span> <span data-ttu-id="44889-153">Se o sombreador definir realmente deseja que cada sombreador veja texturas diferentes, ele pode definir dois slots de assinatura raiz com VISIBILITY \_ VERTEX e \_ PIXEL.</span><span class="sxs-lookup"><span data-stu-id="44889-153">If the shader defines actually wants each shader to see different textures, it can define 2 root signature slots with VISIBILITY\_VERTEX and \_PIXEL.</span></span> <span data-ttu-id="44889-154">Independentemente de qual é a visibilidade em um slot de assinatura raiz, ela sempre tem o mesmo custo (custo apenas dependendo de qual é o SlotType) para um tamanho de assinatura raiz máximo fixo.</span><span class="sxs-lookup"><span data-stu-id="44889-154">No matter what the visibility is on a root signature slot, it always has the same cost (cost only depending on what the SlotType is) towards one fixed maximum root signature size.</span></span>

<span data-ttu-id="44889-155">No hardware D3D11 de baixo nível, a VISIBILIDADE DO SOMBREADOR também é levada em conta usada ao validar os tamanhos de tabelas de descritor em um layout raiz, já que algum hardware D3D11 só pode dar suporte a uma quantidade máxima de vinculações por \_ estágio.</span><span class="sxs-lookup"><span data-stu-id="44889-155">On low end D3D11 hardware, SHADER\_VISIBILITY is also taken into account used when validating the sizes of descriptor tables in a root layout, since some D3D11 hardware can only support a maximum amount of bindings per-stage.</span></span> <span data-ttu-id="44889-156">Essas restrições só são impostas ao executar em hardware de camada baixa e não limitam hardware mais moderno.</span><span class="sxs-lookup"><span data-stu-id="44889-156">These restrictions are only imposed when running on low tier hardware and do not limit more modern hardware at all.</span></span>

<span data-ttu-id="44889-157">Se uma assinatura raiz tiver várias tabelas de descritor definidas que se sobrepõem entre si no namespace (as vinculações de registro ao sombreador) e qualquer uma delas especificar ALL para visibilidade, o layout será inválido (a criação \_ falhará).</span><span class="sxs-lookup"><span data-stu-id="44889-157">If a root signature has multiple descriptor tables defined that overlap each other in namespace (the register bindings to the shader) and any one of them specifies \_ALL for visibility, the layout is invalid (creation will fail).</span></span>

## <a name="root-signature-definition"></a><span data-ttu-id="44889-158">Definição de assinatura raiz</span><span class="sxs-lookup"><span data-stu-id="44889-158">Root Signature Definition</span></span>

<span data-ttu-id="44889-159">A estrutura [**D3D12 \_ ROOT \_ SIGNATURE \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) pode conter tabelas de descritor e constantes em linha, cada tipo de slot definido pela estrutura [**D3D12 \_ ROOT \_ PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) e a enum [**D3D12 \_ ROOT PARAMETER \_ \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_parameter_type).</span><span class="sxs-lookup"><span data-stu-id="44889-159">The [**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) structure can contain descriptor tables and inline constants, each slot type defined by the [**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) structure and the enum [**D3D12\_ROOT\_PARAMETER\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_parameter_type).</span></span>

<span data-ttu-id="44889-160">Para iniciar um slot de assinatura raiz, consulte os métodos **SetComputeRoot \* \* \*** e **\* \* \* SetGraphicsRoot** [**de ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist).</span><span class="sxs-lookup"><span data-stu-id="44889-160">To initiate a root signature slot, refer to the **SetComputeRoot\*\*\*** and **SetGraphicsRoot\*\*\*** methods of [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist).</span></span>

<span data-ttu-id="44889-161">Exemplos estáticos são descritos na assinatura raiz usando a [**estrutura D3D12 \_ STATIC \_ SAMPLER.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)</span><span class="sxs-lookup"><span data-stu-id="44889-161">Static samplers are described in the root signature using the [**D3D12\_STATIC\_SAMPLER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) structure.</span></span>

<span data-ttu-id="44889-162">Vários sinalizadores limitam o acesso de determinados sombreadores à assinatura raiz, consulte SINALIZADORES DE ASSINATURA [**\_ \_ \_ RAIZ D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags).</span><span class="sxs-lookup"><span data-stu-id="44889-162">A number of flags limit the access of certain shaders to the root signature, refer to [**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags).</span></span>

## <a name="root-signature-data-structure-serialization--deserialization"></a><span data-ttu-id="44889-163">Serialização/deserialização da estrutura de dados de assinatura raiz</span><span class="sxs-lookup"><span data-stu-id="44889-163">Root Signature Data Structure Serialization / Deserialization</span></span>

<span data-ttu-id="44889-164">Os métodos descritos nesta seção são exportados por D3D12Core.dll e fornecem métodos para serializar e desseerializar uma estrutura de dados de assinatura raiz.</span><span class="sxs-lookup"><span data-stu-id="44889-164">The methods described in this section are exported by D3D12Core.dll and provide methods for serializing and deserializing a root signature data structure.</span></span>

<span data-ttu-id="44889-165">O formulário serializado é o que é passado para a API ao criar uma assinatura raiz.</span><span class="sxs-lookup"><span data-stu-id="44889-165">The serialized form is what is passed into the API when creating a root signature.</span></span> <span data-ttu-id="44889-166">Se um sombreador tiver sido autor com uma assinatura raiz (quando essa funcionalidade for adicionada), o sombreador compilado já conterá uma assinatura raiz serializada.</span><span class="sxs-lookup"><span data-stu-id="44889-166">If a shader has been authored with a root signature in it (when that capability is added), then the compiled shader will contain a serialized root signature in it already.</span></span>

<span data-ttu-id="44889-167">Se um aplicativo gerar uma estrutura de dados [**D3D12 \_ \_ ROOT SIGNATURE \_ DESC,**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) ele deverá criar o formulário serializado usando [**D3D12SerializeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature).</span><span class="sxs-lookup"><span data-stu-id="44889-167">If an application procedurally generates a [**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) data structure, it must make the serialized form using [**D3D12SerializeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature).</span></span> <span data-ttu-id="44889-168">A saída de que pode ser passada para [**ID3D12Device::CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature).</span><span class="sxs-lookup"><span data-stu-id="44889-168">The output of that can be passed into [**ID3D12Device::CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature).</span></span>

<span data-ttu-id="44889-169">Se um aplicativo já tiver uma assinatura raiz serializada ou tiver um sombreador compilado que contém uma assinatura raiz e quiser descobrir programaticamente a definição de layout (conhecida como "reflexão"), [**D3D12CreateRootSignatureDeserializer**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createrootsignaturedeserializer) poderá ser chamado.</span><span class="sxs-lookup"><span data-stu-id="44889-169">If an application has a serialized root signature already, or has a compiled shader that contains a root signature and wishes to programmatically discover the layout definition (known as "reflection"), [**D3D12CreateRootSignatureDeserializer**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createrootsignaturedeserializer) can be called.</span></span> <span data-ttu-id="44889-170">Isso gera uma interface [**ID3D12RootSignatureDeserializer,**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignaturedeserializer) que contém um método para retornar a estrutura de dados DESC de ASSINATURA RAIZ [**\_ \_ D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) desseializada.</span><span class="sxs-lookup"><span data-stu-id="44889-170">This generates an [**ID3D12RootSignatureDeserializer**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignaturedeserializer) interface, which contains a method to return the deserialized [**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) data structure.</span></span> <span data-ttu-id="44889-171">A interface possui o tempo de vida da estrutura de dados desserializada.</span><span class="sxs-lookup"><span data-stu-id="44889-171">The interface owns the lifetime of the deserialized data structure.</span></span>

## <a name="root-signature-creation-api"></a><span data-ttu-id="44889-172">API de Criação de Assinatura Raiz</span><span class="sxs-lookup"><span data-stu-id="44889-172">Root Signature Creation API</span></span>

<span data-ttu-id="44889-173">A API [**ID3D12Device::CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature) assume uma versão serializada de uma assinatura raiz.</span><span class="sxs-lookup"><span data-stu-id="44889-173">The [**ID3D12Device::CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature) API takes in a serialized version of a root signature.</span></span>

## <a name="root-signature-in-pipeline-state-objects"></a><span data-ttu-id="44889-174">Assinatura raiz em objetos de estado do pipeline</span><span class="sxs-lookup"><span data-stu-id="44889-174">Root Signature in Pipeline State Objects</span></span>

<span data-ttu-id="44889-175">Os métodos para criar o estado do pipeline ([**ID3D12Device::CreateGraphicsPipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) e [**ID3D12Device::CreateComputePipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate) ) levam uma interface [**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature) opcional como um parâmetro de entrada (armazenado em uma estrutura [**D3D12 \_ GRAPHICS \_ PIPELINE STATE \_ \_ DESC).**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc)</span><span class="sxs-lookup"><span data-stu-id="44889-175">The methods to create pipeline state ([**ID3D12Device::CreateGraphicsPipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) and [**ID3D12Device::CreateComputePipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate) ) take an optional [**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature) interface as an input parameter (stored in a [**D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) structure).</span></span> <span data-ttu-id="44889-176">Isso substituirá qualquer assinatura raiz já nos sombreadores.</span><span class="sxs-lookup"><span data-stu-id="44889-176">This will override any root signature already in the shaders.</span></span>

<span data-ttu-id="44889-177">Se uma assinatura raiz for passada para um dos métodos de estado do pipeline de criação, essa assinatura raiz será validada em relação a todos os sombreadores no PSO para compatibilidade e dada ao driver para usar com todos os sombreadores.</span><span class="sxs-lookup"><span data-stu-id="44889-177">If a root signature is passed into one of the create pipeline state methods, this root signature is validated against all the shaders in the PSO for compatibility and given to the driver to use with all the shaders.</span></span> <span data-ttu-id="44889-178">Se algum dos sombreadores tiver uma assinatura raiz diferente, ele será substituído pela assinatura raiz passada na API.</span><span class="sxs-lookup"><span data-stu-id="44889-178">If any of the shaders has a different root signature in it, it gets replaced by the root signature passed in at the API.</span></span> <span data-ttu-id="44889-179">Se uma assinatura raiz não for passada, todos os sombreadores passados deverão ter uma assinatura raiz e devem corresponder – isso será dado ao driver.</span><span class="sxs-lookup"><span data-stu-id="44889-179">If a root signature is not passed in, all shaders passed in must have a root signature and they must match – this will be given to the driver.</span></span> <span data-ttu-id="44889-180">Definir um PSO em uma lista de comandos ou pacote não altera a assinatura raiz.</span><span class="sxs-lookup"><span data-stu-id="44889-180">Setting a PSO on a command list or bundle does not change the root signature.</span></span> <span data-ttu-id="44889-181">Isso é feito pelos métodos [**SetGraphicsRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootsignature) e [**SetComputeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature).</span><span class="sxs-lookup"><span data-stu-id="44889-181">That is accomplished by the methods [**SetGraphicsRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootsignature) and [**SetComputeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature).</span></span> <span data-ttu-id="44889-182">No momento em que draw(graphics)/dispatch(compute) é invocado, o aplicativo deve garantir que o PSO atual corresponde à assinatura raiz atual; caso contrário, o comportamento será indefinido.</span><span class="sxs-lookup"><span data-stu-id="44889-182">By the time draw(graphics)/dispatch(compute) is invoked, the application must ensure that the current PSO matches the current root signature; otherwise, the behavior is undefined.</span></span>

## <a name="code-for-defining-a-version-11-root-signature"></a><span data-ttu-id="44889-183">Código para definir uma assinatura raiz da versão 1.1</span><span class="sxs-lookup"><span data-stu-id="44889-183">Code for Defining a Version 1.1 Root Signature</span></span>

<span data-ttu-id="44889-184">O exemplo a seguir mostra como criar uma assinatura raiz com o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="44889-184">The example below shows how to create a root signature with the following format:</span></span>



| <span data-ttu-id="44889-185">RootParameterIndex</span><span class="sxs-lookup"><span data-stu-id="44889-185">RootParameterIndex</span></span>                       | <span data-ttu-id="44889-186">Sumário</span><span class="sxs-lookup"><span data-stu-id="44889-186">Contents</span></span>                                               | <span data-ttu-id="44889-187">Valores</span><span class="sxs-lookup"><span data-stu-id="44889-187">Values</span></span>                                             |
|------------------------|------------------------------------------------|----------------------------------------------|                                              
| <span data-ttu-id="44889-188">\[0\]</span><span class="sxs-lookup"><span data-stu-id="44889-188">\[0\]</span></span>                  | <span data-ttu-id="44889-189">Constantes raiz: { b2 }</span><span class="sxs-lookup"><span data-stu-id="44889-189">Root constants: { b2 }</span></span>                         | <span data-ttu-id="44889-190">(1 CBV)</span><span class="sxs-lookup"><span data-stu-id="44889-190">(1 CBV)</span></span>                                      |
| <span data-ttu-id="44889-191">\[1\]</span><span class="sxs-lookup"><span data-stu-id="44889-191">\[1\]</span></span>                  | <span data-ttu-id="44889-192">Tabela do descritor: { t2-t7, u0-u3 }</span><span class="sxs-lookup"><span data-stu-id="44889-192">Descriptor table: { t2-t7, u0-u3 }</span></span>             | <span data-ttu-id="44889-193">(6 SRVs + 4 UAVs)</span><span class="sxs-lookup"><span data-stu-id="44889-193">(6 SRVs + 4 UAVs)</span></span>                            |
| <span data-ttu-id="44889-194">\[2\]</span><span class="sxs-lookup"><span data-stu-id="44889-194">\[2\]</span></span>                  | <span data-ttu-id="44889-195">CBV raiz: { b0 }</span><span class="sxs-lookup"><span data-stu-id="44889-195">Root CBV: { b0 }</span></span>                               | <span data-ttu-id="44889-196">(1 CBV, dados estáticos)</span><span class="sxs-lookup"><span data-stu-id="44889-196">(1 CBV, static data)</span></span>                         |
| <span data-ttu-id="44889-197">\[3\]</span><span class="sxs-lookup"><span data-stu-id="44889-197">\[3\]</span></span>                  | <span data-ttu-id="44889-198">Tabela do descritor: { s0-s1 }</span><span class="sxs-lookup"><span data-stu-id="44889-198">Descriptor table: { s0-s1 }</span></span>                    | <span data-ttu-id="44889-199">(2 exemplos)</span><span class="sxs-lookup"><span data-stu-id="44889-199">(2 Samplers)</span></span>                                 |
| <span data-ttu-id="44889-200">\[4\]</span><span class="sxs-lookup"><span data-stu-id="44889-200">\[4\]</span></span>                  | <span data-ttu-id="44889-201">Tabela de descritores: {T8}</span><span class="sxs-lookup"><span data-stu-id="44889-201">Descriptor table: { t8 - unbounded }</span></span>           | <span data-ttu-id="44889-202">(não limitado \# de SRVs, descritores voláteis)</span><span class="sxs-lookup"><span data-stu-id="44889-202">(unbounded \# of SRVs, volatile descriptors)</span></span> |
| <span data-ttu-id="44889-203">\[5\]</span><span class="sxs-lookup"><span data-stu-id="44889-203">\[5\]</span></span>                  | <span data-ttu-id="44889-204">Tabela de descritores: {(T0, space1) – não associado}</span><span class="sxs-lookup"><span data-stu-id="44889-204">Descriptor table: { (t0, space1) - unbounded }</span></span> | <span data-ttu-id="44889-205">(não limitado \# de SRVs, descritores voláteis)</span><span class="sxs-lookup"><span data-stu-id="44889-205">(unbounded \# of SRVs, volatile descriptors)</span></span> |
| <span data-ttu-id="44889-206">\[6\]</span><span class="sxs-lookup"><span data-stu-id="44889-206">\[6\]</span></span>                  | <span data-ttu-id="44889-207">Tabela de descritores: {B1}</span><span class="sxs-lookup"><span data-stu-id="44889-207">Descriptor table: { b1 }</span></span>                       | <span data-ttu-id="44889-208">(1 CBV, dados estáticos)</span><span class="sxs-lookup"><span data-stu-id="44889-208">(1 CBV, static data)</span></span>                         |



 

<span data-ttu-id="44889-209">Se a maioria das partes da assinatura raiz for usada na maior parte do tempo, pode ser melhor ter que mudar a assinatura raiz com muita frequência.</span><span class="sxs-lookup"><span data-stu-id="44889-209">If most parts of the root signature get used most of the time it can be better than having to switch the root signature too frequently.</span></span> <span data-ttu-id="44889-210">Os aplicativos devem classificar as entradas na assinatura raiz da alteração mais frequente para o mínimo.</span><span class="sxs-lookup"><span data-stu-id="44889-210">Applications should sort entries in the root signature from most frequently changing to least.</span></span> <span data-ttu-id="44889-211">Quando um aplicativo altera as associações para qualquer parte da assinatura raiz, o driver pode ter que fazer uma cópia de algum ou de todo o estado de assinatura raiz, o que pode se tornar um custo não trivial quando multiplicado por muitas alterações de estado.</span><span class="sxs-lookup"><span data-stu-id="44889-211">When an app changes the bindings to any part of the root signature, the driver may have to make a copy of some or all of root signature state, which can become a nontrivial cost when multiplied across many state changes.</span></span>

<span data-ttu-id="44889-212">Além disso, a assinatura raiz definirá uma amostra estática que faz a filtragem de textura anisotropic no sombreador de registro S3.</span><span class="sxs-lookup"><span data-stu-id="44889-212">In addition, the root signature will define a static sampler that does anisotropic texture filtering at shader register s3.</span></span>

<span data-ttu-id="44889-213">Depois que essa assinatura raiz é associada, as tabelas de descritores, CBV e constantes raiz podem ser atribuídas ao \[ espaço de parâmetro 0.. 6 \] .</span><span class="sxs-lookup"><span data-stu-id="44889-213">After this root signature is bound, descriptor tables, root CBV and constants can be assigned to the \[0..6\] parameter space.</span></span> <span data-ttu-id="44889-214">por exemplo, as tabelas de descritores (intervalos em um heap de descritor) podem ser associadas a cada um dos parâmetros de raiz \[ 1 \] e \[ 3.. 6 \] .</span><span class="sxs-lookup"><span data-stu-id="44889-214">e.g. descriptor tables (ranges in a descriptor heap) can be bound at each of root parameters \[1\] and \[3..6\].</span></span>

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

<span data-ttu-id="44889-215">O código a seguir ilustra como a assinatura raiz acima pode ser usada em uma lista de comandos gráficos.</span><span class="sxs-lookup"><span data-stu-id="44889-215">The following code illustrates how the above root signature might be used on a graphics command list.</span></span>

``` syntax
InitializeMyDescriptorHeapContentsAheadOfTime(); // for simplicity of the 
                                                 // example
CreatePipelineStatesAhreadOfTime(pRootSignature); // The root signature is passed into 
                                     // shader / pipeline state creation
...

ID3D12DescriptorHeap* pHeaps[2] = {pCommonHeap, pSamplerHeap};
pGraphicsCommandList->SetDescriptorHeaps(2,pHeaps);
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

## <a name="related-topics"></a><span data-ttu-id="44889-216">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="44889-216">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44889-217">Assinaturas raiz</span><span class="sxs-lookup"><span data-stu-id="44889-217">Root Signatures</span></span>](root-signatures.md)
</dt> <dt>

[<span data-ttu-id="44889-218">Como especificar assinaturas raiz no HLSL</span><span class="sxs-lookup"><span data-stu-id="44889-218">Specifying Root Signatures in HLSL</span></span>](specifying-root-signatures-in-hlsl.md)
</dt> <dt>

[<span data-ttu-id="44889-219">Como usar uma assinatura raiz</span><span class="sxs-lookup"><span data-stu-id="44889-219">Using a Root Signature</span></span>](using-a-root-signature.md)
</dt> </dl>

 

 
