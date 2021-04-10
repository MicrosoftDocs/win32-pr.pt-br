---
description: Inicie a renderização de um mapa de ambiente parabólico.
ms.assetid: 80456084-f5f5-4dfe-805a-7eaaf7f7cb2a
title: 'Método ID3DXRenderToEnvMap:: BeginParabolic (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.BeginParabolic
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5a818abb424fa55bc01eca7ce9f64bc5629a7d50
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012084"
---
# <a name="id3dxrendertoenvmapbeginparabolic-method"></a><span data-ttu-id="cf300-103">Método ID3DXRenderToEnvMap:: BeginParabolic</span><span class="sxs-lookup"><span data-stu-id="cf300-103">ID3DXRenderToEnvMap::BeginParabolic method</span></span>

<span data-ttu-id="cf300-104">Inicie a renderização de um mapa de ambiente parabólico.</span><span class="sxs-lookup"><span data-stu-id="cf300-104">Initiate the rendering of a parabolic environment map.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf300-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cf300-105">Syntax</span></span>


```C++
HRESULT BeginParabolic(
  [in] LPDIRECT3DTEXTURE9 pTexZPos,
  [in] LPDIRECT3DTEXTURE9 pTexZNeg
);
```



## <a name="parameters"></a><span data-ttu-id="cf300-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cf300-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf300-107">*pTexZPos* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cf300-107">*pTexZPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf300-108">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="cf300-108">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="cf300-109">Ponteiro para uma interface [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) que representa a textura de renderização positiva.</span><span class="sxs-lookup"><span data-stu-id="cf300-109">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface that represents the positive render texture.</span></span>

</dd> <dt>

<span data-ttu-id="cf300-110">*pTexZNeg* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cf300-110">*pTexZNeg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf300-111">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="cf300-111">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="cf300-112">Ponteiro para uma interface [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) que representa a textura de renderização negativa.</span><span class="sxs-lookup"><span data-stu-id="cf300-112">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface that represents the negative render texture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf300-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cf300-113">Return value</span></span>

<span data-ttu-id="cf300-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cf300-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cf300-115">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cf300-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="cf300-116">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL. E \_ falha</span><span class="sxs-lookup"><span data-stu-id="cf300-116">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL.E\_FAIL</span></span>

## <a name="remarks"></a><span data-ttu-id="cf300-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="cf300-117">Remarks</span></span>

<span data-ttu-id="cf300-118">Consulte [**ID3DXRenderToEnvMap:: face**](id3dxrendertoenvmap--face.md) para desenhar as faces.</span><span class="sxs-lookup"><span data-stu-id="cf300-118">See [**ID3DXRenderToEnvMap::Face**](id3dxrendertoenvmap--face.md) to draw the faces.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf300-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf300-119">Requirements</span></span>



| <span data-ttu-id="cf300-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf300-120">Requirement</span></span> | <span data-ttu-id="cf300-121">Valor</span><span class="sxs-lookup"><span data-stu-id="cf300-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf300-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cf300-122">Header</span></span><br/>  | <dl> <span data-ttu-id="cf300-123"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf300-123"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="cf300-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cf300-124">Library</span></span><br/> | <dl> <span data-ttu-id="cf300-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cf300-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cf300-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="cf300-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf300-127">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="cf300-127">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> <dt>

[<span data-ttu-id="cf300-128">**ID3DXRenderToEnvMap:: End**</span><span class="sxs-lookup"><span data-stu-id="cf300-128">**ID3DXRenderToEnvMap::End**</span></span>](id3dxrendertoenvmap--end.md)
</dt> </dl>

 

 
