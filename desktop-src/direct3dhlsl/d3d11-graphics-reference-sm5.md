---
title: Modelo de sombreador 5
description: Esta seção contém as páginas de referência para o HLSL Shader Model 5.
ms.assetid: ec646940-8901-45c5-a44c-434c8acae2aa
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f379301008190367a40959a319d01cfad127f6b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366210"
---
# <a name="shader-model-5"></a><span data-ttu-id="bee19-103">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="bee19-103">Shader Model 5</span></span>

<span data-ttu-id="bee19-104">Esta seção contém as páginas de referência para o HLSL Shader Model 5.</span><span class="sxs-lookup"><span data-stu-id="bee19-104">This section contains the reference pages for HLSL Shader Model 5.</span></span>

<span data-ttu-id="bee19-105">O Shader Model 5 é um superconjunto dos recursos no [Shader Model 4](dx-graphics-hlsl-sm4.md).</span><span class="sxs-lookup"><span data-stu-id="bee19-105">Shader Model 5 is a superset of the capabilites in [Shader Model 4](dx-graphics-hlsl-sm4.md).</span></span> <span data-ttu-id="bee19-106">Ele foi projetado usando um núcleo de sombreador comum que fornece um conjunto comum de recursos para todos os sombreadores programáveis, que só podem ser programados usando HLSL.</span><span class="sxs-lookup"><span data-stu-id="bee19-106">It has been designed using a common-shader core which provides a common set of features to all programmable shaders, which are only programmable using HLSL.</span></span>



| <span data-ttu-id="bee19-107">Recurso</span><span class="sxs-lookup"><span data-stu-id="bee19-107">Feature</span></span>                   | <span data-ttu-id="bee19-108">Funcionalidade</span><span class="sxs-lookup"><span data-stu-id="bee19-108">Capability</span></span>                                                                                                                                             |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bee19-109">Conjunto de instruções</span><span class="sxs-lookup"><span data-stu-id="bee19-109">Instruction Set</span></span>           | [<span data-ttu-id="bee19-110">**Funções intrínsecas HLSL**</span><span class="sxs-lookup"><span data-stu-id="bee19-110">**HLSL intrinsic functions**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                                               |
| <span data-ttu-id="bee19-111">Sombreador máximo do vértice</span><span class="sxs-lookup"><span data-stu-id="bee19-111">Vertex Shader Max</span></span>         | <span data-ttu-id="bee19-112">Nenhuma restrição</span><span class="sxs-lookup"><span data-stu-id="bee19-112">No restriction</span></span>                                                                                                                                         |
| <span data-ttu-id="bee19-113">Sombreador máximo de pixel</span><span class="sxs-lookup"><span data-stu-id="bee19-113">Pixel Shader Max</span></span>          | <span data-ttu-id="bee19-114">Nenhuma restrição</span><span class="sxs-lookup"><span data-stu-id="bee19-114">No restriction</span></span>                                                                                                                                         |
| <span data-ttu-id="bee19-115">Novos perfis de sombreador adicionados</span><span class="sxs-lookup"><span data-stu-id="bee19-115">New Shader Profiles Added</span></span> | <span data-ttu-id="bee19-116">cs \_ 4 \_ 0, GS \_ 4 \_ 0 \* , PS \_ 4 \_ 0 \* , vs \_ 4 \_ 0 \* , cs \_ 4 \_ 1, GS \_ 4 \_ 1 \* , PS \_ 4 \_ 1 \* , vs \_ 4 \_ 1 \* , cs \_ 5 0, DS 5 0, GS 5 0, HS 5 0, \_ \_ \_ \_ \_ \_ \_ PS \_ 5 \_ 0, vs \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bee19-116">cs\_4\_0, gs\_4\_0\*, ps\_4\_0\*, vs\_4\_0\*, cs\_4\_1, gs\_4\_1\*, ps\_4\_1\*, vs\_4\_1\*, cs\_5\_0, ds\_5\_0, gs\_5\_0, hs\_5\_0, ps\_5\_0, vs\_5\_0</span></span> |



 

<span data-ttu-id="bee19-117">\* -GS \_ 4 \_ 0, GS \_ 4 \_ 1, PS \_ 4 \_ 0, PS \_ 4 \_ 1, vs \_ 4 \_ 0 e vs \_ 4 \_ 1 foram introduzidos no modelo do sombreador 4,0, no entanto, o DirectX 11 adiciona suporte para [buffers estruturados](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) e buffers de endereço de bytes para o modelo do sombreador 4 em execução no hardware do DirectX 10.</span><span class="sxs-lookup"><span data-stu-id="bee19-117">\* - gs\_4\_0, gs\_4\_1, ps\_4\_0, ps\_4\_1, vs\_4\_0 and vs\_4\_1 were introduced in Shader Model 4.0, however, DirectX 11 adds support for [structured buffers](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) and byte address buffers to Shader Model 4 running on DirectX 10 hardware.</span></span>

<span data-ttu-id="bee19-118">O Shader Model 5 apresenta o [sombreador de computação](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader) que fornece computação de uso geral de alta velocidade.</span><span class="sxs-lookup"><span data-stu-id="bee19-118">Shader Model 5 introduces the [compute shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader) which provides high-speed general purpose computing.</span></span>

<span data-ttu-id="bee19-119">Uma lista mais completa dos recursos do Shader Model 5 está incluída na listagem dos [recursos do Direct3D 11](/windows/desktop/direct3d11/direct3d-11-features).</span><span class="sxs-lookup"><span data-stu-id="bee19-119">A more complete listing of Shader Model 5 features is included in a listing of the [Direct3D 11 features](/windows/desktop/direct3d11/direct3d-11-features).</span></span>

<span data-ttu-id="bee19-120">A seção de [assembly do Shader Model 5](shader-model-5-assembly--directx-hlsl-.md) descreve as instruções do assembly com suporte no modelo do sombreador 5.</span><span class="sxs-lookup"><span data-stu-id="bee19-120">The [Shader Model 5 Assembly](shader-model-5-assembly--directx-hlsl-.md) section describes the assembly instructions that the Shader Model 5 supports.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="bee19-121">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="bee19-121">In This Section</span></span>



| <span data-ttu-id="bee19-122">Item</span><span class="sxs-lookup"><span data-stu-id="bee19-122">Item</span></span>                                                                                                                                                                                                                                                        | <span data-ttu-id="bee19-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="bee19-123">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="bee19-124"><span id="Shader_Model_5_Attributes"></span><span id="shader_model_5_attributes"></span><span id="SHADER_MODEL_5_ATTRIBUTES"></span>[Atributos do Shader Model 5](d3d11-graphics-reference-sm5-attributes.md)</span><span class="sxs-lookup"><span data-stu-id="bee19-124"><span id="Shader_Model_5_Attributes"></span><span id="shader_model_5_attributes"></span><span id="SHADER_MODEL_5_ATTRIBUTES"></span>[Shader Model 5 Attributes](d3d11-graphics-reference-sm5-attributes.md)</span></span><br/>                                     | <span data-ttu-id="bee19-125">Páginas de referência para atributos do Shader Model 5.</span><span class="sxs-lookup"><span data-stu-id="bee19-125">Reference pages for Shader Model 5 attributes.</span></span><br/>          |
| <span data-ttu-id="bee19-126"><span id="Shader_Model_5_Intrinsic_Functions"></span><span id="shader_model_5_intrinsic_functions"></span><span id="SHADER_MODEL_5_INTRINSIC_FUNCTIONS"></span>[Funções intrínsecas do modelo de sombreador 5](d3d11-graphics-reference-sm5-intrinsics.md)</span><span class="sxs-lookup"><span data-stu-id="bee19-126"><span id="Shader_Model_5_Intrinsic_Functions"></span><span id="shader_model_5_intrinsic_functions"></span><span id="SHADER_MODEL_5_INTRINSIC_FUNCTIONS"></span>[Shader Model 5 Intrinsic Functions](d3d11-graphics-reference-sm5-intrinsics.md)</span></span><br/> | <span data-ttu-id="bee19-127">Páginas de referência para funções intrínsecas do modelo de sombreador 5.</span><span class="sxs-lookup"><span data-stu-id="bee19-127">Reference pages for Shader Model 5 intrinsic functions.</span></span><br/> |
| <span data-ttu-id="bee19-128"><span id="Shader_Model_5_Objects"></span><span id="shader_model_5_objects"></span><span id="SHADER_MODEL_5_OBJECTS"></span>[Objetos do Shader Model 5](d3d11-graphics-reference-sm5-objects.md)</span><span class="sxs-lookup"><span data-stu-id="bee19-128"><span id="Shader_Model_5_Objects"></span><span id="shader_model_5_objects"></span><span id="SHADER_MODEL_5_OBJECTS"></span>[Shader Model 5 Objects](d3d11-graphics-reference-sm5-objects.md)</span></span><br/>                                                    | <span data-ttu-id="bee19-129">Páginas de referência para objetos e métodos do Shader Model 5.</span><span class="sxs-lookup"><span data-stu-id="bee19-129">Reference pages for Shader Model 5 objects and methods.</span></span><br/> |
| <span data-ttu-id="bee19-130"><span id="Shader_Model_5_System_Values"></span><span id="shader_model_5_system_values"></span><span id="SHADER_MODEL_5_SYSTEM_VALUES"></span>[Valores de sistema do Shader Model 5](d3d11-graphics-reference-sm5-system-values.md)</span><span class="sxs-lookup"><span data-stu-id="bee19-130"><span id="Shader_Model_5_System_Values"></span><span id="shader_model_5_system_values"></span><span id="SHADER_MODEL_5_SYSTEM_VALUES"></span>[Shader Model 5 System Values](d3d11-graphics-reference-sm5-system-values.md)</span></span><br/>                      | <span data-ttu-id="bee19-131">Páginas de referência para valores de sistema do Shader Model 5.</span><span class="sxs-lookup"><span data-stu-id="bee19-131">Reference pages for Shader Model 5 system values.</span></span><br/>       |



 

## <a name="related-topics"></a><span data-ttu-id="bee19-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bee19-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bee19-133">Modelos de sombreador vs. perfis de sombreador</span><span class="sxs-lookup"><span data-stu-id="bee19-133">Shader Models vs Shader Profiles</span></span>](dx-graphics-hlsl-models.md)
</dt> </dl>

 

