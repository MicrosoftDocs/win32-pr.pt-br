---
title: Estrutura de CD3DX12_STATIC_SAMPLER_DESC (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ \_ estrutura desc de amostra estática D3D12 \_ .
ms.assetid: C402415D-7BD5-4E23-82C9-B29B0B5669B8
keywords:
- Estrutura de CD3DX12_STATIC_SAMPLER_DESC
topic_type:
- apiref
api_name:
- CD3DX12_STATIC_SAMPLER_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d6b10749f7a56d928e0a4218d534cc2a8ec4fab
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105768255"
---
# <a name="cd3dx12_static_sampler_desc-structure"></a><span data-ttu-id="94b6c-104">\_ \_ Estrutura desc de amostra estática CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="94b6c-104">CD3DX12\_STATIC\_SAMPLER\_DESC structure</span></span>

<span data-ttu-id="94b6c-105">Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura [**\_ \_ \_ desc de amostra estática D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) .</span><span class="sxs-lookup"><span data-stu-id="94b6c-105">A helper structure to enable easy initialization of a [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="94b6c-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="94b6c-106">Syntax</span></span>


```C++
struct CD3DX12_STATIC_SAMPLER_DESC  : public D3D12_STATIC_SAMPLER_DESC{
       CD3DX12_STATIC_SAMPLER_DESC();
       explicit CD3DX12_STATIC_SAMPLER_DESC(const D3D12_STATIC_SAMPLER_DESC &o);
       CD3DX12_STATIC_SAMPLER_DESC(UINT shaderRegister, D3D12_FILTER filter = D3D12_FILTER_ANISOTROPIC, D3D12_TEXTURE_ADDRESS_MODE addressU = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressV = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressW = D3D12_TEXTURE_ADDRESS_MODE_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12_COMPARISON_FUNC comparisonFunc = D3D12_COMPARISON_FUNC_LESS_EQUAL, D3D12_STATIC_BORDER_COLOR borderColor = D3D12_STATIC_BORDER_COLOR_OPAQUE_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12_FLOAT32_MAX, D3D12_SHADER_VISIBILITY shaderVisibility = D3D12_SHADER_VISIBILITY_ALL, UINT registerSpace = 0);
  void static inline Init(D3D12_STATIC_SAMPLER_DESC &samplerDesc, UINT shaderRegister, D3D12_FILTER filter = D3D12_FILTER_ANISOTROPIC, D3D12_TEXTURE_ADDRESS_MODE addressU = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressV = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressW = D3D12_TEXTURE_ADDRESS_MODE_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12_COMPARISON_FUNC comparisonFunc = D3D12_COMPARISON_FUNC_LESS_EQUAL, D3D12_STATIC_BORDER_COLOR borderColor = D3D12_STATIC_BORDER_COLOR_OPAQUE_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12_FLOAT32_MAX, D3D12_SHADER_VISIBILITY shaderVisibility = D3D12_SHADER_VISIBILITY_ALL, UINT registerSpace = 0);
  void inline Init(UINT shaderRegister, D3D12_FILTER filter = D3D12_FILTER_ANISOTROPIC, D3D12_TEXTURE_ADDRESS_MODE addressU = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressV = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressW = D3D12_TEXTURE_ADDRESS_MODE_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12_COMPARISON_FUNC comparisonFunc = D3D12_COMPARISON_FUNC_LESS_EQUAL, D3D12_STATIC_BORDER_COLOR borderColor = D3D12_STATIC_BORDER_COLOR_OPAQUE_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12_FLOAT32_MAX, D3D12_SHADER_VISIBILITY shaderVisibility = D3D12_SHADER_VISIBILITY_ALL, UINT registerSpace = 0);
};
```



## <a name="members"></a><span data-ttu-id="94b6c-107">Membros</span><span class="sxs-lookup"><span data-stu-id="94b6c-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="94b6c-108">**\_ \_ Amostra de CD3DX12 estática \_ DESC ()**</span><span class="sxs-lookup"><span data-stu-id="94b6c-108">**CD3DX12\_STATIC\_SAMPLER\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="94b6c-109">Cria uma nova instância, não inicializada, de uma amostra de CD3DX12 \_ estática \_ \_ desc.</span><span class="sxs-lookup"><span data-stu-id="94b6c-109">Creates a new, uninitialized, instance of a CD3DX12\_STATIC\_SAMPLER\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="94b6c-110">**\_amostras estáticas CD3DX12 explícita \_ \_ DESC (const D3D12 de \_ \_ amostra estática \_ desc &o)**</span><span class="sxs-lookup"><span data-stu-id="94b6c-110">**explicit CD3DX12\_STATIC\_SAMPLER\_DESC(const D3D12\_STATIC\_SAMPLER\_DESC &o)**</span></span>
</dt> <dd>

<span data-ttu-id="94b6c-111">Cria uma nova instância de uma \_ amostra CD3DX12 \_ estática \_ DESC, inicializada com o conteúdo de outra estrutura [**\_ \_ \_ desc de amostra estática D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) .</span><span class="sxs-lookup"><span data-stu-id="94b6c-111">Creates a new instance of a CD3DX12\_STATIC\_SAMPLER\_DESC, initialized with the contents of another [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="94b6c-112">**CD3DX12 \_ \_ de amostra estática \_ DESC (UINT shaderRegister, \_ filtro de filtro D3D12 = D3D12 \_ filtro \_ ANISOTROPIC, D3D12 \_ textura de endereço modo endereçou = D3D12 modo de \_ \_ \_ \_ endereço de textura \_ \_ encapsulado, D3D12 \_ modo de endereço de textura \_ \_ addressV = D3D12 \_ \_ \_ modo de endereço de textura com \_ encapsulamento, \_ \_ \_ modo de endereço de textura D3D12 addressW = \_ \_ \_ modo de endereço de textura de D3D12 \_ encapsulado, float mipLODBias = 0, uint maxAnisotropy = 16, D3D12 \_ Comparison \_ Func COMPARISONFUNC = D3D12 \_ comparation \_ Func \_ \_ Equals, D3D12 \_ static \_ Border \_ Color BorderColor = D3D12 \_ static \_ Border \_ Color \_ opaco \_ , float minLOD = 0. f, float maxLOD = D3D12 \_ FLOAT32 \_ Max, D3D12 \_ Shader \_ Visibility shaderVisibility = D3D12 \_ Shader \_ visibilidade \_ All, uint registerSpace**</span><span class="sxs-lookup"><span data-stu-id="94b6c-112">**CD3DX12\_STATIC\_SAMPLER\_DESC(UINT shaderRegister, D3D12\_FILTER filter = D3D12\_FILTER\_ANISOTROPIC, D3D12\_TEXTURE\_ADDRESS\_MODE addressU = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, D3D12\_TEXTURE\_ADDRESS\_MODE addressV = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, D3D12\_TEXTURE\_ADDRESS\_MODE addressW = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12\_COMPARISON\_FUNC comparisonFunc = D3D12\_COMPARISON\_FUNC\_LESS\_EQUAL, D3D12\_STATIC\_BORDER\_COLOR borderColor = D3D12\_STATIC\_BORDER\_COLOR\_OPAQUE\_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12\_FLOAT32\_MAX, D3D12\_SHADER\_VISIBILITY shaderVisibility = D3D12\_SHADER\_VISIBILITY\_ALL, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="94b6c-113">Cria uma nova instância de uma \_ amostra CD3DX12 \_ estática \_ DESC, inicializando os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="94b6c-113">Creates a new instance of a CD3DX12\_STATIC\_SAMPLER\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="94b6c-114">ShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="94b6c-114">UINT shaderRegister</span></span>

<span data-ttu-id="94b6c-115">opt [**D3D12 \_ Filtro filtro =**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) \_ filtro D3D12 \_ ANISOTROPIC</span><span class="sxs-lookup"><span data-stu-id="94b6c-115">(opt) [**D3D12\_FILTER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) filter = D3D12\_FILTER\_ANISOTROPIC</span></span>

<span data-ttu-id="94b6c-116">opt [**D3D12 \_ \_ \_ Modo de endereço de textura**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressexception = modo de endereço de textura de D3D12 \_ \_ \_ \_ Wrap</span><span class="sxs-lookup"><span data-stu-id="94b6c-116">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressU = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="94b6c-117">opt [**D3D12 \_ \_ \_ Modo de endereço de textura**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressV = \_ \_ \_ \_ encapsulamento do modo de endereço de textura D3D12</span><span class="sxs-lookup"><span data-stu-id="94b6c-117">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressV = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="94b6c-118">opt [**D3D12 \_ \_ \_ Modo de endereço de textura**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressW = \_ \_ \_ \_ encapsulamento do modo de endereço de textura D3D12</span><span class="sxs-lookup"><span data-stu-id="94b6c-118">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressW = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="94b6c-119">opt FLOAT mipLODBias = 0</span><span class="sxs-lookup"><span data-stu-id="94b6c-119">(opt) FLOAT mipLODBias = 0</span></span>

<span data-ttu-id="94b6c-120">opt UINT maxAnisotropy = 16</span><span class="sxs-lookup"><span data-stu-id="94b6c-120">(opt) UINT maxAnisotropy = 16</span></span>

<span data-ttu-id="94b6c-121">opt [**D3D12 \_ COMPARAÇÃO \_ Func**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) COMPARISONFUNC = D3D12 \_ Comparison \_ Func \_ menos \_ igual</span><span class="sxs-lookup"><span data-stu-id="94b6c-121">(opt) [**D3D12\_COMPARISON\_FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) comparisonFunc = D3D12\_COMPARISON\_FUNC\_LESS\_EQUAL</span></span>

<span data-ttu-id="94b6c-122">opt [**D3D12 \_ \_ \_ Cor da borda estática**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) BorderColor = D3D12 de \_ \_ borda estática \_ cor \_ \_ branco opaco</span><span class="sxs-lookup"><span data-stu-id="94b6c-122">(opt) [**D3D12\_STATIC\_BORDER\_COLOR**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) borderColor = D3D12\_STATIC\_BORDER\_COLOR\_OPAQUE\_WHITE</span></span>

<span data-ttu-id="94b6c-123">opt FLOAT minLOD = 0. f</span><span class="sxs-lookup"><span data-stu-id="94b6c-123">(opt) FLOAT minLOD = 0.f</span></span>

<span data-ttu-id="94b6c-124">opt FLOAT maxLOD = D3D12 \_ FLOAT32 \_ Max</span><span class="sxs-lookup"><span data-stu-id="94b6c-124">(opt) FLOAT maxLOD = D3D12\_FLOAT32\_MAX</span></span>

<span data-ttu-id="94b6c-125">opt [**D3D12 \_ SHADER \_ Visibility**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) SHADERVISIBILITY = D3D12 \_ Shader \_ visibilidade \_ All</span><span class="sxs-lookup"><span data-stu-id="94b6c-125">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) shaderVisibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

<span data-ttu-id="94b6c-126">opt UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="94b6c-126">(opt) UINT registerSpace = 0</span></span>

</dd> <dt>

<span data-ttu-id="94b6c-127">**Inicialização embutida estática ( \_ D3D12 \_ de amostra de estática \_ desc &SamplerDesc, uint shaderRegister, D3D12 \_ filtro filtro = D3D12 \_ filtro \_ ANISOTROPIC, D3D12 \_ modo de endereço de textura \_ \_ endereçou = D3D12 modo \_ de endereço de textura de \_ \_ encapsulado, D3D12 modo de endereço de textura addressV \_ \_ \_ \_ = D3D12 \_ \_ \_ modo de endereço de textura \_ \_ \_ \_ modo de endereço de textura D3D12 addressW = \_ \_ \_ modo de endereço de textura de D3D12 \_ encapsulado, float mipLODBias = 0, uint maxAnisotropy = 16, D3D12 \_ Comparison \_ Func COMPARISONFUNC = D3D12 \_ comparation \_ Func \_ \_ Equals, D3D12 \_ static \_ Border \_ Color BorderColor = D3D12 \_ static \_ Border \_ Color \_ opaco \_ , float minLOD = 0. f, float maxLOD = D3D12 \_ FLOAT32 \_ Max, D3D12 \_ Shader \_ Visibility shaderVisibility = D3D12 \_ Shader \_ visibilidade \_ All, uint registerSpace**</span><span class="sxs-lookup"><span data-stu-id="94b6c-127">**static inline Init(D3D12\_STATIC\_SAMPLER\_DESC &samplerDesc, UINT shaderRegister, D3D12\_FILTER filter = D3D12\_FILTER\_ANISOTROPIC, D3D12\_TEXTURE\_ADDRESS\_MODE addressU = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, D3D12\_TEXTURE\_ADDRESS\_MODE addressV = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, D3D12\_TEXTURE\_ADDRESS\_MODE addressW = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12\_COMPARISON\_FUNC comparisonFunc = D3D12\_COMPARISON\_FUNC\_LESS\_EQUAL, D3D12\_STATIC\_BORDER\_COLOR borderColor = D3D12\_STATIC\_BORDER\_COLOR\_OPAQUE\_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12\_FLOAT32\_MAX, D3D12\_SHADER\_VISIBILITY shaderVisibility = D3D12\_SHADER\_VISIBILITY\_ALL, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="94b6c-128">Especifica uma função que inicializa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="94b6c-128">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="94b6c-129">[**D3D12 \_ \_Amostra \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) de samplerDesc &desc de forma estática</span><span class="sxs-lookup"><span data-stu-id="94b6c-129">[**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) &samplerDesc</span></span>

<span data-ttu-id="94b6c-130">ShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="94b6c-130">UINT shaderRegister</span></span>

<span data-ttu-id="94b6c-131">opt [**D3D12 \_ Filtro filtro =**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) \_ filtro D3D12 \_ ANISOTROPIC</span><span class="sxs-lookup"><span data-stu-id="94b6c-131">(opt) [**D3D12\_FILTER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) filter = D3D12\_FILTER\_ANISOTROPIC</span></span>

<span data-ttu-id="94b6c-132">opt [**D3D12 \_ \_ \_ Modo de endereço de textura**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressexception = modo de endereço de textura de D3D12 \_ \_ \_ \_ Wrap</span><span class="sxs-lookup"><span data-stu-id="94b6c-132">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressU = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="94b6c-133">opt [**D3D12 \_ \_ \_ Modo de endereço de textura**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressV = \_ \_ \_ \_ encapsulamento do modo de endereço de textura D3D12</span><span class="sxs-lookup"><span data-stu-id="94b6c-133">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressV = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="94b6c-134">opt [**D3D12 \_ \_ \_ Modo de endereço de textura**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressW = \_ \_ \_ \_ encapsulamento do modo de endereço de textura D3D12</span><span class="sxs-lookup"><span data-stu-id="94b6c-134">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressW = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="94b6c-135">opt FLOAT mipLODBias = 0</span><span class="sxs-lookup"><span data-stu-id="94b6c-135">(opt) FLOAT mipLODBias = 0</span></span>

<span data-ttu-id="94b6c-136">opt UINT maxAnisotropy = 16</span><span class="sxs-lookup"><span data-stu-id="94b6c-136">(opt) UINT maxAnisotropy = 16</span></span>

<span data-ttu-id="94b6c-137">opt [**D3D12 \_ COMPARAÇÃO \_ Func**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) COMPARISONFUNC = D3D12 \_ Comparison \_ Func \_ menos \_ igual</span><span class="sxs-lookup"><span data-stu-id="94b6c-137">(opt) [**D3D12\_COMPARISON\_FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) comparisonFunc = D3D12\_COMPARISON\_FUNC\_LESS\_EQUAL</span></span>

<span data-ttu-id="94b6c-138">opt [**D3D12 \_ \_ \_ Cor da borda estática**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) BorderColor = D3D12 de \_ \_ borda estática \_ cor \_ \_ branco opaco</span><span class="sxs-lookup"><span data-stu-id="94b6c-138">(opt) [**D3D12\_STATIC\_BORDER\_COLOR**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) borderColor = D3D12\_STATIC\_BORDER\_COLOR\_OPAQUE\_WHITE</span></span>

<span data-ttu-id="94b6c-139">opt FLOAT minLOD = 0. f</span><span class="sxs-lookup"><span data-stu-id="94b6c-139">(opt) FLOAT minLOD = 0.f</span></span>

<span data-ttu-id="94b6c-140">opt FLOAT maxLOD = D3D12 \_ FLOAT32 \_ Max</span><span class="sxs-lookup"><span data-stu-id="94b6c-140">(opt) FLOAT maxLOD = D3D12\_FLOAT32\_MAX</span></span>

<span data-ttu-id="94b6c-141">opt [**D3D12 \_ SHADER \_ Visibility**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) SHADERVISIBILITY = D3D12 \_ Shader \_ visibilidade \_ All</span><span class="sxs-lookup"><span data-stu-id="94b6c-141">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) shaderVisibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

<span data-ttu-id="94b6c-142">opt UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="94b6c-142">(opt) UINT registerSpace = 0</span></span>

</dd> <dt>

<span data-ttu-id="94b6c-143">**Init embutido (UINT shaderRegister, filtro de \_ filtro D3D12 = D3D12 \_ filtro \_ ANISOTROPIC, D3D12 \_ modo de endereço de textura \_ \_ endereçou = D3D12 modo de endereço \_ de textura \_ de D3D12 \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ modo de endereço de textura D3D12 addressW = \_ \_ \_ modo de endereço de textura de D3D12 \_ encapsulado, float mipLODBias = 0, uint maxAnisotropy = 16, D3D12 \_ Comparison \_ Func comparisonFunc = D3D12 \_ comparation \_ Func \_ \_ Equals, D3D12 \_ static \_ Border \_ Color BorderColor = D3D12 \_ static \_ Border \_ Color \_ opaco \_ , float minLOD = 0. f, float maxLOD = D3D12 \_ FLOAT32 \_ Max, D3D12 \_ Shader \_ Visibility shaderVisibility = D3D12 \_ Shader \_ visibilidade \_ All, uint registerSpace**</span><span class="sxs-lookup"><span data-stu-id="94b6c-143">**inline Init(UINT shaderRegister, D3D12\_FILTER filter = D3D12\_FILTER\_ANISOTROPIC, D3D12\_TEXTURE\_ADDRESS\_MODE addressU = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, D3D12\_TEXTURE\_ADDRESS\_MODE addressV = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, D3D12\_TEXTURE\_ADDRESS\_MODE addressW = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12\_COMPARISON\_FUNC comparisonFunc = D3D12\_COMPARISON\_FUNC\_LESS\_EQUAL, D3D12\_STATIC\_BORDER\_COLOR borderColor = D3D12\_STATIC\_BORDER\_COLOR\_OPAQUE\_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12\_FLOAT32\_MAX, D3D12\_SHADER\_VISIBILITY shaderVisibility = D3D12\_SHADER\_VISIBILITY\_ALL, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="94b6c-144">Especifica uma função que inicializa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="94b6c-144">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="94b6c-145">ShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="94b6c-145">UINT shaderRegister</span></span>

<span data-ttu-id="94b6c-146">opt [**D3D12 \_ Filtro filtro =**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) \_ filtro D3D12 \_ ANISOTROPIC</span><span class="sxs-lookup"><span data-stu-id="94b6c-146">(opt) [**D3D12\_FILTER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) filter = D3D12\_FILTER\_ANISOTROPIC</span></span>

<span data-ttu-id="94b6c-147">opt [**D3D12 \_ \_ \_ Modo de endereço de textura**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressexception = modo de endereço de textura de D3D12 \_ \_ \_ \_ Wrap</span><span class="sxs-lookup"><span data-stu-id="94b6c-147">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressU = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="94b6c-148">opt [**D3D12 \_ \_ \_ Modo de endereço de textura**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressV = \_ \_ \_ \_ encapsulamento do modo de endereço de textura D3D12</span><span class="sxs-lookup"><span data-stu-id="94b6c-148">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressV = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="94b6c-149">opt [**D3D12 \_ \_ \_ Modo de endereço de textura**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressW = \_ \_ \_ \_ encapsulamento do modo de endereço de textura D3D12</span><span class="sxs-lookup"><span data-stu-id="94b6c-149">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressW = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="94b6c-150">opt FLOAT mipLODBias = 0</span><span class="sxs-lookup"><span data-stu-id="94b6c-150">(opt) FLOAT mipLODBias = 0</span></span>

<span data-ttu-id="94b6c-151">opt UINT maxAnisotropy = 16</span><span class="sxs-lookup"><span data-stu-id="94b6c-151">(opt) UINT maxAnisotropy = 16</span></span>

<span data-ttu-id="94b6c-152">opt [**D3D12 \_ COMPARAÇÃO \_ Func**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) COMPARISONFUNC = D3D12 \_ Comparison \_ Func \_ menos \_ igual</span><span class="sxs-lookup"><span data-stu-id="94b6c-152">(opt) [**D3D12\_COMPARISON\_FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) comparisonFunc = D3D12\_COMPARISON\_FUNC\_LESS\_EQUAL</span></span>

<span data-ttu-id="94b6c-153">opt [**D3D12 \_ \_ \_ Cor da borda estática**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) BorderColor = D3D12 de \_ \_ borda estática \_ cor \_ \_ branco opaco</span><span class="sxs-lookup"><span data-stu-id="94b6c-153">(opt) [**D3D12\_STATIC\_BORDER\_COLOR**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) borderColor = D3D12\_STATIC\_BORDER\_COLOR\_OPAQUE\_WHITE</span></span>

<span data-ttu-id="94b6c-154">opt FLOAT minLOD = 0. f</span><span class="sxs-lookup"><span data-stu-id="94b6c-154">(opt) FLOAT minLOD = 0.f</span></span>

<span data-ttu-id="94b6c-155">opt FLOAT maxLOD = D3D12 \_ FLOAT32 \_ Max</span><span class="sxs-lookup"><span data-stu-id="94b6c-155">(opt) FLOAT maxLOD = D3D12\_FLOAT32\_MAX</span></span>

<span data-ttu-id="94b6c-156">opt [**D3D12 \_ SHADER \_ Visibility**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) SHADERVISIBILITY = D3D12 \_ Shader \_ visibilidade \_ All</span><span class="sxs-lookup"><span data-stu-id="94b6c-156">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) shaderVisibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

<span data-ttu-id="94b6c-157">opt UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="94b6c-157">(opt) UINT registerSpace = 0</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="94b6c-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94b6c-158">Requirements</span></span>



| <span data-ttu-id="94b6c-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="94b6c-159">Requirement</span></span> | <span data-ttu-id="94b6c-160">Valor</span><span class="sxs-lookup"><span data-stu-id="94b6c-160">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="94b6c-161">parâmetro</span><span class="sxs-lookup"><span data-stu-id="94b6c-161">Header</span></span><br/> | <dl> <span data-ttu-id="94b6c-162"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="94b6c-162"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94b6c-163">Confira também</span><span class="sxs-lookup"><span data-stu-id="94b6c-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94b6c-164">**Amostra de D3D12 \_ estática \_ \_ desc**</span><span class="sxs-lookup"><span data-stu-id="94b6c-164">**D3D12\_STATIC\_SAMPLER\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)
</dt> <dt>

[<span data-ttu-id="94b6c-165">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="94b6c-165">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





