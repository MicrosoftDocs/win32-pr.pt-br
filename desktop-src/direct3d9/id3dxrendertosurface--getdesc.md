---
description: Recupera os parâmetros da superfície de renderização.
ms.assetid: 4f46a4c6-7c50-479c-b2f5-24edff590c57
title: 'Método ID3DXRenderToSurface:: GetDesc (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 00824c6b418a3e6707ebfd588d8d32d4e38f173d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173176"
---
# <a name="id3dxrendertosurfacegetdesc-method"></a><span data-ttu-id="8e574-103">Método ID3DXRenderToSurface:: GetDesc</span><span class="sxs-lookup"><span data-stu-id="8e574-103">ID3DXRenderToSurface::GetDesc method</span></span>

<span data-ttu-id="8e574-104">Recupera os parâmetros da superfície de renderização.</span><span class="sxs-lookup"><span data-stu-id="8e574-104">Retrieves the parameters of the render surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e574-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8e574-105">Syntax</span></span>


```C++
HRESULT GetDesc(
  [out] D3DXRTS_DESC *pParameters
);
```



## <a name="parameters"></a><span data-ttu-id="8e574-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8e574-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e574-107">*pParameters* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8e574-107">*pParameters* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8e574-108">Tipo: **[ **D3DXRTS \_ desc**](d3dxrts-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="8e574-108">Type: **[**D3DXRTS\_DESC**](d3dxrts-desc.md)\***</span></span>

<span data-ttu-id="8e574-109">Ponteiro para uma [**estrutura \_ desc de D3DXRTS**](d3dxrts-desc.md) , descrevendo os parâmetros da superfície de renderização.</span><span class="sxs-lookup"><span data-stu-id="8e574-109">Pointer to a [**D3DXRTS\_DESC**](d3dxrts-desc.md) structure, describing the parameters of the render surface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e574-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8e574-110">Return value</span></span>

<span data-ttu-id="8e574-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8e574-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8e574-112">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8e574-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8e574-113">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="8e574-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e574-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e574-114">Requirements</span></span>



| <span data-ttu-id="8e574-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e574-115">Requirement</span></span> | <span data-ttu-id="8e574-116">Valor</span><span class="sxs-lookup"><span data-stu-id="8e574-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e574-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8e574-117">Header</span></span><br/>  | <dl> <span data-ttu-id="8e574-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e574-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="8e574-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8e574-119">Library</span></span><br/> | <dl> <span data-ttu-id="8e574-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8e574-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8e574-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="8e574-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e574-122">ID3DXRenderToSurface</span><span class="sxs-lookup"><span data-stu-id="8e574-122">ID3DXRenderToSurface</span></span>](id3dxrendertosurface.md)
</dt> </dl>

 

 




