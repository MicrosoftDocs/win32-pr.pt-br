---
description: Os destinos de renderização múltipla (MRT) referem-se à capacidade de renderização em várias superfícies (consulte IDirect3D9Surface) com uma única chamada de desenho.
ms.assetid: ae48c5ce-b7f5-4189-8b04-880836be3fe0
title: Vários destinos de renderização (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bb7aafeedb621e43abb288eb9bbceb17ddb0cc0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456706"
---
# <a name="multiple-render-targets-direct3d-9"></a><span data-ttu-id="d6307-103">Vários destinos de renderização (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d6307-103">Multiple Render Targets (Direct3D 9)</span></span>

<span data-ttu-id="d6307-104">Os destinos de renderização múltipla (MRT) referem-se à capacidade de renderização em várias superfícies (consulte [**IDirect3D9Surface**](/windows/desktop/api)) com uma única chamada de desenho.</span><span class="sxs-lookup"><span data-stu-id="d6307-104">Multiple Render Targets (MRT) refers to the ability to render to multiple surfaces (see [**IDirect3D9Surface**](/windows/desktop/api)) with a single draw call.</span></span> <span data-ttu-id="d6307-105">Essas superfícies podem ser criadas independentemente uma da outra.</span><span class="sxs-lookup"><span data-stu-id="d6307-105">These surfaces can be created independently of each other.</span></span> <span data-ttu-id="d6307-106">Os destinos de renderização podem ser definidos usando [**IDirect3DDevice9:: SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget).</span><span class="sxs-lookup"><span data-stu-id="d6307-106">Render targets can be set using [**IDirect3DDevice9::SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget).</span></span>

<span data-ttu-id="d6307-107">Vários destinos de renderização têm as seguintes restrições:</span><span class="sxs-lookup"><span data-stu-id="d6307-107">Multiple render targets have the following restrictions:</span></span>

-   <span data-ttu-id="d6307-108">Todas as superfícies de destino de renderização usadas juntas devem ter a mesma profundidade de bits, mas podem ser de formatos diferentes, a menos que o \_ limite de MRTINDEPENDENTBITDEPTHS D3DPMISCCAPS seja definido.</span><span class="sxs-lookup"><span data-stu-id="d6307-108">All render target surfaces used together must have the same bit depth but can be of different formats, unless the D3DPMISCCAPS\_MRTINDEPENDENTBITDEPTHS cap is set.</span></span>
-   <span data-ttu-id="d6307-109">Todas as superfícies de um destino de processamento múltiplo devem ter a mesma largura e altura.</span><span class="sxs-lookup"><span data-stu-id="d6307-109">All surfaces of a multiple render target should have the same width and height.</span></span>
-   <span data-ttu-id="d6307-110">Algumas implementações não podem executar operações de sombreador pós-pixel em vários destinos de renderização, incluindo: sem pontilhamento, teste alfa, sem fogging, sem mesclagem ou mascaramento, exceto o teste de z e de estêncil.</span><span class="sxs-lookup"><span data-stu-id="d6307-110">Some implementations cannot perform post-pixel shader operations on multiple render targets, including: no dithering, alpha test, no fogging, no blending or masking, except the z-test and stencil test.</span></span> <span data-ttu-id="d6307-111">Dispositivos que podem dar suporte a operações de sombreador após pixel definem o bit de extremidade como D3DPMISCCAPS \_ MRTPOSTPIXELSHADERBLENDING.</span><span class="sxs-lookup"><span data-stu-id="d6307-111">Devices that can support post-pixel shader operations set the cap bit to D3DPMISCCAPS\_MRTPOSTPIXELSHADERBLENDING.</span></span>

    <span data-ttu-id="d6307-112">Quando o \_ limite de MRTPOSTPIXELSHADERBLENDING D3DPMISCCAPS é definido, você deve primeiro consultar o [**IDirect3D9:: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) com o \_ resultado de \_ mesclagem POSTPIXELSHADER de consulta de uso \_ para o formato de superfície específico.</span><span class="sxs-lookup"><span data-stu-id="d6307-112">When the D3DPMISCCAPS\_MRTPOSTPIXELSHADERBLENDING cap is set, you must first consult the [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) with the USAGE\_QUERY\_POSTPIXELSHADER\_BLENDING result for the specific surface format.</span></span> <span data-ttu-id="d6307-113">Se for false, nenhuma operação de mesclagem de sombreador após pixel estará disponível para esse formato de superfície específico.</span><span class="sxs-lookup"><span data-stu-id="d6307-113">If false, no post-pixel shader blending operations will be available for that specific surface format.</span></span> <span data-ttu-id="d6307-114">Se for true, o dispositivo deverá aplicar o mesmo estado a todos os destinos de renderização simultâneos da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="d6307-114">If true, the device is expected to apply the same state to all simultaneous render targets as follows:</span></span>

    -   <span data-ttu-id="d6307-115">Mistura alfa: o valor de cor em oCi é combinado com o destino de renderização i.</span><span class="sxs-lookup"><span data-stu-id="d6307-115">Alpha blend: The color value in oCi is blended with the ith render target.</span></span>
    -   <span data-ttu-id="d6307-116">Teste alfa: a comparação ocorrerá com oC0.</span><span class="sxs-lookup"><span data-stu-id="d6307-116">Alpha test: Comparison will happen with oC0.</span></span> <span data-ttu-id="d6307-117">Se a comparação falhar, o teste de pixel será encerrado para todos os destinos de renderização.</span><span class="sxs-lookup"><span data-stu-id="d6307-117">If the comparison fails, the pixel test is terminated for all render targets.</span></span>
    -   <span data-ttu-id="d6307-118">Neblina: o destino de renderização 0 receberá fogged.</span><span class="sxs-lookup"><span data-stu-id="d6307-118">Fog: Render target 0 will get fogged.</span></span> <span data-ttu-id="d6307-119">Outros destinos de renderização são indefinidos.</span><span class="sxs-lookup"><span data-stu-id="d6307-119">Other render targets are undefined.</span></span> <span data-ttu-id="d6307-120">As implementações podem optar por fazer a sombra de todas elas usando o mesmo estado.</span><span class="sxs-lookup"><span data-stu-id="d6307-120">Implementations can choose to fog them all using the same state.</span></span>
    -   <span data-ttu-id="d6307-121">Pontilhamento: indefinido.</span><span class="sxs-lookup"><span data-stu-id="d6307-121">Dithering: Undefined.</span></span>

-   <span data-ttu-id="d6307-122">Não há suporte para anti-aliasing.</span><span class="sxs-lookup"><span data-stu-id="d6307-122">No antialiasing is supported.</span></span>
-   <span data-ttu-id="d6307-123">Algumas das implementações não aplicam a máscara de gravação de saída (D3DRS \_ COLORWRITEENABLE).</span><span class="sxs-lookup"><span data-stu-id="d6307-123">Some of the implementations do not apply the output write mask (D3DRS\_COLORWRITEENABLE).</span></span> <span data-ttu-id="d6307-124">Os que podem ter máscaras de gravação de cores independentes.</span><span class="sxs-lookup"><span data-stu-id="d6307-124">Those that can, have independent color write masks.</span></span> <span data-ttu-id="d6307-125">Isso é expresso usando um novo bit de recurso.</span><span class="sxs-lookup"><span data-stu-id="d6307-125">This is expressed using a new capability bit.</span></span> <span data-ttu-id="d6307-126">O número de máscaras de gravação de cor independentes disponíveis será igual ao número máximo de elementos que o dispositivo é capaz de.</span><span class="sxs-lookup"><span data-stu-id="d6307-126">The number of independent color write masks available will be equal to the maximum number of elements the device is capable of.</span></span>

<span data-ttu-id="d6307-127">Novos limites de hardware:</span><span class="sxs-lookup"><span data-stu-id="d6307-127">New hardware caps:</span></span>


```
D3DCAPS9.NumSimultaneousRTs         
// The value is 1 for all hardware except those that  
//   can support this feature. It is never 0.
D3DPMISCCAPS_MRTINDEPENDENTBITDEPTHS - True if the hardware can support it
D3DPMISCCAPS_MRTPOSTPIXELSHADERBLENDING - True if the hardware can support it
```



## <a name="related-topics"></a><span data-ttu-id="d6307-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d6307-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6307-129">Pipeline de pixel</span><span class="sxs-lookup"><span data-stu-id="d6307-129">Pixel Pipeline</span></span>](pixel-pipeline.md)
</dt> </dl>

 

 
