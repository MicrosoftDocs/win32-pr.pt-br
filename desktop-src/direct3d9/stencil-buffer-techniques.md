---
description: Os aplicativos usam o buffer de estêncil para mascarar pixels em uma imagem. A máscara controla se o pixel é desenhado ou não. Alguns dos efeitos mais comuns são mostrados abaixo.
ms.assetid: 984f0a98-4a74-44c3-a9d0-f5d3f12f7e4e
title: Técnicas de buffer de estêncil (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c2dcc05475a3ddfc13e456faf60ec2d11e271a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370332"
---
# <a name="stencil-buffer-techniques-direct3d-9"></a><span data-ttu-id="9120c-105">Técnicas de buffer de estêncil (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="9120c-105">Stencil Buffer Techniques (Direct3D 9)</span></span>

<span data-ttu-id="9120c-106">Os aplicativos usam o buffer de estêncil para mascarar pixels em uma imagem.</span><span class="sxs-lookup"><span data-stu-id="9120c-106">Applications use the stencil buffer to mask pixels in an image.</span></span> <span data-ttu-id="9120c-107">A máscara controla se o pixel é desenhado ou não.</span><span class="sxs-lookup"><span data-stu-id="9120c-107">The mask controls whether the pixel is drawn or not.</span></span> <span data-ttu-id="9120c-108">Alguns dos efeitos mais comuns são mostrados abaixo.</span><span class="sxs-lookup"><span data-stu-id="9120c-108">Some of the more common effects are shown below.</span></span>

-   [<span data-ttu-id="9120c-109">Composição</span><span class="sxs-lookup"><span data-stu-id="9120c-109">Compositing</span></span>](compositing.md)
-   [<span data-ttu-id="9120c-110">Decaling</span><span class="sxs-lookup"><span data-stu-id="9120c-110">Decaling</span></span>](decaling.md)
-   [<span data-ttu-id="9120c-111">Dessolucionar, esmaecer e passar o dedo</span><span class="sxs-lookup"><span data-stu-id="9120c-111">Dissolves, Fades, and Swipes</span></span>](dissolves--fades--and-swipes.md)
-   [<span data-ttu-id="9120c-112">Contornos e silhuetas</span><span class="sxs-lookup"><span data-stu-id="9120c-112">Outlines and Silhouettes</span></span>](outlines-and-silhouettes.md)
-   [<span data-ttu-id="9120c-113">Estêncil de duas pontas</span><span class="sxs-lookup"><span data-stu-id="9120c-113">Two-Sided Stencil</span></span>](two-sided-stencil.md)

<span data-ttu-id="9120c-114">O buffer de estêncil habilita ou desabilita o desenho na superfície de destino de renderização em uma base de pixel por pixel.</span><span class="sxs-lookup"><span data-stu-id="9120c-114">The stencil buffer enables or disables drawing to the rendering target surface on a pixel-by-pixel basis.</span></span> <span data-ttu-id="9120c-115">No nível mais fundamental, ele permite que aplicativos mascarem seções da imagem renderizada para que elas não sejam exibidas.</span><span class="sxs-lookup"><span data-stu-id="9120c-115">At its most fundamental level, it enables applications to mask sections of the rendered image so that they are not displayed.</span></span> <span data-ttu-id="9120c-116">Aplicativos geralmente usam buffers de estêncil de efeitos especiais, como desintegração, decalque e contorno.</span><span class="sxs-lookup"><span data-stu-id="9120c-116">Applications often use stencil buffers for special effects such as dissolves, decaling, and outlining.</span></span>

<span data-ttu-id="9120c-117">Informações de buffer de estêncil são incorporadas nos dados do buffer z.</span><span class="sxs-lookup"><span data-stu-id="9120c-117">Stencil buffer information is embedded in the z-buffer data.</span></span> <span data-ttu-id="9120c-118">Seu aplicativo pode usar o método [**IDirect3D9:: CheckDeviceFormat**](/windows/desktop/api) para verificar o suporte ao estêncil de hardware, conforme mostrado no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="9120c-118">Your application can use the [**IDirect3D9::CheckDeviceFormat**](/windows/desktop/api) method to check for hardware stencil support, as shown in the following code example.</span></span>


```
// Reject devices that cannot perform 8-bit stencil buffering. 
// The following example assumes that pCaps is a valid pointer 
// to an initialized D3DCAPS9 structure. 

if( FAILED( m_pD3D->CheckDeviceFormat( pCaps->AdapterOrdinal,
                                       pCaps->DeviceType,  
                                       Format,  
                                       D3DUSAGE_DEPTHSTENCIL, 
                                       D3DRTYPE_SURFACE,
                                       D3DFMT_D24S8 ) ) )
return E_FAIL;
```



<span data-ttu-id="9120c-119">[**IDirect3D9:: CheckDeviceFormat**](/windows/desktop/api) permite que você escolha um dispositivo para criar com base nos recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9120c-119">[**IDirect3D9::CheckDeviceFormat**](/windows/desktop/api) allows you to choose a device to create based on the capabilities of that device.</span></span> <span data-ttu-id="9120c-120">Nesse caso, os dispositivos que não dão suporte a buffers de estêncil de 8 bits são rejeitados.</span><span class="sxs-lookup"><span data-stu-id="9120c-120">In this case, devices that do not support 8-bit stencil buffers are rejected.</span></span> <span data-ttu-id="9120c-121">Observe que esse é apenas um possível uso para **IDirect3D9:: CheckDeviceFormat**; para obter detalhes, consulte [determinando o suporte de hardware (Direct3D 9)](determining-hardware-support.md).</span><span class="sxs-lookup"><span data-stu-id="9120c-121">Note that this is only one possible use for **IDirect3D9::CheckDeviceFormat**; for details see [Determining Hardware Support (Direct3D 9)](determining-hardware-support.md).</span></span>

## <a name="how-the-stencil-buffer-works"></a><span data-ttu-id="9120c-122">Como o buffer de estêncil funciona</span><span class="sxs-lookup"><span data-stu-id="9120c-122">How the Stencil Buffer Works</span></span>

<span data-ttu-id="9120c-123">O Direct3D realiza um teste no conteúdo do buffer de estêncil em uma base de pixel por pixel.</span><span class="sxs-lookup"><span data-stu-id="9120c-123">Direct3D performs a test on the contents of the stencil buffer on a pixel-by-pixel basis.</span></span> <span data-ttu-id="9120c-124">Para cada pixel na superfície do destino, ele executa um teste usando o valor correspondente no buffer de estêncil, um valor de referência de estêncil e um valor de máscara de estêncil.</span><span class="sxs-lookup"><span data-stu-id="9120c-124">For each pixel in the target surface, it performs a test using the corresponding value in the stencil buffer, a stencil reference value, and a stencil mask value.</span></span> <span data-ttu-id="9120c-125">Se o teste for aprovado, o Direct3D executa uma ação.</span><span class="sxs-lookup"><span data-stu-id="9120c-125">If the test passes, Direct3D performs an action.</span></span> <span data-ttu-id="9120c-126">O teste é realizado usando as seguintes etapas.</span><span class="sxs-lookup"><span data-stu-id="9120c-126">The test is performed using the following steps.</span></span>

1.  <span data-ttu-id="9120c-127">Execute uma operação AND bit a bit do valor de referência do estêncil com a máscara de estêncil.</span><span class="sxs-lookup"><span data-stu-id="9120c-127">Perform a bitwise AND operation of the stencil reference value with the stencil mask.</span></span>
2.  <span data-ttu-id="9120c-128">Execute uma operação AND bit a bit do valor de buffer do estêncil do pixel atual com a máscara de estêncil.</span><span class="sxs-lookup"><span data-stu-id="9120c-128">Perform a bitwise AND operation of the stencil buffer value for the current pixel with the stencil mask.</span></span>
3.  <span data-ttu-id="9120c-129">Compare o resultado da etapa 1 com o resultado da etapa 2, usando a função de comparação.</span><span class="sxs-lookup"><span data-stu-id="9120c-129">Compare the result of step 1 to the result of step 2, using the comparison function.</span></span>

<span data-ttu-id="9120c-130">Essas etapas são mostradas no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="9120c-130">These steps are shown in the following code example.</span></span>


```
(StencilRef & StencilMask) CompFunc (StencilBufferValue & StencilMask)
```




```
StencilBufferValue
```



<span data-ttu-id="9120c-131">é o conteúdo do buffer de estêncil para o pixel atual.</span><span class="sxs-lookup"><span data-stu-id="9120c-131">is the contents of the stencil buffer for the current pixel.</span></span> <span data-ttu-id="9120c-132">Este exemplo de código usa o símbolo de e comercial (&) para representar o bit e a operação.</span><span class="sxs-lookup"><span data-stu-id="9120c-132">This code example uses the ampersand (&) symbol to represent the bitwise AND operation.</span></span>


```
StencilMask
```



<span data-ttu-id="9120c-133">representa o valor da máscara do estêncil e</span><span class="sxs-lookup"><span data-stu-id="9120c-133">represents the value of the stencil mask, and</span></span>


```
StencilRef
```



<span data-ttu-id="9120c-134">representa o valor de referência do estêncil.</span><span class="sxs-lookup"><span data-stu-id="9120c-134">represents the stencil reference value.</span></span>


```
CompFunc
```



<span data-ttu-id="9120c-135">é a função de comparação.</span><span class="sxs-lookup"><span data-stu-id="9120c-135">is the comparison function.</span></span>

<span data-ttu-id="9120c-136">O pixel atual é escrito na superfície de destino se o teste de estêncil for aprovado, caso contrário, é ignorado.</span><span class="sxs-lookup"><span data-stu-id="9120c-136">The current pixel is written to the target surface if the stencil test passes, and is ignored otherwise.</span></span> <span data-ttu-id="9120c-137">O comportamento de comparação padrão é gravar o pixel, não importa a diferença entre cada operação de bit de bits (D3DCMP \_ Always).</span><span class="sxs-lookup"><span data-stu-id="9120c-137">The default comparison behavior is to write the pixel, no matter how each bitwise operation turns out (D3DCMP\_ALWAYS).</span></span> <span data-ttu-id="9120c-138">Você pode alterar esse comportamento alterando o valor do estado de \_ RENDERIZAÇÃO D3DRS STENCILFUNC, passando um membro do tipo enumerado [**D3DCMPFUNC**](./d3dcmpfunc.md) para identificar a função de comparação desejada.</span><span class="sxs-lookup"><span data-stu-id="9120c-138">You can change this behavior by changing the value of the D3DRS\_STENCILFUNC render state, passing a member of the [**D3DCMPFUNC**](./d3dcmpfunc.md) enumerated type to identify the desired comparison function.</span></span>

<span data-ttu-id="9120c-139">Seu aplicativo pode personalizar a operação do buffer de estêncil.</span><span class="sxs-lookup"><span data-stu-id="9120c-139">Your application can customize the operation of the stencil buffer.</span></span> <span data-ttu-id="9120c-140">Ele pode definir a função de comparação, a máscara de estêncil e o valor de referência de estêncil.</span><span class="sxs-lookup"><span data-stu-id="9120c-140">It can set the comparison function, the stencil mask, and the stencil reference value.</span></span> <span data-ttu-id="9120c-141">Ele também pode controlar a ação que o Direct3D executa quando o teste de estêncil passa ou falha.</span><span class="sxs-lookup"><span data-stu-id="9120c-141">It can also control the action that Direct3D takes when the stencil test passes or fails.</span></span> <span data-ttu-id="9120c-142">Para obter mais informações, consulte o [estado do buffer do estêncil (Direct3D 9)](stencil-buffer-state.md).</span><span class="sxs-lookup"><span data-stu-id="9120c-142">For more information, see [Stencil Buffer State (Direct3D 9)](stencil-buffer-state.md).</span></span>

## <a name="examples"></a><span data-ttu-id="9120c-143">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9120c-143">Examples</span></span>

<span data-ttu-id="9120c-144">Os exemplos de código a seguir demonstram como configurar o buffer de estêncil.</span><span class="sxs-lookup"><span data-stu-id="9120c-144">The following code examples demonstrate setting up the stencil buffer.</span></span>


```
// Enable stencil testing
pDevice->SetRenderState(D3DRS_STENCILENABLE, TRUE);

// Specify the stencil comparison function
pDevice->SetRenderState(D3DRS_STENCILFUNC, D3DCMP_EQUAL);

// Set the comparison reference value
pDevice->SetRenderState(D3DRS_STENCILREF, 0);

//  Specify a stencil mask 
pDevice->SetRenderState(D3DRS_STENCILMASK, 0);
```



<span data-ttu-id="9120c-145">Por padrão, o valor de referência do estêncil é zero.</span><span class="sxs-lookup"><span data-stu-id="9120c-145">By default, the stencil reference value is zero.</span></span> <span data-ttu-id="9120c-146">Qualquer valor inteiro é válido.</span><span class="sxs-lookup"><span data-stu-id="9120c-146">Any integer value is valid.</span></span> <span data-ttu-id="9120c-147">O Direct3D executa uma e/ou um valor de referência de estêncil e uma máscara de estêncil antes do teste de estêncil.</span><span class="sxs-lookup"><span data-stu-id="9120c-147">Direct3D performs a bitwise AND of the stencil reference value and a stencil mask value before the stencil test.</span></span>

<span data-ttu-id="9120c-148">Você pode controlar quais informações de pixel são gravadas dependendo da comparação do estêncil.</span><span class="sxs-lookup"><span data-stu-id="9120c-148">You can control what pixel information is written out depending on the stencil comparison.</span></span>


```
// A write mask controls what is written
pDevice->SetRenderState(D3DRS_STENCILWRITEMASK, D3DSTENCILOP_KEEP);
// Specify when to write stencil data
pDevice->SetRenderState(D3DRS_STENCILFAIL, D3DSTENCILOP_KEEP);
```



<span data-ttu-id="9120c-149">Você pode escrever sua própria fórmula para o valor que deseja gravar no buffer do estêncil, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="9120c-149">You can write your own formula for the value you want written into the stencil buffer as shown in the following example.</span></span>


```
NewStencilBufferValue = (StencilBufferValue & ~StencilWriteMask) | 
                        (StencilWriteMask & StencilOp(StencilBufferValue))
```



## <a name="related-topics"></a><span data-ttu-id="9120c-150">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9120c-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9120c-151">Pipeline de pixel</span><span class="sxs-lookup"><span data-stu-id="9120c-151">Pixel Pipeline</span></span>](pixel-pipeline.md)
</dt> </dl>

 

 
