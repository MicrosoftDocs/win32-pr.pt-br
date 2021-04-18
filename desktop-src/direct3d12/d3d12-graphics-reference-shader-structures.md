---
title: Estruturas de sombreador (gráficos do Direct3D 12)
description: d3d12shader. h declara as seguintes estruturas, que são usadas para criar e usar sombreadores.
ms.assetid: b8ece5c3-5065-4711-b12c-6cf7ea0e1ba0
keywords:
- estruturas, Direct3D 12 shaders
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 400d50c48b8b94fc9a59d8e48179aae43e14a4f5
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105781199"
---
# <a name="shader-structures-direct3d-12-graphics"></a><span data-ttu-id="9507e-104">Estruturas de sombreador (gráficos do Direct3D 12)</span><span class="sxs-lookup"><span data-stu-id="9507e-104">Shader Structures (Direct3D 12 Graphics)</span></span>

<span data-ttu-id="9507e-105">d3d12shader. h declara as seguintes estruturas, que são usadas para criar e usar sombreadores.</span><span class="sxs-lookup"><span data-stu-id="9507e-105">d3d12shader.h declares the following structures, which are used to create and use shaders.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9507e-106">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="9507e-106">In this section</span></span>



| <span data-ttu-id="9507e-107">Tópico</span><span class="sxs-lookup"><span data-stu-id="9507e-107">Topic</span></span>                                                                                  | <span data-ttu-id="9507e-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="9507e-108">Description</span></span>                                                             |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="9507e-109">**\_Função D3D12 \_ desc**</span><span class="sxs-lookup"><span data-stu-id="9507e-109">**D3D12\_FUNCTION\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_function_desc)<br/>                        | <span data-ttu-id="9507e-110">Descreve uma função.</span><span class="sxs-lookup"><span data-stu-id="9507e-110">Describes a function.</span></span> <br/>                                       |
| [<span data-ttu-id="9507e-111">**\_Desc de biblioteca D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="9507e-111">**D3D12\_LIBRARY\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_library_desc)<br/>                          | <span data-ttu-id="9507e-112">Descreve uma biblioteca do.</span><span class="sxs-lookup"><span data-stu-id="9507e-112">Describes a library.</span></span> <br/>                                        |
| [<span data-ttu-id="9507e-113">**D3D12 do \_ parâmetro \_ desc**</span><span class="sxs-lookup"><span data-stu-id="9507e-113">**D3D12\_PARAMETER\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_parameter_desc)<br/>                      | <span data-ttu-id="9507e-114">Descreve um parâmetro de função.</span><span class="sxs-lookup"><span data-stu-id="9507e-114">Describes a function parameter.</span></span> <br/>                             |
| [<span data-ttu-id="9507e-115">**\_Desc buffer de sombreador D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9507e-115">**D3D12\_SHADER\_BUFFER\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_shader_buffer_desc)<br/>             | <span data-ttu-id="9507e-116">Descreve um buffer de constante de sombreador.</span><span class="sxs-lookup"><span data-stu-id="9507e-116">Describes a shader constant-buffer.</span></span> <br/>                         |
| [<span data-ttu-id="9507e-117">**D3D12 de \_ sombreador \_ desc**</span><span class="sxs-lookup"><span data-stu-id="9507e-117">**D3D12\_SHADER\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_shader_desc)<br/>                            | <span data-ttu-id="9507e-118">Descreve um sombreador.</span><span class="sxs-lookup"><span data-stu-id="9507e-118">Describes a shader.</span></span> <br/>                                         |
| [<span data-ttu-id="9507e-119">**\_Desc de \_ entrada de SOMBREAdor D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9507e-119">**D3D12\_SHADER\_INPUT\_BIND\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_shader_input_bind_desc)<br/>    | <span data-ttu-id="9507e-120">Descreve como um recurso de sombreador está associado a uma entrada de sombreador.</span><span class="sxs-lookup"><span data-stu-id="9507e-120">Describes how a shader resource is bound to a shader input.</span></span> <br/> |
| [<span data-ttu-id="9507e-121">**D3D12 \_ sombreador \_ tipo \_ desc**</span><span class="sxs-lookup"><span data-stu-id="9507e-121">**D3D12\_SHADER\_TYPE\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_shader_type_desc)<br/>                 | <span data-ttu-id="9507e-122">Descreve um tipo de variável de sombreador.</span><span class="sxs-lookup"><span data-stu-id="9507e-122">Describes a shader-variable type.</span></span> <br/>                           |
| [<span data-ttu-id="9507e-123">**\_Variável de sombreador D3D12 \_ \_ desc**</span><span class="sxs-lookup"><span data-stu-id="9507e-123">**D3D12\_SHADER\_VARIABLE\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_shader_variable_desc)<br/>         | <span data-ttu-id="9507e-124">Descreve uma variável de sombreador.</span><span class="sxs-lookup"><span data-stu-id="9507e-124">Describes a shader variable.</span></span> <br/>                                |
| [<span data-ttu-id="9507e-125">**D3D12 \_ de \_ parâmetro de assinatura \_ desc**</span><span class="sxs-lookup"><span data-stu-id="9507e-125">**D3D12\_SIGNATURE\_PARAMETER\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_signature_parameter_desc)<br/> | <span data-ttu-id="9507e-126">Descreve uma assinatura de sombreador.</span><span class="sxs-lookup"><span data-stu-id="9507e-126">Describes a shader signature.</span></span> <br/>                               |



 

## <a name="related-topics"></a><span data-ttu-id="9507e-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9507e-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9507e-128">Referência do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="9507e-128">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> <dt>

[<span data-ttu-id="9507e-129">Referência do sombreador</span><span class="sxs-lookup"><span data-stu-id="9507e-129">Shader Reference</span></span>](d3d12-graphics-reference-shader-reference.md)
</dt> </dl>

 

 





