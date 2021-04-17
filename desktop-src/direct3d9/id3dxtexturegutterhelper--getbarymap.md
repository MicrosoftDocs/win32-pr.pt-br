---
description: Recupera as coordenadas Texel barycentric.
ms.assetid: f380a37f-b9c1-4433-b1d6-e9feeca79b30
title: 'Método ID3DXTextureGutterHelper:: GetBaryMap (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.GetBaryMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 246117569b9106de18a31d08613146a3aa0d88c2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105811713"
---
# <a name="id3dxtexturegutterhelpergetbarymap-method"></a><span data-ttu-id="ddc60-103">Método ID3DXTextureGutterHelper:: GetBaryMap</span><span class="sxs-lookup"><span data-stu-id="ddc60-103">ID3DXTextureGutterHelper::GetBaryMap method</span></span>

<span data-ttu-id="ddc60-104">Recupera as coordenadas Texel barycentric.</span><span class="sxs-lookup"><span data-stu-id="ddc60-104">Retrieves texel barycentric coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddc60-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ddc60-105">Syntax</span></span>


```C++
HRESULT GetBaryMap(
  [in, out] D3DXVECTOR2 *pBaryData
);
```



## <a name="parameters"></a><span data-ttu-id="ddc60-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ddc60-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ddc60-107">*pBaryData* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="ddc60-107">*pBaryData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ddc60-108">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="ddc60-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="ddc60-109">Ponteiro para uma estrutura [**D3DXVECTOR2**](d3dxvector2.md) que contém as duas primeiras coordenadas barycentric de cada Texel.</span><span class="sxs-lookup"><span data-stu-id="ddc60-109">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that contains the first two barycentric coordinates of each texel.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ddc60-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ddc60-110">Return value</span></span>

<span data-ttu-id="ddc60-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ddc60-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ddc60-112">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ddc60-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ddc60-113">Se o método falhar, o valor a seguir será retornado. D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="ddc60-113">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="ddc60-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="ddc60-114">Remarks</span></span>

<span data-ttu-id="ddc60-115">A terceira coordenada barycentric é fornecida por:</span><span class="sxs-lookup"><span data-stu-id="ddc60-115">The third barycentric coordinate is given by:</span></span>


```
    1 - ( pBaryData.x + pBaryData.y )
```



<span data-ttu-id="ddc60-116">As coordenadas barycentric são sempre especificadas em relação ao triângulo retornado por [**ID3DXTextureGutterHelper:: GetFaceMap**](id3dxtexturegutterhelper--getfacemap.md).</span><span class="sxs-lookup"><span data-stu-id="ddc60-116">Barycentric coordinates are always specified with respect to the triangle returned by [**ID3DXTextureGutterHelper::GetFaceMap**](id3dxtexturegutterhelper--getfacemap.md).</span></span>

<span data-ttu-id="ddc60-117">As coordenadas de Barycentric retornadas por esse método são válidas somente para texels válidas (não classe 0).</span><span class="sxs-lookup"><span data-stu-id="ddc60-117">The barycentric coordinates returned by this method are valid only for valid (non-class 0) texels.</span></span> <span data-ttu-id="ddc60-118">[**ID3DXTextureGutterHelper:: GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) retornará valores diferentes de zero para texels válidas.</span><span class="sxs-lookup"><span data-stu-id="ddc60-118">[**ID3DXTextureGutterHelper::GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) will return nonzero values for valid texels.</span></span>

<span data-ttu-id="ddc60-119">A [**classe 2 texels**](id3dxtexturegutterhelper.md) são mapeadas para o ponto mais próximo no triângulo no espaço Texel.</span><span class="sxs-lookup"><span data-stu-id="ddc60-119">[**Class 2 texels**](id3dxtexturegutterhelper.md) are mapped to the nearest point on the triangle in texel space.</span></span>

<span data-ttu-id="ddc60-120">O aplicativo deve alocar e gerenciar pBaryData.</span><span class="sxs-lookup"><span data-stu-id="ddc60-120">The application must allocate and manage pBaryData.</span></span>

<span data-ttu-id="ddc60-121">As coordenadas barycentric definem um ponto dentro de um triângulo em termos dos vértices do triângulo.</span><span class="sxs-lookup"><span data-stu-id="ddc60-121">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="ddc60-122">Para obter uma descrição mais detalhada das coordenadas de barycentric, consulte [Descrição de coordenadas barycentric do MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="ddc60-122">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="ddc60-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ddc60-123">Requirements</span></span>



| <span data-ttu-id="ddc60-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ddc60-124">Requirement</span></span> | <span data-ttu-id="ddc60-125">Valor</span><span class="sxs-lookup"><span data-stu-id="ddc60-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ddc60-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ddc60-126">Header</span></span><br/>  | <dl> <span data-ttu-id="ddc60-127"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="ddc60-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="ddc60-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ddc60-128">Library</span></span><br/> | <dl> <span data-ttu-id="ddc60-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ddc60-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ddc60-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="ddc60-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddc60-131">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="ddc60-131">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 




