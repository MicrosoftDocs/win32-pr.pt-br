---
description: O anti-aliasing em cena completa se refere a desfocar as bordas de cada polígono na cena, já que ela é rasterizada em uma única passagem; Não é necessária uma segunda passagem.
ms.assetid: b57974ab-5654-412d-ae59-58f67a88c121
title: Anti-aliasing Full-Scene (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d73d559c4b4fec060efbff7468ee29e6c83b64c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500265"
---
# <a name="full-scene-antialiasing-direct3d-9"></a><span data-ttu-id="6b1de-103">Anti-aliasing Full-Scene (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="6b1de-103">Full-Scene Antialiasing (Direct3D 9)</span></span>

<span data-ttu-id="6b1de-104">O anti-aliasing em cena completa se refere a desfocar as bordas de cada polígono na cena, já que ela é rasterizada em uma única passagem; Não é necessária uma segunda passagem.</span><span class="sxs-lookup"><span data-stu-id="6b1de-104">Full-scene antialiasing refers to blurring the edges of each polygon in the scene as it is rasterized in a single pass; no second pass is required.</span></span> <span data-ttu-id="6b1de-105">A suavização completa da cena, quando há suporte, afeta apenas os triângulos e os grupos de triângulos.</span><span class="sxs-lookup"><span data-stu-id="6b1de-105">Full-scene antialiasing, when supported, affects only triangles and groups of triangles.</span></span> <span data-ttu-id="6b1de-106">Não é possível suavizar as linhas usando os serviços do Direct3D.</span><span class="sxs-lookup"><span data-stu-id="6b1de-106">Lines cannot be antialiased by using Direct3D services.</span></span> <span data-ttu-id="6b1de-107">A suavização completa da cena é feita no Direct3D usando a multiamostragem em cada pixel.</span><span class="sxs-lookup"><span data-stu-id="6b1de-107">Full-scene antialiasing is done in Direct3D by using multisampling on each pixel.</span></span> <span data-ttu-id="6b1de-108">Quando a multiamostragem está habilitada, todas as subamostras de um pixel são atualizadas em uma passagem, mas quando usadas para outros efeitos que envolvem várias passagens de renderização, o aplicativo pode especificar que apenas alguns subamostras serão afetados por uma determinada passagem de renderização.</span><span class="sxs-lookup"><span data-stu-id="6b1de-108">When multisampling is enabled, all subsamples of a pixel are updated in one pass but when used for other effects that involve multiple rendering passes, the application can specify that only some subsamples are to be affected by a given rendering pass.</span></span> <span data-ttu-id="6b1de-109">Essa última abordagem habilita a simulação de desfoque de movimento, efeitos de foco de profundidade de campo, Desfoque de reflexo e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="6b1de-109">This latter approach enables simulation of motion blur, depth-of-field focus effects, reflection blur, and so on.</span></span>

<span data-ttu-id="6b1de-110">Em ambos os casos, os vários exemplos registrados para cada pixel são mesclados e são impressos na tela.</span><span class="sxs-lookup"><span data-stu-id="6b1de-110">In both cases, the various samples recorded for each pixel are blended together and output to the screen.</span></span> <span data-ttu-id="6b1de-111">Isso permite a qualidade de imagem aprimorada de anti-aliasing ou outros efeitos.</span><span class="sxs-lookup"><span data-stu-id="6b1de-111">This enables the improved image quality of antialiasing or other effects.</span></span>

<span data-ttu-id="6b1de-112">Antes de criar um dispositivo com o método [**IDirect3D9:: CreateDevice**](/windows/desktop/api) , você precisa determinar se há suporte para anti-aliasing na cena completa.</span><span class="sxs-lookup"><span data-stu-id="6b1de-112">Before creating a device with the [**IDirect3D9::CreateDevice**](/windows/desktop/api) method, you need to determine if full-scene antialiasing is supported.</span></span> <span data-ttu-id="6b1de-113">Faça isso chamando o método [**IDirect3D9:: CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) , conforme mostrado no exemplo de código abaixo.</span><span class="sxs-lookup"><span data-stu-id="6b1de-113">Do this by calling the [**IDirect3D9::CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) method as shown in the code example below.</span></span>


```
/*
* The code below assumes that pD3D is a valid pointer 
*   to a IDirect3D9 interface.
*/

if( SUCCEEDED(pD3D->CheckDeviceMultiSampleType( D3DADAPTER_DEFAULT, 
                    D3DDEVTYPE_HAL , D3DFMT_R8G8B8, FALSE, 
                    D3DMULTISAMPLE_2_SAMPLES, NULL ) ) )
// Full-scene antialiasing is supported. Enable it here.
```



<span data-ttu-id="6b1de-114">O primeiro parâmetro que [**IDirect3D9:: CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) aceita é um número ordinal que denota o adaptador de vídeo a ser consultado.</span><span class="sxs-lookup"><span data-stu-id="6b1de-114">The first parameter that [**IDirect3D9::CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) accepts is an ordinal number that denotes the display adapter to query.</span></span> <span data-ttu-id="6b1de-115">Este exemplo usa D3DADAPTER \_ padrão para especificar o adaptador de vídeo primário.</span><span class="sxs-lookup"><span data-stu-id="6b1de-115">This sample uses D3DADAPTER\_DEFAULT to specify the primary display adapter.</span></span> <span data-ttu-id="6b1de-116">O segundo parâmetro é um valor do tipo enumerado [**D3DDEVTYPE**](./d3ddevtype.md) , especificando o tipo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6b1de-116">The second parameter is a value from the [**D3DDEVTYPE**](./d3ddevtype.md) enumerated type, specifying the device type.</span></span> <span data-ttu-id="6b1de-117">O terceiro parâmetro especifica o formato da superfície.</span><span class="sxs-lookup"><span data-stu-id="6b1de-117">The third parameter specifies the format of the surface.</span></span> <span data-ttu-id="6b1de-118">O quarto parâmetro informa ao Direct3D se deve ser consultado sobre a multiamostragem completa (**true**) ou a anti-aliasing na cena completa (**false**).</span><span class="sxs-lookup"><span data-stu-id="6b1de-118">The fourth parameter tells Direct3D whether to inquire about full-windowed multisampling (**TRUE**) or full-scene antialiasing (**FALSE**).</span></span> <span data-ttu-id="6b1de-119">Este exemplo usa **false** para informar ao Direct3D que ele está consultando a anti-aliasing na cena completa.</span><span class="sxs-lookup"><span data-stu-id="6b1de-119">This sample uses **FALSE** to tell Direct3D that it is inquiring about full-scene antialiasing.</span></span> <span data-ttu-id="6b1de-120">O último parâmetro especifica a técnica de multiamostragem que você deseja testar.</span><span class="sxs-lookup"><span data-stu-id="6b1de-120">The last parameter specifies the multisampling technique that you want to test.</span></span> <span data-ttu-id="6b1de-121">Use um valor do tipo enumerado do [**\_ tipo D3DMULTISAMPLE**](./d3dmultisample-type.md) .</span><span class="sxs-lookup"><span data-stu-id="6b1de-121">Use a value from the [**D3DMULTISAMPLE\_TYPE**](./d3dmultisample-type.md) enumerated type.</span></span> <span data-ttu-id="6b1de-122">Este exemplo testa para ver se há suporte para dois níveis de multiamostragens.</span><span class="sxs-lookup"><span data-stu-id="6b1de-122">This sample tests to see if two levels of multisampling are supported.</span></span>

<span data-ttu-id="6b1de-123">Se o dispositivo der suporte ao nível de várias amostras que você deseja usar, a próxima etapa será definir os parâmetros de apresentação preenchendo os membros apropriados da estrutura [**de \_ parâmetros D3DPRESENT**](d3dpresent-parameters.md) para criar uma superfície de renderização de várias amostras.</span><span class="sxs-lookup"><span data-stu-id="6b1de-123">If the device supports the level of multisampling that you want to use, the next step is to set the presentation parameters by filling in the appropriate members of the [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md) structure to create a multisample rendering surface.</span></span> <span data-ttu-id="6b1de-124">Depois disso, você pode criar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6b1de-124">After that, you can create the device.</span></span> <span data-ttu-id="6b1de-125">O código de exemplo a seguir mostra como configurar um dispositivo com uma superfície de renderização de multiamostragem.</span><span class="sxs-lookup"><span data-stu-id="6b1de-125">The sample code below shows how to set up a device with a multisampling render surface.</span></span>


```
/*
* The example below assumes that pD3D is a valid pointer 
* to a IDirect3D9 interface, d3dDevice is a pointer to a 
* IDirect3DDevice9 interface, and hWnd is a valid handle
* to a window.
*/

D3DPRESENT_PARAMETER d3dPP
ZeroMemory( &d3dPP, sizeof( d3dPP ) );
d3dPP.Windowed        = FALSE
d3dPP.SwapEffect      = D3DSWAPEFFECT_DISCARD;
d3dPP.MultiSampleType = D3DMULTISAMPLE_2_SAMPLES;
pD3D->CreateDevice(D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                    D3DCREATE_SOFTWARE_VERTEXPROCESSING,
                    &d3dpp, &d3dDevice)
```



<span data-ttu-id="6b1de-126">Para usar a multiamostral, o membro SwapEffect do \_ parâmetro D3DPRESENT deve ser definido como \_ descartar D3DSWAPEFFECT.</span><span class="sxs-lookup"><span data-stu-id="6b1de-126">To use multisampling, the SwapEffect member of D3DPRESENT\_PARAMETER must be set to D3DSWAPEFFECT\_DISCARD.</span></span>

<span data-ttu-id="6b1de-127">A última etapa é habilitar a suavização de várias amostras chamando o método [**IDirect3DDevice9:: Setrenderingstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) e definindo D3DRS \_ MULTISAMPLEANTIALIAS como **true**.</span><span class="sxs-lookup"><span data-stu-id="6b1de-127">The last step is to enable multisampling antialiasing by calling the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method and setting the D3DRS\_MULTISAMPLEANTIALIAS to **TRUE**.</span></span> <span data-ttu-id="6b1de-128">Depois de definir esse valor como **true**, qualquer renderização que você fizer terá uma multiamostra aplicada a ele.</span><span class="sxs-lookup"><span data-stu-id="6b1de-128">After setting this value to **TRUE**, any rendering that you do will have multisampling applied to it.</span></span> <span data-ttu-id="6b1de-129">Talvez você queira habilitar e desabilitar a multiamostragem, dependendo do que está renderizando.</span><span class="sxs-lookup"><span data-stu-id="6b1de-129">You might want to enable and disable multisampling, depending on what you are rendering.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6b1de-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6b1de-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b1de-131">Suavização</span><span class="sxs-lookup"><span data-stu-id="6b1de-131">Antialiasing</span></span>](antialiasing.md)
</dt> </dl>

 

 
