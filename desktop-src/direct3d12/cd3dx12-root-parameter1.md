---
title: Estrutura de CD3DX12_ROOT_PARAMETER1 (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ estrutura D3D12 raiz \_ parâmetro1.
ms.assetid: CDE0C02E-0112-4FD9-A4A2-36E8C326715C
keywords:
- Estrutura de CD3DX12_ROOT_PARAMETER1
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_PARAMETER1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d582016b26df0d57f7792afd30fc4fcbf3ba97b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105793389"
---
# <a name="cd3dx12_root_parameter1-structure"></a><span data-ttu-id="8063c-104">\_ \_ Estrutura PARÂMETRO1 raiz CD3DX12</span><span class="sxs-lookup"><span data-stu-id="8063c-104">CD3DX12\_ROOT\_PARAMETER1 structure</span></span>

<span data-ttu-id="8063c-105">Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura [**D3D12 \_ raiz \_ parâmetro1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) .</span><span class="sxs-lookup"><span data-stu-id="8063c-105">A helper structure to enable easy initialization of a [**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="8063c-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8063c-106">Syntax</span></span>


```C++
struct CD3DX12_ROOT_PARAMETER1  : public D3D12_ROOT_PARAMETER1{
       CD3DX12_ROOT_PARAMETER1();
       explicit CD3DX12_ROOT_PARAMETER1(const D3D12_ROOT_PARAMETER1 &o);
  void static inline InitAsDescriptorTable(D3D12_ROOT_PARAMETER1 &rootParam, UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* pDescriptorRanges, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsConstants(D3D12_ROOT_PARAMETER1 &rootParam, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsConstantBufferView(D3D12_ROOT_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsShaderResourceView(D3D12_ROOT_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsUnorderedAccessView(D3D12_ROOT_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsDescriptorTable(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* pDescriptorRanges, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsConstants(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsConstantBufferView(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsShaderResourceView(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsUnorderedAccessView(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
};
```



## <a name="members"></a><span data-ttu-id="8063c-107">Membros</span><span class="sxs-lookup"><span data-stu-id="8063c-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="8063c-108">**CD3DX12 \_ raiz \_ parâmetro1 ()**</span><span class="sxs-lookup"><span data-stu-id="8063c-108">**CD3DX12\_ROOT\_PARAMETER1()**</span></span>
</dt> <dd>

<span data-ttu-id="8063c-109">Cria uma nova instância, não inicializada, de um \_ parâmetro1 raiz CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="8063c-109">Creates a new, uninitialized, instance of a CD3DX12\_ROOT\_PARAMETER1.</span></span>

</dd> <dt>

<span data-ttu-id="8063c-110">**CD3DX12id \_ raiz explícita \_ (const D3D12 \_ raiz \_ parâmetro1 &o)**</span><span class="sxs-lookup"><span data-stu-id="8063c-110">**explicit CD3DX12\_ROOT\_PARAMETER1(const D3D12\_ROOT\_PARAMETER1 &o)**</span></span>
</dt> <dd>

<span data-ttu-id="8063c-111">Cria uma nova instância de um \_ parâmetro1 raiz CD3DX12 \_ , inicializada com o conteúdo de outra estrutura [**\_ \_ parâmetro1 raiz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) .</span><span class="sxs-lookup"><span data-stu-id="8063c-111">Creates a new instance of a CD3DX12\_ROOT\_PARAMETER1, initialized with the contents of another [**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) structure.</span></span>

</dd> <dt>

<span data-ttu-id="8063c-112">**estático embutido InitAsDescriptorTable (D3D12 a \_ raiz \_ parâmetro1 &ROOTPARAM, uint numDescriptorRanges, const D3D12 \_ DESCRIPTOR \_ RANGE1 \* pDescriptorRanges, D3D12 \_ sombreador Visibility \_ visibilidade = D3D12 \_ Shader \_ Visibility \_ All)**</span><span class="sxs-lookup"><span data-stu-id="8063c-112">**static inline InitAsDescriptorTable(D3D12\_ROOT\_PARAMETER1 &rootParam, UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE1\* pDescriptorRanges, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="8063c-113">Especifica uma função que inicializa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="8063c-113">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="8063c-114">[**D3D12 \_ RootParam do &\_ PARÂMETRO1 raiz**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)</span><span class="sxs-lookup"><span data-stu-id="8063c-114">[**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam</span></span>

<span data-ttu-id="8063c-115">NumDescriptorRanges UINT</span><span class="sxs-lookup"><span data-stu-id="8063c-115">UINT numDescriptorRanges</span></span>

<span data-ttu-id="8063c-116">const [**D3D12 \_ DESCRIPTOR \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* pDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="8063c-116">const [**D3D12\_DESCRIPTOR\_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)\* pDescriptorRanges</span></span>

<span data-ttu-id="8063c-117">[**D3D12 \_ Visibilidade de \_ visibilidade do sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = visibilidade D3D12 do \_ sombreador \_ \_</span><span class="sxs-lookup"><span data-stu-id="8063c-117">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="8063c-118">**estático embutido InitAsConstants (D3D12 a \_ raiz \_ parâmetro1 &ROOTPARAM, uint NUM32BITVALUES, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ Shader \_ Visibility Visibility = D3D12 \_ Shader \_ visibilidade \_ All)**</span><span class="sxs-lookup"><span data-stu-id="8063c-118">**static inline InitAsConstants(D3D12\_ROOT\_PARAMETER1 &rootParam, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="8063c-119">Especifica uma função que inicializa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="8063c-119">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="8063c-120">[**D3D12 \_ RootParam do &\_ PARÂMETRO1 raiz**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)</span><span class="sxs-lookup"><span data-stu-id="8063c-120">[**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam</span></span>

<span data-ttu-id="8063c-121">Num32BitValues UINT</span><span class="sxs-lookup"><span data-stu-id="8063c-121">UINT num32BitValues</span></span>

<span data-ttu-id="8063c-122">ShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="8063c-122">UINT shaderRegister</span></span>

<span data-ttu-id="8063c-123">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="8063c-123">UINT registerSpace = 0</span></span>

<span data-ttu-id="8063c-124">[**D3D12 \_ Visibilidade de \_ visibilidade do sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = visibilidade D3D12 do \_ sombreador \_ \_</span><span class="sxs-lookup"><span data-stu-id="8063c-124">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="8063c-125">**estático embutido InitAsConstantBufferView (D3D12 a \_ raiz \_ parâmetro1 &ROOTPARAM, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ sinalizadores de \_ descritor de raiz \_ sinalizadores = D3D12 \_ descritor de raiz \_ \_ sinalizador \_ nenhum, D3D12 de \_ visibilidade de sombreador \_ = D3D12 a visibilidade do \_ sombreador \_ \_ todos)**</span><span class="sxs-lookup"><span data-stu-id="8063c-125">**static inline InitAsConstantBufferView(D3D12\_ROOT\_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="8063c-126">Especifica uma função que inicializa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="8063c-126">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="8063c-127">[**D3D12 \_ RootParam do &\_ PARÂMETRO1 raiz**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)</span><span class="sxs-lookup"><span data-stu-id="8063c-127">[**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam</span></span>

<span data-ttu-id="8063c-128">ShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="8063c-128">UINT shaderRegister</span></span>

<span data-ttu-id="8063c-129">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="8063c-129">UINT registerSpace = 0</span></span>

<span data-ttu-id="8063c-130">[**D3D12 \_ Sinalizadores \_ de \_ sinalizadores de descritor de raiz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = \_ sinalizador de \_ descritor raiz D3D12 \_ \_ nenhum</span><span class="sxs-lookup"><span data-stu-id="8063c-130">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

<span data-ttu-id="8063c-131">[**D3D12 \_ Visibilidade de \_ visibilidade do sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = visibilidade D3D12 do \_ sombreador \_ \_</span><span class="sxs-lookup"><span data-stu-id="8063c-131">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="8063c-132">**estático embutido InitAsShaderResourceView (D3D12 a \_ raiz \_ parâmetro1 &ROOTPARAM, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ sinalizadores de \_ descritor de raiz \_ sinalizadores = D3D12 \_ descritor de raiz \_ \_ sinalizador \_ nenhum, D3D12 de \_ visibilidade de sombreador \_ = D3D12 a visibilidade do \_ sombreador \_ \_ todos)**</span><span class="sxs-lookup"><span data-stu-id="8063c-132">**static inline InitAsShaderResourceView(D3D12\_ROOT\_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="8063c-133">Especifica uma função que inicializa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="8063c-133">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="8063c-134">[**D3D12 \_ RootParam do &\_ PARÂMETRO1 raiz**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)</span><span class="sxs-lookup"><span data-stu-id="8063c-134">[**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam</span></span>

<span data-ttu-id="8063c-135">ShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="8063c-135">UINT shaderRegister</span></span>

<span data-ttu-id="8063c-136">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="8063c-136">UINT registerSpace = 0</span></span>

<span data-ttu-id="8063c-137">[**D3D12 \_ Sinalizadores \_ de \_ sinalizadores de descritor de raiz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = \_ sinalizador de \_ descritor raiz D3D12 \_ \_ nenhum</span><span class="sxs-lookup"><span data-stu-id="8063c-137">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

<span data-ttu-id="8063c-138">[**D3D12 \_ Visibilidade de \_ visibilidade do sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = visibilidade D3D12 do \_ sombreador \_ \_</span><span class="sxs-lookup"><span data-stu-id="8063c-138">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="8063c-139">**estático embutido InitAsUnorderedAccessView (D3D12 a \_ raiz \_ parâmetro1 &ROOTPARAM, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ sinalizadores de \_ descritor de raiz \_ sinalizadores = D3D12 \_ descritor de raiz \_ \_ sinalizador \_ nenhum, D3D12 de \_ visibilidade de sombreador \_ = D3D12 a visibilidade do \_ sombreador \_ \_ todos)**</span><span class="sxs-lookup"><span data-stu-id="8063c-139">**static inline InitAsUnorderedAccessView(D3D12\_ROOT\_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="8063c-140">Especifica uma função que inicializa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="8063c-140">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="8063c-141">[**D3D12 \_ RootParam do &\_ PARÂMETRO1 raiz**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)</span><span class="sxs-lookup"><span data-stu-id="8063c-141">[**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam</span></span>

<span data-ttu-id="8063c-142">ShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="8063c-142">UINT shaderRegister</span></span>

<span data-ttu-id="8063c-143">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="8063c-143">UINT registerSpace = 0</span></span>

<span data-ttu-id="8063c-144">[**D3D12 \_ Sinalizadores \_ de \_ sinalizadores de descritor de raiz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = \_ sinalizador de \_ descritor raiz D3D12 \_ \_ nenhum</span><span class="sxs-lookup"><span data-stu-id="8063c-144">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

<span data-ttu-id="8063c-145">[**D3D12 \_ Visibilidade de \_ visibilidade do sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = visibilidade D3D12 do \_ sombreador \_ \_</span><span class="sxs-lookup"><span data-stu-id="8063c-145">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="8063c-146">**InitAsDescriptorTable embutido (UINT numDescriptorRanges, const D3D12 \_ DESCRIPTOR \_ RANGE1 \* pDescriptorRanges, D3D12 \_ Shader \_ visibilidade Visibility = D3D12 \_ Shader \_ visibilidade \_ All)**</span><span class="sxs-lookup"><span data-stu-id="8063c-146">**inline InitAsDescriptorTable(UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE1\* pDescriptorRanges, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="8063c-147">Especifica uma função que inicializa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="8063c-147">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="8063c-148">NumDescriptorRanges UINT</span><span class="sxs-lookup"><span data-stu-id="8063c-148">UINT numDescriptorRanges</span></span>

<span data-ttu-id="8063c-149">const [**D3D12 \_ DESCRIPTOR \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* pDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="8063c-149">const [**D3D12\_DESCRIPTOR\_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)\* pDescriptorRanges</span></span>

<span data-ttu-id="8063c-150">[**D3D12 \_ Visibilidade de \_ visibilidade do sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = visibilidade D3D12 do \_ sombreador \_ \_</span><span class="sxs-lookup"><span data-stu-id="8063c-150">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="8063c-151">**InitAsConstants embutido (UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ Shader Visibility \_ VISIBILITY = D3D12 \_ Shader \_ visibilidade \_ All)**</span><span class="sxs-lookup"><span data-stu-id="8063c-151">**inline InitAsConstants(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="8063c-152">Especifica uma função que inicializa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="8063c-152">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="8063c-153">Num32BitValues UINT</span><span class="sxs-lookup"><span data-stu-id="8063c-153">UINT num32BitValues</span></span>

<span data-ttu-id="8063c-154">ShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="8063c-154">UINT shaderRegister</span></span>

<span data-ttu-id="8063c-155">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="8063c-155">UINT registerSpace = 0</span></span>

<span data-ttu-id="8063c-156">[**D3D12 \_ Visibilidade de \_ visibilidade do sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = visibilidade D3D12 do \_ sombreador \_ \_</span><span class="sxs-lookup"><span data-stu-id="8063c-156">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="8063c-157">**InitAsConstantBufferView embutido (UINT shaderRegister, UINT registerSpace = 0, D3D12 sinalizadores do \_ \_ descritor de raiz \_ sinalizadores = D3D12 do \_ \_ descritor \_ de raiz \_ nenhum, D3D12 de \_ visibilidade de sombreador \_ = D3D12 a visibilidade do \_ sombreador \_ \_ tudo)**</span><span class="sxs-lookup"><span data-stu-id="8063c-157">**inline InitAsConstantBufferView(UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="8063c-158">Especifica uma função que inicializa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="8063c-158">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="8063c-159">ShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="8063c-159">UINT shaderRegister</span></span>

<span data-ttu-id="8063c-160">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="8063c-160">UINT registerSpace = 0</span></span>

<span data-ttu-id="8063c-161">[**D3D12 \_ Sinalizadores \_ de \_ sinalizadores de descritor de raiz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = \_ sinalizador de \_ descritor raiz D3D12 \_ \_ nenhum</span><span class="sxs-lookup"><span data-stu-id="8063c-161">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

<span data-ttu-id="8063c-162">[**D3D12 \_ Visibilidade de \_ visibilidade do sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = visibilidade D3D12 do \_ sombreador \_ \_</span><span class="sxs-lookup"><span data-stu-id="8063c-162">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="8063c-163">**InitAsShaderResourceView embutido (UINT shaderRegister, UINT registerSpace = 0, D3D12 sinalizadores do \_ \_ descritor de raiz \_ sinalizadores = D3D12 do \_ \_ descritor \_ de raiz \_ nenhum, D3D12 de \_ visibilidade de sombreador \_ = D3D12 a visibilidade do \_ sombreador \_ \_ tudo)**</span><span class="sxs-lookup"><span data-stu-id="8063c-163">**inline InitAsShaderResourceView(UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="8063c-164">Especifica uma função que inicializa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="8063c-164">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="8063c-165">ShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="8063c-165">UINT shaderRegister</span></span>

<span data-ttu-id="8063c-166">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="8063c-166">UINT registerSpace = 0</span></span>

<span data-ttu-id="8063c-167">[**D3D12 \_ Sinalizadores \_ de \_ sinalizadores de descritor de raiz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = \_ sinalizador de \_ descritor raiz D3D12 \_ \_ nenhum</span><span class="sxs-lookup"><span data-stu-id="8063c-167">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

<span data-ttu-id="8063c-168">[**D3D12 \_ Visibilidade de \_ visibilidade do sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = visibilidade D3D12 do \_ sombreador \_ \_</span><span class="sxs-lookup"><span data-stu-id="8063c-168">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="8063c-169">**InitAsUnorderedAccessView embutido (UINT shaderRegister, UINT registerSpace = 0, D3D12 sinalizadores do \_ \_ descritor de raiz \_ sinalizadores = D3D12 do \_ \_ descritor \_ de raiz \_ nenhum, D3D12 de \_ visibilidade de sombreador \_ = D3D12 a visibilidade do \_ sombreador \_ \_ tudo)**</span><span class="sxs-lookup"><span data-stu-id="8063c-169">**inline InitAsUnorderedAccessView(UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="8063c-170">Especifica uma função que inicializa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="8063c-170">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="8063c-171">ShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="8063c-171">UINT shaderRegister</span></span>

<span data-ttu-id="8063c-172">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="8063c-172">UINT registerSpace = 0</span></span>

<span data-ttu-id="8063c-173">[**D3D12 \_ Sinalizadores \_ de \_ sinalizadores de descritor de raiz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = \_ sinalizador de \_ descritor raiz D3D12 \_ \_ nenhum</span><span class="sxs-lookup"><span data-stu-id="8063c-173">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

<span data-ttu-id="8063c-174">[**D3D12 \_ Visibilidade de \_ visibilidade do sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = visibilidade D3D12 do \_ sombreador \_ \_</span><span class="sxs-lookup"><span data-stu-id="8063c-174">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8063c-175">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8063c-175">Requirements</span></span>



| <span data-ttu-id="8063c-176">Requisito</span><span class="sxs-lookup"><span data-stu-id="8063c-176">Requirement</span></span> | <span data-ttu-id="8063c-177">Valor</span><span class="sxs-lookup"><span data-stu-id="8063c-177">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8063c-178">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8063c-178">Header</span></span><br/> | <dl> <span data-ttu-id="8063c-179"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="8063c-179"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8063c-180">Confira também</span><span class="sxs-lookup"><span data-stu-id="8063c-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8063c-181">**D3D12 \_ raiz \_ parâmetro1**</span><span class="sxs-lookup"><span data-stu-id="8063c-181">**D3D12\_ROOT\_PARAMETER1**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)
</dt> <dt>

[<span data-ttu-id="8063c-182">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="8063c-182">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





