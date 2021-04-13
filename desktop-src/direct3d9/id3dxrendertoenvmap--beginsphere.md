---
description: Inicie a renderização de um mapa de ambiente esférico.
ms.assetid: b0634120-f5ad-48b3-979a-30b0a53d22a2
title: 'Método ID3DXRenderToEnvMap:: BeginSphere (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.BeginSphere
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 872aa06734ae818ef248b03fbc14dcd1c33fe815
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298563"
---
# <a name="id3dxrendertoenvmapbeginsphere-method"></a><span data-ttu-id="e8478-103">Método ID3DXRenderToEnvMap:: BeginSphere</span><span class="sxs-lookup"><span data-stu-id="e8478-103">ID3DXRenderToEnvMap::BeginSphere method</span></span>

<span data-ttu-id="e8478-104">Inicie a renderização de um mapa de ambiente esférico.</span><span class="sxs-lookup"><span data-stu-id="e8478-104">Initiate the rendering of a spherical environment map.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8478-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e8478-105">Syntax</span></span>


```C++
HRESULT BeginSphere(
  [in] LPDIRECT3DTEXTURE9 pTex
);
```



## <a name="parameters"></a><span data-ttu-id="e8478-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e8478-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8478-107">*pTeX* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e8478-107">*pTex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8478-108">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="e8478-108">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="e8478-109">Ponteiro para uma interface [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) que representa a textura a ser renderizada.</span><span class="sxs-lookup"><span data-stu-id="e8478-109">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface that represents the texture to which to render.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8478-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e8478-110">Return value</span></span>

<span data-ttu-id="e8478-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e8478-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e8478-112">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e8478-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e8478-113">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL. E \_ falha</span><span class="sxs-lookup"><span data-stu-id="e8478-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL.E\_FAIL</span></span>

## <a name="remarks"></a><span data-ttu-id="e8478-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e8478-114">Remarks</span></span>

<span data-ttu-id="e8478-115">Consulte [**ID3DXRenderToEnvMap:: face**](id3dxrendertoenvmap--face.md) para desenhar a face.</span><span class="sxs-lookup"><span data-stu-id="e8478-115">See [**ID3DXRenderToEnvMap::Face**](id3dxrendertoenvmap--face.md) to draw the face.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8478-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8478-116">Requirements</span></span>



| <span data-ttu-id="e8478-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8478-117">Requirement</span></span> | <span data-ttu-id="e8478-118">Valor</span><span class="sxs-lookup"><span data-stu-id="e8478-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e8478-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e8478-119">Header</span></span><br/>  | <dl> <span data-ttu-id="e8478-120"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8478-120"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="e8478-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e8478-121">Library</span></span><br/> | <dl> <span data-ttu-id="e8478-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e8478-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e8478-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="e8478-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8478-124">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="e8478-124">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> <dt>

[<span data-ttu-id="e8478-125">**ID3DXRenderToEnvMap:: End**</span><span class="sxs-lookup"><span data-stu-id="e8478-125">**ID3DXRenderToEnvMap::End**</span></span>](id3dxrendertoenvmap--end.md)
</dt> </dl>

 

 
