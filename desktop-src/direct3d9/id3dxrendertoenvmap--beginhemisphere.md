---
description: Inicie a renderização de um mapa de ambiente Hemispheric.
ms.assetid: 1150aad9-dd8c-4943-afaf-90794faaaf70
title: 'Método ID3DXRenderToEnvMap:: BeginHemisphere (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.BeginHemisphere
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 96eb4bbf4cfc6cac952368337456b946f64cf711
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104172973"
---
# <a name="id3dxrendertoenvmapbeginhemisphere-method"></a><span data-ttu-id="eb99e-103">Método ID3DXRenderToEnvMap:: BeginHemisphere</span><span class="sxs-lookup"><span data-stu-id="eb99e-103">ID3DXRenderToEnvMap::BeginHemisphere method</span></span>

<span data-ttu-id="eb99e-104">Inicie a renderização de um mapa de ambiente Hemispheric.</span><span class="sxs-lookup"><span data-stu-id="eb99e-104">Initiate the rendering of a hemispheric environment map.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb99e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eb99e-105">Syntax</span></span>


```C++
HRESULT BeginHemisphere(
  [in] LPDIRECT3DTEXTURE9 pTexZPos,
  [in] LPDIRECT3DTEXTURE9 pTexZNeg
);
```



## <a name="parameters"></a><span data-ttu-id="eb99e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eb99e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb99e-107">*pTexZPos* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="eb99e-107">*pTexZPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb99e-108">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="eb99e-108">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="eb99e-109">Ponteiro para uma interface [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) que representa a superfície de renderização de textura positiva.</span><span class="sxs-lookup"><span data-stu-id="eb99e-109">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface that represents the positive texture render surface.</span></span>

</dd> <dt>

<span data-ttu-id="eb99e-110">*pTexZNeg* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="eb99e-110">*pTexZNeg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb99e-111">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="eb99e-111">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="eb99e-112">Ponteiro para uma interface [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) que representa a superfície de renderização de textura negativa.</span><span class="sxs-lookup"><span data-stu-id="eb99e-112">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface that represents the negative texture render surface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb99e-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="eb99e-113">Return value</span></span>

<span data-ttu-id="eb99e-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="eb99e-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="eb99e-115">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="eb99e-115">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="eb99e-116">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL. E \_ falha</span><span class="sxs-lookup"><span data-stu-id="eb99e-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL.E\_FAIL</span></span>

## <a name="remarks"></a><span data-ttu-id="eb99e-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="eb99e-117">Remarks</span></span>

<span data-ttu-id="eb99e-118">Consulte [**ID3DXRenderToEnvMap:: face**](id3dxrendertoenvmap--face.md) para desenhar a face.</span><span class="sxs-lookup"><span data-stu-id="eb99e-118">See [**ID3DXRenderToEnvMap::Face**](id3dxrendertoenvmap--face.md) to draw the face.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb99e-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb99e-119">Requirements</span></span>



| <span data-ttu-id="eb99e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb99e-120">Requirement</span></span> | <span data-ttu-id="eb99e-121">Valor</span><span class="sxs-lookup"><span data-stu-id="eb99e-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb99e-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="eb99e-122">Header</span></span><br/>  | <dl> <span data-ttu-id="eb99e-123"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb99e-123"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="eb99e-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="eb99e-124">Library</span></span><br/> | <dl> <span data-ttu-id="eb99e-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eb99e-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="eb99e-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="eb99e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb99e-127">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="eb99e-127">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> <dt>

[<span data-ttu-id="eb99e-128">**ID3DXRenderToEnvMap:: End**</span><span class="sxs-lookup"><span data-stu-id="eb99e-128">**ID3DXRenderToEnvMap::End**</span></span>](id3dxrendertoenvmap--end.md)
</dt> </dl>

 

 
