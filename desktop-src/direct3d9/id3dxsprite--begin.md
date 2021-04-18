---
description: Prepara um dispositivo para desenhar sprites.
ms.assetid: ec9eb069-0a41-4dd5-bbd5-5a31133550b6
title: 'Método ID3DXSprite:: Begin (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.Begin
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7670c3c516627283a466b3adbb369dc76bbe0d45
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105764166"
---
# <a name="id3dxspritebegin-method"></a><span data-ttu-id="be3d4-103">Método ID3DXSprite:: Begin</span><span class="sxs-lookup"><span data-stu-id="be3d4-103">ID3DXSprite::Begin method</span></span>

<span data-ttu-id="be3d4-104">Prepara um dispositivo para desenhar sprites.</span><span class="sxs-lookup"><span data-stu-id="be3d4-104">Prepares a device for drawing sprites.</span></span>

## <a name="syntax"></a><span data-ttu-id="be3d4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="be3d4-105">Syntax</span></span>


```C++
HRESULT Begin(
  [in] DWORD Flags
);
```



## <a name="parameters"></a><span data-ttu-id="be3d4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="be3d4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be3d4-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="be3d4-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be3d4-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="be3d4-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="be3d4-109">Combinação de zero ou mais sinalizadores que descrevem as opções de renderização de Sprite.</span><span class="sxs-lookup"><span data-stu-id="be3d4-109">Combination of zero or more flags that describe sprite rendering options.</span></span> <span data-ttu-id="be3d4-110">Para esse método, os sinalizadores válidos são:</span><span class="sxs-lookup"><span data-stu-id="be3d4-110">For this method, the valid flags are:</span></span>

-   <span data-ttu-id="be3d4-111">D3DXSPRITE \_ ALPHABLEND</span><span class="sxs-lookup"><span data-stu-id="be3d4-111">D3DXSPRITE\_ALPHABLEND</span></span>
-   <span data-ttu-id="be3d4-112">D3DXSPRITE de \_ \_ mensagem</span><span class="sxs-lookup"><span data-stu-id="be3d4-112">D3DXSPRITE\_\_BILLBOARD</span></span>
-   <span data-ttu-id="be3d4-113">D3DXSPRITE \_ DONOTMODIFY \_ renderingstate</span><span class="sxs-lookup"><span data-stu-id="be3d4-113">D3DXSPRITE\_DONOTMODIFY\_RENDERSTATE</span></span>
-   <span data-ttu-id="be3d4-114">D3DXSPRITE \_ DONOTSAVESTATE</span><span class="sxs-lookup"><span data-stu-id="be3d4-114">D3DXSPRITE\_DONOTSAVESTATE</span></span>
-   <span data-ttu-id="be3d4-115">D3DXSPRITE \_ OBJECTspace</span><span class="sxs-lookup"><span data-stu-id="be3d4-115">D3DXSPRITE\_OBJECTSPACE</span></span>
-   <span data-ttu-id="be3d4-116">D3DXSPRITE \_ \_ \_ BACKTOFRONT profundidade de classificação \_</span><span class="sxs-lookup"><span data-stu-id="be3d4-116">D3DXSPRITE\_\_SORT\_DEPTH\_BACKTOFRONT</span></span>
-   <span data-ttu-id="be3d4-117">D3DXSPRITE \_ \_ \_ FRONTTOBACK profundidade de classificação \_</span><span class="sxs-lookup"><span data-stu-id="be3d4-117">D3DXSPRITE\_\_SORT\_DEPTH\_FRONTTOBACK</span></span>
-   <span data-ttu-id="be3d4-118">\_ \_ Textura de classificação D3DXSPRITE \_</span><span class="sxs-lookup"><span data-stu-id="be3d4-118">D3DXSPRITE\_\_SORT\_TEXTURE</span></span>

<span data-ttu-id="be3d4-119">Para obter uma descrição dos sinalizadores e informações sobre como controlar a captura de estado do dispositivo e as transformações de exibição do dispositivo, consulte [D3DXSPRITE](d3dxsprite.md).</span><span class="sxs-lookup"><span data-stu-id="be3d4-119">For a description of the flags and for information on how to control device state capture and device view transforms, see [D3DXSPRITE](d3dxsprite.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be3d4-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="be3d4-120">Return value</span></span>

<span data-ttu-id="be3d4-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="be3d4-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="be3d4-122">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="be3d4-122">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="be3d4-123">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="be3d4-123">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="be3d4-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="be3d4-124">Remarks</span></span>

<span data-ttu-id="be3d4-125">Esse método deve ser chamado de dentro de um [**IDirect3DDevice9:: BeginScene**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="be3d4-125">This method must be called from inside a [**IDirect3DDevice9::BeginScene**](/windows/desktop/api) .</span></span> <span data-ttu-id="be3d4-126">.</span><span class="sxs-lookup"><span data-stu-id="be3d4-126">.</span></span> <span data-ttu-id="be3d4-127">.</span><span class="sxs-lookup"><span data-stu-id="be3d4-127">.</span></span> <span data-ttu-id="be3d4-128">Sequência [**IDirect3DDevice9:: endcena**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="be3d4-128">[**IDirect3DDevice9::EndScene**](/windows/desktop/api) sequence.</span></span> <span data-ttu-id="be3d4-129">**ID3DXSprite:: Begin** não pode ser usado como um substituto para **IDirect3DDevice9:: BeginScene** ou [**ID3DXRenderToSurface:: BeginScene**](id3dxrendertosurface--beginscene.md).</span><span class="sxs-lookup"><span data-stu-id="be3d4-129">**ID3DXSprite::Begin** cannot be used as a substitute for either **IDirect3DDevice9::BeginScene** or [**ID3DXRenderToSurface::BeginScene**](id3dxrendertosurface--beginscene.md).</span></span>

<span data-ttu-id="be3d4-130">Esse método irá definir os seguintes Estados no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="be3d4-130">This method will set the following states on the device.</span></span>

<span data-ttu-id="be3d4-131">Processar estados:</span><span class="sxs-lookup"><span data-stu-id="be3d4-131">Render States:</span></span>



| <span data-ttu-id="be3d4-132">Tipo ([**D3DRENDERSTATETYPE**](./d3drenderstatetype.md))</span><span class="sxs-lookup"><span data-stu-id="be3d4-132">Type ([**D3DRENDERSTATETYPE**](./d3drenderstatetype.md))</span></span> | <span data-ttu-id="be3d4-133">Valor</span><span class="sxs-lookup"><span data-stu-id="be3d4-133">Value</span></span>                                                                                                             |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be3d4-134">D3DRS \_ ALPHABLENDENABLE</span><span class="sxs-lookup"><span data-stu-id="be3d4-134">D3DRS\_ALPHABLENDENABLE</span></span>                                       | <span data-ttu-id="be3d4-135">TRUE</span><span class="sxs-lookup"><span data-stu-id="be3d4-135">TRUE</span></span>                                                                                                              |
| <span data-ttu-id="be3d4-136">D3DRS \_ ALPHAFUNC</span><span class="sxs-lookup"><span data-stu-id="be3d4-136">D3DRS\_ALPHAFUNC</span></span>                                              | <span data-ttu-id="be3d4-137">D3DCMP \_ maior</span><span class="sxs-lookup"><span data-stu-id="be3d4-137">D3DCMP\_GREATER</span></span>                                                                                                   |
| <span data-ttu-id="be3d4-138">D3DRS \_ ALPHAREF</span><span class="sxs-lookup"><span data-stu-id="be3d4-138">D3DRS\_ALPHAREF</span></span>                                               | <span data-ttu-id="be3d4-139">0x00</span><span class="sxs-lookup"><span data-stu-id="be3d4-139">0x00</span></span>                                                                                                              |
| <span data-ttu-id="be3d4-140">D3DRS \_ ALPHATESTENABLE</span><span class="sxs-lookup"><span data-stu-id="be3d4-140">D3DRS\_ALPHATESTENABLE</span></span>                                        | <span data-ttu-id="be3d4-141">AlphaCmpCaps</span><span class="sxs-lookup"><span data-stu-id="be3d4-141">AlphaCmpCaps</span></span>                                                                                                      |
| <span data-ttu-id="be3d4-142">D3DRS \_ BLENDOP</span><span class="sxs-lookup"><span data-stu-id="be3d4-142">D3DRS\_BLENDOP</span></span>                                                | <span data-ttu-id="be3d4-143">D3DBLENDOP \_ Adicionar</span><span class="sxs-lookup"><span data-stu-id="be3d4-143">D3DBLENDOP\_ADD</span></span>                                                                                                   |
| <span data-ttu-id="be3d4-144">Recorte de D3DRS \_</span><span class="sxs-lookup"><span data-stu-id="be3d4-144">D3DRS\_CLIPPING</span></span>                                               | <span data-ttu-id="be3d4-145">TRUE</span><span class="sxs-lookup"><span data-stu-id="be3d4-145">TRUE</span></span>                                                                                                              |
| <span data-ttu-id="be3d4-146">D3DRS \_ CLIPPLANEENABLE</span><span class="sxs-lookup"><span data-stu-id="be3d4-146">D3DRS\_CLIPPLANEENABLE</span></span>                                        | <span data-ttu-id="be3d4-147">FALSE</span><span class="sxs-lookup"><span data-stu-id="be3d4-147">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="be3d4-148">D3DRS \_ COLORWRITEENABLE</span><span class="sxs-lookup"><span data-stu-id="be3d4-148">D3DRS\_COLORWRITEENABLE</span></span>                                       | <span data-ttu-id="be3d4-149">D3DCOLORWRITEENABLE \_ Alpha \| D3DCOLORWRITEENABLE \_ Blue \| D3DCOLORWRITEENABLE \_ verde \| D3DCOLORWRITEENABLE \_ vermelho</span><span class="sxs-lookup"><span data-stu-id="be3d4-149">D3DCOLORWRITEENABLE\_ALPHA \| D3DCOLORWRITEENABLE\_BLUE \| D3DCOLORWRITEENABLE\_GREEN \| D3DCOLORWRITEENABLE\_RED</span></span> |
| <span data-ttu-id="be3d4-150">D3DRS de \_ seleção</span><span class="sxs-lookup"><span data-stu-id="be3d4-150">D3DRS\_CULLMODE</span></span>                                               | <span data-ttu-id="be3d4-151">D3DCULL \_ nenhum</span><span class="sxs-lookup"><span data-stu-id="be3d4-151">D3DCULL\_NONE</span></span>                                                                                                     |
| <span data-ttu-id="be3d4-152">D3DRS \_ DESTBLEND</span><span class="sxs-lookup"><span data-stu-id="be3d4-152">D3DRS\_DESTBLEND</span></span>                                              | <span data-ttu-id="be3d4-153">D3DBLEND \_ INVSRCALPHA</span><span class="sxs-lookup"><span data-stu-id="be3d4-153">D3DBLEND\_INVSRCALPHA</span></span>                                                                                             |
| <span data-ttu-id="be3d4-154">D3DRS \_ DiffuseMaterialSource</span><span class="sxs-lookup"><span data-stu-id="be3d4-154">D3DRS\_DIFFUSEMATERIALSOURCE</span></span>                                  | <span data-ttu-id="be3d4-155">D3DMCS \_ COLOR1</span><span class="sxs-lookup"><span data-stu-id="be3d4-155">D3DMCS\_COLOR1</span></span>                                                                                                    |
| <span data-ttu-id="be3d4-156">D3DRS \_ ENABLEADAPTIVETESSELLATION</span><span class="sxs-lookup"><span data-stu-id="be3d4-156">D3DRS\_ENABLEADAPTIVETESSELLATION</span></span>                             | <span data-ttu-id="be3d4-157">FALSE</span><span class="sxs-lookup"><span data-stu-id="be3d4-157">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="be3d4-158">D3DRS \_ FillMode</span><span class="sxs-lookup"><span data-stu-id="be3d4-158">D3DRS\_FILLMODE</span></span>                                               | <span data-ttu-id="be3d4-159">D3DFILL \_ sólido</span><span class="sxs-lookup"><span data-stu-id="be3d4-159">D3DFILL\_SOLID</span></span>                                                                                                    |
| <span data-ttu-id="be3d4-160">D3DRS \_ FOGENABLE</span><span class="sxs-lookup"><span data-stu-id="be3d4-160">D3DRS\_FOGENABLE</span></span>                                              | <span data-ttu-id="be3d4-161">FALSE</span><span class="sxs-lookup"><span data-stu-id="be3d4-161">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="be3d4-162">D3DRS \_ INDEXEDVERTEXBLENDENABLE</span><span class="sxs-lookup"><span data-stu-id="be3d4-162">D3DRS\_INDEXEDVERTEXBLENDENABLE</span></span>                               | <span data-ttu-id="be3d4-163">FALSE</span><span class="sxs-lookup"><span data-stu-id="be3d4-163">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="be3d4-164">\_Iluminação D3DRS</span><span class="sxs-lookup"><span data-stu-id="be3d4-164">D3DRS\_LIGHTING</span></span>                                               | <span data-ttu-id="be3d4-165">FALSE</span><span class="sxs-lookup"><span data-stu-id="be3d4-165">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="be3d4-166">D3DRS \_ RANGEFOGENABLE</span><span class="sxs-lookup"><span data-stu-id="be3d4-166">D3DRS\_RANGEFOGENABLE</span></span>                                         | <span data-ttu-id="be3d4-167">FALSE</span><span class="sxs-lookup"><span data-stu-id="be3d4-167">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="be3d4-168">D3DRS \_ SEPARATEALPHABLENDENABLE</span><span class="sxs-lookup"><span data-stu-id="be3d4-168">D3DRS\_SEPARATEALPHABLENDENABLE</span></span>                               | <span data-ttu-id="be3d4-169">FALSE</span><span class="sxs-lookup"><span data-stu-id="be3d4-169">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="be3d4-170">D3DRS \_ shadmode</span><span class="sxs-lookup"><span data-stu-id="be3d4-170">D3DRS\_SHADEMODE</span></span>                                              | <span data-ttu-id="be3d4-171">D3DSHADE \_ GOURAUD</span><span class="sxs-lookup"><span data-stu-id="be3d4-171">D3DSHADE\_GOURAUD</span></span>                                                                                                 |
| <span data-ttu-id="be3d4-172">D3DRS \_ SPECULARENABLE</span><span class="sxs-lookup"><span data-stu-id="be3d4-172">D3DRS\_SPECULARENABLE</span></span>                                         | <span data-ttu-id="be3d4-173">FALSE</span><span class="sxs-lookup"><span data-stu-id="be3d4-173">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="be3d4-174">D3DRS \_ SRCBLEND</span><span class="sxs-lookup"><span data-stu-id="be3d4-174">D3DRS\_SRCBLEND</span></span>                                               | <span data-ttu-id="be3d4-175">D3DBLEND \_ SRCALPHA</span><span class="sxs-lookup"><span data-stu-id="be3d4-175">D3DBLEND\_SRCALPHA</span></span>                                                                                                |
| <span data-ttu-id="be3d4-176">D3DRS \_ SRGBWRITEENABLE</span><span class="sxs-lookup"><span data-stu-id="be3d4-176">D3DRS\_SRGBWRITEENABLE</span></span>                                        | <span data-ttu-id="be3d4-177">FALSE</span><span class="sxs-lookup"><span data-stu-id="be3d4-177">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="be3d4-178">D3DRS \_ STENCILENABLE</span><span class="sxs-lookup"><span data-stu-id="be3d4-178">D3DRS\_STENCILENABLE</span></span>                                          | <span data-ttu-id="be3d4-179">FALSE</span><span class="sxs-lookup"><span data-stu-id="be3d4-179">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="be3d4-180">D3DRS \_ VERTEXBLEND</span><span class="sxs-lookup"><span data-stu-id="be3d4-180">D3DRS\_VERTEXBLEND</span></span>                                            | <span data-ttu-id="be3d4-181">FALSE</span><span class="sxs-lookup"><span data-stu-id="be3d4-181">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="be3d4-182">D3DRS \_ WRAP0</span><span class="sxs-lookup"><span data-stu-id="be3d4-182">D3DRS\_WRAP0</span></span>                                                  | <span data-ttu-id="be3d4-183">0</span><span class="sxs-lookup"><span data-stu-id="be3d4-183">0</span></span>                                                                                                                 |



 

<span data-ttu-id="be3d4-184">Estados de estágio de textura:</span><span class="sxs-lookup"><span data-stu-id="be3d4-184">Texture Stage States:</span></span>



| <span data-ttu-id="be3d4-185">Identificador de estágio</span><span class="sxs-lookup"><span data-stu-id="be3d4-185">Stage Identifier</span></span> | <span data-ttu-id="be3d4-186">Tipo ([**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md))</span><span class="sxs-lookup"><span data-stu-id="be3d4-186">Type ([**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md))</span></span> | <span data-ttu-id="be3d4-187">Valor</span><span class="sxs-lookup"><span data-stu-id="be3d4-187">Value</span></span>            |
|------------------|---------------------------------------------------------------------------|------------------|
| <span data-ttu-id="be3d4-188">0</span><span class="sxs-lookup"><span data-stu-id="be3d4-188">0</span></span>                | <span data-ttu-id="be3d4-189">D3DTSS \_ ALPHAARG1</span><span class="sxs-lookup"><span data-stu-id="be3d4-189">D3DTSS\_ALPHAARG1</span></span>                                                         | <span data-ttu-id="be3d4-190">\_Textura D3DTA</span><span class="sxs-lookup"><span data-stu-id="be3d4-190">D3DTA\_TEXTURE</span></span>   |
| <span data-ttu-id="be3d4-191">0</span><span class="sxs-lookup"><span data-stu-id="be3d4-191">0</span></span>                | <span data-ttu-id="be3d4-192">D3DTSS \_ ALPHAARG2</span><span class="sxs-lookup"><span data-stu-id="be3d4-192">D3DTSS\_ALPHAARG2</span></span>                                                         | <span data-ttu-id="be3d4-193">D3DTA \_ difuso</span><span class="sxs-lookup"><span data-stu-id="be3d4-193">D3DTA\_DIFFUSE</span></span>   |
| <span data-ttu-id="be3d4-194">0</span><span class="sxs-lookup"><span data-stu-id="be3d4-194">0</span></span>                | <span data-ttu-id="be3d4-195">D3DTSS \_ ALPHAOP</span><span class="sxs-lookup"><span data-stu-id="be3d4-195">D3DTSS\_ALPHAOP</span></span>                                                           | <span data-ttu-id="be3d4-196">\_Modular D3DTOP</span><span class="sxs-lookup"><span data-stu-id="be3d4-196">D3DTOP\_MODULATE</span></span> |
| <span data-ttu-id="be3d4-197">0</span><span class="sxs-lookup"><span data-stu-id="be3d4-197">0</span></span>                | <span data-ttu-id="be3d4-198">D3DTSS \_ COLORARG1</span><span class="sxs-lookup"><span data-stu-id="be3d4-198">D3DTSS\_COLORARG1</span></span>                                                         | <span data-ttu-id="be3d4-199">\_Textura D3DTA</span><span class="sxs-lookup"><span data-stu-id="be3d4-199">D3DTA\_TEXTURE</span></span>   |
| <span data-ttu-id="be3d4-200">0</span><span class="sxs-lookup"><span data-stu-id="be3d4-200">0</span></span>                | <span data-ttu-id="be3d4-201">D3DTSS \_ COLORARG2</span><span class="sxs-lookup"><span data-stu-id="be3d4-201">D3DTSS\_COLORARG2</span></span>                                                         | <span data-ttu-id="be3d4-202">D3DTA \_ difuso</span><span class="sxs-lookup"><span data-stu-id="be3d4-202">D3DTA\_DIFFUSE</span></span>   |
| <span data-ttu-id="be3d4-203">0</span><span class="sxs-lookup"><span data-stu-id="be3d4-203">0</span></span>                | <span data-ttu-id="be3d4-204">D3DTSS \_ COLOROP</span><span class="sxs-lookup"><span data-stu-id="be3d4-204">D3DTSS\_COLOROP</span></span>                                                           | <span data-ttu-id="be3d4-205">\_Modular D3DTOP</span><span class="sxs-lookup"><span data-stu-id="be3d4-205">D3DTOP\_MODULATE</span></span> |
| <span data-ttu-id="be3d4-206">0</span><span class="sxs-lookup"><span data-stu-id="be3d4-206">0</span></span>                | <span data-ttu-id="be3d4-207">D3DTSS \_ TEXCOORDINDEX</span><span class="sxs-lookup"><span data-stu-id="be3d4-207">D3DTSS\_TEXCOORDINDEX</span></span>                                                     | <span data-ttu-id="be3d4-208">0</span><span class="sxs-lookup"><span data-stu-id="be3d4-208">0</span></span>                |
| <span data-ttu-id="be3d4-209">0</span><span class="sxs-lookup"><span data-stu-id="be3d4-209">0</span></span>                | <span data-ttu-id="be3d4-210">D3DTSS \_ TEXTURETRANSFORMFLAGS</span><span class="sxs-lookup"><span data-stu-id="be3d4-210">D3DTSS\_TEXTURETRANSFORMFLAGS</span></span>                                             | <span data-ttu-id="be3d4-211">D3DTTFF \_ desabilitar</span><span class="sxs-lookup"><span data-stu-id="be3d4-211">D3DTTFF\_DISABLE</span></span> |
| <span data-ttu-id="be3d4-212">1</span><span class="sxs-lookup"><span data-stu-id="be3d4-212">1</span></span>                | <span data-ttu-id="be3d4-213">D3DTSS \_ ALPHAOP</span><span class="sxs-lookup"><span data-stu-id="be3d4-213">D3DTSS\_ALPHAOP</span></span>                                                           | <span data-ttu-id="be3d4-214">D3DTOP \_ desabilitar</span><span class="sxs-lookup"><span data-stu-id="be3d4-214">D3DTOP\_DISABLE</span></span>  |
| <span data-ttu-id="be3d4-215">1</span><span class="sxs-lookup"><span data-stu-id="be3d4-215">1</span></span>                | <span data-ttu-id="be3d4-216">D3DTSS \_ COLOROP</span><span class="sxs-lookup"><span data-stu-id="be3d4-216">D3DTSS\_COLOROP</span></span>                                                           | <span data-ttu-id="be3d4-217">D3DTOP \_ desabilitar</span><span class="sxs-lookup"><span data-stu-id="be3d4-217">D3DTOP\_DISABLE</span></span>  |



 

<span data-ttu-id="be3d4-218">Estados de amostra:</span><span class="sxs-lookup"><span data-stu-id="be3d4-218">Sampler States:</span></span>



| <span data-ttu-id="be3d4-219">Índice de estágio de amostra</span><span class="sxs-lookup"><span data-stu-id="be3d4-219">Sampler Stage Index</span></span> | <span data-ttu-id="be3d4-220">Tipo ([**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md))</span><span class="sxs-lookup"><span data-stu-id="be3d4-220">Type ([**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md))</span></span> | <span data-ttu-id="be3d4-221">Valor</span><span class="sxs-lookup"><span data-stu-id="be3d4-221">Value</span></span>                                                                                                          |
|---------------------|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be3d4-222">0</span><span class="sxs-lookup"><span data-stu-id="be3d4-222">0</span></span>                   | <span data-ttu-id="be3d4-223">Endereço de D3DSAMP \_</span><span class="sxs-lookup"><span data-stu-id="be3d4-223">D3DSAMP\_ADDRESSU</span></span>                                               | <span data-ttu-id="be3d4-224">D3DTADDRESS \_ fixe</span><span class="sxs-lookup"><span data-stu-id="be3d4-224">D3DTADDRESS\_CLAMP</span></span>                                                                                             |
| <span data-ttu-id="be3d4-225">0</span><span class="sxs-lookup"><span data-stu-id="be3d4-225">0</span></span>                   | <span data-ttu-id="be3d4-226">D3DSAMP \_ ADDRESSV</span><span class="sxs-lookup"><span data-stu-id="be3d4-226">D3DSAMP\_ADDRESSV</span></span>                                               | <span data-ttu-id="be3d4-227">D3DTADDRESS \_ fixe</span><span class="sxs-lookup"><span data-stu-id="be3d4-227">D3DTADDRESS\_CLAMP</span></span>                                                                                             |
| <span data-ttu-id="be3d4-228">0</span><span class="sxs-lookup"><span data-stu-id="be3d4-228">0</span></span>                   | <span data-ttu-id="be3d4-229">D3DSAMP \_ MAGFILTER</span><span class="sxs-lookup"><span data-stu-id="be3d4-229">D3DSAMP\_MAGFILTER</span></span>                                              | <span data-ttu-id="be3d4-230">D3DTEXF \_ ANISOTROPIC se TextureFilterCaps incluir D3DPTFILTERCAPS \_ MAGFANISOTROPIC; caso contrário, D3DTEXF \_ linear</span><span class="sxs-lookup"><span data-stu-id="be3d4-230">D3DTEXF\_ANISOTROPIC if TextureFilterCaps includes D3DPTFILTERCAPS\_MAGFANISOTROPIC; otherwise D3DTEXF\_LINEAR</span></span> |
| <span data-ttu-id="be3d4-231">0</span><span class="sxs-lookup"><span data-stu-id="be3d4-231">0</span></span>                   | <span data-ttu-id="be3d4-232">D3DSAMP \_ MAXMIPLEVEL</span><span class="sxs-lookup"><span data-stu-id="be3d4-232">D3DSAMP\_MAXMIPLEVEL</span></span>                                            | <span data-ttu-id="be3d4-233">0</span><span class="sxs-lookup"><span data-stu-id="be3d4-233">0</span></span>                                                                                                              |
| <span data-ttu-id="be3d4-234">0</span><span class="sxs-lookup"><span data-stu-id="be3d4-234">0</span></span>                   | <span data-ttu-id="be3d4-235">D3DSAMP \_ MAXANISOTROPY</span><span class="sxs-lookup"><span data-stu-id="be3d4-235">D3DSAMP\_MAXANISOTROPY</span></span>                                          | <span data-ttu-id="be3d4-236">MaxAnisotropy</span><span class="sxs-lookup"><span data-stu-id="be3d4-236">MaxAnisotropy</span></span>                                                                                                  |
| <span data-ttu-id="be3d4-237">0</span><span class="sxs-lookup"><span data-stu-id="be3d4-237">0</span></span>                   | <span data-ttu-id="be3d4-238">D3DSAMP \_ MINFILTER</span><span class="sxs-lookup"><span data-stu-id="be3d4-238">D3DSAMP\_MINFILTER</span></span>                                              | <span data-ttu-id="be3d4-239">D3DTEXF \_ ANISOTROPIC se TextureFilterCaps incluir D3DPTFILTERCAPS \_ MINFANISOTROPIC; caso contrário, D3DTEXF \_ linear</span><span class="sxs-lookup"><span data-stu-id="be3d4-239">D3DTEXF\_ANISOTROPIC if TextureFilterCaps includes D3DPTFILTERCAPS\_MINFANISOTROPIC; otherwise D3DTEXF\_LINEAR</span></span> |
| <span data-ttu-id="be3d4-240">0</span><span class="sxs-lookup"><span data-stu-id="be3d4-240">0</span></span>                   | <span data-ttu-id="be3d4-241">D3DSAMP \_ MIPFILTER</span><span class="sxs-lookup"><span data-stu-id="be3d4-241">D3DSAMP\_MIPFILTER</span></span>                                              | <span data-ttu-id="be3d4-242">D3DTEXF \_ linear se TextureFilterCaps inclui D3DPTFILTERCAPS \_ MIPFLINEAR; caso contrário, D3DTEXF \_ ponto</span><span class="sxs-lookup"><span data-stu-id="be3d4-242">D3DTEXF\_LINEAR if TextureFilterCaps includes D3DPTFILTERCAPS\_MIPFLINEAR; otherwise D3DTEXF\_POINT</span></span>            |
| <span data-ttu-id="be3d4-243">0</span><span class="sxs-lookup"><span data-stu-id="be3d4-243">0</span></span>                   | <span data-ttu-id="be3d4-244">D3DSAMP \_ MIPMAPLODBIAS</span><span class="sxs-lookup"><span data-stu-id="be3d4-244">D3DSAMP\_MIPMAPLODBIAS</span></span>                                          | <span data-ttu-id="be3d4-245">0</span><span class="sxs-lookup"><span data-stu-id="be3d4-245">0</span></span>                                                                                                              |
| <span data-ttu-id="be3d4-246">0</span><span class="sxs-lookup"><span data-stu-id="be3d4-246">0</span></span>                   | <span data-ttu-id="be3d4-247">D3DSAMP \_ SRGBTEXTURE</span><span class="sxs-lookup"><span data-stu-id="be3d4-247">D3DSAMP\_SRGBTEXTURE</span></span>                                            | <span data-ttu-id="be3d4-248">0</span><span class="sxs-lookup"><span data-stu-id="be3d4-248">0</span></span>                                                                                                              |



 

> [!Note]  
> <span data-ttu-id="be3d4-249">Esse método desabilita N-patches.</span><span class="sxs-lookup"><span data-stu-id="be3d4-249">This method disables N-patches.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="be3d4-250">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be3d4-250">Requirements</span></span>



| <span data-ttu-id="be3d4-251">Requisito</span><span class="sxs-lookup"><span data-stu-id="be3d4-251">Requirement</span></span> | <span data-ttu-id="be3d4-252">Valor</span><span class="sxs-lookup"><span data-stu-id="be3d4-252">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="be3d4-253">parâmetro</span><span class="sxs-lookup"><span data-stu-id="be3d4-253">Header</span></span><br/>  | <dl> <span data-ttu-id="be3d4-254"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="be3d4-254"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="be3d4-255">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="be3d4-255">Library</span></span><br/> | <dl> <span data-ttu-id="be3d4-256"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="be3d4-256"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="be3d4-257">Confira também</span><span class="sxs-lookup"><span data-stu-id="be3d4-257">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be3d4-258">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="be3d4-258">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> <dt>

[<span data-ttu-id="be3d4-259">D3DXSPRITE</span><span class="sxs-lookup"><span data-stu-id="be3d4-259">D3DXSPRITE</span></span>](d3dxsprite.md)
</dt> </dl>

 

 
