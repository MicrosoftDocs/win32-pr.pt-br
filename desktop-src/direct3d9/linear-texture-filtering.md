---
description: O Direct3D usa uma forma de filtragem de textura linear chamada filtragem biline.
ms.assetid: vs|directx_sdk|~\linear_texture_filtering.htm
title: Filtragem de textura linear (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7940bd693ec42ef4f48920a5a362fad5f5b0bf02
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500519"
---
# <a name="linear-texture-filtering-direct3d-9"></a><span data-ttu-id="025cb-103">Filtragem de textura linear (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="025cb-103">Linear Texture Filtering (Direct3D 9)</span></span>

<span data-ttu-id="025cb-104">O Direct3D usa uma forma de filtragem de textura linear chamada filtragem biline.</span><span class="sxs-lookup"><span data-stu-id="025cb-104">Direct3D uses a form of linear texture filtering called bilinear filtering.</span></span> <span data-ttu-id="025cb-105">Assim como a [amostragem de ponto mais próximo (Direct3D 9)](nearest-point-sampling.md), a filtragem de textura bilinear primeiro computa um endereço Texel, que geralmente não é um endereço inteiro.</span><span class="sxs-lookup"><span data-stu-id="025cb-105">Like [Nearest-Point Sampling (Direct3D 9)](nearest-point-sampling.md), bilinear texture filtering first computes a texel address, which is usually not an integer address.</span></span> <span data-ttu-id="025cb-106">A filtragem bilinear localiza o Texel cujo endereço de inteiro é mais próximo do endereço computado.</span><span class="sxs-lookup"><span data-stu-id="025cb-106">Bilinear filtering then finds the texel whose integer address is closest to the computed address.</span></span> <span data-ttu-id="025cb-107">Além disso, o módulo de renderização do Direct3D computa uma média ponderada dos texels que estão imediatamente acima, abaixo, à esquerda de e à direita do ponto de exemplo mais próximo.</span><span class="sxs-lookup"><span data-stu-id="025cb-107">In addition, the Direct3D rendering module computes a weighted average of the texels that are immediately above, below, to the left of, and to the right of the nearest sample point.</span></span>

<span data-ttu-id="025cb-108">Selecione filtragem de textura bilinear invocando o método [**IDirect3DDevice9:: Setsamplestate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) .</span><span class="sxs-lookup"><span data-stu-id="025cb-108">Select bilinear texture filtering by invoking the [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) method.</span></span> <span data-ttu-id="025cb-109">Defina o valor do primeiro parâmetro como o número de índice inteiro (0-7) da textura para a qual você está selecionando um método de filtragem de textura.</span><span class="sxs-lookup"><span data-stu-id="025cb-109">Set the value of the first parameter to the integer index number (0-7) of the texture for which you are selecting a texture filtering method.</span></span> <span data-ttu-id="025cb-110">Pass D3DSAMP \_ MAGFILTER, D3DSAMP \_ MINFILTER ou D3DSAMP \_ MIPFILTER para o segundo parâmetro para definir o filtro de ampliação, minificação ou mipmapping.</span><span class="sxs-lookup"><span data-stu-id="025cb-110">Pass D3DSAMP\_MAGFILTER, D3DSAMP\_MINFILTER, or D3DSAMP\_MIPFILTER for the second parameter to set the magnification, minification, or mipmapping filter.</span></span> <span data-ttu-id="025cb-111">Passe D3DTEXF \_ linear no terceiro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="025cb-111">Pass D3DTEXF\_LINEAR in the third parameter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="025cb-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="025cb-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="025cb-113">Filtragem de textura</span><span class="sxs-lookup"><span data-stu-id="025cb-113">Texture Filtering</span></span>](texture-filtering.md)
</dt> </dl>

 

 
