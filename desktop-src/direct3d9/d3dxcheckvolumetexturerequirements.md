---
description: Verifica os parâmetros de criação de textura de volume.
ms.assetid: 1a02cb99-2582-4d8f-aacf-67ed75f6deb8
title: Função D3DXCheckVolumeTextureRequirements (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCheckVolumeTextureRequirements
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4940cab936ed14c847e7224c9f619244c6e422a9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104370967"
---
# <a name="d3dxcheckvolumetexturerequirements-function"></a><span data-ttu-id="76f72-103">Função D3DXCheckVolumeTextureRequirements</span><span class="sxs-lookup"><span data-stu-id="76f72-103">D3DXCheckVolumeTextureRequirements function</span></span>

<span data-ttu-id="76f72-104">Verifica os parâmetros de criação de textura de volume.</span><span class="sxs-lookup"><span data-stu-id="76f72-104">Checks volume-texture-creation parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="76f72-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="76f72-105">Syntax</span></span>


```C++
HRESULT D3DXCheckVolumeTextureRequirements(
  _In_    LPDIRECT3DDEVICE9 pDevice,
  _Inout_ UINT              *pWidth,
  _Inout_ UINT              *pHeight,
  _Inout_ UINT              *pDepth,
  _Inout_ UINT              *pNumMipLevels,
  _In_    DWORD             Usage,
  _Inout_ D3DFORMAT         *pFormat,
  _In_    D3DPOOL           Pool
);
```



## <a name="parameters"></a><span data-ttu-id="76f72-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="76f72-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76f72-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="76f72-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76f72-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="76f72-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="76f72-109">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , representando o dispositivo a ser associado à textura do volume.</span><span class="sxs-lookup"><span data-stu-id="76f72-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the volume texture.</span></span>

</dd> <dt>

<span data-ttu-id="76f72-110">*pWidth* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="76f72-110">*pWidth* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="76f72-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="76f72-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="76f72-112">Ponteiro para a largura solicitada em pixels ou **nulo**.</span><span class="sxs-lookup"><span data-stu-id="76f72-112">Pointer to the requested width in pixels, or **NULL**.</span></span> <span data-ttu-id="76f72-113">Retorna o tamanho corrigido.</span><span class="sxs-lookup"><span data-stu-id="76f72-113">Returns the corrected size.</span></span>

</dd> <dt>

<span data-ttu-id="76f72-114">*pHeight* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="76f72-114">*pHeight* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="76f72-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="76f72-115">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="76f72-116">Ponteiro para a altura solicitada em pixels, ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="76f72-116">Pointer to the requested height in pixels, or **NULL**.</span></span> <span data-ttu-id="76f72-117">Retorna o tamanho corrigido.</span><span class="sxs-lookup"><span data-stu-id="76f72-117">Returns the corrected size.</span></span>

</dd> <dt>

<span data-ttu-id="76f72-118">*pDepth* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="76f72-118">*pDepth* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="76f72-119">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="76f72-119">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="76f72-120">Ponteiro para a profundidade solicitada em pixels ou **nulo**.</span><span class="sxs-lookup"><span data-stu-id="76f72-120">Pointer to the requested depth in pixels, or **NULL**.</span></span> <span data-ttu-id="76f72-121">Retorna o tamanho corrigido.</span><span class="sxs-lookup"><span data-stu-id="76f72-121">Returns the corrected size.</span></span>

</dd> <dt>

<span data-ttu-id="76f72-122">*pNumMipLevels* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="76f72-122">*pNumMipLevels* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="76f72-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="76f72-123">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="76f72-124">Aponta para o número de níveis de mipmap solicitados ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="76f72-124">Pointer to the number of requested mipmap levels, or **NULL**.</span></span> <span data-ttu-id="76f72-125">Retorna o número corrigido de níveis de mipmap.</span><span class="sxs-lookup"><span data-stu-id="76f72-125">Returns the corrected number of mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="76f72-126">*Uso* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="76f72-126">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76f72-127">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="76f72-127">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="76f72-128">Atualmente não usado, defina como 0.</span><span class="sxs-lookup"><span data-stu-id="76f72-128">Currently not used, set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="76f72-129">*pFormat* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="76f72-129">*pFormat* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="76f72-130">Tipo: **[D3DFORMAT](d3dformat.md)\***</span><span class="sxs-lookup"><span data-stu-id="76f72-130">Type: **[D3DFORMAT](d3dformat.md)\***</span></span>

<span data-ttu-id="76f72-131">Ponteiro para um membro do tipo enumerado [D3DFORMAT](d3dformat.md) .</span><span class="sxs-lookup"><span data-stu-id="76f72-131">Pointer to a member of the [D3DFORMAT](d3dformat.md) enumerated type.</span></span> <span data-ttu-id="76f72-132">Especifica o formato de pixel desejado ou **nulo**.</span><span class="sxs-lookup"><span data-stu-id="76f72-132">Specifies the desired pixel format, or **NULL**.</span></span> <span data-ttu-id="76f72-133">Retorna o formato corrigido.</span><span class="sxs-lookup"><span data-stu-id="76f72-133">Returns the corrected format.</span></span>

</dd> <dt>

<span data-ttu-id="76f72-134">*Pool* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="76f72-134">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76f72-135">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="76f72-135">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="76f72-136">Membro do tipo enumerado [**D3DPOOL**](./d3dpool.md) , descrevendo a classe de memória na qual a textura de volume deve ser colocada.</span><span class="sxs-lookup"><span data-stu-id="76f72-136">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the volume texture should be placed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76f72-137">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="76f72-137">Return value</span></span>

<span data-ttu-id="76f72-138">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="76f72-138">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="76f72-139">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="76f72-139">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="76f72-140">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ não disponível, D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="76f72-140">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="76f72-141">Comentários</span><span class="sxs-lookup"><span data-stu-id="76f72-141">Remarks</span></span>

<span data-ttu-id="76f72-142">Se os parâmetros para essa função forem inválidos, essa função retornará parâmetros corrigidos.</span><span class="sxs-lookup"><span data-stu-id="76f72-142">If parameters to this function are invalid, this function returns corrected parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="76f72-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="76f72-143">Requirements</span></span>



| <span data-ttu-id="76f72-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="76f72-144">Requirement</span></span> | <span data-ttu-id="76f72-145">Valor</span><span class="sxs-lookup"><span data-stu-id="76f72-145">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="76f72-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="76f72-146">Header</span></span><br/>  | <dl> <span data-ttu-id="76f72-147"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="76f72-147"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="76f72-148">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="76f72-148">Library</span></span><br/> | <dl> <span data-ttu-id="76f72-149"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="76f72-149"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="76f72-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="76f72-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76f72-151">Funções de textura no D3DX 9</span><span class="sxs-lookup"><span data-stu-id="76f72-151">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
