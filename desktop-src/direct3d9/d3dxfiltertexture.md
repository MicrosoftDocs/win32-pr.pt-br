---
description: Filtra os níveis de mipmap de uma textura.
ms.assetid: bfeae9b0-9480-4a26-a225-4a34780546ce
title: Função D3DXFilterTexture (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFilterTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e8a0d1c211b50379451c8b04830e9c97fe988137
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105785270"
---
# <a name="d3dxfiltertexture-function"></a><span data-ttu-id="959e5-103">Função D3DXFilterTexture</span><span class="sxs-lookup"><span data-stu-id="959e5-103">D3DXFilterTexture function</span></span>

<span data-ttu-id="959e5-104">Filtra os níveis de mipmap de uma textura.</span><span class="sxs-lookup"><span data-stu-id="959e5-104">Filters mipmap levels of a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="959e5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="959e5-105">Syntax</span></span>


```C++
HRESULT D3DXFilterTexture(
  _In_        LPDIRECT3DBASETEXTURE9 pBaseTexture,
  _Out_ const PALETTEENTRY           *pPalette,
  _In_        UINT                   SrcLevel,
  _In_        DWORD                  MipFilter
);
```



## <a name="parameters"></a><span data-ttu-id="959e5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="959e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="959e5-107">*pBaseTexture* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="959e5-107">*pBaseTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="959e5-108">Tipo: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span><span class="sxs-lookup"><span data-stu-id="959e5-108">Type: **[**LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span></span>

<span data-ttu-id="959e5-109">Ponteiro para uma interface [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) que representa o objeto de textura a ser filtrado.</span><span class="sxs-lookup"><span data-stu-id="959e5-109">Pointer to an [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) interface that represents the texture object to filter.</span></span>

</dd> <dt>

<span data-ttu-id="959e5-110">*pPalette* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="959e5-110">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="959e5-111">Tipo: **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="959e5-111">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="959e5-112">Ponteiro para uma estrutura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) que representa uma paleta de cor de 256 para preencher ou **nulo** para formatos nonpalettized.</span><span class="sxs-lookup"><span data-stu-id="959e5-112">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure that represents a 256-color palette to fill in, or **NULL** for nonpalettized formats.</span></span> <span data-ttu-id="959e5-113">Se uma paleta não for especificada, a paleta padrão do Direct3D (uma paleta branca opaca) será fornecida.</span><span class="sxs-lookup"><span data-stu-id="959e5-113">If a palette is not specified, the default Direct3D palette (an all opaque white palette) is provided.</span></span> <span data-ttu-id="959e5-114">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="959e5-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="959e5-115">*SrcLevel* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="959e5-115">*SrcLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="959e5-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="959e5-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="959e5-117">Nível cuja imagem é usada para gerar os níveis subsequentes.</span><span class="sxs-lookup"><span data-stu-id="959e5-117">Level whose image is used to generate the subsequent levels.</span></span> <span data-ttu-id="959e5-118">A especificação \_ do padrão D3DX para esse parâmetro é equivalente à especificação de 0.</span><span class="sxs-lookup"><span data-stu-id="959e5-118">Specifying D3DX\_DEFAULT for this parameter is equivalent to specifying 0.</span></span>

</dd> <dt>

<span data-ttu-id="959e5-119">*MipFilter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="959e5-119">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="959e5-120">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="959e5-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="959e5-121">Combinação de um ou mais [ \_ filtros D3DX](d3dx-filter.md) controlando como o mipmap é filtrado.</span><span class="sxs-lookup"><span data-stu-id="959e5-121">Combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the mipmap is filtered.</span></span> <span data-ttu-id="959e5-122">A especificação de D3DX \_ padrão para esse parâmetro é o equivalente à especificação da \_ caixa de filtro D3DX \_ se o tamanho da textura for uma potência de dois e D3DX \_ caixa de filtro D3DX de filtro de \_ \| \_ \_ outra forma.</span><span class="sxs-lookup"><span data-stu-id="959e5-122">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX if the texture size is a power of two, and D3DX\_FILTER\_BOX \| D3DX\_FILTER\_DITHER otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="959e5-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="959e5-123">Return value</span></span>

<span data-ttu-id="959e5-124">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="959e5-124">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="959e5-125">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="959e5-125">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="959e5-126">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="959e5-126">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="959e5-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="959e5-127">Remarks</span></span>

<span data-ttu-id="959e5-128">Um filtro é aplicado recursivamente a cada nível de textura para gerar o próximo nível de textura.</span><span class="sxs-lookup"><span data-stu-id="959e5-128">A filter is recursively applied to each texture level to generate the next texture level.</span></span>

<span data-ttu-id="959e5-129">Gravar em uma superfície de não nível zero da textura não fará com que o retângulo sujo seja atualizado.</span><span class="sxs-lookup"><span data-stu-id="959e5-129">Writing to a non-level-zero surface of the texture will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="959e5-130">Se **D3DXFilterTexture** for chamado e a superfície já não tiver sido suja (isso é improvável em cenários de uso normal), o aplicativo precisa chamar [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) explicitamente na textura.</span><span class="sxs-lookup"><span data-stu-id="959e5-130">If **D3DXFilterTexture** is called and the surface was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) on the texture.</span></span>

<span data-ttu-id="959e5-131">As texturas criadas no pool padrão (D3DPOOL \_ padrão) não podem ser usadas com **D3DXFilterTexture** (a menos que criadas com D3DUSAGE \_ dinâmico), pois uma operação de bloqueio é necessária no objeto.</span><span class="sxs-lookup"><span data-stu-id="959e5-131">Textures created in the default pool (D3DPOOL\_DEFAULT) cannot be used with **D3DXFilterTexture** (unless created with D3DUSAGE\_DYNAMIC) because a lock operation is needed on the object.</span></span> <span data-ttu-id="959e5-132">Observe que os bloqueios são proibidos em texturas no pool padrão (a menos que sejam dinâmicos).</span><span class="sxs-lookup"><span data-stu-id="959e5-132">Note that locks are prohibited on textures in the default pool (unless they are dynamic).</span></span>

<span data-ttu-id="959e5-133">Para obter detalhes sobre o [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry), consulte o SDK da plataforma.</span><span class="sxs-lookup"><span data-stu-id="959e5-133">For details on [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry), see the Platform SDK.</span></span> <span data-ttu-id="959e5-134">Observe que, a partir do DirectX 8,0, o membro peFlags da estrutura **PaletteEntry** não funciona conforme documentado no SDK da plataforma.</span><span class="sxs-lookup"><span data-stu-id="959e5-134">Note that as of DirectX 8.0, the peFlags member of the **PALETTEENTRY** structure does not function as documented in the Platform SDK.</span></span> <span data-ttu-id="959e5-135">O membro peFlags agora é o canal alfa para formatos de palettized de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="959e5-135">The peFlags member is now the alpha channel for 8-bit palettized formats.</span></span>

<span data-ttu-id="959e5-136">Há apenas uma função de filtragem de textura, mas duas macros que chamam esse método.</span><span class="sxs-lookup"><span data-stu-id="959e5-136">There is only one texture filtering function, but two macros that call this method.</span></span>


```
#define D3DXFilterCubeTexture D3DXFilterTexture
#define D3DXFilterVolumeTexture D3DXFilterTexture
```



## <a name="requirements"></a><span data-ttu-id="959e5-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="959e5-137">Requirements</span></span>



| <span data-ttu-id="959e5-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="959e5-138">Requirement</span></span> | <span data-ttu-id="959e5-139">Valor</span><span class="sxs-lookup"><span data-stu-id="959e5-139">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="959e5-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="959e5-140">Header</span></span><br/>  | <dl> <span data-ttu-id="959e5-141"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="959e5-141"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="959e5-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="959e5-142">Library</span></span><br/> | <dl> <span data-ttu-id="959e5-143"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="959e5-143"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="959e5-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="959e5-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="959e5-145">Funções de textura no D3DX 9</span><span class="sxs-lookup"><span data-stu-id="959e5-145">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
