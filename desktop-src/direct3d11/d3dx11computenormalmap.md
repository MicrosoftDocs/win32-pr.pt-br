---
title: Função D3DX11ComputeNormalMap (D3DX11tex. h)
description: Observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Observação em vez de usar essa função, recomendamos que você use a biblioteca DirectXTex, ComputeNormalMap.
ms.assetid: 3ccdbd9a-669e-48ff-97d5-e5a6c7d2fb26
keywords:
- Função D3DX11ComputeNormalMap Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11ComputeNormalMap
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4399282c325fde0ea46679da9e9b84331b8c125b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173118"
---
# <a name="d3dx11computenormalmap-function"></a><span data-ttu-id="bba39-105">Função D3DX11ComputeNormalMap</span><span class="sxs-lookup"><span data-stu-id="bba39-105">D3DX11ComputeNormalMap function</span></span>

> [!Note]  
> <span data-ttu-id="bba39-106">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="bba39-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="bba39-107">Em vez de usar essa função, recomendamos que você use a biblioteca [DirectXTex](https://github.com/Microsoft/DirectXTex) , **ComputeNormalMap**.</span><span class="sxs-lookup"><span data-stu-id="bba39-107">Instead of using this function, we recommend that you use the [DirectXTex](https://github.com/Microsoft/DirectXTex) library, **ComputeNormalMap**.</span></span>

 

<span data-ttu-id="bba39-108">Converte um mapa de altura em um mapa normal.</span><span class="sxs-lookup"><span data-stu-id="bba39-108">Converts a height map into a normal map.</span></span> <span data-ttu-id="bba39-109">Os componentes (x, y, z) de cada normal são mapeados para os canais (r, g, b) da textura de saída.</span><span class="sxs-lookup"><span data-stu-id="bba39-109">The (x,y,z) components of each normal are mapped to the (r,g,b) channels of the output texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="bba39-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bba39-110">Syntax</span></span>


```C++
HRESULT D3DX11ComputeNormalMap(
  _In_ ID3D11DeviceContext *pContext,
  _In_ ID3D11Texture2D     *pSrcTexture,
  _In_ UINT                Flags,
  _In_ UINT                Channel,
  _In_ FLOAT               Amplitude,
  _In_ ID3D11Texture2D     *pDestTexture
);
```



## <a name="parameters"></a><span data-ttu-id="bba39-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bba39-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bba39-112">*pContext* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bba39-112">*pContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bba39-113">Tipo: **[ **ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span><span class="sxs-lookup"><span data-stu-id="bba39-113">Type: **[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span></span>

<span data-ttu-id="bba39-114">Ponteiro para uma interface [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) , representando a textura de mapa de altura de origem.</span><span class="sxs-lookup"><span data-stu-id="bba39-114">Pointer to an [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) interface, representing the source height-map texture.</span></span>

</dd> <dt>

<span data-ttu-id="bba39-115">*pSrcTexture* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bba39-115">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bba39-116">Tipo: **[ **ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***</span><span class="sxs-lookup"><span data-stu-id="bba39-116">Type: **[**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***</span></span>

<span data-ttu-id="bba39-117">Ponteiro para uma interface [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) , representando a textura de mapa de altura de origem.</span><span class="sxs-lookup"><span data-stu-id="bba39-117">Pointer to an [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) interface, representing the source height-map texture.</span></span>

</dd> <dt>

<span data-ttu-id="bba39-118">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="bba39-118">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bba39-119">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="bba39-119">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="bba39-120">Um ou mais \_ sinalizadores D3DX NormalMap que controlam a geração de mapas normais.</span><span class="sxs-lookup"><span data-stu-id="bba39-120">One or more D3DX\_NORMALMAP flags that control generation of normal maps.</span></span>

</dd> <dt>

<span data-ttu-id="bba39-121">*Canal* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bba39-121">*Channel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bba39-122">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="bba39-122">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="bba39-123">Um \_ sinalizador de canal D3DX especificando a fonte de informações de altura.</span><span class="sxs-lookup"><span data-stu-id="bba39-123">One D3DX\_CHANNEL flag specifying the source of height information.</span></span>

</dd> <dt>

<span data-ttu-id="bba39-124">*Amplitude* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bba39-124">*Amplitude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bba39-125">Tipo: **[ **float**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="bba39-125">Type: **[**FLOAT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="bba39-126">Multiplicador de valor constante que aumenta (ou diminui) os valores no mapa normal.</span><span class="sxs-lookup"><span data-stu-id="bba39-126">Constant value multiplier that increases (or decreases) the values in the normal map.</span></span> <span data-ttu-id="bba39-127">Valores mais altos geralmente tornam os choques mais visíveis, os valores mais baixos geralmente tornam os choques menos visíveis.</span><span class="sxs-lookup"><span data-stu-id="bba39-127">Higher values usually make bumps more visible, lower values usually make bumps less visible.</span></span>

</dd> <dt>

<span data-ttu-id="bba39-128">*pDestTexture* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bba39-128">*pDestTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bba39-129">Tipo: **[ **ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***</span><span class="sxs-lookup"><span data-stu-id="bba39-129">Type: **[**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***</span></span>

<span data-ttu-id="bba39-130">Ponteiro para uma interface [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) , representando a textura de destino.</span><span class="sxs-lookup"><span data-stu-id="bba39-130">Pointer to an [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) interface, representing the destination texture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bba39-131">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bba39-131">Return value</span></span>

<span data-ttu-id="bba39-132">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bba39-132">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bba39-133">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bba39-133">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="bba39-134">Se a função falhar, o valor de retorno poderá ser o seguinte valor: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="bba39-134">If the function fails, the return value can be the following value: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="bba39-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="bba39-135">Remarks</span></span>

<span data-ttu-id="bba39-136">Esse método computa o normal usando a diferença central com um tamanho de kernel de 3x3.</span><span class="sxs-lookup"><span data-stu-id="bba39-136">This method computes the normal by using the central difference with a kernel size of 3x3.</span></span> <span data-ttu-id="bba39-137">Os canais RGB no destino contêm componentes com tendência (x, y, z) do normal.</span><span class="sxs-lookup"><span data-stu-id="bba39-137">RGB channels in the destination contain biased (x,y,z) components of the normal.</span></span> <span data-ttu-id="bba39-138">O denominador diferencial central está codificado para 2,0.</span><span class="sxs-lookup"><span data-stu-id="bba39-138">The central differencing denominator is hardcoded to 2.0.</span></span>

## <a name="requirements"></a><span data-ttu-id="bba39-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bba39-139">Requirements</span></span>



| <span data-ttu-id="bba39-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="bba39-140">Requirement</span></span> | <span data-ttu-id="bba39-141">Valor</span><span class="sxs-lookup"><span data-stu-id="bba39-141">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bba39-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bba39-142">Header</span></span><br/>  | <dl> <span data-ttu-id="bba39-143"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="bba39-143"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="bba39-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bba39-144">Library</span></span><br/> | <dl> <span data-ttu-id="bba39-145"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bba39-145"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="bba39-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="bba39-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bba39-147">Funções D3DX</span><span class="sxs-lookup"><span data-stu-id="bba39-147">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

