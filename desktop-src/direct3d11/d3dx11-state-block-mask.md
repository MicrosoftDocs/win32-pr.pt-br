---
title: Estrutura de D3DX11_STATE_BLOCK_MASK (D3dx11effect. h)
description: Indica o estado do dispositivo.
ms.assetid: 42044a6d-6a11-4f90-889a-82e7954da6c7
keywords:
- Estrutura D3DX11_STATE_BLOCK_MASK Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_STATE_BLOCK_MASK
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41236c541fc251902a7a0a5ad6030a28dd36e3a4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298721"
---
# <a name="d3dx11_state_block_mask-structure"></a><span data-ttu-id="b3535-104">\_Estrutura de \_ máscara de bloco de estado D3DX11 \_</span><span class="sxs-lookup"><span data-stu-id="b3535-104">D3DX11\_STATE\_BLOCK\_MASK structure</span></span>

<span data-ttu-id="b3535-105">Indica o estado do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b3535-105">Indicates the device state.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3535-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b3535-106">Syntax</span></span>


```C++
typedef struct _D3DX11_STATE_BLOCK_MASK {
  BYTE VS;
  BYTE VSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE VSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE VSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE VSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE HS;
  BYTE HSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE HSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE HSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE HSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE DS;
  BYTE DSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE DSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE DSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE DSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE GS;
  BYTE GSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE GSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE GSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE GSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE PS;
  BYTE PSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE PSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE PSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE PSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE PSUnorderedAccessViews;
  BYTE CS;
  BYTE CSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE CSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE CSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE CSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE CSUnorderedAccessViews;
  BYTE IAVertexBuffers[D3DX11_BYTES_FROM_BITS(D3D11_IA_VERTEX_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE IAIndexBuffer;
  BYTE IAInputLayout;
  BYTE IAPrimitiveTopology;
  BYTE OMRenderTargets;
  BYTE OMDepthStencilState;
  BYTE OMBlendState;
  BYTE RSViewports;
  BYTE RSScissorRects;
  BYTE RSRasterizerState;
  BYTE SOBuffers;
  BYTE Predication;
} D3DX11_STATE_BLOCK_MASK;
```



## <a name="members"></a><span data-ttu-id="b3535-107">Membros</span><span class="sxs-lookup"><span data-stu-id="b3535-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="b3535-108">**VS**</span><span class="sxs-lookup"><span data-stu-id="b3535-108">**VS**</span></span>
</dt> <dd>

<span data-ttu-id="b3535-109">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b3535-109">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b3535-110">Valor booliano que indica se o estado do sombreador de vértice deve ser salvo.</span><span class="sxs-lookup"><span data-stu-id="b3535-110">Boolean value indicating whether to save the vertex shader state.</span></span>

</dd> <dt>

<span data-ttu-id="b3535-111">**VSSamplers**</span><span class="sxs-lookup"><span data-stu-id="b3535-111">**VSSamplers**</span></span>
</dt> <dd>

<span data-ttu-id="b3535-112">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b3535-112">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b3535-113">Matriz de amostras de Vertex-Shader.</span><span class="sxs-lookup"><span data-stu-id="b3535-113">Array of vertex-shader samplers.</span></span> <span data-ttu-id="b3535-114">A matriz é um bitmask de vários bytes em que cada bit representa um slot de amostra.</span><span class="sxs-lookup"><span data-stu-id="b3535-114">The array is a multi-byte bitmask where each bit represents one sampler slot.</span></span>

</dd> <dt>

<span data-ttu-id="b3535-115">**VSShaderResources**</span><span class="sxs-lookup"><span data-stu-id="b3535-115">**VSShaderResources**</span></span>
</dt> <dd>

<span data-ttu-id="b3535-116">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b3535-116">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b3535-117">Matriz de recursos de sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="b3535-117">Array of vertex-shader resources.</span></span> <span data-ttu-id="b3535-118">A matriz é um bitmask de vários bytes em que cada bit representa um slot de recurso.</span><span class="sxs-lookup"><span data-stu-id="b3535-118">The array is a multi-byte bitmask where each bit represents one resource slot.</span></span>

</dd> <dt>

<span data-ttu-id="b3535-119">**VSConstantBuffers**</span><span class="sxs-lookup"><span data-stu-id="b3535-119">**VSConstantBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="b3535-120">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b3535-120">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b3535-121">Matriz de buffers de constante de sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="b3535-121">Array of vertex-shader constant buffers.</span></span> <span data-ttu-id="b3535-122">A matriz é um bitmask de vários bytes em que cada bit representa um slot de buffer constante.</span><span class="sxs-lookup"><span data-stu-id="b3535-122">The array is a multi-byte bitmask where each bit represents one constant buffer slot.</span></span>

</dd> <dt>

<span data-ttu-id="b3535-123">**VSInterfaces**</span><span class="sxs-lookup"><span data-stu-id="b3535-123">**VSInterfaces**</span></span>
</dt> <dd>

<span data-ttu-id="b3535-124">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b3535-124">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b3535-125">Matriz de interfaces de sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="b3535-125">Array of vertex-shader interfaces.</span></span> <span data-ttu-id="b3535-126">A matriz é um bitmask de vários bytes em que cada bit representa um slot de interface.</span><span class="sxs-lookup"><span data-stu-id="b3535-126">The array is a multi-byte bitmask where each bit represents one interface slot.</span></span>

</dd> <dt>

<span data-ttu-id="b3535-127">**HS**</span><span class="sxs-lookup"><span data-stu-id="b3535-127">**HS**</span></span>
</dt> <dd>

<span data-ttu-id="b3535-128">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b3535-128">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b3535-129">Valor booliano que indica se o estado do sombreador envoltória deve ser salvo.</span><span class="sxs-lookup"><span data-stu-id="b3535-129">Boolean value indicating whether to save the hull shader state.</span></span>

</dd> <dt>

<span data-ttu-id="b3535-130">**HSSamplers**</span><span class="sxs-lookup"><span data-stu-id="b3535-130">**HSSamplers**</span></span>
</dt> <dd>

<span data-ttu-id="b3535-131">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b3535-131">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b3535-132">Matriz de amostragens envoltória-Shader.</span><span class="sxs-lookup"><span data-stu-id="b3535-132">Array of hull-shader samplers.</span></span> <span data-ttu-id="b3535-133">A matriz é um bitmask de vários bytes em que cada bit representa um slot de amostra.</span><span class="sxs-lookup"><span data-stu-id="b3535-133">The array is a multi-byte bitmask where each bit represents one sampler slot.</span></span>

</dd> <dt>

<span data-ttu-id="b3535-134">**HSShaderResources**</span><span class="sxs-lookup"><span data-stu-id="b3535-134">**HSShaderResources**</span></span>
</dt> <dd>

<span data-ttu-id="b3535-135">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b3535-135">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b3535-136">Matriz de recursos envoltória-Shader.</span><span class="sxs-lookup"><span data-stu-id="b3535-136">Array of hull-shader resources.</span></span> <span data-ttu-id="b3535-137">A matriz é um bitmask de vários bytes em que cada bit representa um slot de recurso.</span><span class="sxs-lookup"><span data-stu-id="b3535-137">The array is a multi-byte bitmask where each bit represents one resource slot.</span></span>

</dd> <dt>

<span data-ttu-id="b3535-138">**HSConstantBuffers**</span><span class="sxs-lookup"><span data-stu-id="b3535-138">**HSConstantBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="b3535-139">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b3535-139">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b3535-140">Matriz de buffers de constante envoltória-Shader.</span><span class="sxs-lookup"><span data-stu-id="b3535-140">Array of hull-shader constant buffers.</span></span> <span data-ttu-id="b3535-141">A matriz é um bitmask de vários bytes em que cada bit representa um slot de buffer constante.</span><span class="sxs-lookup"><span data-stu-id="b3535-141">The array is a multi-byte bitmask where each bit represents one constant buffer slot.</span></span>

</dd> <dt>

<span data-ttu-id="b3535-142">**HSInterfaces**</span><span class="sxs-lookup"><span data-stu-id="b3535-142">**HSInterfaces**</span></span>
</dt> <dd>

<span data-ttu-id="b3535-143">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b3535-143">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b3535-144">Matriz de interfaces envoltória-Shader.</span><span class="sxs-lookup"><span data-stu-id="b3535-144">Array of hull-shader interfaces.</span></span> <span data-ttu-id="b3535-145">A matriz é um bitmask de vários bytes em que cada bit representa um slot de interface.</span><span class="sxs-lookup"><span data-stu-id="b3535-145">The array is a multi-byte bitmask where each bit represents one interface slot.</span></span>

</dd> <dt>

<span data-ttu-id="b3535-146">**AD**</span><span class="sxs-lookup"><span data-stu-id="b3535-146">**DS**</span></span>
</dt> <dd>

<span data-ttu-id="b3535-147">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b3535-147">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b3535-148">Valor booliano que indica se o estado do sombreador do domínio deve ser salvo.</span><span class="sxs-lookup"><span data-stu-id="b3535-148">Boolean value indicating whether to save the domain shader state.</span></span>

</dd> <dt>

<span data-ttu-id="b3535-149">**DSSamplers**</span><span class="sxs-lookup"><span data-stu-id="b3535-149">**DSSamplers**</span></span>
</dt> <dd>

<span data-ttu-id="b3535-150">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b3535-150">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b3535-151">Matriz de amostras de sombreador de domínio.</span><span class="sxs-lookup"><span data-stu-id="b3535-151">Array of domain-shader samplers.</span></span> <span data-ttu-id="b3535-152">A matriz é um bitmask de vários bytes em que cada bit representa um slot de amostra.</span><span class="sxs-lookup"><span data-stu-id="b3535-152">The array is a multi-byte bitmask where each bit represents one sampler slot.</span></span>

</dd> <dt>

<span data-ttu-id="b3535-153">**DSShaderResources**</span><span class="sxs-lookup"><span data-stu-id="b3535-153">**DSShaderResources**</span></span>
</dt> <dd>

<span data-ttu-id="b3535-154">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b3535-154">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b3535-155">Matriz de recursos de sombreador de domínio.</span><span class="sxs-lookup"><span data-stu-id="b3535-155">Array of domain-shader resources.</span></span> <span data-ttu-id="b3535-156">A matriz é um bitmask de vários bytes em que cada bit representa um slot de recurso.</span><span class="sxs-lookup"><span data-stu-id="b3535-156">The array is a multi-byte bitmask where each bit represents one resource slot.</span></span>

</dd> <dt>

<span data-ttu-id="b3535-157">**DSConstantBuffers**</span><span class="sxs-lookup"><span data-stu-id="b3535-157">**DSConstantBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="b3535-158">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b3535-158">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b3535-159">Matriz de buffers de constante de sombreador de domínio.</span><span class="sxs-lookup"><span data-stu-id="b3535-159">Array of domain-shader constant buffers.</span></span> <span data-ttu-id="b3535-160">A matriz é um bitmask de vários bytes em que cada bit representa um slot de buffer.</span><span class="sxs-lookup"><span data-stu-id="b3535-160">The array is a multi-byte bitmask where each bit represents one buffer slot.</span></span>

</dd> <dt>

<span data-ttu-id="b3535-161">**DSInterfaces**</span><span class="sxs-lookup"><span data-stu-id="b3535-161">**DSInterfaces**</span></span>
</dt> <dd>

<span data-ttu-id="b3535-162">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b3535-162">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b3535-163">Matriz de interfaces de sombreador de domínio.</span><span class="sxs-lookup"><span data-stu-id="b3535-163">Array of domain-shader interfaces.</span></span> <span data-ttu-id="b3535-164">A matriz é um bitmask de vários bytes em que cada bit representa um slot de interface.</span><span class="sxs-lookup"><span data-stu-id="b3535-164">The array is a multi-byte bitmask where each bit represents one interface slot.</span></span>

</dd> <dt>

<span data-ttu-id="b3535-165">**GS**</span><span class="sxs-lookup"><span data-stu-id="b3535-165">**GS**</span></span>
</dt> <dd>

<span data-ttu-id="b3535-166">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b3535-166">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b3535-167">Valor booliano que indica se o estado do sombreador de geometria deve ser salvo.</span><span class="sxs-lookup"><span data-stu-id="b3535-167">Boolean value indicating whether to save the geometry shader state.</span></span>

</dd> <dt>

<span data-ttu-id="b3535-168">**GSSamplers**</span><span class="sxs-lookup"><span data-stu-id="b3535-168">**GSSamplers**</span></span>
</dt> <dd>

<span data-ttu-id="b3535-169">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b3535-169">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b3535-170">Matriz de amostragens Geometry-Shader.</span><span class="sxs-lookup"><span data-stu-id="b3535-170">Array of geometry-shader samplers.</span></span> <span data-ttu-id="b3535-171">A matriz é um bitmask de vários bytes em que cada bit representa um slot de amostra.</span><span class="sxs-lookup"><span data-stu-id="b3535-171">The array is a multi-byte bitmask where each bit represents one sampler slot.</span></span>

</dd> <dt>

<span data-ttu-id="b3535-172">**GSShaderResources**</span><span class="sxs-lookup"><span data-stu-id="b3535-172">**GSShaderResources**</span></span>
</dt> <dd>

<span data-ttu-id="b3535-173">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b3535-173">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b3535-174">Matriz de recursos Geometry-Shader.</span><span class="sxs-lookup"><span data-stu-id="b3535-174">Array of geometry-shader resources.</span></span> <span data-ttu-id="b3535-175">A matriz é um bitmask de vários bytes em que cada bit representa um slot de recurso.</span><span class="sxs-lookup"><span data-stu-id="b3535-175">The array is a multi-byte bitmask where each bit represents one resource slot.</span></span>

</dd> <dt>

<span data-ttu-id="b3535-176">**GSConstantBuffers**</span><span class="sxs-lookup"><span data-stu-id="b3535-176">**GSConstantBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="b3535-177">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b3535-177">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b3535-178">Matriz de buffers de constante Geometry-Shader.</span><span class="sxs-lookup"><span data-stu-id="b3535-178">Array of geometry-shader constant buffers.</span></span> <span data-ttu-id="b3535-179">A matriz é um bitmask de vários bytes em que cada bit representa um slot de buffer.</span><span class="sxs-lookup"><span data-stu-id="b3535-179">The array is a multi-byte bitmask where each bit represents one buffer slot.</span></span>

</dd> <dt>

<span data-ttu-id="b3535-180">**GSInterfaces**</span><span class="sxs-lookup"><span data-stu-id="b3535-180">**GSInterfaces**</span></span>
</dt> <dd>

<span data-ttu-id="b3535-181">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b3535-181">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b3535-182">Matriz de interfaces Geometry-Shader.</span><span class="sxs-lookup"><span data-stu-id="b3535-182">Array of geometry-shader interfaces.</span></span> <span data-ttu-id="b3535-183">A matriz é um bitmask de vários bytes em que cada bit representa um slot de interface.</span><span class="sxs-lookup"><span data-stu-id="b3535-183">The array is a multi-byte bitmask where each bit represents one interface slot.</span></span>

</dd> <dt>

<span data-ttu-id="b3535-184">**PROFISSIONAIS**</span><span class="sxs-lookup"><span data-stu-id="b3535-184">**PS**</span></span>
</dt> <dd>

<span data-ttu-id="b3535-185">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b3535-185">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b3535-186">Valor booliano que indica se o estado do sombreador de pixel deve ser salvo.</span><span class="sxs-lookup"><span data-stu-id="b3535-186">Boolean value indicating whether to save the pixel shader state.</span></span>

</dd> <dt>

<span data-ttu-id="b3535-187">**PSSamplers**</span><span class="sxs-lookup"><span data-stu-id="b3535-187">**PSSamplers**</span></span>
</dt> <dd>

<span data-ttu-id="b3535-188">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b3535-188">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b3535-189">Matriz de amostras de sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="b3535-189">Array of pixel-shader samplers.</span></span> <span data-ttu-id="b3535-190">A matriz é um bitmask de vários bytes em que cada bit representa um slot de amostra.</span><span class="sxs-lookup"><span data-stu-id="b3535-190">The array is a multi-byte bitmask where each bit represents one sampler slot.</span></span>

</dd> <dt>

<span data-ttu-id="b3535-191">**PSShaderResources**</span><span class="sxs-lookup"><span data-stu-id="b3535-191">**PSShaderResources**</span></span>
</dt> <dd>

<span data-ttu-id="b3535-192">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b3535-192">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b3535-193">Matriz de recursos de sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="b3535-193">Array of pixel-shader resources.</span></span> <span data-ttu-id="b3535-194">A matriz é um bitmask de vários bytes em que cada bit representa um slot de recurso.</span><span class="sxs-lookup"><span data-stu-id="b3535-194">The array is a multi-byte bitmask where each bit represents one resource slot.</span></span>

</dd> <dt>

<span data-ttu-id="b3535-195">**PSConstantBuffers**</span><span class="sxs-lookup"><span data-stu-id="b3535-195">**PSConstantBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="b3535-196">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b3535-196">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b3535-197">Matriz de buffers de constante de sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="b3535-197">Array of pixel-shader constant buffers.</span></span> <span data-ttu-id="b3535-198">A matriz é um bitmask de vários bytes em que cada bit representa um slot de buffer constante.</span><span class="sxs-lookup"><span data-stu-id="b3535-198">The array is a multi-byte bitmask where each bit represents one constant buffer slot.</span></span>

</dd> <dt>

<span data-ttu-id="b3535-199">**PSInterfaces**</span><span class="sxs-lookup"><span data-stu-id="b3535-199">**PSInterfaces**</span></span>
</dt> <dd>

<span data-ttu-id="b3535-200">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b3535-200">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b3535-201">Matriz de interfaces de sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="b3535-201">Array of pixel-shader interfaces.</span></span> <span data-ttu-id="b3535-202">A matriz é um bitmask de vários bytes em que cada bit representa um slot de interface.</span><span class="sxs-lookup"><span data-stu-id="b3535-202">The array is a multi-byte bitmask where each bit represents one interface slot.</span></span>

</dd> <dt>

<span data-ttu-id="b3535-203">**PSUnorderedAccessViews**</span><span class="sxs-lookup"><span data-stu-id="b3535-203">**PSUnorderedAccessViews**</span></span>
</dt> <dd>

<span data-ttu-id="b3535-204">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b3535-204">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b3535-205">Valor booliano que indica se as exibições de acesso não ordenadas do sombreador de pixel devem ser salvas.</span><span class="sxs-lookup"><span data-stu-id="b3535-205">Boolean value indicating whether to save the pixel shader unordered access views.</span></span>

</dd> <dt>

<span data-ttu-id="b3535-206">**CS**</span><span class="sxs-lookup"><span data-stu-id="b3535-206">**CS**</span></span>
</dt> <dd>

<span data-ttu-id="b3535-207">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b3535-207">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b3535-208">Valor booliano que indica se o estado do sombreador de computação deve ser salvo.</span><span class="sxs-lookup"><span data-stu-id="b3535-208">Boolean value indicating whether to save the compute shader state.</span></span>

</dd> <dt>

<span data-ttu-id="b3535-209">**CSSamplers**</span><span class="sxs-lookup"><span data-stu-id="b3535-209">**CSSamplers**</span></span>
</dt> <dd>

<span data-ttu-id="b3535-210">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b3535-210">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b3535-211">Matriz de amostras de sombreador de computação.</span><span class="sxs-lookup"><span data-stu-id="b3535-211">Array of compute-shader samplers.</span></span> <span data-ttu-id="b3535-212">A matriz é um bitmask de vários bytes em que cada bit representa um slot de amostra.</span><span class="sxs-lookup"><span data-stu-id="b3535-212">The array is a multi-byte bitmask where each bit represents one sampler slot.</span></span>

</dd> <dt>

<span data-ttu-id="b3535-213">**CSShaderResources**</span><span class="sxs-lookup"><span data-stu-id="b3535-213">**CSShaderResources**</span></span>
</dt> <dd>

<span data-ttu-id="b3535-214">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b3535-214">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b3535-215">Matriz de recursos de sombreador de computação.</span><span class="sxs-lookup"><span data-stu-id="b3535-215">Array of compute-shader resources.</span></span> <span data-ttu-id="b3535-216">A matriz é um bitmask de vários bytes em que cada bit representa um slot de recurso.</span><span class="sxs-lookup"><span data-stu-id="b3535-216">The array is a multi-byte bitmask where each bit represents one resource slot.</span></span>

</dd> <dt>

<span data-ttu-id="b3535-217">**CSConstantBuffers**</span><span class="sxs-lookup"><span data-stu-id="b3535-217">**CSConstantBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="b3535-218">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b3535-218">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b3535-219">Matriz de buffers de constante Compute-Shader.</span><span class="sxs-lookup"><span data-stu-id="b3535-219">Array of compute-shader constant buffers.</span></span> <span data-ttu-id="b3535-220">A matriz é um bitmask de vários bytes em que cada bit representa um slot de buffer constante.</span><span class="sxs-lookup"><span data-stu-id="b3535-220">The array is a multi-byte bitmask where each bit represents one constant buffer slot.</span></span>

</dd> <dt>

<span data-ttu-id="b3535-221">**CSInterfaces**</span><span class="sxs-lookup"><span data-stu-id="b3535-221">**CSInterfaces**</span></span>
</dt> <dd>

<span data-ttu-id="b3535-222">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b3535-222">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b3535-223">Matriz de interfaces de sombreador de computação.</span><span class="sxs-lookup"><span data-stu-id="b3535-223">Array of compute-shader interfaces.</span></span> <span data-ttu-id="b3535-224">A matriz é um bitmask de vários bytes em que cada bit representa um slot de interface.</span><span class="sxs-lookup"><span data-stu-id="b3535-224">The array is a multi-byte bitmask where each bit represents one interface slot.</span></span>

</dd> <dt>

<span data-ttu-id="b3535-225">**CSUnorderedAccessViews**</span><span class="sxs-lookup"><span data-stu-id="b3535-225">**CSUnorderedAccessViews**</span></span>
</dt> <dd>

<span data-ttu-id="b3535-226">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b3535-226">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b3535-227">Valor booliano que indica se as exibições de acesso não ordenadas do sombreador de computação devem ser salvas.</span><span class="sxs-lookup"><span data-stu-id="b3535-227">Boolean value indicating whether to save the compute shader unordered access views.</span></span>

</dd> <dt>

<span data-ttu-id="b3535-228">**IAVertexBuffers**</span><span class="sxs-lookup"><span data-stu-id="b3535-228">**IAVertexBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="b3535-229">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b3535-229">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b3535-230">Matriz de buffers de vértice.</span><span class="sxs-lookup"><span data-stu-id="b3535-230">Array of vertex buffers.</span></span> <span data-ttu-id="b3535-231">A matriz é um bitmask de vários bytes em que cada bit representa um slot de recurso.</span><span class="sxs-lookup"><span data-stu-id="b3535-231">The array is a multi-byte bitmask where each bit represents one resource slot.</span></span>

</dd> <dt>

<span data-ttu-id="b3535-232">**IAIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="b3535-232">**IAIndexBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="b3535-233">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b3535-233">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b3535-234">Valor booliano que indica se o estado do buffer de índice deve ser salvo.</span><span class="sxs-lookup"><span data-stu-id="b3535-234">Boolean value indicating whether to save the index buffer state.</span></span>

</dd> <dt>

<span data-ttu-id="b3535-235">**IAInputLayout**</span><span class="sxs-lookup"><span data-stu-id="b3535-235">**IAInputLayout**</span></span>
</dt> <dd>

<span data-ttu-id="b3535-236">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b3535-236">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b3535-237">Valor booliano que indica se o estado de layout de entrada deve ser salvo.</span><span class="sxs-lookup"><span data-stu-id="b3535-237">Boolean value indicating whether to save the input layout state.</span></span>

</dd> <dt>

<span data-ttu-id="b3535-238">**IAPrimitiveTopology**</span><span class="sxs-lookup"><span data-stu-id="b3535-238">**IAPrimitiveTopology**</span></span>
</dt> <dd>

<span data-ttu-id="b3535-239">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b3535-239">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b3535-240">Valor booliano que indica se o estado da topologia primitiva deve ser salvo.</span><span class="sxs-lookup"><span data-stu-id="b3535-240">Boolean value indicating whether to save the primitive topology state.</span></span>

</dd> <dt>

<span data-ttu-id="b3535-241">**OMRenderTargets**</span><span class="sxs-lookup"><span data-stu-id="b3535-241">**OMRenderTargets**</span></span>
</dt> <dd>

<span data-ttu-id="b3535-242">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b3535-242">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b3535-243">Valor booliano que indica se os Estados de destino de renderização devem ser salvos.</span><span class="sxs-lookup"><span data-stu-id="b3535-243">Boolean value indicating whether to save the render targets states.</span></span>

</dd> <dt>

<span data-ttu-id="b3535-244">**OMDepthStencilState**</span><span class="sxs-lookup"><span data-stu-id="b3535-244">**OMDepthStencilState**</span></span>
</dt> <dd>

<span data-ttu-id="b3535-245">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b3535-245">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b3535-246">Valor booliano que indica se o estado de estêncil de profundidade deve ser salvo.</span><span class="sxs-lookup"><span data-stu-id="b3535-246">Boolean value indicating whether to save the depth-stencil state.</span></span>

</dd> <dt>

<span data-ttu-id="b3535-247">**OMBlendState**</span><span class="sxs-lookup"><span data-stu-id="b3535-247">**OMBlendState**</span></span>
</dt> <dd>

<span data-ttu-id="b3535-248">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b3535-248">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b3535-249">Valor booliano que indica se o estado de mesclagem deve ser salvo.</span><span class="sxs-lookup"><span data-stu-id="b3535-249">Boolean value indicating whether to save the blend state.</span></span>

</dd> <dt>

<span data-ttu-id="b3535-250">**RSViewports**</span><span class="sxs-lookup"><span data-stu-id="b3535-250">**RSViewports**</span></span>
</dt> <dd>

<span data-ttu-id="b3535-251">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b3535-251">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b3535-252">Valor booliano que indica se os Estados de visores devem ser salvos.</span><span class="sxs-lookup"><span data-stu-id="b3535-252">Boolean value indicating whether to save the viewports states.</span></span>

</dd> <dt>

<span data-ttu-id="b3535-253">**RSScissorRects**</span><span class="sxs-lookup"><span data-stu-id="b3535-253">**RSScissorRects**</span></span>
</dt> <dd>

<span data-ttu-id="b3535-254">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b3535-254">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b3535-255">Valor booliano que indica se os Estados dos retângulos da mola devem ser salvos.</span><span class="sxs-lookup"><span data-stu-id="b3535-255">Boolean value indicating whether to save the scissor rectangles states.</span></span>

</dd> <dt>

<span data-ttu-id="b3535-256">**RSRasterizerState**</span><span class="sxs-lookup"><span data-stu-id="b3535-256">**RSRasterizerState**</span></span>
</dt> <dd>

<span data-ttu-id="b3535-257">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b3535-257">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b3535-258">Valor booliano que indica se o estado do rasterizador deve ser salvo.</span><span class="sxs-lookup"><span data-stu-id="b3535-258">Boolean value indicating whether to save the rasterizer state.</span></span>

</dd> <dt>

<span data-ttu-id="b3535-259">**SOBuffers**</span><span class="sxs-lookup"><span data-stu-id="b3535-259">**SOBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="b3535-260">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b3535-260">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b3535-261">Valor booliano que indica se os Estados de buffers de saída de streaming devem ser salvos.</span><span class="sxs-lookup"><span data-stu-id="b3535-261">Boolean value indicating whether to save the stream-out buffers states.</span></span>

</dd> <dt>

<span data-ttu-id="b3535-262">**Predicação**</span><span class="sxs-lookup"><span data-stu-id="b3535-262">**Predication**</span></span>
</dt> <dd>

<span data-ttu-id="b3535-263">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b3535-263">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="b3535-264">Valor booliano que indica se o estado predicação deve ser salvo.</span><span class="sxs-lookup"><span data-stu-id="b3535-264">Boolean value indicating whether to save the predication state.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b3535-265">Comentários</span><span class="sxs-lookup"><span data-stu-id="b3535-265">Remarks</span></span>

<span data-ttu-id="b3535-266">Uma máscara de bloco de estado indica que o dispositivo informa que uma passagem ou uma técnica altera.</span><span class="sxs-lookup"><span data-stu-id="b3535-266">A state-block mask indicates the device states that a pass or a technique changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3535-267">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3535-267">Requirements</span></span>



| <span data-ttu-id="b3535-268">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3535-268">Requirement</span></span> | <span data-ttu-id="b3535-269">Valor</span><span class="sxs-lookup"><span data-stu-id="b3535-269">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3535-270">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b3535-270">Header</span></span><br/> | <dl> <span data-ttu-id="b3535-271"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3535-271"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3535-272">Confira também</span><span class="sxs-lookup"><span data-stu-id="b3535-272">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3535-273">Efeitos 11 estruturas</span><span class="sxs-lookup"><span data-stu-id="b3535-273">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

