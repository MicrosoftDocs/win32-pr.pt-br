---
description: Cria um mapa de ambiente de renderização.
ms.assetid: 5ca10602-5ab1-4766-a350-706c46c55df2
title: Função D3DXCreateRenderToEnvMap (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateRenderToEnvMap
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6829d53f53bd6a4783f5873eeed614e48bbe1088
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012096"
---
# <a name="d3dxcreaterendertoenvmap-function"></a><span data-ttu-id="20549-103">Função D3DXCreateRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="20549-103">D3DXCreateRenderToEnvMap function</span></span>

<span data-ttu-id="20549-104">Cria um mapa de ambiente de renderização.</span><span class="sxs-lookup"><span data-stu-id="20549-104">Creates a render environment map.</span></span>

## <a name="syntax"></a><span data-ttu-id="20549-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="20549-105">Syntax</span></span>


```C++
HRESULT D3DXCreateRenderToEnvMap(
  _In_  LPDIRECT3DDEVICE9    pDevice,
  _In_  UINT                 Size,
  _In_  UINT                 MipLevels,
  _In_  D3DFORMAT            Format,
  _In_  BOOL                 DepthStencil,
  _In_  D3DFORMAT            DepthStencilFormat,
  _Out_ LPD3DXRENDERTOENVMAP *ppRenderToEnvMap
);
```



## <a name="parameters"></a><span data-ttu-id="20549-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="20549-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20549-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="20549-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20549-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="20549-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="20549-109">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , que é o dispositivo a ser associado à superfície de renderização.</span><span class="sxs-lookup"><span data-stu-id="20549-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, which is the device to associate with the render surface.</span></span>

</dd> <dt>

<span data-ttu-id="20549-110">*Tamanho* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="20549-110">*Size* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20549-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="20549-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="20549-112">Tamanho da superfície de renderização.</span><span class="sxs-lookup"><span data-stu-id="20549-112">Size of the render surface.</span></span>

</dd> <dt>

<span data-ttu-id="20549-113">*MipLevels* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="20549-113">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20549-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="20549-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="20549-115">O número de níveis de mipmap.</span><span class="sxs-lookup"><span data-stu-id="20549-115">The number of mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="20549-116">*Formato* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="20549-116">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20549-117">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="20549-117">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="20549-118">Membro do tipo enumerado [D3DFORMAT](d3dformat.md) que descreve o formato de pixel do mapa de ambiente.</span><span class="sxs-lookup"><span data-stu-id="20549-118">Member of the [D3DFORMAT](d3dformat.md) enumerated type that describes the pixel format of the environment map.</span></span>

</dd> <dt>

<span data-ttu-id="20549-119">*DepthStencil* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="20549-119">*DepthStencil* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20549-120">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="20549-120">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="20549-121">Se **for true**, a superfície de renderização dará suporte a uma superfície de estêncil de profundidade.</span><span class="sxs-lookup"><span data-stu-id="20549-121">If **TRUE**, the render surface supports a depth-stencil surface.</span></span> <span data-ttu-id="20549-122">Caso contrário, esse membro será definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="20549-122">Otherwise, this member is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="20549-123">*DepthStencilFormat* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="20549-123">*DepthStencilFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20549-124">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="20549-124">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="20549-125">Se DepthStencil for definido como **true**, esse parâmetro será um membro do tipo enumerado [D3DFORMAT](d3dformat.md) que descreve o formato de estêncil de profundidade do mapa de ambiente.</span><span class="sxs-lookup"><span data-stu-id="20549-125">If DepthStencil is set to **TRUE**, this parameter is a member of the [D3DFORMAT](d3dformat.md) enumerated type that describes the depth-stencil format of the environment map.</span></span>

</dd> <dt>

<span data-ttu-id="20549-126">*ppRenderToEnvMap* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="20549-126">*ppRenderToEnvMap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="20549-127">Tipo: **[ **LPD3DXRENDERTOENVMAP**](id3dxrendertoenvmap.md)\***</span><span class="sxs-lookup"><span data-stu-id="20549-127">Type: **[**LPD3DXRENDERTOENVMAP**](id3dxrendertoenvmap.md)\***</span></span>

<span data-ttu-id="20549-128">Endereço de um ponteiro para uma interface [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md) que representa o mapa de ambiente de renderização criado.</span><span class="sxs-lookup"><span data-stu-id="20549-128">Address of a pointer to an [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md) interface that represents the created render environment map.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20549-129">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="20549-129">Return value</span></span>

<span data-ttu-id="20549-130">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="20549-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="20549-131">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="20549-131">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="20549-132">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="20549-132">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="20549-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20549-133">Requirements</span></span>



| <span data-ttu-id="20549-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="20549-134">Requirement</span></span> | <span data-ttu-id="20549-135">Valor</span><span class="sxs-lookup"><span data-stu-id="20549-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="20549-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="20549-136">Header</span></span><br/>  | <dl> <span data-ttu-id="20549-137"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="20549-137"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="20549-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="20549-138">Library</span></span><br/> | <dl> <span data-ttu-id="20549-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="20549-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="20549-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="20549-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20549-141">Funções de Uso Geral</span><span class="sxs-lookup"><span data-stu-id="20549-141">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
