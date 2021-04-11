---
description: Verifica os parâmetros de criação de textura.
ms.assetid: f8e788f3-02a9-4ee7-b74d-9e781a2fb39f
title: Função D3DXCheckTextureRequirements (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCheckTextureRequirements
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d4fdc0998bfda2144e900c099919bc75c01e8ee3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173046"
---
# <a name="d3dxchecktexturerequirements-function"></a><span data-ttu-id="a7b8c-103">Função D3DXCheckTextureRequirements</span><span class="sxs-lookup"><span data-stu-id="a7b8c-103">D3DXCheckTextureRequirements function</span></span>

<span data-ttu-id="a7b8c-104">Verifica os parâmetros de criação de textura.</span><span class="sxs-lookup"><span data-stu-id="a7b8c-104">Checks texture-creation parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7b8c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a7b8c-105">Syntax</span></span>


```C++
HRESULT D3DXCheckTextureRequirements(
  _In_    LPDIRECT3DDEVICE9 pDevice,
  _Inout_ UINT              *pWidth,
  _Inout_ UINT              *pHeight,
  _Inout_ UINT              *pNumMipLevels,
  _In_    DWORD             Usage,
  _Inout_ D3DFORMAT         *pFormat,
  _In_    D3DPOOL           Pool
);
```



## <a name="parameters"></a><span data-ttu-id="a7b8c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a7b8c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7b8c-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a7b8c-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7b8c-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="a7b8c-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="a7b8c-109">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , representando o dispositivo a ser associado à textura.</span><span class="sxs-lookup"><span data-stu-id="a7b8c-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="a7b8c-110">*pWidth* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="a7b8c-110">*pWidth* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a7b8c-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="a7b8c-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a7b8c-112">Ponteiro para a largura solicitada em pixels ou **nulo**.</span><span class="sxs-lookup"><span data-stu-id="a7b8c-112">Pointer to the requested width in pixels, or **NULL**.</span></span> <span data-ttu-id="a7b8c-113">Retorna o tamanho corrigido.</span><span class="sxs-lookup"><span data-stu-id="a7b8c-113">Returns the corrected size.</span></span>

</dd> <dt>

<span data-ttu-id="a7b8c-114">*pHeight* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="a7b8c-114">*pHeight* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a7b8c-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="a7b8c-115">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a7b8c-116">Ponteiro para a altura solicitada em pixels, ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="a7b8c-116">Pointer to the requested height in pixels, or **NULL**.</span></span> <span data-ttu-id="a7b8c-117">Retorna o tamanho corrigido.</span><span class="sxs-lookup"><span data-stu-id="a7b8c-117">Returns the corrected size.</span></span>

</dd> <dt>

<span data-ttu-id="a7b8c-118">*pNumMipLevels* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="a7b8c-118">*pNumMipLevels* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a7b8c-119">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="a7b8c-119">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a7b8c-120">Ponteiro para o número de níveis de mipmap solicitados ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="a7b8c-120">Pointer to number of requested mipmap levels, or **NULL**.</span></span> <span data-ttu-id="a7b8c-121">Retorna o número corrigido de níveis de mipmap.</span><span class="sxs-lookup"><span data-stu-id="a7b8c-121">Returns the corrected number of mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="a7b8c-122">*Uso* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="a7b8c-122">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7b8c-123">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a7b8c-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a7b8c-124">0 ou [**D3DUSAGE \_ RENDERTARGET**](d3dusage.md).</span><span class="sxs-lookup"><span data-stu-id="a7b8c-124">0 or [**D3DUSAGE\_RENDERTARGET**](d3dusage.md).</span></span> <span data-ttu-id="a7b8c-125">Definir esse sinalizador como D3DUSAGE \_ RENDERTARGET indica que a superfície deve ser usada como um destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="a7b8c-125">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="a7b8c-126">O recurso pode então ser passado para o parâmetro pNewRenderTarget do método [**SetRenderTarget**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="a7b8c-126">The resource can then be passed to the pNewRenderTarget parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="a7b8c-127">Se **D3DUSAGE \_ RENDERTARGET** for especificado, o aplicativo deverá verificar se o dispositivo dá suporte a essa operação chamando [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat).</span><span class="sxs-lookup"><span data-stu-id="a7b8c-127">If **D3DUSAGE\_RENDERTARGET** is specified, the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat).</span></span>

</dd> <dt>

<span data-ttu-id="a7b8c-128">*pFormat* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="a7b8c-128">*pFormat* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a7b8c-129">Tipo: **[D3DFORMAT](d3dformat.md)\***</span><span class="sxs-lookup"><span data-stu-id="a7b8c-129">Type: **[D3DFORMAT](d3dformat.md)\***</span></span>

<span data-ttu-id="a7b8c-130">Ponteiro para um membro do tipo enumerado [D3DFORMAT](d3dformat.md) .</span><span class="sxs-lookup"><span data-stu-id="a7b8c-130">Pointer to a member of the [D3DFORMAT](d3dformat.md) enumerated type.</span></span> <span data-ttu-id="a7b8c-131">Especifica o formato de pixel desejado ou **nulo**.</span><span class="sxs-lookup"><span data-stu-id="a7b8c-131">Specifies the desired pixel format, or **NULL**.</span></span> <span data-ttu-id="a7b8c-132">Retorna o formato corrigido.</span><span class="sxs-lookup"><span data-stu-id="a7b8c-132">Returns the corrected format.</span></span>

</dd> <dt>

<span data-ttu-id="a7b8c-133">*Pool* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="a7b8c-133">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7b8c-134">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="a7b8c-134">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="a7b8c-135">Membro do tipo enumerado [**D3DPOOL**](./d3dpool.md) , que descreve a classe de memória na qual a textura deve ser colocada.</span><span class="sxs-lookup"><span data-stu-id="a7b8c-135">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7b8c-136">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a7b8c-136">Return value</span></span>

<span data-ttu-id="a7b8c-137">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a7b8c-137">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a7b8c-138">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a7b8c-138">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a7b8c-139">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DERR \_ não disponível.</span><span class="sxs-lookup"><span data-stu-id="a7b8c-139">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7b8c-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="a7b8c-140">Remarks</span></span>

<span data-ttu-id="a7b8c-141">Se os parâmetros para essa função forem inválidos, essa função retornará parâmetros corrigidos.</span><span class="sxs-lookup"><span data-stu-id="a7b8c-141">If parameters to this function are invalid, this function returns corrected parameters.</span></span>

<span data-ttu-id="a7b8c-142">Essa função usa a heurística a seguir ao comparar os requisitos solicitados com os formatos disponíveis:</span><span class="sxs-lookup"><span data-stu-id="a7b8c-142">This function uses the following heuristics when comparing the requested requirements against available formats:</span></span>

-   <span data-ttu-id="a7b8c-143">Não escolha um formato que tenha menos canais.</span><span class="sxs-lookup"><span data-stu-id="a7b8c-143">Do not choose a format that has fewer channels.</span></span>
-   <span data-ttu-id="a7b8c-144">Evite formatos [FOURCC](d3dformat.md) e de 24 bits, a menos que solicitado explicitamente.</span><span class="sxs-lookup"><span data-stu-id="a7b8c-144">Avoid [FOURCC](d3dformat.md) And 24-bit formats unless explicitly requested.</span></span>
-   <span data-ttu-id="a7b8c-145">Tente não adicionar novos canais.</span><span class="sxs-lookup"><span data-stu-id="a7b8c-145">Try not to add new channels.</span></span>
-   <span data-ttu-id="a7b8c-146">Tente não alterar o número de bits por canal.</span><span class="sxs-lookup"><span data-stu-id="a7b8c-146">Try not to change the number of bits per channel.</span></span>
-   <span data-ttu-id="a7b8c-147">Tente evitar a conversão entre tipos de formatos.</span><span class="sxs-lookup"><span data-stu-id="a7b8c-147">Try to avoid converting between types of formats.</span></span> <span data-ttu-id="a7b8c-148">Por exemplo, evite converter um formato ARGB em um formato de profundidade.</span><span class="sxs-lookup"><span data-stu-id="a7b8c-148">For instance, avoid converting an ARGB format to a depth format.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7b8c-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7b8c-149">Requirements</span></span>



| <span data-ttu-id="a7b8c-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7b8c-150">Requirement</span></span> | <span data-ttu-id="a7b8c-151">Valor</span><span class="sxs-lookup"><span data-stu-id="a7b8c-151">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a7b8c-152">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a7b8c-152">Header</span></span><br/>  | <dl> <span data-ttu-id="a7b8c-153"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7b8c-153"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="a7b8c-154">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a7b8c-154">Library</span></span><br/> | <dl> <span data-ttu-id="a7b8c-155"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a7b8c-155"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="a7b8c-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="a7b8c-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7b8c-157">Funções de textura no D3DX 9</span><span class="sxs-lookup"><span data-stu-id="a7b8c-157">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
