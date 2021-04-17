---
title: Estrutura de CD3DX12_ROOT_PARAMETER (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ estrutura de parâmetro raiz D3D12 \_ .
ms.assetid: CDDF84D0-4E66-4CF2-999B-3F401E8DD17F
keywords:
- Estrutura de CD3DX12_ROOT_PARAMETER
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_PARAMETER
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9099b0839b6b55676d5a8afdfb913948e70bbb7f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105798041"
---
# <a name="cd3dx12_root_parameter-structure"></a><span data-ttu-id="9d23c-104">\_Estrutura de \_ parâmetro raiz CD3DX12</span><span class="sxs-lookup"><span data-stu-id="9d23c-104">CD3DX12\_ROOT\_PARAMETER structure</span></span>

<span data-ttu-id="9d23c-105">Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura de [**\_ \_ parâmetro raiz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) .</span><span class="sxs-lookup"><span data-stu-id="9d23c-105">A helper structure to enable easy initialization of a [**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d23c-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9d23c-106">Syntax</span></span>


```C++
struct CD3DX12_ROOT_PARAMETER  : public D3D12_ROOT_PARAMETER{
       CD3DX12_ROOT_PARAMETER();
       explicit CD3DX12_ROOT_PARAMETER(const D3D12_ROOT_PARAMETER &o);
  void static inline InitAsDescriptorTable(D3D12_ROOT_PARAMETER &rootParam, UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* pDescriptorRanges, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsConstants(D3D12_ROOT_PARAMETER &rootParam, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsConstantBufferView(D3D12_ROOT_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsShaderResourceView(D3D12_ROOT_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsUnorderedAccessView(D3D12_ROOT_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsDescriptorTable(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* pDescriptorRanges, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsConstants(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsConstantBufferView(UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsShaderResourceView(UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsUnorderedAccessView(UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
};
```



## <a name="members"></a><span data-ttu-id="9d23c-107">Membros</span><span class="sxs-lookup"><span data-stu-id="9d23c-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="9d23c-108">**\_Parâmetro raiz CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="9d23c-108">**CD3DX12\_ROOT\_PARAMETER()**</span></span>
</dt> <dd>

<span data-ttu-id="9d23c-109">Cria uma nova instância, não inicializada, de um \_ parâmetro raiz CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="9d23c-109">Creates a new, uninitialized, instance of a CD3DX12\_ROOT\_PARAMETER.</span></span>

</dd> <dt>

<span data-ttu-id="9d23c-110">**\_parâmetro raiz CD3DX12 explícito \_ (parâmetro const D3D12 \_ raiz \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="9d23c-110">**explicit CD3DX12\_ROOT\_PARAMETER(const D3D12\_ROOT\_PARAMETER &o)**</span></span>
</dt> <dd>

<span data-ttu-id="9d23c-111">Cria uma nova instância de um \_ parâmetro raiz CD3DX12 \_ , inicializada com o conteúdo de outra estrutura de [**\_ \_ parâmetro raiz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) .</span><span class="sxs-lookup"><span data-stu-id="9d23c-111">Creates a new instance of a CD3DX12\_ROOT\_PARAMETER, initialized with the contents of another [**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) structure.</span></span>

</dd> <dt>

<span data-ttu-id="9d23c-112">**estático embutido InitAsDescriptorTable (D3D12 de \_ parâmetro de raiz \_ &ROOTPARAM, uint numDescriptorRanges, const D3D12 \_ DESCRIPTOR \_ intervalo \* pDescriptorRanges, D3D12 \_ Shader Visibility \_ Visibility = D3D12 \_ Shader \_ visibilidade \_ All)**</span><span class="sxs-lookup"><span data-stu-id="9d23c-112">**static inline InitAsDescriptorTable(D3D12\_ROOT\_PARAMETER &rootParam, UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE\* pDescriptorRanges, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="9d23c-113">Especifica uma função que inicializa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="9d23c-113">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="9d23c-114">[**D3D12 \_ \_Parâmetro raiz**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span><span class="sxs-lookup"><span data-stu-id="9d23c-114">[**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span></span>

<span data-ttu-id="9d23c-115">NumDescriptorRanges UINT</span><span class="sxs-lookup"><span data-stu-id="9d23c-115">UINT numDescriptorRanges</span></span>

<span data-ttu-id="9d23c-116">[**D3D12 \_ \_Intervalo de descritores**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* pDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="9d23c-116">[**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)\* pDescriptorRanges</span></span>

<span data-ttu-id="9d23c-117">opt [**D3D12 \_ Visibilidade de \_ visibilidade do sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = visibilidade D3D12 do \_ sombreador \_ \_</span><span class="sxs-lookup"><span data-stu-id="9d23c-117">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="9d23c-118">**InitAsConstants embutido estático ( \_ parâmetro de raiz D3D12 \_ &ROOTPARAM, uint NUM32BITVALUES, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ Shader \_ Visibility Visibility = D3D12 \_ Shader \_ visibilidade \_ All)**</span><span class="sxs-lookup"><span data-stu-id="9d23c-118">**static inline InitAsConstants(D3D12\_ROOT\_PARAMETER &rootParam, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="9d23c-119">Especifica uma função que inicializa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="9d23c-119">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="9d23c-120">[**D3D12 \_ \_Parâmetro raiz**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span><span class="sxs-lookup"><span data-stu-id="9d23c-120">[**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span></span>

<span data-ttu-id="9d23c-121">Num32BitValues UINT</span><span class="sxs-lookup"><span data-stu-id="9d23c-121">UINT num32BitValues</span></span>

<span data-ttu-id="9d23c-122">ShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="9d23c-122">UINT shaderRegister</span></span>

<span data-ttu-id="9d23c-123">opt UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="9d23c-123">(opt) UINT registerSpace = 0</span></span>

<span data-ttu-id="9d23c-124">opt [**D3D12 \_ Visibilidade de \_ visibilidade do sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = visibilidade D3D12 do \_ sombreador \_ \_</span><span class="sxs-lookup"><span data-stu-id="9d23c-124">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="9d23c-125">**InitAsConstantBufferView embutido estático ( \_ parâmetro de raiz D3D12 \_ &ROOTPARAM, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ Shader \_ Visibility Visibility = D3D12 \_ Shader \_ visibilidade \_ All)**</span><span class="sxs-lookup"><span data-stu-id="9d23c-125">**static inline InitAsConstantBufferView(D3D12\_ROOT\_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="9d23c-126">Especifica uma função que inicializa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="9d23c-126">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="9d23c-127">[**D3D12 \_ \_Parâmetro raiz**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span><span class="sxs-lookup"><span data-stu-id="9d23c-127">[**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span></span>

<span data-ttu-id="9d23c-128">ShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="9d23c-128">UINT shaderRegister</span></span>

<span data-ttu-id="9d23c-129">opt UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="9d23c-129">(opt) UINT registerSpace = 0</span></span>

<span data-ttu-id="9d23c-130">opt [**D3D12 \_ Visibilidade de \_ visibilidade do sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = visibilidade D3D12 do \_ sombreador \_ \_</span><span class="sxs-lookup"><span data-stu-id="9d23c-130">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="9d23c-131">**InitAsShaderResourceView embutido estático ( \_ parâmetro de raiz D3D12 \_ &ROOTPARAM, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ Shader \_ Visibility Visibility = D3D12 \_ Shader \_ visibilidade \_ All)**</span><span class="sxs-lookup"><span data-stu-id="9d23c-131">**static inline InitAsShaderResourceView(D3D12\_ROOT\_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="9d23c-132">Especifica uma função que inicializa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="9d23c-132">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="9d23c-133">[**D3D12 \_ \_Parâmetro raiz**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span><span class="sxs-lookup"><span data-stu-id="9d23c-133">[**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span></span>

<span data-ttu-id="9d23c-134">ShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="9d23c-134">UINT shaderRegister</span></span>

<span data-ttu-id="9d23c-135">opt UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="9d23c-135">(opt) UINT registerSpace = 0</span></span>

<span data-ttu-id="9d23c-136">opt [**D3D12 \_ Visibilidade de \_ visibilidade do sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = visibilidade D3D12 do \_ sombreador \_ \_</span><span class="sxs-lookup"><span data-stu-id="9d23c-136">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="9d23c-137">**InitAsUnorderedAccessView embutido estático ( \_ parâmetro de raiz D3D12 \_ &ROOTPARAM, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ Shader \_ Visibility Visibility = D3D12 \_ Shader \_ visibilidade \_ All)**</span><span class="sxs-lookup"><span data-stu-id="9d23c-137">**static inline InitAsUnorderedAccessView(D3D12\_ROOT\_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="9d23c-138">Especifica uma função que inicializa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="9d23c-138">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="9d23c-139">[**D3D12 \_ \_Parâmetro raiz**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span><span class="sxs-lookup"><span data-stu-id="9d23c-139">[**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span></span>

<span data-ttu-id="9d23c-140">ShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="9d23c-140">UINT shaderRegister</span></span>

<span data-ttu-id="9d23c-141">opt UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="9d23c-141">(opt) UINT registerSpace = 0</span></span>

<span data-ttu-id="9d23c-142">opt [**D3D12 \_ Visibilidade de \_ visibilidade do sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = visibilidade D3D12 do \_ sombreador \_ \_</span><span class="sxs-lookup"><span data-stu-id="9d23c-142">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="9d23c-143">**InitAsDescriptorTable embutido (UINT numDescriptorRanges, const D3D12 \_ DESCRIPTOR \_ intervalo \* pDescriptorRanges, D3D12 \_ Shader Visibility \_ Visibility = D3D12 \_ Shader \_ visibilidade \_ All)**</span><span class="sxs-lookup"><span data-stu-id="9d23c-143">**inline InitAsDescriptorTable(UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE\* pDescriptorRanges, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="9d23c-144">Especifica uma função que inicializa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="9d23c-144">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="9d23c-145">NumDescriptorRanges UINT</span><span class="sxs-lookup"><span data-stu-id="9d23c-145">UINT numDescriptorRanges</span></span>

<span data-ttu-id="9d23c-146">[**D3D12 \_ \_Intervalo de descritores**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* pDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="9d23c-146">[**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)\* pDescriptorRanges</span></span>

<span data-ttu-id="9d23c-147">opt [**D3D12 \_ Visibilidade de \_ visibilidade do sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = visibilidade D3D12 do \_ sombreador \_ \_</span><span class="sxs-lookup"><span data-stu-id="9d23c-147">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="9d23c-148">**InitAsConstants embutido (UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ Shader Visibility \_ VISIBILITY = D3D12 \_ Shader \_ visibilidade \_ All)**</span><span class="sxs-lookup"><span data-stu-id="9d23c-148">**inline InitAsConstants(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="9d23c-149">Especifica uma função que inicializa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="9d23c-149">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="9d23c-150">Num32BitValues UINT</span><span class="sxs-lookup"><span data-stu-id="9d23c-150">UINT num32BitValues</span></span>

<span data-ttu-id="9d23c-151">ShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="9d23c-151">UINT shaderRegister</span></span>

<span data-ttu-id="9d23c-152">opt UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="9d23c-152">(opt) UINT registerSpace = 0</span></span>

<span data-ttu-id="9d23c-153">opt [**D3D12 \_ Visibilidade de \_ visibilidade do sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = visibilidade D3D12 do \_ sombreador \_ \_</span><span class="sxs-lookup"><span data-stu-id="9d23c-153">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="9d23c-154">**InitAsConstantBufferView embutido (UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ sombreador de visibilidade \_ visibilidade = D3D12 de \_ visibilidade do sombreador \_ \_ tudo)**</span><span class="sxs-lookup"><span data-stu-id="9d23c-154">**inline InitAsConstantBufferView(UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="9d23c-155">Especifica uma função que inicializa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="9d23c-155">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="9d23c-156">ShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="9d23c-156">UINT shaderRegister</span></span>

<span data-ttu-id="9d23c-157">opt UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="9d23c-157">(opt) UINT registerSpace = 0</span></span>

<span data-ttu-id="9d23c-158">opt [**D3D12 \_ Visibilidade de \_ visibilidade do sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = visibilidade D3D12 do \_ sombreador \_ \_</span><span class="sxs-lookup"><span data-stu-id="9d23c-158">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="9d23c-159">**InitAsShaderResourceView embutido (UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ sombreador de visibilidade \_ visibilidade = D3D12 de \_ visibilidade do sombreador \_ \_ tudo)**</span><span class="sxs-lookup"><span data-stu-id="9d23c-159">**inline InitAsShaderResourceView(UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="9d23c-160">Especifica uma função que inicializa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="9d23c-160">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="9d23c-161">ShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="9d23c-161">UINT shaderRegister</span></span>

<span data-ttu-id="9d23c-162">opt UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="9d23c-162">(opt) UINT registerSpace = 0</span></span>

<span data-ttu-id="9d23c-163">opt [**D3D12 \_ Visibilidade de \_ visibilidade do sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = visibilidade D3D12 do \_ sombreador \_ \_</span><span class="sxs-lookup"><span data-stu-id="9d23c-163">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="9d23c-164">**InitAsUnorderedAccessView embutido (UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ sombreador de visibilidade \_ visibilidade = D3D12 de \_ visibilidade do sombreador \_ \_ tudo)**</span><span class="sxs-lookup"><span data-stu-id="9d23c-164">**inline InitAsUnorderedAccessView(UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="9d23c-165">Especifica uma função que inicializa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="9d23c-165">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="9d23c-166">ShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="9d23c-166">UINT shaderRegister</span></span>

<span data-ttu-id="9d23c-167">opt UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="9d23c-167">(opt) UINT registerSpace = 0</span></span>

<span data-ttu-id="9d23c-168">opt [**D3D12 \_ Visibilidade de \_ visibilidade do sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = visibilidade D3D12 do \_ sombreador \_ \_</span><span class="sxs-lookup"><span data-stu-id="9d23c-168">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9d23c-169">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d23c-169">Requirements</span></span>



| <span data-ttu-id="9d23c-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d23c-170">Requirement</span></span> | <span data-ttu-id="9d23c-171">Valor</span><span class="sxs-lookup"><span data-stu-id="9d23c-171">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9d23c-172">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9d23c-172">Header</span></span><br/> | <dl> <span data-ttu-id="9d23c-173"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d23c-173"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d23c-174">Confira também</span><span class="sxs-lookup"><span data-stu-id="9d23c-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d23c-175">**\_Parâmetro raiz \_ D3D12**</span><span class="sxs-lookup"><span data-stu-id="9d23c-175">**D3D12\_ROOT\_PARAMETER**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)
</dt> <dt>

[<span data-ttu-id="9d23c-176">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="9d23c-176">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





