---
title: Estrutura de CD3DX12_RESOURCE_DESC (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ estrutura desc de recurso D3D12 \_ .
ms.assetid: F18D41BE-8AEF-444E-AC8B-EC57C63BF083
keywords:
- Estrutura de CD3DX12_RESOURCE_DESC
topic_type:
- apiref
api_name:
- CD3DX12_RESOURCE_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b341646b2dee7f469235c0b0bc9bb4550e56ff5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105798043"
---
# <a name="cd3dx12_resource_desc-structure"></a><span data-ttu-id="9a5c0-104">\_Estrutura desc de recurso CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="9a5c0-104">CD3DX12\_RESOURCE\_DESC structure</span></span>

<span data-ttu-id="9a5c0-105">Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura [**\_ \_ desc de recurso D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) .</span><span class="sxs-lookup"><span data-stu-id="9a5c0-105">A helper structure to enable easy initialization of a [**D3D12\_RESOURCE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a5c0-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9a5c0-106">Syntax</span></span>


```C++
struct CD3DX12_RESOURCE_DESC  : public D3D12_RESOURCE_DESC{
                        CD3DX12_RESOURCE_DESC();
                        explicit CD3DX12_RESOURCE_DESC(const D3D12_RESOURCE_DESC& o);
                        CD3DX12_RESOURCE_DESC(D3D12_RESOURCE_DIMENSION dimension, UINT64 alignment, UINT64 width, UINT height, UINT16 depthOrArraySize, UINT16 mipLevels, DXGI_FORMAT format, UINT sampleCount, UINT sampleQuality, D3D12_TEXTURE_LAYOUT layout, D3D12_RESOURCE_FLAGS flags);
  CD3DX12_RESOURCE_DESC static inline Buffer(const D3D12_RESOURCE_ALLOCATION_INFO& resAllocInfo, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE);
  CD3DX12_RESOURCE_DESC static inline Buffer(UINT64 width, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE, UINT64 alignment = 0);
  CD3DX12_RESOURCE_DESC static inline Tex1D(DXGI_FORMAT format, UINT64 width, UINT16 arraySize = 1, UINT16 mipLevels = 0, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 alignment = 0);
  CD3DX12_RESOURCE_DESC static inline Tex2D(DXGI_FORMAT format, UINT64 width, UINT height, UINT16 arraySize = 1, UINT16 mipLevels = 0, UINT sampleCount = 1, UINT sampleQuality = 0, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 alignment = 0);
  CD3DX12_RESOURCE_DESC static inline Tex3D(DXGI_FORMAT format, UINT64 width, UINT height, UINT16 depth, UINT16 mipLevels = 0, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 alignment = 0);
  UINT16                inline Depth() const;
  UINT16                inline ArraySize() const;
  UINT8                 inline PlaneCount(ID3D12Device* pDevice) const;
  UINT                  inline Subresources(ID3D12Device* pDevice) const;
  UINT                  inline CalcSubresource(UINT MipSlice, UINT ArraySlice, UINT PlaneSlice);
                        operator const D3D12_RESOURCE_DESC&() const;
                        operator == (const D3D12_RESOURCE_DESC& l, const D3D12_RESOURCE_DESC& r);
                        operator !=  (const D3D12_RESOURCE_DESC& l, const D3D12_RESOURCE_DESC& r);
};
```



## <a name="members"></a><span data-ttu-id="9a5c0-107">Membros</span><span class="sxs-lookup"><span data-stu-id="9a5c0-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="9a5c0-108">**\_Recurso CD3DX12 \_ DESC ()**</span><span class="sxs-lookup"><span data-stu-id="9a5c0-108">**CD3DX12\_RESOURCE\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="9a5c0-109">Cria uma nova instância, não inicializada, de um \_ recurso CD3DX12 \_ desc.</span><span class="sxs-lookup"><span data-stu-id="9a5c0-109">Creates a new, uninitialized, instance of a CD3DX12\_RESOURCE\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="9a5c0-110">**recurso CD3DX12 \_ explícito \_ DESC (const D3D12 \_ recurso \_ desc& o)**</span><span class="sxs-lookup"><span data-stu-id="9a5c0-110">**explicit CD3DX12\_RESOURCE\_DESC(const D3D12\_RESOURCE\_DESC& o)**</span></span>
</dt> <dd>

<span data-ttu-id="9a5c0-111">Cria uma nova instância de um \_ recurso CD3DX12 \_ DESC, inicializada com o conteúdo de outra estrutura [**\_ \_ desc de recurso D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) .</span><span class="sxs-lookup"><span data-stu-id="9a5c0-111">Creates a new instance of a CD3DX12\_RESOURCE\_DESC, initialized with the contents of another [**D3D12\_RESOURCE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="9a5c0-112">**\_Recurso CD3DX12 \_ DESC ( \_ \_ dimensão de dimensão de recurso D3D12, alinhamento de UINT64, largura de UInt64, altura uint, UInt16 depthOrArraySize, UInt16 mipLevels, \_ formato de formato dxgi, uint SAMPLECOUNT, uint sampleQuality, D3D12 \_ \_ layout de layout de textura, D3D12 \_ flags de sinalizadores de recurso \_ )**</span><span class="sxs-lookup"><span data-stu-id="9a5c0-112">**CD3DX12\_RESOURCE\_DESC(D3D12\_RESOURCE\_DIMENSION dimension, UINT64 alignment, UINT64 width, UINT height, UINT16 depthOrArraySize, UINT16 mipLevels, DXGI\_FORMAT format, UINT sampleCount, UINT sampleQuality, D3D12\_TEXTURE\_LAYOUT layout, D3D12\_RESOURCE\_FLAGS flags)**</span></span>
</dt> <dd>

<span data-ttu-id="9a5c0-113">Cria uma nova instância de um \_ recurso CD3DX12 \_ DESC, inicializando os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="9a5c0-113">Creates a new instance of a CD3DX12\_RESOURCE\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="9a5c0-114">[**D3D12 \_ Dimensão de \_ dimensão de recurso**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension)</span><span class="sxs-lookup"><span data-stu-id="9a5c0-114">[**D3D12\_RESOURCE\_DIMENSION**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension) dimension</span></span>

<span data-ttu-id="9a5c0-115">Alinhamento de UINT64</span><span class="sxs-lookup"><span data-stu-id="9a5c0-115">UINT64 alignment</span></span>

<span data-ttu-id="9a5c0-116">Largura de UINT64</span><span class="sxs-lookup"><span data-stu-id="9a5c0-116">UINT64 width</span></span>

<span data-ttu-id="9a5c0-117">Altura UINT</span><span class="sxs-lookup"><span data-stu-id="9a5c0-117">UINT height</span></span>

<span data-ttu-id="9a5c0-118">UINT16 depthOrArraySize</span><span class="sxs-lookup"><span data-stu-id="9a5c0-118">UINT16 depthOrArraySize</span></span>

<span data-ttu-id="9a5c0-119">UINT16 mipLevels</span><span class="sxs-lookup"><span data-stu-id="9a5c0-119">UINT16 mipLevels</span></span>

<span data-ttu-id="9a5c0-120">[**Dxgi \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Formato de formato</span><span class="sxs-lookup"><span data-stu-id="9a5c0-120">[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) format</span></span>

<span data-ttu-id="9a5c0-121">SampleCount UINT</span><span class="sxs-lookup"><span data-stu-id="9a5c0-121">UINT sampleCount</span></span>

<span data-ttu-id="9a5c0-122">SampleQuality UINT</span><span class="sxs-lookup"><span data-stu-id="9a5c0-122">UINT sampleQuality</span></span>

<span data-ttu-id="9a5c0-123">[**D3D12 \_ Layout de \_ layout de textura**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout)</span><span class="sxs-lookup"><span data-stu-id="9a5c0-123">[**D3D12\_TEXTURE\_LAYOUT**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) layout</span></span>

<span data-ttu-id="9a5c0-124">[**D3D12 \_ Sinalizadores de \_ sinalizadores de recurso**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags)</span><span class="sxs-lookup"><span data-stu-id="9a5c0-124">[**D3D12\_RESOURCE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) flags</span></span>

</dd> <dt>

<span data-ttu-id="9a5c0-125">**Buffer embutido estático (const \_ D3D12 \_ informações de alocação de recursos \_& resAllocInfo, \_ sinalizadores de sinalizadores de recursos D3D12 \_ = D3D12 \_ sinalizador de recurso \_ \_ nenhum)**</span><span class="sxs-lookup"><span data-stu-id="9a5c0-125">**static inline Buffer(const D3D12\_RESOURCE\_ALLOCATION\_INFO& resAllocInfo, D3D12\_RESOURCE\_FLAGS flags = D3D12\_RESOURCE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="9a5c0-126">Especifica uma função que inicializa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="9a5c0-126">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="9a5c0-127">[**D3D12 \_ \_ \_ Informações de alocação de recursos**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo</span><span class="sxs-lookup"><span data-stu-id="9a5c0-127">[**D3D12\_RESOURCE\_ALLOCATION\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo</span></span>

<span data-ttu-id="9a5c0-128">opt [**D3D12 \_ Sinalizadores de \_ sinalizadores de recurso**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) = sinalizador de recurso D3D12 \_ \_ \_ nenhum</span><span class="sxs-lookup"><span data-stu-id="9a5c0-128">(opt) [**D3D12\_RESOURCE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) flags = D3D12\_RESOURCE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="9a5c0-129">**Buffer embutido estático (largura de UINT64, sinalizadores de \_ sinalizadores de recurso D3D12 \_ = \_ \_ sinalizador de recurso D3D12 \_ nenhum, alinhamento de UInt64 = 0)**</span><span class="sxs-lookup"><span data-stu-id="9a5c0-129">**static inline Buffer(UINT64 width, D3D12\_RESOURCE\_FLAGS flags = D3D12\_RESOURCE\_FLAG\_NONE, UINT64 alignment = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="9a5c0-130">Especifica uma função que inicializa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="9a5c0-130">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="9a5c0-131">Largura de UINT64</span><span class="sxs-lookup"><span data-stu-id="9a5c0-131">UINT64 width</span></span>

<span data-ttu-id="9a5c0-132">opt [**D3D12 \_ Sinalizadores de \_ sinalizadores de recurso**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) = sinalizador de recurso D3D12 \_ \_ \_ nenhum</span><span class="sxs-lookup"><span data-stu-id="9a5c0-132">(opt) [**D3D12\_RESOURCE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) flags = D3D12\_RESOURCE\_FLAG\_NONE</span></span>

<span data-ttu-id="9a5c0-133">opt Alinhamento de UINT64 = 0</span><span class="sxs-lookup"><span data-stu-id="9a5c0-133">(opt) UINT64 alignment = 0</span></span>

</dd> <dt>

<span data-ttu-id="9a5c0-134">**Tex1D embutido estático ( \_ formato de formato dxgi, largura de UINT64, UINT16-matrizes = 1, UINT16 mipLevels = 0, D3D12 sinalizadores de \_ sinalizadores de recursos \_ = D3D12 \_ \_ sinalizador \_ de recurso nenhum, D3D12 de layout de textura de vetor \_ \_ = D3D12 \_ \_ layout de textura \_ desconhecido, alinhamento de UINT64 = 0)**</span><span class="sxs-lookup"><span data-stu-id="9a5c0-134">**static inline Tex1D(DXGI\_FORMAT format, UINT64 width, UINT16 arraySize = 1, UINT16 mipLevels = 0, D3D12\_RESOURCE\_FLAGS flags = D3D12\_RESOURCE\_FLAG\_NONE, D3D12\_TEXTURE\_LAYOUT layout = D3D12\_TEXTURE\_LAYOUT\_UNKNOWN, UINT64 alignment = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="9a5c0-135">Especifica uma função que inicializa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="9a5c0-135">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="9a5c0-136">[**Dxgi \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Formato de formato</span><span class="sxs-lookup"><span data-stu-id="9a5c0-136">[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) format</span></span>

<span data-ttu-id="9a5c0-137">Largura de UINT64</span><span class="sxs-lookup"><span data-stu-id="9a5c0-137">UINT64 width</span></span>

<span data-ttu-id="9a5c0-138">opt UINT16 matrizes = 1</span><span class="sxs-lookup"><span data-stu-id="9a5c0-138">(opt) UINT16 arraySize = 1</span></span>

<span data-ttu-id="9a5c0-139">opt UINT16 mipLevels = 0</span><span class="sxs-lookup"><span data-stu-id="9a5c0-139">(opt) UINT16 mipLevels = 0</span></span>

<span data-ttu-id="9a5c0-140">opt [**D3D12 \_ Sinalizadores de \_ sinalizadores de recurso**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) = sinalizador de recurso D3D12 \_ \_ \_ nenhum</span><span class="sxs-lookup"><span data-stu-id="9a5c0-140">(opt) [**D3D12\_RESOURCE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) flags = D3D12\_RESOURCE\_FLAG\_NONE</span></span>

<span data-ttu-id="9a5c0-141">opt [**D3D12 \_ Layout do \_ layout de textura**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) = layout de textura D3D12 \_ \_ \_ desconhecido</span><span class="sxs-lookup"><span data-stu-id="9a5c0-141">(opt) [**D3D12\_TEXTURE\_LAYOUT**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) layout = D3D12\_TEXTURE\_LAYOUT\_UNKNOWN</span></span>

<span data-ttu-id="9a5c0-142">opt Alinhamento de UINT64 = 0</span><span class="sxs-lookup"><span data-stu-id="9a5c0-142">(opt) UINT64 alignment = 0</span></span>

</dd> <dt>

<span data-ttu-id="9a5c0-143">**estático embutido Tex2D ( \_ formato de formato dxgi, largura de UINT64, altura uint, UINT16 matrizes = 1, UINT16 mipLevels = 0, uint sampleCount = 1, uint sampleQuality = 0, sinalizadores de sinalizadores de recursos de D3D12 \_ \_ = D3D12 \_ \_ sinalizador de recurso \_ nenhum, D3D12 layout de \_ layout de textura \_ = D3D12 \_ \_ layout de textura \_ desconhecido, alinhamento de UINT64 = 0)**</span><span class="sxs-lookup"><span data-stu-id="9a5c0-143">**static inline Tex2D(DXGI\_FORMAT format, UINT64 width, UINT height, UINT16 arraySize = 1, UINT16 mipLevels = 0, UINT sampleCount = 1, UINT sampleQuality = 0, D3D12\_RESOURCE\_FLAGS flags = D3D12\_RESOURCE\_FLAG\_NONE, D3D12\_TEXTURE\_LAYOUT layout = D3D12\_TEXTURE\_LAYOUT\_UNKNOWN, UINT64 alignment = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="9a5c0-144">Especifica uma função que inicializa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="9a5c0-144">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="9a5c0-145">[**Dxgi \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Formato de formato</span><span class="sxs-lookup"><span data-stu-id="9a5c0-145">[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) format</span></span>

<span data-ttu-id="9a5c0-146">Largura de UINT64</span><span class="sxs-lookup"><span data-stu-id="9a5c0-146">UINT64 width</span></span>

<span data-ttu-id="9a5c0-147">Altura UINT</span><span class="sxs-lookup"><span data-stu-id="9a5c0-147">UINT height</span></span>

<span data-ttu-id="9a5c0-148">opt UINT16 matrizes = 1</span><span class="sxs-lookup"><span data-stu-id="9a5c0-148">(opt) UINT16 arraySize = 1</span></span>

<span data-ttu-id="9a5c0-149">opt UINT16 mipLevels = 0</span><span class="sxs-lookup"><span data-stu-id="9a5c0-149">(opt) UINT16 mipLevels = 0</span></span>

<span data-ttu-id="9a5c0-150">opt UINT sampleCount = 1</span><span class="sxs-lookup"><span data-stu-id="9a5c0-150">(opt) UINT sampleCount = 1</span></span>

<span data-ttu-id="9a5c0-151">opt UINT sampleQuality = 0</span><span class="sxs-lookup"><span data-stu-id="9a5c0-151">(opt) UINT sampleQuality = 0</span></span>

<span data-ttu-id="9a5c0-152">opt [**D3D12 \_ Sinalizadores de \_ sinalizadores de recurso**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) = sinalizador de recurso D3D12 \_ \_ \_ nenhum</span><span class="sxs-lookup"><span data-stu-id="9a5c0-152">(opt) [**D3D12\_RESOURCE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) flags = D3D12\_RESOURCE\_FLAG\_NONE</span></span>

<span data-ttu-id="9a5c0-153">opt [**D3D12 \_ Layout do \_ layout de textura**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) = layout de textura D3D12 \_ \_ \_ desconhecido</span><span class="sxs-lookup"><span data-stu-id="9a5c0-153">(opt) [**D3D12\_TEXTURE\_LAYOUT**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) layout = D3D12\_TEXTURE\_LAYOUT\_UNKNOWN</span></span>

<span data-ttu-id="9a5c0-154">opt Alinhamento de UINT64 = 0</span><span class="sxs-lookup"><span data-stu-id="9a5c0-154">(opt) UINT64 alignment = 0</span></span>

</dd> <dt>

<span data-ttu-id="9a5c0-155">**estático embutido Tex3D ( \_ formato de formato dxgi, largura UINT64, altura uint, intensidade de UInt16, UInt16 mipLevels = 0, D3D12 sinalizadores de \_ recurso \_ sinalizadores = D3D12 \_ sinalizador de recurso \_ \_ nenhum, D3D12 layout de \_ layout de textura \_ = D3D12 de \_ \_ layout de textura \_ desconhecido, alinhamento de UINT64 = 0)**</span><span class="sxs-lookup"><span data-stu-id="9a5c0-155">**static inline Tex3D(DXGI\_FORMAT format, UINT64 width, UINT height, UINT16 depth, UINT16 mipLevels = 0, D3D12\_RESOURCE\_FLAGS flags = D3D12\_RESOURCE\_FLAG\_NONE, D3D12\_TEXTURE\_LAYOUT layout = D3D12\_TEXTURE\_LAYOUT\_UNKNOWN, UINT64 alignment = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="9a5c0-156">Especifica uma função que inicializa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="9a5c0-156">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="9a5c0-157">[**Dxgi \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Formato de formato</span><span class="sxs-lookup"><span data-stu-id="9a5c0-157">[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) format</span></span>

<span data-ttu-id="9a5c0-158">Largura de UINT64</span><span class="sxs-lookup"><span data-stu-id="9a5c0-158">UINT64 width</span></span>

<span data-ttu-id="9a5c0-159">Altura UINT</span><span class="sxs-lookup"><span data-stu-id="9a5c0-159">UINT height</span></span>

<span data-ttu-id="9a5c0-160">Profundidade de UINT16</span><span class="sxs-lookup"><span data-stu-id="9a5c0-160">UINT16 depth</span></span>

<span data-ttu-id="9a5c0-161">opt UINT16 mipLevels = 0</span><span class="sxs-lookup"><span data-stu-id="9a5c0-161">(opt) UINT16 mipLevels = 0</span></span>

<span data-ttu-id="9a5c0-162">opt [**D3D12 \_ Sinalizadores de \_ sinalizadores de recurso**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) = sinalizador de recurso D3D12 \_ \_ \_ nenhum</span><span class="sxs-lookup"><span data-stu-id="9a5c0-162">(opt) [**D3D12\_RESOURCE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) flags = D3D12\_RESOURCE\_FLAG\_NONE</span></span>

<span data-ttu-id="9a5c0-163">opt [**D3D12 \_ Layout do \_ layout de textura**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) = layout de textura D3D12 \_ \_ \_ desconhecido</span><span class="sxs-lookup"><span data-stu-id="9a5c0-163">(opt) [**D3D12\_TEXTURE\_LAYOUT**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) layout = D3D12\_TEXTURE\_LAYOUT\_UNKNOWN</span></span>

<span data-ttu-id="9a5c0-164">opt Alinhamento de UINT64 = 0</span><span class="sxs-lookup"><span data-stu-id="9a5c0-164">(opt) UINT64 alignment = 0</span></span>

</dd> <dt>

<span data-ttu-id="9a5c0-165">**constante embutida () const**</span><span class="sxs-lookup"><span data-stu-id="9a5c0-165">**inline Depth() const**</span></span>
</dt> <dd>

<span data-ttu-id="9a5c0-166">Se Dimension = = [**D3D12 \_ Resource \_ Dimension**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension) \_ TEXTURE3D, retornará DepthOrArraySize.</span><span class="sxs-lookup"><span data-stu-id="9a5c0-166">If Dimension == [**D3D12\_RESOURCE\_DIMENSION**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension)\_TEXTURE3D, returns DepthOrArraySize.</span></span> <span data-ttu-id="9a5c0-167">Se Dimension! = D3D12 \_ Resource \_ Dimension \_ TEXTURE3D, retornará 1.</span><span class="sxs-lookup"><span data-stu-id="9a5c0-167">If Dimension != D3D12\_RESOURCE\_DIMENSION\_TEXTURE3D, returns 1.</span></span>

</dd> <dt>

<span data-ttu-id="9a5c0-168">**constante de matrizes embutidas () const**</span><span class="sxs-lookup"><span data-stu-id="9a5c0-168">**inline ArraySize() const**</span></span>
</dt> <dd>

<span data-ttu-id="9a5c0-169">Se Dimension! = D3D12 \_ Resource \_ Dimension \_ TEXTURE3D, retornará DepthOrArraySize.</span><span class="sxs-lookup"><span data-stu-id="9a5c0-169">If Dimension != D3D12\_RESOURCE\_DIMENSION\_TEXTURE3D, returns DepthOrArraySize.</span></span> <span data-ttu-id="9a5c0-170">Se Dimension = = D3D12 \_ Resource \_ Dimension \_ TEXTURE3D, retornará 1.</span><span class="sxs-lookup"><span data-stu-id="9a5c0-170">If Dimension == D3D12\_RESOURCE\_DIMENSION\_TEXTURE3D, returns 1.</span></span> <span data-ttu-id="9a5c0-171">Consulte [**D3D12 \_ Resource \_ Dimension**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension) \_ TEXTURE3D.</span><span class="sxs-lookup"><span data-stu-id="9a5c0-171">See [**D3D12\_RESOURCE\_DIMENSION**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension)\_TEXTURE3D.</span></span>

</dd> <dt>

<span data-ttu-id="9a5c0-172">**PlaneCount embutida (ID3D12Device \* pDevice) const**</span><span class="sxs-lookup"><span data-stu-id="9a5c0-172">**inline PlaneCount(ID3D12Device\* pDevice) const**</span></span>
</dt> <dd>

<span data-ttu-id="9a5c0-173">Retorna D3D12GetFormatPlaneCount (pDevice, Format).</span><span class="sxs-lookup"><span data-stu-id="9a5c0-173">Returns D3D12GetFormatPlaneCount(pDevice, Format).</span></span> <span data-ttu-id="9a5c0-174">Consulte [**D3D12GetFormatPlaneCount**](d3d12getformatplanecount.md) e [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device).</span><span class="sxs-lookup"><span data-stu-id="9a5c0-174">See [**D3D12GetFormatPlaneCount**](d3d12getformatplanecount.md) and [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device).</span></span>

</dd> <dt>

<span data-ttu-id="9a5c0-175">**ID3D12Device de subrecursos embutidos ( \* pDevice) const**</span><span class="sxs-lookup"><span data-stu-id="9a5c0-175">**inline Subresources(ID3D12Device\* pDevice) const**</span></span>
</dt> <dd>

<span data-ttu-id="9a5c0-176">Retorna o número de subrecursos, calculado como MipLevels de \* matrizize () \* PlaneCount (pDevice).</span><span class="sxs-lookup"><span data-stu-id="9a5c0-176">Returns the number of subresources, calculated as MipLevels \* ArraySize() \* PlaneCount(pDevice).</span></span>

</dd> <dt>

<span data-ttu-id="9a5c0-177">**CalcSubresource embutido (UINT MipSlice, UINT ArraySlice, UINT PlaneSlice)**</span><span class="sxs-lookup"><span data-stu-id="9a5c0-177">**inline CalcSubresource(UINT MipSlice, UINT ArraySlice, UINT PlaneSlice)**</span></span>
</dt> <dd>

<span data-ttu-id="9a5c0-178">Calcula um índice de subrecurso usando [**D3D12CalcSubresource**](d3d12calcsubresource.md).</span><span class="sxs-lookup"><span data-stu-id="9a5c0-178">Calculates a subresource index, by using [**D3D12CalcSubresource**](d3d12calcsubresource.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a5c0-179">**\_ \_ constante de& de recurso const D3D12 () const**</span><span class="sxs-lookup"><span data-stu-id="9a5c0-179">**operator const D3D12\_RESOURCE\_DESC&() const**</span></span>
</dt> <dd>

<span data-ttu-id="9a5c0-180">Define o & operador de passagem por referência para o tipo de estrutura pai.</span><span class="sxs-lookup"><span data-stu-id="9a5c0-180">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> <dt>

<span data-ttu-id="9a5c0-181">**Operator = = (const D3D12 \_ recurso \_ desc& l, const D3D12 \_ recurso \_ desc& r)**</span><span class="sxs-lookup"><span data-stu-id="9a5c0-181">**operator == (const D3D12\_RESOURCE\_DESC& l, const D3D12\_RESOURCE\_DESC& r)**</span></span>
</dt> <dd>

<span data-ttu-id="9a5c0-182">Retornará true se todos os membros de cada estrutura forem idênticos.</span><span class="sxs-lookup"><span data-stu-id="9a5c0-182">Returns true if all members of each structure are identical.</span></span>

</dd> <dt>

<span data-ttu-id="9a5c0-183">**Operator! = (const D3D12 \_ Resource \_ desc& l, const D3D12 \_ Resource \_ desc& r)**</span><span class="sxs-lookup"><span data-stu-id="9a5c0-183">**operator != (const D3D12\_RESOURCE\_DESC& l, const D3D12\_RESOURCE\_DESC& r)**</span></span>
</dt> <dd>

<span data-ttu-id="9a5c0-184">Retornará false se todos os membros de cada estrutura forem idênticos.</span><span class="sxs-lookup"><span data-stu-id="9a5c0-184">Returns false if all members of each structure are identical.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9a5c0-185">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a5c0-185">Requirements</span></span>



| <span data-ttu-id="9a5c0-186">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a5c0-186">Requirement</span></span> | <span data-ttu-id="9a5c0-187">Valor</span><span class="sxs-lookup"><span data-stu-id="9a5c0-187">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9a5c0-188">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9a5c0-188">Header</span></span><br/> | <dl> <span data-ttu-id="9a5c0-189"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a5c0-189"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a5c0-190">Confira também</span><span class="sxs-lookup"><span data-stu-id="9a5c0-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a5c0-191">**D3D12 de \_ recurso \_ desc**</span><span class="sxs-lookup"><span data-stu-id="9a5c0-191">**D3D12\_RESOURCE\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc)
</dt> <dt>

[<span data-ttu-id="9a5c0-192">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="9a5c0-192">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

