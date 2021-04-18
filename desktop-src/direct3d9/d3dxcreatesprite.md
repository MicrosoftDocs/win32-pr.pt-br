---
description: Cria um objeto Sprite associado a um dispositivo específico. Os objetos Sprite são usados para desenhar imagens 2D na tela.
ms.assetid: 1611073f-0590-415a-8ea5-dc1d224f20b9
title: Função D3DXCreateSprite (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSprite
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1e16feb2ff07f10703c5243ebeaaee3a2a15e7f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105798196"
---
# <a name="d3dxcreatesprite-function"></a><span data-ttu-id="bba37-104">Função D3DXCreateSprite</span><span class="sxs-lookup"><span data-stu-id="bba37-104">D3DXCreateSprite function</span></span>

<span data-ttu-id="bba37-105">Cria um objeto Sprite associado a um dispositivo específico.</span><span class="sxs-lookup"><span data-stu-id="bba37-105">Creates a sprite object which is associated with a particular device.</span></span> <span data-ttu-id="bba37-106">Os objetos Sprite são usados para desenhar imagens 2D na tela.</span><span class="sxs-lookup"><span data-stu-id="bba37-106">Sprite objects are used to draw 2D images to the screen.</span></span>

## <a name="syntax"></a><span data-ttu-id="bba37-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bba37-107">Syntax</span></span>


```C++
HRESULT D3DXCreateSprite(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _Out_ LPD3DXSPRITE      *ppSprite
);
```



## <a name="parameters"></a><span data-ttu-id="bba37-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bba37-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bba37-109">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bba37-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bba37-110">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="bba37-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="bba37-111">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , o dispositivo a ser associado ao Sprite.</span><span class="sxs-lookup"><span data-stu-id="bba37-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device to be associated with the sprite.</span></span>

</dd> <dt>

<span data-ttu-id="bba37-112">*ppSprite* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="bba37-112">*ppSprite* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bba37-113">Tipo: **[ **LPD3DXSPRITE**](id3dxsprite.md)\***</span><span class="sxs-lookup"><span data-stu-id="bba37-113">Type: **[**LPD3DXSPRITE**](id3dxsprite.md)\***</span></span>

<span data-ttu-id="bba37-114">Endereço de um ponteiro para uma interface [**ID3DXSprite**](id3dxsprite.md) .</span><span class="sxs-lookup"><span data-stu-id="bba37-114">Address of a pointer to an [**ID3DXSprite**](id3dxsprite.md) interface.</span></span> <span data-ttu-id="bba37-115">Essa interface permite que o usuário acesse as funções Sprite.</span><span class="sxs-lookup"><span data-stu-id="bba37-115">This interface allows the user to access sprite functions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bba37-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bba37-116">Return value</span></span>

<span data-ttu-id="bba37-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bba37-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bba37-118">Se a função for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bba37-118">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="bba37-119">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="bba37-119">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="bba37-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="bba37-120">Remarks</span></span>

<span data-ttu-id="bba37-121">Essa interface pode ser usada para desenhar duas imagens dimensionais no espaço da tela do dispositivo associado.</span><span class="sxs-lookup"><span data-stu-id="bba37-121">This interface can be used to draw two dimensional images in screen space of the associated device.</span></span>

## <a name="requirements"></a><span data-ttu-id="bba37-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bba37-122">Requirements</span></span>



| <span data-ttu-id="bba37-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="bba37-123">Requirement</span></span> | <span data-ttu-id="bba37-124">Valor</span><span class="sxs-lookup"><span data-stu-id="bba37-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bba37-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bba37-125">Header</span></span><br/>  | <dl> <span data-ttu-id="bba37-126"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="bba37-126"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="bba37-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bba37-127">Library</span></span><br/> | <dl> <span data-ttu-id="bba37-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bba37-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bba37-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="bba37-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bba37-130">Funções de Uso Geral</span><span class="sxs-lookup"><span data-stu-id="bba37-130">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
