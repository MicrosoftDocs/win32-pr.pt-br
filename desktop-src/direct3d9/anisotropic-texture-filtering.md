---
description: A distorção visível no texels de um objeto 3D cuja superfície é orientada a um ângulo em relação ao plano da tela é chamado de anisotropy.
ms.assetid: f6c8a9e2-aab0-4f06-956e-bb86557c72e7
title: Filtragem de textura anisotropic (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3443696e54410c6edc6a9998d4fcfd86b537a0e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457132"
---
# <a name="anisotropic-texture-filtering-direct3d-9"></a><span data-ttu-id="f1b52-103">Filtragem de textura anisotropic (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f1b52-103">Anisotropic Texture Filtering (Direct3D 9)</span></span>

<span data-ttu-id="f1b52-104">A distorção visível no texels de um objeto 3D cuja superfície é orientada a um ângulo em relação ao plano da tela é chamado de anisotropy.</span><span class="sxs-lookup"><span data-stu-id="f1b52-104">The distortion visible in the texels of a 3D object whose surface is oriented at an angle with respect to the plane of the screen is called anisotropy.</span></span> <span data-ttu-id="f1b52-105">Quando um pixel de uma primitiva anisotrópica é mapeado para texels, sua forma é distorcida.</span><span class="sxs-lookup"><span data-stu-id="f1b52-105">When a pixel from an anisotropic primitive is mapped to texels, its shape is distorted.</span></span> <span data-ttu-id="f1b52-106">O Direct3D mede a anisotropia de um pixel como o prolongamento - ou seja, comprimento dividido pela largura - de um pixel de tela é mapeado inverso no espaço de textura.</span><span class="sxs-lookup"><span data-stu-id="f1b52-106">Direct3D measures the anisotropy of a pixel as the elongation - that is, length divided by width - of a screen pixel that is inverse-mapped into texture space.</span></span>

<span data-ttu-id="f1b52-107">Você pode usar a filtragem de textura anisotrópica em conjunto com filtragem de textura linear ou a filtragem de textura mipmap para melhorar os resultados da renderização.</span><span class="sxs-lookup"><span data-stu-id="f1b52-107">You can use anisotropic texture filtering in conjunction with linear texture filtering or mipmap texture filtering to improve rendering results.</span></span> <span data-ttu-id="f1b52-108">Seu aplicativo permite a filtragem de textura anisotropic chamando o método [**IDirect3DDevice9:: Setsamplestate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) .</span><span class="sxs-lookup"><span data-stu-id="f1b52-108">Your application enables anisotropic texture filtering by calling the [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) method.</span></span> <span data-ttu-id="f1b52-109">Defina o valor do primeiro parâmetro como o número de índice inteiro (0-7) da textura para a qual você está selecionando um método de filtragem de textura.</span><span class="sxs-lookup"><span data-stu-id="f1b52-109">Set the value of the first parameter to the integer index number (0-7) of the texture for which you are selecting a texture filtering method.</span></span> <span data-ttu-id="f1b52-110">Pass D3DSAMP \_ MAGFILTER, D3DSAMP \_ MINFILTER ou D3DSAMP \_ MIPFILTER para o segundo parâmetro para definir o filtro de ampliação, minificação ou mipmapping.</span><span class="sxs-lookup"><span data-stu-id="f1b52-110">Pass D3DSAMP\_MAGFILTER, D3DSAMP\_MINFILTER, or D3DSAMP\_MIPFILTER for the second parameter to set the magnification, minification, or mipmapping filter.</span></span> <span data-ttu-id="f1b52-111">Defina o terceiro parâmetro como D3DTEXF \_ ANISOTROPIC.</span><span class="sxs-lookup"><span data-stu-id="f1b52-111">Set the third parameter to D3DTEXF\_ANISOTROPIC.</span></span>

<span data-ttu-id="f1b52-112">Seu aplicativo também deve definir o grau de anisotropy como um valor maior que um.</span><span class="sxs-lookup"><span data-stu-id="f1b52-112">Your application must also set the degree of anisotropy to a value greater than one.</span></span> <span data-ttu-id="f1b52-113">Faça isso chamando o método [**IDirect3DDevice9:: Setsamplestate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) .</span><span class="sxs-lookup"><span data-stu-id="f1b52-113">Do this by calling the [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) method.</span></span> <span data-ttu-id="f1b52-114">Defina o valor do primeiro parâmetro como o número de índice inteiro (0-7) da textura para a qual você está definindo o grau de isotropy.</span><span class="sxs-lookup"><span data-stu-id="f1b52-114">Set the value of the first parameter to the integer index number (0-7) of the texture for which you are setting the degree of isotropy.</span></span> <span data-ttu-id="f1b52-115">Passe D3DSAMP \_ MAXANISOTROPY como o valor do segundo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="f1b52-115">Pass D3DSAMP\_MAXANISOTROPY as the value of the second parameter.</span></span> <span data-ttu-id="f1b52-116">O parâmetro final deve ser o grau de isotropy.</span><span class="sxs-lookup"><span data-stu-id="f1b52-116">The final parameter should be the degree of isotropy.</span></span>

<span data-ttu-id="f1b52-117">Você pode desabilitar a filtragem de isotropic definindo o grau de isotropy como um; qualquer valor maior que um o habilita.</span><span class="sxs-lookup"><span data-stu-id="f1b52-117">You can disable isotropic filtering by setting the degree of isotropy to one; any value larger than one enables it.</span></span> <span data-ttu-id="f1b52-118">Verifique o sinalizador MaxAnisotropy na estrutura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) para determinar o intervalo de valores possível para o grau de anisotropy.</span><span class="sxs-lookup"><span data-stu-id="f1b52-118">Check the MaxAnisotropy flag in the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure to determine the possible range of values for the degree of anisotropy.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f1b52-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f1b52-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1b52-120">Filtragem de textura</span><span class="sxs-lookup"><span data-stu-id="f1b52-120">Texture Filtering</span></span>](texture-filtering.md)
</dt> </dl>

 

 
