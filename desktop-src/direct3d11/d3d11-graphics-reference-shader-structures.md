---
title: Estruturas de sombreador (gráficos do Direct3D 11)
description: As estruturas são usadas para criar e usar sombreadores.
ms.assetid: 3b8ece5c-5065-4711-b12c-06cf7ea0e1ba
keywords:
- estruturas, sombreadores do Direct3D 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14739e3db38c075e19e58a90b12bbf7d06b48a4e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103644172"
---
# <a name="shader-structures-direct3d-11-graphics"></a><span data-ttu-id="23104-104">Estruturas de sombreador (gráficos do Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="23104-104">Shader Structures (Direct3D 11 Graphics)</span></span>

<span data-ttu-id="23104-105">As estruturas são usadas para criar e usar sombreadores.</span><span class="sxs-lookup"><span data-stu-id="23104-105">Structures are used to create and use shaders.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="23104-106">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="23104-106">In this section</span></span>



| <span data-ttu-id="23104-107">Tópico</span><span class="sxs-lookup"><span data-stu-id="23104-107">Topic</span></span>                                                                                       | <span data-ttu-id="23104-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="23104-108">Description</span></span>                                                            |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="23104-109">**\_Desc de \_ instância de classe D3D11 \_**</span><span class="sxs-lookup"><span data-stu-id="23104-109">**D3D11\_CLASS\_INSTANCE\_DESC**</span></span>](/windows/desktop/api/D3D11/ns-d3d11-d3d11_class_instance_desc)<br/>                | <span data-ttu-id="23104-110">Descreve uma instância de classe HLSL.</span><span class="sxs-lookup"><span data-stu-id="23104-110">Describes an HLSL class instance.</span></span><br/>                           |
| [<span data-ttu-id="23104-111">**\_Desc de \_ rastreamento de sombreador de computação D3D11 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="23104-111">**D3D11\_COMPUTE\_SHADER\_TRACE\_DESC**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_compute_shader_trace_desc)<br/>   | <span data-ttu-id="23104-112">Descreve uma instância de um sombreador de computação a ser rastreado.</span><span class="sxs-lookup"><span data-stu-id="23104-112">Describes an instance of a compute shader to trace.</span></span><br/>         |
| [<span data-ttu-id="23104-113">**\_Desc de \_ rastreamento de sombreador de domínio D3D11 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="23104-113">**D3D11\_DOMAIN\_SHADER\_TRACE\_DESC**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_domain_shader_trace_desc)<br/>     | <span data-ttu-id="23104-114">Descreve uma instância de um sombreador de domínio para rastrear.</span><span class="sxs-lookup"><span data-stu-id="23104-114">Describes an instance of a domain shader to trace.</span></span><br/>          |
| [<span data-ttu-id="23104-115">**\_Função D3D11 \_ desc**</span><span class="sxs-lookup"><span data-stu-id="23104-115">**D3D11\_FUNCTION\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_function_desc)<br/>                             | <span data-ttu-id="23104-116">Descreve uma função.</span><span class="sxs-lookup"><span data-stu-id="23104-116">Describes a function.</span></span><br/>                                       |
| [<span data-ttu-id="23104-117">**\_Desc de \_ rastreamento de sombreador de geometria D3D11 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="23104-117">**D3D11\_GEOMETRY\_SHADER\_TRACE\_DESC**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_geometry_shader_trace_desc)<br/> | <span data-ttu-id="23104-118">Descreve uma instância de um sombreador Geometry a ser rastreado.</span><span class="sxs-lookup"><span data-stu-id="23104-118">Describes an instance of a geometry shader to trace.</span></span><br/>        |
| [<span data-ttu-id="23104-119">**Desc. de \_ \_ rastreamento de sombreador D3D11 envoltória \_ \_**</span><span class="sxs-lookup"><span data-stu-id="23104-119">**D3D11\_HULL\_SHADER\_TRACE\_DESC**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_hull_shader_trace_desc)<br/>         | <span data-ttu-id="23104-120">Descreve uma instância de um sombreador envoltória para rastrear.</span><span class="sxs-lookup"><span data-stu-id="23104-120">Describes an instance of a hull shader to trace.</span></span><br/>            |
| [<span data-ttu-id="23104-121">**\_Desc de biblioteca D3D11 \_**</span><span class="sxs-lookup"><span data-stu-id="23104-121">**D3D11\_LIBRARY\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_library_desc)<br/>                               | <span data-ttu-id="23104-122">Descreve uma biblioteca do.</span><span class="sxs-lookup"><span data-stu-id="23104-122">Describes a library.</span></span><br/>                                        |
| [<span data-ttu-id="23104-123">**D3D11 do \_ parâmetro \_ desc**</span><span class="sxs-lookup"><span data-stu-id="23104-123">**D3D11\_PARAMETER\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_parameter_desc)<br/>                           | <span data-ttu-id="23104-124">Descreve um parâmetro de função.</span><span class="sxs-lookup"><span data-stu-id="23104-124">Describes a function parameter.</span></span> <br/>                            |
| [<span data-ttu-id="23104-125">**\_Desc de \_ rastreamento de sombreador de pixel D3D11 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="23104-125">**D3D11\_PIXEL\_SHADER\_TRACE\_DESC**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_pixel_shader_trace_desc)<br/>       | <span data-ttu-id="23104-126">Descreve uma instância de um sombreador de pixel para rastreamento.</span><span class="sxs-lookup"><span data-stu-id="23104-126">Describes an instance of a pixel shader to trace.</span></span><br/>           |
| [<span data-ttu-id="23104-127">**\_Desc buffer de sombreador D3D11 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="23104-127">**D3D11\_SHADER\_BUFFER\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_buffer_desc)<br/>                  | <span data-ttu-id="23104-128">Descreve um buffer de constante de sombreador.</span><span class="sxs-lookup"><span data-stu-id="23104-128">Describes a shader constant-buffer.</span></span><br/>                         |
| [<span data-ttu-id="23104-129">**D3D11 de \_ sombreador \_ desc**</span><span class="sxs-lookup"><span data-stu-id="23104-129">**D3D11\_SHADER\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_desc)<br/>                                 | <span data-ttu-id="23104-130">Descreve um sombreador.</span><span class="sxs-lookup"><span data-stu-id="23104-130">Describes a shader.</span></span><br/>                                         |
| [<span data-ttu-id="23104-131">**\_Desc de \_ entrada de SOMBREAdor D3D11 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="23104-131">**D3D11\_SHADER\_INPUT\_BIND\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_input_bind_desc)<br/>         | <span data-ttu-id="23104-132">Descreve como um recurso de sombreador está associado a uma entrada de sombreador.</span><span class="sxs-lookup"><span data-stu-id="23104-132">Describes how a shader resource is bound to a shader input.</span></span><br/> |
| [<span data-ttu-id="23104-133">**\_Desc de rastreamento do sombreador D3D11 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="23104-133">**D3D11\_SHADER\_TRACE\_DESC**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_shader_trace_desc)<br/>                    | <span data-ttu-id="23104-134">Descreve um objeto de rastreamento de sombreador.</span><span class="sxs-lookup"><span data-stu-id="23104-134">Describes a shader-trace object.</span></span><br/>                            |
| [<span data-ttu-id="23104-135">**D3D11 \_ sombreador \_ tipo \_ desc**</span><span class="sxs-lookup"><span data-stu-id="23104-135">**D3D11\_SHADER\_TYPE\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_type_desc)<br/>                      | <span data-ttu-id="23104-136">Descreve um tipo de variável de sombreador.</span><span class="sxs-lookup"><span data-stu-id="23104-136">Describes a shader-variable type.</span></span><br/>                           |
| [<span data-ttu-id="23104-137">**\_Variável de sombreador D3D11 \_ \_ desc**</span><span class="sxs-lookup"><span data-stu-id="23104-137">**D3D11\_SHADER\_VARIABLE\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_variable_desc)<br/>              | <span data-ttu-id="23104-138">Descreve uma variável de sombreador.</span><span class="sxs-lookup"><span data-stu-id="23104-138">Describes a shader variable.</span></span><br/>                                |
| [<span data-ttu-id="23104-139">**D3D11 \_ de \_ parâmetro de assinatura \_ desc**</span><span class="sxs-lookup"><span data-stu-id="23104-139">**D3D11\_SIGNATURE\_PARAMETER\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)<br/>      | <span data-ttu-id="23104-140">Descreve uma assinatura de sombreador.</span><span class="sxs-lookup"><span data-stu-id="23104-140">Describes a shader signature.</span></span><br/>                               |
| [<span data-ttu-id="23104-141">**\_Registro de rastreamento do D3D11 \_**</span><span class="sxs-lookup"><span data-stu-id="23104-141">**D3D11\_TRACE\_REGISTER**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_register)<br/>                           | <span data-ttu-id="23104-142">Descreve um registro de rastreamento.</span><span class="sxs-lookup"><span data-stu-id="23104-142">Describes a trace register.</span></span><br/>                                 |
| [<span data-ttu-id="23104-143">**\_Estatísticas de rastreamento do D3D11 \_**</span><span class="sxs-lookup"><span data-stu-id="23104-143">**D3D11\_TRACE\_STATS**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_stats)<br/>                                 | <span data-ttu-id="23104-144">Especifica estatísticas sobre um rastreamento.</span><span class="sxs-lookup"><span data-stu-id="23104-144">Specifies statistics about a trace.</span></span><br/>                         |
| [<span data-ttu-id="23104-145">**\_Etapa de rastreamento de D3D11 \_**</span><span class="sxs-lookup"><span data-stu-id="23104-145">**D3D11\_TRACE\_STEP**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_step)<br/>                                   | <span data-ttu-id="23104-146">Descreve uma etapa de rastreamento, que é uma instrução.</span><span class="sxs-lookup"><span data-stu-id="23104-146">Describes a trace step, which is an instruction.</span></span><br/>            |
| [<span data-ttu-id="23104-147">**\_Valor de rastreamento de D3D11 \_**</span><span class="sxs-lookup"><span data-stu-id="23104-147">**D3D11\_TRACE\_VALUE**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_value)<br/>                                 | <span data-ttu-id="23104-148">Descreve um valor de rastreamento.</span><span class="sxs-lookup"><span data-stu-id="23104-148">Describes a trace value.</span></span><br/>                                    |
| [<span data-ttu-id="23104-149">**\_Desc de \_ rastreamento de sombreador de vértice D3D11 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="23104-149">**D3D11\_VERTEX\_SHADER\_TRACE\_DESC**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_vertex_shader_trace_desc)<br/>     | <span data-ttu-id="23104-150">Descreve uma instância de um sombreador de vértice a ser rastreado.</span><span class="sxs-lookup"><span data-stu-id="23104-150">Describes an instance of a vertex shader to trace.</span></span><br/>          |



 

## <a name="related-topics"></a><span data-ttu-id="23104-151">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="23104-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23104-152">Referência do sombreador</span><span class="sxs-lookup"><span data-stu-id="23104-152">Shader Reference</span></span>](d3d11-graphics-reference-d3d11-shader.md)
</dt> </dl>

 

 





