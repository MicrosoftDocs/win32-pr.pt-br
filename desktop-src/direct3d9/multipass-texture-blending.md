---
description: Os apps Direct3D podem conseguir vários efeitos especiais ao aplicar diversas texturas a um primitivo durante múltiplas passagens de renderização.
ms.assetid: 884cc928-305e-46b9-acbf-ca58dfbc05e6
title: Mesclagem de textura de passagem (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df0a042088694f686003a6dc259cf1d914db2b59
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087590"
---
# <a name="multipass-texture-blending-direct3d-9"></a><span data-ttu-id="e6b3f-103">Mesclagem de textura de passagem (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="e6b3f-103">Multipass Texture Blending (Direct3D 9)</span></span>

<span data-ttu-id="e6b3f-104">Os apps Direct3D podem conseguir vários efeitos especiais ao aplicar diversas texturas a um primitivo durante múltiplas passagens de renderização.</span><span class="sxs-lookup"><span data-stu-id="e6b3f-104">Direct3D applications can achieve numerous special effects by applying various textures to a primitive over the course of multiple rendering passes.</span></span> <span data-ttu-id="e6b3f-105">O termo comum para isso é mesclagem de texturas de passagem múltipla.</span><span class="sxs-lookup"><span data-stu-id="e6b3f-105">The common term for this is multipass texture blending.</span></span> <span data-ttu-id="e6b3f-106">O uso típico da mesclagem de textura com passagens múltiplas é emular os efeitos de iluminação complexos e os modelos de sombreamento ao aplicar várias cores de diversas texturas diferentes.</span><span class="sxs-lookup"><span data-stu-id="e6b3f-106">A typical use for multipass texture blending is to emulate the effects of complex lighting and shading models by applying multiple colors from several different textures.</span></span> <span data-ttu-id="e6b3f-107">Uma dessas aplicações é chamada de mapeamento suave.</span><span class="sxs-lookup"><span data-stu-id="e6b3f-107">One such application is called light mapping.</span></span> <span data-ttu-id="e6b3f-108">Para obter mais informações, consulte [mapeamento claro com texturas (Direct3D 9)](light-mapping-with-textures.md).</span><span class="sxs-lookup"><span data-stu-id="e6b3f-108">For more information, see [Light Mapping with Textures (Direct3D 9)](light-mapping-with-textures.md).</span></span>

> [!Note]  
> <span data-ttu-id="e6b3f-109">Alguns dispositivos são capazes de aplicar várias texturas a primitivos em uma única passagem.</span><span class="sxs-lookup"><span data-stu-id="e6b3f-109">Some devices are capable of applying multiple textures to primitives in a single pass.</span></span> <span data-ttu-id="e6b3f-110">Para obter detalhes, consulte [mesclagem de textura (Direct3D 9)](texture-blending.md).</span><span class="sxs-lookup"><span data-stu-id="e6b3f-110">For details, see [Texture Blending (Direct3D 9)](texture-blending.md).</span></span>

 

<span data-ttu-id="e6b3f-111">Se o hardware do usuário não oferecer suporte à mistura de textura múltipla, o app pode usar a mistura de textura com passagem múltipla para obter os mesmo efeitos visuais.</span><span class="sxs-lookup"><span data-stu-id="e6b3f-111">If the user's hardware does not support multiple texture blending, your application can use multipass texture blending to achieve the same visual effects.</span></span> <span data-ttu-id="e6b3f-112">No entanto, o app não pode manter as taxas de quadros que são possíveis ao usar a mistura de textura múltipla.</span><span class="sxs-lookup"><span data-stu-id="e6b3f-112">However, the application cannot sustain the frame rates that are possible when using multiple texture blending.</span></span>

<span data-ttu-id="e6b3f-113">Para executar a mesclagem de textura de passagem em um aplicativo C/C++.</span><span class="sxs-lookup"><span data-stu-id="e6b3f-113">To perform multipass texture blending in a C/C++ application.</span></span>

1.  <span data-ttu-id="e6b3f-114">Defina uma textura no estágio de textura 0 chamando o método [**IDirect3DDevice9:: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) .</span><span class="sxs-lookup"><span data-stu-id="e6b3f-114">Set a texture in texture stage 0 by calling the [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) method.</span></span>
2.  <span data-ttu-id="e6b3f-115">Selecione a cor desejada e os argumentos de mesclagem alfa e as operações com o método [**IDirect3DDevice9:: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) .</span><span class="sxs-lookup"><span data-stu-id="e6b3f-115">Select the desired color and alpha blending arguments and operations with the [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) method.</span></span> <span data-ttu-id="e6b3f-116">As configurações padrão são adequadas para a mistura de textura com passagem múltipla.</span><span class="sxs-lookup"><span data-stu-id="e6b3f-116">The default settings are well-suited for multipass texture blending.</span></span>
3.  <span data-ttu-id="e6b3f-117">Renderize os objetos adequados na cena.</span><span class="sxs-lookup"><span data-stu-id="e6b3f-117">Render the appropriate objects in the scene.</span></span>
4.  <span data-ttu-id="e6b3f-118">Defina a textura seguinte no estágio de textura 0.</span><span class="sxs-lookup"><span data-stu-id="e6b3f-118">Set the next texture in texture stage 0.</span></span>
5.  <span data-ttu-id="e6b3f-119">Defina os \_ Estados de RENDERIZAÇÃO D3DRS SRCBLEND e D3DRS \_ DESTBLEND para ajustar os fatores de mesclagem de origem e destino, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="e6b3f-119">Set the D3DRS\_SRCBLEND and D3DRS\_DESTBLEND render states to adjust the source and destination blending factors as needed.</span></span> <span data-ttu-id="e6b3f-120">O sistema combina as novas texturas aos pixels existentes na superfície de destino de renderização de acordo com esses parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e6b3f-120">The system blends the new textures with the existing pixels in the render-target surface according to these parameters.</span></span>
6.  <span data-ttu-id="e6b3f-121">Repita as etapas 3, 4 e 5 com a quantidade de texturas necessária.</span><span class="sxs-lookup"><span data-stu-id="e6b3f-121">Repeat Steps 3, 4, and 5 with as many textures as needed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e6b3f-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e6b3f-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6b3f-123">Mesclagem de textura</span><span class="sxs-lookup"><span data-stu-id="e6b3f-123">Texture Blending</span></span>](texture-blending.md)
</dt> </dl>

 

 
