---
description: Verifica os parâmetros de criação de textura de cubo.
ms.assetid: 56ced947-1142-4d05-95e3-ca6a26b147d4
title: Função D3DXCheckCubeTextureRequirements (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCheckCubeTextureRequirements
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9f800617920c5d79361b5e6da291fd88b5b963b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664106"
---
# <a name="d3dxcheckcubetexturerequirements-function"></a><span data-ttu-id="0c456-103">Função D3DXCheckCubeTextureRequirements</span><span class="sxs-lookup"><span data-stu-id="0c456-103">D3DXCheckCubeTextureRequirements function</span></span>

<span data-ttu-id="0c456-104">Verifica os parâmetros de criação de textura de cubo.</span><span class="sxs-lookup"><span data-stu-id="0c456-104">Checks cube-texture-creation parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c456-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0c456-105">Syntax</span></span>


```C++
HRESULT D3DXCheckCubeTextureRequirements(
  _In_    LPDIRECT3DDEVICE9 pDevice,
  _Inout_ UINT              *pSize,
  _Inout_ UINT              *pNumMipLevels,
  _In_    DWORD             Usage,
  _Inout_ D3DFORMAT         *pFormat,
  _In_    D3DPOOL           Pool
);
```



## <a name="parameters"></a><span data-ttu-id="0c456-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0c456-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c456-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0c456-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c456-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="0c456-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="0c456-109">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , representando o dispositivo a ser associado à textura do cubo.</span><span class="sxs-lookup"><span data-stu-id="0c456-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="0c456-110">*psize* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="0c456-110">*pSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0c456-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0c456-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0c456-112">Ponteiro para a largura e a altura solicitadas em pixels, ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="0c456-112">Pointer to the requested width and height in pixels, or **NULL**.</span></span> <span data-ttu-id="0c456-113">Retorna o tamanho corrigido.</span><span class="sxs-lookup"><span data-stu-id="0c456-113">Returns the corrected size.</span></span>

</dd> <dt>

<span data-ttu-id="0c456-114">*pNumMipLevels* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="0c456-114">*pNumMipLevels* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0c456-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0c456-115">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0c456-116">Aponta para o número de níveis de mipmap solicitados ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="0c456-116">Pointer to the number of requested mipmap levels, or **NULL**.</span></span> <span data-ttu-id="0c456-117">Retorna o número corrigido de níveis de mipmap.</span><span class="sxs-lookup"><span data-stu-id="0c456-117">Returns the corrected number of mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="0c456-118">*Uso* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="0c456-118">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c456-119">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0c456-119">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0c456-120">0 ou D3DUSAGE \_ RENDERTARGET.</span><span class="sxs-lookup"><span data-stu-id="0c456-120">0 or D3DUSAGE\_RENDERTARGET.</span></span> <span data-ttu-id="0c456-121">Definir esse sinalizador como D3DUSAGE \_ RENDERTARGET indica que a superfície deve ser usada como um destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="0c456-121">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="0c456-122">O recurso pode então ser passado para o parâmetro pNewRenderTarget do método [**SetRenderTarget**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="0c456-122">The resource can then be passed to the pNewRenderTarget parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="0c456-123">Se D3DUSAGE \_ RENDERTARGET for especificado, o aplicativo deverá verificar se o dispositivo dá suporte a essa operação [**chamando CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat).</span><span class="sxs-lookup"><span data-stu-id="0c456-123">If D3DUSAGE\_RENDERTARGET is specified, the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat).</span></span>

</dd> <dt>

<span data-ttu-id="0c456-124">*pFormat* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="0c456-124">*pFormat* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0c456-125">Tipo: **[D3DFORMAT](d3dformat.md)\***</span><span class="sxs-lookup"><span data-stu-id="0c456-125">Type: **[D3DFORMAT](d3dformat.md)\***</span></span>

<span data-ttu-id="0c456-126">Ponteiro para um membro do tipo enumerado [D3DFORMAT](d3dformat.md) .</span><span class="sxs-lookup"><span data-stu-id="0c456-126">Pointer to a member of the [D3DFORMAT](d3dformat.md) enumerated type.</span></span> <span data-ttu-id="0c456-127">Especifica o formato de pixel desejado ou **nulo**.</span><span class="sxs-lookup"><span data-stu-id="0c456-127">Specifies the desired pixel format, or **NULL**.</span></span> <span data-ttu-id="0c456-128">Retorna o formato corrigido.</span><span class="sxs-lookup"><span data-stu-id="0c456-128">Returns the corrected format.</span></span>

</dd> <dt>

<span data-ttu-id="0c456-129">*Pool* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="0c456-129">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c456-130">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="0c456-130">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="0c456-131">Membro do tipo enumerado [**D3DPOOL**](./d3dpool.md) , que descreve a classe de memória na qual a textura deve ser colocada.</span><span class="sxs-lookup"><span data-stu-id="0c456-131">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c456-132">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0c456-132">Return value</span></span>

<span data-ttu-id="0c456-133">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0c456-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0c456-134">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0c456-134">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0c456-135">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ não disponível, D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="0c456-135">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c456-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="0c456-136">Remarks</span></span>

<span data-ttu-id="0c456-137">Se os parâmetros para essa função forem inválidos, essa função retornará parâmetros corrigidos.</span><span class="sxs-lookup"><span data-stu-id="0c456-137">If parameters to this function are invalid, this function returns corrected parameters.</span></span>

<span data-ttu-id="0c456-138">Texturas de cubos diferem de outras superfícies em que são coleções de superfícies.</span><span class="sxs-lookup"><span data-stu-id="0c456-138">Cube textures differ from other surfaces in that they are collections of surfaces.</span></span> <span data-ttu-id="0c456-139">Para chamar [**SetRenderTarget**](/windows/desktop/api) com uma textura de cubo, você deve selecionar uma face individual usando [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) e passar a superfície resultante para **SetRenderTarget**.</span><span class="sxs-lookup"><span data-stu-id="0c456-139">To call [**SetRenderTarget**](/windows/desktop/api) with a cube texture, you must select an individual face using [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) and pass the resulting surface to **SetRenderTarget**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c456-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c456-140">Requirements</span></span>



| <span data-ttu-id="0c456-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c456-141">Requirement</span></span> | <span data-ttu-id="0c456-142">Valor</span><span class="sxs-lookup"><span data-stu-id="0c456-142">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0c456-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0c456-143">Header</span></span><br/>  | <dl> <span data-ttu-id="0c456-144"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c456-144"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="0c456-145">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0c456-145">Library</span></span><br/> | <dl> <span data-ttu-id="0c456-146"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0c456-146"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="0c456-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="0c456-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c456-148">Funções de textura no D3DX 9</span><span class="sxs-lookup"><span data-stu-id="0c456-148">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
