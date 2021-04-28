---
description: Função D3DX10ComputeNormalMap – converte um mapa de altura em um mapa normal. Os componentes (x, y, z) de cada normal são mapeados para os canais (r, g, b) da textura de saída.
ms.assetid: 535033dd-f078-4d56-8e5d-cdda80ef5992
title: Função D3DX10ComputeNormalMap (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10ComputeNormalMap
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 173a8e0c1b3130a399152187eb52288a0306051c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105314"
---
# <a name="d3dx10computenormalmap-function"></a><span data-ttu-id="68811-104">Função D3DX10ComputeNormalMap</span><span class="sxs-lookup"><span data-stu-id="68811-104">D3DX10ComputeNormalMap function</span></span>

<span data-ttu-id="68811-105">Converte um mapa de altura em um mapa normal.</span><span class="sxs-lookup"><span data-stu-id="68811-105">Converts a height map into a normal map.</span></span> <span data-ttu-id="68811-106">Os componentes (x, y, z) de cada normal são mapeados para os canais (r, g, b) da textura de saída.</span><span class="sxs-lookup"><span data-stu-id="68811-106">The (x,y,z) components of each normal are mapped to the (r,g,b) channels of the output texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="68811-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="68811-107">Syntax</span></span>


```C++
HRESULT D3DX10ComputeNormalMap(
  _In_ ID3D10Texture2D *pSrcTexture,
  _In_ UINT            Flags,
  _In_ UINT            Channel,
  _In_ FLOAT           Amplitude,
  _In_ ID3D10Texture2D *pDestTexture
);
```



## <a name="parameters"></a><span data-ttu-id="68811-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="68811-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68811-109">*pSrcTexture* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="68811-109">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68811-110">Tipo: **[ **ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***</span><span class="sxs-lookup"><span data-stu-id="68811-110">Type: **[**ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***</span></span>

<span data-ttu-id="68811-111">Ponteiro para uma interface ID3D10Texture2D, representando a textura de mapa de altura de origem.</span><span class="sxs-lookup"><span data-stu-id="68811-111">Pointer to an ID3D10Texture2D interface, representing the source height-map texture.</span></span>

</dd> <dt>

<span data-ttu-id="68811-112">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="68811-112">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68811-113">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="68811-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="68811-114">Um ou mais \_ sinalizadores D3DX NormalMap que controlam a geração de mapas normais.</span><span class="sxs-lookup"><span data-stu-id="68811-114">One or more D3DX\_NORMALMAP flags that control generation of normal maps.</span></span>

</dd> <dt>

<span data-ttu-id="68811-115">*Canal* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="68811-115">*Channel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68811-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="68811-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="68811-117">Um \_ sinalizador de canal D3DX especificando a fonte de informações de altura.</span><span class="sxs-lookup"><span data-stu-id="68811-117">One D3DX\_CHANNEL flag specifying the source of height information.</span></span>

</dd> <dt>

<span data-ttu-id="68811-118">*Amplitude* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="68811-118">*Amplitude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68811-119">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="68811-119">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="68811-120">Multiplicador de valor constante que aumenta (ou diminui) os valores no mapa normal.</span><span class="sxs-lookup"><span data-stu-id="68811-120">Constant value multiplier that increases (or decreases) the values in the normal map.</span></span> <span data-ttu-id="68811-121">Valores mais altos geralmente tornam os choques mais visíveis, os valores mais baixos geralmente tornam os choques menos visíveis.</span><span class="sxs-lookup"><span data-stu-id="68811-121">Higher values usually make bumps more visible, lower values usually make bumps less visible.</span></span>

</dd> <dt>

<span data-ttu-id="68811-122">*pDestTexture* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="68811-122">*pDestTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68811-123">Tipo: **[ **ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***</span><span class="sxs-lookup"><span data-stu-id="68811-123">Type: **[**ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***</span></span>

<span data-ttu-id="68811-124">Ponteiro para uma interface ID3D10Texture2D, representando a textura de destino.</span><span class="sxs-lookup"><span data-stu-id="68811-124">Pointer to an ID3D10Texture2D interface, representing the destination texture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68811-125">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="68811-125">Return value</span></span>

<span data-ttu-id="68811-126">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="68811-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="68811-127">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="68811-127">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="68811-128">Se a função falhar, o valor de retorno poderá ser o seguinte valor: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="68811-128">If the function fails, the return value can be the following value: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="68811-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="68811-129">Remarks</span></span>

<span data-ttu-id="68811-130">Esse método computa o normal usando a diferença central com um tamanho de kernel de 3x3.</span><span class="sxs-lookup"><span data-stu-id="68811-130">This method computes the normal by using the central difference with a kernel size of 3x3.</span></span> <span data-ttu-id="68811-131">Os canais RGB no destino contêm componentes com tendência (x, y, z) do normal.</span><span class="sxs-lookup"><span data-stu-id="68811-131">RGB channels in the destination contain biased (x,y,z) components of the normal.</span></span> <span data-ttu-id="68811-132">O denominador diferencial central está codificado para 2,0.</span><span class="sxs-lookup"><span data-stu-id="68811-132">The central differencing denominator is hardcoded to 2.0.</span></span>

## <a name="requirements"></a><span data-ttu-id="68811-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68811-133">Requirements</span></span>



| <span data-ttu-id="68811-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="68811-134">Requirement</span></span> | <span data-ttu-id="68811-135">Valor</span><span class="sxs-lookup"><span data-stu-id="68811-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="68811-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="68811-136">Header</span></span><br/>  | <dl> <span data-ttu-id="68811-137"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="68811-137"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="68811-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="68811-138">Library</span></span><br/> | <dl> <span data-ttu-id="68811-139"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="68811-139"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="68811-140">Consulte também</span><span class="sxs-lookup"><span data-stu-id="68811-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68811-141">Funções de textura no D3DX 10</span><span class="sxs-lookup"><span data-stu-id="68811-141">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
