---
description: Converte um mapa de altura em um mapa normal. Os componentes (x, y, z) de cada normal são mapeados para os canais (r, g, b) da textura de saída.
ms.assetid: ed9053c0-b1df-4f74-bdee-627c0f60d942
title: Função D3DXComputeNormalMap (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeNormalMap
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6e22418f5a023dbe70fee8ea0fba8a449abbcc8d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105814444"
---
# <a name="d3dxcomputenormalmap-function"></a><span data-ttu-id="541c5-104">Função D3DXComputeNormalMap</span><span class="sxs-lookup"><span data-stu-id="541c5-104">D3DXComputeNormalMap function</span></span>

<span data-ttu-id="541c5-105">Converte um mapa de altura em um mapa normal.</span><span class="sxs-lookup"><span data-stu-id="541c5-105">Converts a height map into a normal map.</span></span> <span data-ttu-id="541c5-106">Os componentes (x, y, z) de cada normal são mapeados para os canais (r, g, b) da textura de saída.</span><span class="sxs-lookup"><span data-stu-id="541c5-106">The (x,y,z) components of each normal are mapped to the (r,g,b) channels of the output texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="541c5-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="541c5-107">Syntax</span></span>


```C++
HRESULT D3DXComputeNormalMap(
  _Out_       LPDIRECT3DTEXTURE9 pTexture,
  _In_        LPDIRECT3DTEXTURE9 pSrcTexture,
  _In_  const PALETTEENTRY       *pSrcPalette,
  _In_        DWORD              Flags,
  _In_        DWORD              Channel,
  _In_        FLOAT              Amplitude
);
```



## <a name="parameters"></a><span data-ttu-id="541c5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="541c5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="541c5-109">*pTexture* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="541c5-109">*pTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="541c5-110">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="541c5-110">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="541c5-111">Ponteiro para uma interface [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , representando a textura de destino.</span><span class="sxs-lookup"><span data-stu-id="541c5-111">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the destination texture.</span></span>

</dd> <dt>

<span data-ttu-id="541c5-112">*pSrcTexture* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="541c5-112">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="541c5-113">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="541c5-113">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="541c5-114">Ponteiro para uma interface [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , representando a textura de mapa de altura de origem.</span><span class="sxs-lookup"><span data-stu-id="541c5-114">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the source height-map texture.</span></span>

</dd> <dt>

<span data-ttu-id="541c5-115">*pSrcPalette* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="541c5-115">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="541c5-116">Tipo: **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="541c5-116">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="541c5-117">Ponteiro para um tipo [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) que contém a paleta de origem de 256 cores ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="541c5-117">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) type that contains the source palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="541c5-118">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="541c5-118">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="541c5-119">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="541c5-119">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="541c5-120">Um ou mais sinalizadores [D3DX \_ NormalMap](d3dx-normalmap.md) que controlam a geração de mapas normais.</span><span class="sxs-lookup"><span data-stu-id="541c5-120">One or more [D3DX\_NORMALMAP](d3dx-normalmap.md) flags that control generation of normal maps.</span></span>

</dd> <dt>

<span data-ttu-id="541c5-121">*Canal* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="541c5-121">*Channel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="541c5-122">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="541c5-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="541c5-123">Um sinalizador de [ \_ canal D3DX](d3dx-channel.md) especificando a fonte de informações de altura.</span><span class="sxs-lookup"><span data-stu-id="541c5-123">One [D3DX\_CHANNEL](d3dx-channel.md) flag specifying the source of height information.</span></span>

</dd> <dt>

<span data-ttu-id="541c5-124">*Amplitude* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="541c5-124">*Amplitude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="541c5-125">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="541c5-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="541c5-126">Multiplicador de valor constante que aumenta (ou diminui) os valores no mapa normal.</span><span class="sxs-lookup"><span data-stu-id="541c5-126">Constant value multiplier that increases (or decreases) the values in the normal map.</span></span> <span data-ttu-id="541c5-127">Valores mais altos geralmente tornam os choques mais visíveis, os valores mais baixos geralmente tornam os choques menos visíveis.</span><span class="sxs-lookup"><span data-stu-id="541c5-127">Higher values usually make bumps more visible, lower values usually make bumps less visible.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="541c5-128">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="541c5-128">Return value</span></span>

<span data-ttu-id="541c5-129">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="541c5-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="541c5-130">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="541c5-130">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="541c5-131">Se a função falhar, o valor de retorno poderá ser o seguinte valor: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="541c5-131">If the function fails, the return value can be the following value: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="541c5-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="541c5-132">Remarks</span></span>

<span data-ttu-id="541c5-133">Esse método computa o normal usando a diferença central com um tamanho de kernel de 3x3.</span><span class="sxs-lookup"><span data-stu-id="541c5-133">This method computes the normal by using the central difference with a kernel size of 3x3.</span></span> <span data-ttu-id="541c5-134">O denominador diferencial central usado é 2,0.</span><span class="sxs-lookup"><span data-stu-id="541c5-134">The central differencing denominator used is 2.0.</span></span> <span data-ttu-id="541c5-135">Os canais RGB no destino contêm componentes com tendência (x, y, z) do normal.</span><span class="sxs-lookup"><span data-stu-id="541c5-135">RGB channels in the destination contain biased (x,y,z) components of the normal.</span></span>

## <a name="requirements"></a><span data-ttu-id="541c5-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="541c5-136">Requirements</span></span>



| <span data-ttu-id="541c5-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="541c5-137">Requirement</span></span> | <span data-ttu-id="541c5-138">Valor</span><span class="sxs-lookup"><span data-stu-id="541c5-138">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="541c5-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="541c5-139">Header</span></span><br/>  | <dl> <span data-ttu-id="541c5-140"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="541c5-140"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="541c5-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="541c5-141">Library</span></span><br/> | <dl> <span data-ttu-id="541c5-142"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="541c5-142"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="541c5-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="541c5-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="541c5-144">Funções de textura no D3DX 9</span><span class="sxs-lookup"><span data-stu-id="541c5-144">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
