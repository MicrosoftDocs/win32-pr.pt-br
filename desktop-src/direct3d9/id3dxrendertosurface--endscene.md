---
description: Encerra uma cena.
ms.assetid: f721593e-6cba-4569-8276-6a4ffc0fc37a
title: 'Método ID3DXRenderToSurface:: endcena (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.EndScene
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d5aa0c1fbccb756ac612b813ad151813a782b122
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103663987"
---
# <a name="id3dxrendertosurfaceendscene-method"></a><span data-ttu-id="f68e0-103">Método ID3DXRenderToSurface:: EndScene</span><span class="sxs-lookup"><span data-stu-id="f68e0-103">ID3DXRenderToSurface::EndScene method</span></span>

<span data-ttu-id="f68e0-104">Encerra uma cena.</span><span class="sxs-lookup"><span data-stu-id="f68e0-104">Ends a scene.</span></span>

## <a name="syntax"></a><span data-ttu-id="f68e0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f68e0-105">Syntax</span></span>


```C++
HRESULT EndScene(
  [in] DWORD MipFilter
);
```



## <a name="parameters"></a><span data-ttu-id="f68e0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f68e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f68e0-107">*MipFilter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f68e0-107">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f68e0-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f68e0-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f68e0-109">Opções de filtro, enumeradas [no \_ filtro D3DX](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="f68e0-109">Filter options, enumerated in [D3DX\_FILTER](d3dx-filter.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f68e0-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f68e0-110">Return value</span></span>

<span data-ttu-id="f68e0-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f68e0-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f68e0-112">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f68e0-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f68e0-113">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="f68e0-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="f68e0-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f68e0-114">Requirements</span></span>



| <span data-ttu-id="f68e0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f68e0-115">Requirement</span></span> | <span data-ttu-id="f68e0-116">Valor</span><span class="sxs-lookup"><span data-stu-id="f68e0-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f68e0-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f68e0-117">Header</span></span><br/>  | <dl> <span data-ttu-id="f68e0-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="f68e0-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="f68e0-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f68e0-119">Library</span></span><br/> | <dl> <span data-ttu-id="f68e0-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f68e0-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f68e0-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="f68e0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f68e0-122">ID3DXRenderToSurface</span><span class="sxs-lookup"><span data-stu-id="f68e0-122">ID3DXRenderToSurface</span></span>](id3dxrendertosurface.md)
</dt> <dt>

[<span data-ttu-id="f68e0-123">**ID3DXRenderToSurface::BeginScene**</span><span class="sxs-lookup"><span data-stu-id="f68e0-123">**ID3DXRenderToSurface::BeginScene**</span></span>](id3dxrendertosurface--beginscene.md)
</dt> </dl>

 

 
