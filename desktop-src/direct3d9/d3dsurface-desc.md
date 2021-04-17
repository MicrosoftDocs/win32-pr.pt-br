---
description: Descreve uma superfície.
ms.assetid: fad8ffdb-36e5-4695-b343-e1315357c31a
title: Estrutura de D3DSURFACE_DESC (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSURFACE_DESC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 6424bbe9b78532657670bc5cd9ad0705de89a3b0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105768379"
---
# <a name="d3dsurface_desc-structure"></a><span data-ttu-id="c327f-103">\_Estrutura desc de D3DSURFACE</span><span class="sxs-lookup"><span data-stu-id="c327f-103">D3DSURFACE\_DESC structure</span></span>

<span data-ttu-id="c327f-104">Descreve uma superfície.</span><span class="sxs-lookup"><span data-stu-id="c327f-104">Describes a surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="c327f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c327f-105">Syntax</span></span>


```C++
typedef struct D3DSURFACE_DESC {
  D3DFORMAT           Format;
  D3DRESOURCETYPE     Type;
  DWORD               Usage;
  D3DPOOL             Pool;
  D3DMULTISAMPLE_TYPE MultiSampleType;
  DWORD               MultiSampleQuality;
  UINT                Width;
  UINT                Height;
} D3DSURFACE_DESC, *LPD3DSURFACE_DESC;
```



## <a name="members"></a><span data-ttu-id="c327f-106">Membros</span><span class="sxs-lookup"><span data-stu-id="c327f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c327f-107">**Formato**</span><span class="sxs-lookup"><span data-stu-id="c327f-107">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="c327f-108">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="c327f-108">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c327f-109">Membro do tipo enumerado [D3DFORMAT](d3dformat.md) , que descreve o formato da superfície.</span><span class="sxs-lookup"><span data-stu-id="c327f-109">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the surface format.</span></span>

</dd> <dt>

<span data-ttu-id="c327f-110">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c327f-110">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="c327f-111">Tipo: **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**</span><span class="sxs-lookup"><span data-stu-id="c327f-111">Type: **[**D3DRESOURCETYPE**](./d3dresourcetype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c327f-112">Membro do tipo enumerado [**D3DRESOURCETYPE**](./d3dresourcetype.md) , identificando esse recurso como uma superfície.</span><span class="sxs-lookup"><span data-stu-id="c327f-112">Member of the [**D3DRESOURCETYPE**](./d3dresourcetype.md) enumerated type, identifying this resource as a surface.</span></span>

</dd> <dt>

<span data-ttu-id="c327f-113">**Usage**</span><span class="sxs-lookup"><span data-stu-id="c327f-113">**Usage**</span></span>
</dt> <dd>

<span data-ttu-id="c327f-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c327f-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c327f-115">Os valores D3DUSAGE \_ DEPTHSTENCIL ou D3DUSAGE \_ RENDERTARGET.</span><span class="sxs-lookup"><span data-stu-id="c327f-115">Either the D3DUSAGE\_DEPTHSTENCIL or D3DUSAGE\_RENDERTARGET values.</span></span> <span data-ttu-id="c327f-116">Para obter mais informações, consulte [**D3DUSAGE**](d3dusage.md).</span><span class="sxs-lookup"><span data-stu-id="c327f-116">For more information, see [**D3DUSAGE**](d3dusage.md).</span></span>

</dd> <dt>

<span data-ttu-id="c327f-117">**Pool**</span><span class="sxs-lookup"><span data-stu-id="c327f-117">**Pool**</span></span>
</dt> <dd>

<span data-ttu-id="c327f-118">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="c327f-118">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c327f-119">Membro do tipo enumerado [**D3DPOOL**](./d3dpool.md) , especificando a classe de memória alocada para essa superfície.</span><span class="sxs-lookup"><span data-stu-id="c327f-119">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, specifying the class of memory allocated for this surface.</span></span>

</dd> <dt>

<span data-ttu-id="c327f-120">**Multiamostratype**</span><span class="sxs-lookup"><span data-stu-id="c327f-120">**MultiSampleType**</span></span>
</dt> <dd>

<span data-ttu-id="c327f-121">Tipo: **[ **\_ tipo de D3DMULTISAMPLE**](./d3dmultisample-type.md)**</span><span class="sxs-lookup"><span data-stu-id="c327f-121">Type: **[**D3DMULTISAMPLE\_TYPE**](./d3dmultisample-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c327f-122">Membro do tipo [**\_ enumerado D3DMULTISAMPLE**](./d3dmultisample-type.md) , especificando os níveis de multiamostragens de cena completa com suporte na superfície.</span><span class="sxs-lookup"><span data-stu-id="c327f-122">Member of the [**D3DMULTISAMPLE\_TYPE**](./d3dmultisample-type.md) enumerated type, specifying the levels of full-scene multisampling supported by the surface.</span></span>

</dd> <dt>

<span data-ttu-id="c327f-123">**MultiSampleQuality**</span><span class="sxs-lookup"><span data-stu-id="c327f-123">**MultiSampleQuality**</span></span>
</dt> <dd>

<span data-ttu-id="c327f-124">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c327f-124">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c327f-125">Nível de qualidade.</span><span class="sxs-lookup"><span data-stu-id="c327f-125">Quality level.</span></span> <span data-ttu-id="c327f-126">O intervalo válido é entre zero e um menor que o nível retornado por pQualityLevels usado pelo [**CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype).</span><span class="sxs-lookup"><span data-stu-id="c327f-126">The valid range is between zero and one less than the level returned by pQualityLevels used by [**CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype).</span></span> <span data-ttu-id="c327f-127">Passar um valor maior retorna o erro D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="c327f-127">Passing a larger value returns the error, D3DERR\_INVALIDCALL.</span></span> <span data-ttu-id="c327f-128">Os valores MultisampleQuality de destinos de renderização emparelhados, superfícies de estêncil de profundidade e o tipo multiamostral devem corresponder a todos.</span><span class="sxs-lookup"><span data-stu-id="c327f-128">The MultisampleQuality values of paired render targets, depth stencil surfaces and the MultiSample type must all match.</span></span>

</dd> <dt>

<span data-ttu-id="c327f-129">**Largura**</span><span class="sxs-lookup"><span data-stu-id="c327f-129">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="c327f-130">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c327f-130">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c327f-131">Largura da superfície, em pixels.</span><span class="sxs-lookup"><span data-stu-id="c327f-131">Width of the surface, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="c327f-132">**Altura**</span><span class="sxs-lookup"><span data-stu-id="c327f-132">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="c327f-133">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c327f-133">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c327f-134">Altura da superfície, em pixels.</span><span class="sxs-lookup"><span data-stu-id="c327f-134">Height of the surface, in pixels.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c327f-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c327f-135">Requirements</span></span>



| <span data-ttu-id="c327f-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="c327f-136">Requirement</span></span> | <span data-ttu-id="c327f-137">Valor</span><span class="sxs-lookup"><span data-stu-id="c327f-137">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c327f-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c327f-138">Header</span></span><br/> | <dl> <span data-ttu-id="c327f-139"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="c327f-139"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c327f-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="c327f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c327f-141">Estruturas do Direct3D</span><span class="sxs-lookup"><span data-stu-id="c327f-141">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="c327f-142">**GetLevelDesc**</span><span class="sxs-lookup"><span data-stu-id="c327f-142">**GetLevelDesc**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getleveldesc)
</dt> <dt>

[<span data-ttu-id="c327f-143">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="c327f-143">**GetDesc**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-getdesc)
</dt> <dt>

[<span data-ttu-id="c327f-144">**GetLevelDesc**</span><span class="sxs-lookup"><span data-stu-id="c327f-144">**GetLevelDesc**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getleveldesc)
</dt> </dl>

 

 
