---
description: Cria uma superfície de renderização.
ms.assetid: 35e0007e-c405-46e1-a52b-625adc84732b
title: Função D3DXCreateRenderToSurface (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateRenderToSurface
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6fc64cbc65d30838db2105e0458d3553247f1ab1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105788752"
---
# <a name="d3dxcreaterendertosurface-function"></a><span data-ttu-id="6aebb-103">Função D3DXCreateRenderToSurface</span><span class="sxs-lookup"><span data-stu-id="6aebb-103">D3DXCreateRenderToSurface function</span></span>

<span data-ttu-id="6aebb-104">Cria uma superfície de renderização.</span><span class="sxs-lookup"><span data-stu-id="6aebb-104">Creates a render surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="6aebb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6aebb-105">Syntax</span></span>


```C++
HRESULT D3DXCreateRenderToSurface(
  _In_  LPDIRECT3DDEVICE9     pDevice,
  _In_  UINT                  Width,
  _In_  UINT                  Height,
  _In_  D3DFORMAT             Format,
  _In_  BOOL                  DepthStencil,
  _In_  D3DFORMAT             DepthStencilFormat,
  _Out_ LPD3DXRENDERTOSURFACE *ppRenderToSurface
);
```



## <a name="parameters"></a><span data-ttu-id="6aebb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6aebb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6aebb-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6aebb-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6aebb-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="6aebb-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="6aebb-109">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , o dispositivo a ser associado à superfície de renderização.</span><span class="sxs-lookup"><span data-stu-id="6aebb-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device to be associated with the render surface.</span></span>

</dd> <dt>

<span data-ttu-id="6aebb-110">*Largura* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6aebb-110">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6aebb-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6aebb-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6aebb-112">Largura da superfície de renderização, em pixels.</span><span class="sxs-lookup"><span data-stu-id="6aebb-112">Width of the render surface, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="6aebb-113">*Altura* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6aebb-113">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6aebb-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6aebb-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6aebb-115">Altura da superfície de renderização, em pixels.</span><span class="sxs-lookup"><span data-stu-id="6aebb-115">Height of the render surface, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="6aebb-116">*Formato* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6aebb-116">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6aebb-117">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="6aebb-117">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="6aebb-118">Membro do tipo enumerado [D3DFORMAT](d3dformat.md) , que descreve o formato de pixel da superfície de renderização.</span><span class="sxs-lookup"><span data-stu-id="6aebb-118">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the pixel format of the render surface.</span></span>

</dd> <dt>

<span data-ttu-id="6aebb-119">*DepthStencil* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6aebb-119">*DepthStencil* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6aebb-120">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6aebb-120">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6aebb-121">Se **for true**, a superfície de renderização dará suporte a uma superfície de estêncil de profundidade.</span><span class="sxs-lookup"><span data-stu-id="6aebb-121">If **TRUE**, the render surface supports a depth-stencil surface.</span></span> <span data-ttu-id="6aebb-122">Caso contrário, esse membro será definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="6aebb-122">Otherwise, this member is set to **FALSE**.</span></span> <span data-ttu-id="6aebb-123">Essa função criará um novo buffer de profundidade.</span><span class="sxs-lookup"><span data-stu-id="6aebb-123">This function will create a new depth buffer.</span></span>

</dd> <dt>

<span data-ttu-id="6aebb-124">*DepthStencilFormat* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6aebb-124">*DepthStencilFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6aebb-125">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="6aebb-125">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="6aebb-126">Se *DepthStencil* for definido como **true**, esse parâmetro será um membro do tipo enumerado [D3DFORMAT](d3dformat.md) , descrevendo o formato de estêncil de profundidade da superfície de renderização.</span><span class="sxs-lookup"><span data-stu-id="6aebb-126">If *DepthStencil* is set to **TRUE**, this parameter is a member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the depth-stencil format of the render surface.</span></span>

</dd> <dt>

<span data-ttu-id="6aebb-127">*ppRenderToSurface* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6aebb-127">*ppRenderToSurface* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6aebb-128">Tipo: **[ **LPD3DXRENDERTOSURFACE**](id3dxrendertosurface.md)\***</span><span class="sxs-lookup"><span data-stu-id="6aebb-128">Type: **[**LPD3DXRENDERTOSURFACE**](id3dxrendertosurface.md)\***</span></span>

<span data-ttu-id="6aebb-129">Endereço de um ponteiro para uma interface [**ID3DXRenderToSurface**](id3dxrendertosurface.md) , que representa a superfície de renderização criada.</span><span class="sxs-lookup"><span data-stu-id="6aebb-129">Address of a pointer to an [**ID3DXRenderToSurface**](id3dxrendertosurface.md) interface, representing the created render surface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6aebb-130">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6aebb-130">Return value</span></span>

<span data-ttu-id="6aebb-131">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6aebb-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6aebb-132">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6aebb-132">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6aebb-133">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="6aebb-133">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="6aebb-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6aebb-134">Requirements</span></span>



| <span data-ttu-id="6aebb-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="6aebb-135">Requirement</span></span> | <span data-ttu-id="6aebb-136">Valor</span><span class="sxs-lookup"><span data-stu-id="6aebb-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6aebb-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6aebb-137">Header</span></span><br/>  | <dl> <span data-ttu-id="6aebb-138"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="6aebb-138"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="6aebb-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6aebb-139">Library</span></span><br/> | <dl> <span data-ttu-id="6aebb-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6aebb-140"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6aebb-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="6aebb-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6aebb-142">Funções de Uso Geral</span><span class="sxs-lookup"><span data-stu-id="6aebb-142">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
