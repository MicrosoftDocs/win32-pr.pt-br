---
description: Define as coordenadas Texel barycentric.
ms.assetid: 6c7c74aa-71a3-45aa-9b18-6409fbd63bda
title: 'Método ID3DXTextureGutterHelper:: SetBaryMap (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.SetBaryMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5e3de61913041a4e59e075ea42dacc308c1ce5f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173146"
---
# <a name="id3dxtexturegutterhelpersetbarymap-method"></a><span data-ttu-id="6c898-103">Método ID3DXTextureGutterHelper:: SetBaryMap</span><span class="sxs-lookup"><span data-stu-id="6c898-103">ID3DXTextureGutterHelper::SetBaryMap method</span></span>

<span data-ttu-id="6c898-104">Define as coordenadas Texel barycentric.</span><span class="sxs-lookup"><span data-stu-id="6c898-104">Sets texel barycentric coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c898-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6c898-105">Syntax</span></span>


```C++
HRESULT SetBaryMap(
  [in] D3DXVECTOR2 *pBaryData
);
```



## <a name="parameters"></a><span data-ttu-id="6c898-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6c898-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c898-107">*pBaryData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6c898-107">*pBaryData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c898-108">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="6c898-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="6c898-109">Ponteiro para uma estrutura [**D3DXVECTOR2**](d3dxvector2.md) que contém as duas primeiras coordenadas barycentric de cada Texel.</span><span class="sxs-lookup"><span data-stu-id="6c898-109">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that contains the first two barycentric coordinates of each texel.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c898-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6c898-110">Return value</span></span>

<span data-ttu-id="6c898-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6c898-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6c898-112">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6c898-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="6c898-113">Se o método falhar, o valor a seguir será retornado. D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="6c898-113">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="6c898-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="6c898-114">Remarks</span></span>

<span data-ttu-id="6c898-115">A terceira coordenada barycentric é fornecida por:</span><span class="sxs-lookup"><span data-stu-id="6c898-115">The third barycentric coordinate is given by:</span></span>


```
1 - ( pBaryData.x + pBaryData.y )
```



<span data-ttu-id="6c898-116">O barycentric coordena a entrada para este método é válido somente para texels válida (não classe 0).</span><span class="sxs-lookup"><span data-stu-id="6c898-116">The barycentric coordinates input to this method are valid only for valid (non-class 0) texels.</span></span> <span data-ttu-id="6c898-117">[**ID3DXTextureGutterHelper:: GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) retornará valores diferentes de zero para texels válidos.</span><span class="sxs-lookup"><span data-stu-id="6c898-117">[**ID3DXTextureGutterHelper::GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) will return non-zero values for valid texels.</span></span>

<span data-ttu-id="6c898-118">As coordenadas barycentric definem um ponto dentro de um triângulo em termos dos vértices do triângulo.</span><span class="sxs-lookup"><span data-stu-id="6c898-118">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="6c898-119">Para obter uma descrição mais detalhada das coordenadas de barycentric, consulte [Descrição de coordenadas barycentric do MathWorld](http://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="6c898-119">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](http://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="6c898-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c898-120">Requirements</span></span>



| <span data-ttu-id="6c898-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c898-121">Requirement</span></span> | <span data-ttu-id="6c898-122">Valor</span><span class="sxs-lookup"><span data-stu-id="6c898-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c898-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6c898-123">Header</span></span><br/>  | <dl> <span data-ttu-id="6c898-124"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c898-124"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="6c898-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6c898-125">Library</span></span><br/> | <dl> <span data-ttu-id="6c898-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6c898-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6c898-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="6c898-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c898-128">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="6c898-128">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 




