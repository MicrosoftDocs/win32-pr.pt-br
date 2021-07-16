---
title: Visão geral de camadas
description: descreve as noções básicas de camadas de Direct2D.
ms.assetid: 22d161fb-8470-49cc-a523-309f90643ea9
keywords:
- Direct2D, camadas
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 027be097c5c21929f3ccdbaa169a1f3dac55b394
ms.sourcegitcommit: 698ce2d9ba2fa650f2875225d99623995fac246a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2021
ms.locfileid: "114231603"
---
# <a name="layers-overview"></a><span data-ttu-id="962fa-104">Visão geral de camadas</span><span class="sxs-lookup"><span data-stu-id="962fa-104">Layers Overview</span></span>

<span data-ttu-id="962fa-105">esta visão geral descreve as noções básicas do uso de camadas de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="962fa-105">This overview describes the basics of using Direct2D layers.</span></span> <span data-ttu-id="962fa-106">Ele contém as seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="962fa-106">It contains the following sections.</span></span>

-   [<span data-ttu-id="962fa-107">O que são camadas?</span><span class="sxs-lookup"><span data-stu-id="962fa-107">What Are Layers?</span></span>](#what-are-layers)
-   [<span data-ttu-id="962fa-108">camadas no Windows 8 e posteriores</span><span class="sxs-lookup"><span data-stu-id="962fa-108">Layers in Windows 8 and later</span></span>](#layers-in-windows-8-and-later)
    -   [<span data-ttu-id="962fa-109">ID2D1DeviceContext e PushLayer</span><span class="sxs-lookup"><span data-stu-id="962fa-109">ID2D1DeviceContext and PushLayer</span></span>](#id2d1devicecontext-and-pushlayer)
    -   [<span data-ttu-id="962fa-110">Camada \_ d2d1 \_ PARAMETERS1 e d2d1 \_ \_ OPTIONS1</span><span class="sxs-lookup"><span data-stu-id="962fa-110">D2D1\_LAYER\_PARAMETERS1 and D2D1\_LAYER\_OPTIONS1</span></span>](/windows)
    -   [<span data-ttu-id="962fa-111">Modos do Blend</span><span class="sxs-lookup"><span data-stu-id="962fa-111">Blend Modes</span></span>](#blend-modes)
    -   [<span data-ttu-id="962fa-112">Interoperação</span><span class="sxs-lookup"><span data-stu-id="962fa-112">Interoperation</span></span>](#interoperation)
-   [<span data-ttu-id="962fa-113">Criando camadas</span><span class="sxs-lookup"><span data-stu-id="962fa-113">Creating Layers</span></span>](#creating-layers)
-   [<span data-ttu-id="962fa-114">Limites de conteúdo</span><span class="sxs-lookup"><span data-stu-id="962fa-114">Content Bounds</span></span>](#content-bounds)
-   [<span data-ttu-id="962fa-115">Máscaras geométricas</span><span class="sxs-lookup"><span data-stu-id="962fa-115">Geometric Masks</span></span>](#geometric-masks)
-   [<span data-ttu-id="962fa-116">Máscaras de opacidade</span><span class="sxs-lookup"><span data-stu-id="962fa-116">Opacity Masks</span></span>](#opacity-masks)
-   [<span data-ttu-id="962fa-117">Alternativas para camadas</span><span class="sxs-lookup"><span data-stu-id="962fa-117">Alternatives to Layers</span></span>](#alternatives-to-layers)
-   [<span data-ttu-id="962fa-118">Recortando uma forma arbitrária</span><span class="sxs-lookup"><span data-stu-id="962fa-118">Clipping an arbitrary shape</span></span>](#clipping-an-arbitrary-shape)
    -   [<span data-ttu-id="962fa-119">Clipes alinhados ao eixo</span><span class="sxs-lookup"><span data-stu-id="962fa-119">Axis aligned clips</span></span>](#axis-aligned-clips)
-   [<span data-ttu-id="962fa-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="962fa-120">Related topics</span></span>](#related-topics)

## <a name="what-are-layers"></a><span data-ttu-id="962fa-121">O que são camadas?</span><span class="sxs-lookup"><span data-stu-id="962fa-121">What Are Layers?</span></span>

<span data-ttu-id="962fa-122">Camadas, representadas por objetos [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) , permitem que um aplicativo manipule um grupo de operações de desenho.</span><span class="sxs-lookup"><span data-stu-id="962fa-122">Layers, represented by [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) objects, enable an application to manipulate a group of drawing operations.</span></span> <span data-ttu-id="962fa-123">Você usa uma camada ao "enviar" por push para um destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="962fa-123">You use a layer by "pushing" it onto a render target.</span></span> <span data-ttu-id="962fa-124">As operações de desenho subsequentes pelo destino de renderização são direcionadas para a camada.</span><span class="sxs-lookup"><span data-stu-id="962fa-124">Subsequent drawing operations by the render target are directed to the layer.</span></span> <span data-ttu-id="962fa-125">Depois de terminar com a camada, você "pop" a camada do destino de renderização, que compõe o conteúdo da camada de volta para o destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="962fa-125">After you're finished with the layer, you "pop" the layer from the render target, which composites the layer's content back to the render target.</span></span>

<span data-ttu-id="962fa-126">Como pincéis, as camadas são recursos dependentes do dispositivo criados por destinos de renderização.</span><span class="sxs-lookup"><span data-stu-id="962fa-126">Like brushes, layers are device-dependent resources created by render targets.</span></span> <span data-ttu-id="962fa-127">As camadas podem ser usadas em qualquer destino de renderização no mesmo domínio de recurso que contém o destino de renderização que a criou.</span><span class="sxs-lookup"><span data-stu-id="962fa-127">Layers can be used on any render target in the same resource domain that contains the render target that created it.</span></span> <span data-ttu-id="962fa-128">No entanto, um recurso de camada só pode ser usado por um destino de renderização por vez.</span><span class="sxs-lookup"><span data-stu-id="962fa-128">However, a layer resource can only be used by one render target at a time.</span></span> <span data-ttu-id="962fa-129">Para obter mais informações sobre recursos, consulte a [visão geral de recursos](resources-and-resource-domains.md).</span><span class="sxs-lookup"><span data-stu-id="962fa-129">For more information about resources, see the [Resources Overview](resources-and-resource-domains.md).</span></span>

<span data-ttu-id="962fa-130">Embora as camadas ofereçam uma poderosa técnica de renderização para produzir efeitos interessantes, o número excessivo de camadas em um aplicativo pode afetar negativamente o desempenho, devido aos vários custos associados ao gerenciamento de camadas e recursos de camada.</span><span class="sxs-lookup"><span data-stu-id="962fa-130">Although layers offer a powerful rendering technique for producing interesting effects, excessive number of layers in an application can adversely affect its performance, because of the various costs associated with managing layers and layer resources.</span></span> <span data-ttu-id="962fa-131">Por exemplo, há o custo de preencher ou limpar a camada e, em seguida, mesclar novamente, especialmente em hardware de extremidade superior.</span><span class="sxs-lookup"><span data-stu-id="962fa-131">For example, there is the cost of filling or clearing the layer and then blending it back, especially on higher-end hardware.</span></span> <span data-ttu-id="962fa-132">Em seguida, há o custo de gerenciar os recursos de camada.</span><span class="sxs-lookup"><span data-stu-id="962fa-132">Then, there is the cost of managing the layer resources.</span></span> <span data-ttu-id="962fa-133">Se você os realocar com frequência, as interrupções resultantes na GPU serão o problema mais significativo.</span><span class="sxs-lookup"><span data-stu-id="962fa-133">If you reallocate these frequently, the resulting stalls against the GPU will be the most significant problem.</span></span> <span data-ttu-id="962fa-134">Ao projetar seu aplicativo, tente maximizar a reutilização de recursos de camada.</span><span class="sxs-lookup"><span data-stu-id="962fa-134">When you design your application, try to maximize reusing layer resources.</span></span>

## <a name="layers-in-windows-8-and-later"></a><span data-ttu-id="962fa-135">camadas no Windows 8 e posteriores</span><span class="sxs-lookup"><span data-stu-id="962fa-135">Layers in Windows 8 and later</span></span>

<span data-ttu-id="962fa-136">Windows 8 introduziu novas APIs relacionadas à camada que simplificam, melhoram o desempenho do e adicionam recursos a camadas.</span><span class="sxs-lookup"><span data-stu-id="962fa-136">Windows 8 introduced new layer related APIs that simplify, improve the performance of, and add features to layers.</span></span>

### <a name="id2d1devicecontext-and-pushlayer"></a><span data-ttu-id="962fa-137">ID2D1DeviceContext e PushLayer</span><span class="sxs-lookup"><span data-stu-id="962fa-137">ID2D1DeviceContext and PushLayer</span></span>

<span data-ttu-id="962fa-138">a interface [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) é derivada da interface [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) e é a chave para exibir Direct2D conteúdo no Windows 8, para obter mais informações sobre essa interface, consulte [dispositivos e contextos de dispositivo](devices-and-device-contexts.md).</span><span class="sxs-lookup"><span data-stu-id="962fa-138">The [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) interface is derived from the [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) interface and is key to displaying Direct2D content in Windows 8, for more information about this interface see [Devices and Device Contexts](devices-and-device-contexts.md).</span></span> <span data-ttu-id="962fa-139">Com a interface de contexto do dispositivo, você pode ignorar a chamada do método [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) e, em seguida, passar NULL para o método [**ID2D1DeviceContext::P ushlayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) .</span><span class="sxs-lookup"><span data-stu-id="962fa-139">With the device context interface, you can skip calling the [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) method and then pass NULL to the [**ID2D1DeviceContext::PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) method.</span></span> <span data-ttu-id="962fa-140">Direct2D gerencia automaticamente o recurso de camada e pode compartilhar recursos entre camadas e grafos de efeito.</span><span class="sxs-lookup"><span data-stu-id="962fa-140">Direct2D automatically manages the layer resource and can share resources between layers and effect graphs.</span></span>

### <a name="d2d1_layer_parameters1-and-d2d1_layer_options1"></a><span data-ttu-id="962fa-141">Camada \_ d2d1 \_ PARAMETERS1 e d2d1 \_ \_ OPTIONS1</span><span class="sxs-lookup"><span data-stu-id="962fa-141">D2D1\_LAYER\_PARAMETERS1 and D2D1\_LAYER\_OPTIONS1</span></span>

<span data-ttu-id="962fa-142">A [**estrutura \_ \_ PARAMETERS1 da camada d2d1**](/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_layer_parameters1) é a mesma que os [**\_ \_ parâmetros da camada d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters), exceto que o membro final da estrutura agora é uma enumeração [**\_ \_ OPTIONS1 da camada d2d1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1) .</span><span class="sxs-lookup"><span data-stu-id="962fa-142">The [**D2D1\_LAYER\_PARAMETERS1**](/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_layer_parameters1) structure is the same as [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters), except the final member of the structure is now a [**D2D1\_LAYER\_OPTIONS1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1) enumeration.</span></span>

<span data-ttu-id="962fa-143">[**D2d1 \_ A camada \_ OPTIONS1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1) não tem nenhuma opção ClearType e tem duas opções diferentes que você pode usar para melhorar o desempenho:</span><span class="sxs-lookup"><span data-stu-id="962fa-143">[**D2D1\_LAYER\_OPTIONS1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1) has no ClearType option and has two different options that you can use to improve performance:</span></span>

-   <span data-ttu-id="962fa-144">[**D2d1 \_ camada \_ OPTIONS1 \_ inicializar a \_ partir do \_ plano de fundo**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1): Direct2D renderiza primitivos para a camada sem limpá-lo com preto transparente.</span><span class="sxs-lookup"><span data-stu-id="962fa-144">[**D2D1\_LAYER\_OPTIONS1\_INITIALIZE\_FROM\_BACKGROUND**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1): Direct2D renders primitives to the layer without clearing it with transparent black.</span></span> <span data-ttu-id="962fa-145">Esse não é o padrão, mas na maioria dos casos resulta em melhor desempenho.</span><span class="sxs-lookup"><span data-stu-id="962fa-145">This is not the default, but in most cases results in better performance.</span></span>

-   <span data-ttu-id="962fa-146">[**D2d1 \_ camada \_ OPTIONS1 \_ ignorar \_ alfa**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1): se a superfície subjacente estiver definida como [**D2D1 \_ \_ modo alfa \_ ignorar**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode), essa opção permitirá que Direct2D evite modificar o canal alfa da camada.</span><span class="sxs-lookup"><span data-stu-id="962fa-146">[**D2D1\_LAYER\_OPTIONS1\_IGNORE\_ALPHA**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1): if the underlying surface is set to [**D2D1\_ALPHA\_MODE\_IGNORE**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode), this option lets Direct2D avoid modifying the alpha channel of the layer.</span></span> <span data-ttu-id="962fa-147">Não use isso em outros casos.</span><span class="sxs-lookup"><span data-stu-id="962fa-147">Do not use this in other cases.</span></span>

### <a name="blend-modes"></a><span data-ttu-id="962fa-148">Modos do Blend</span><span class="sxs-lookup"><span data-stu-id="962fa-148">Blend Modes</span></span>

<span data-ttu-id="962fa-149">a partir do Windows 8, o contexto do dispositivo tem um [**modo de mistura primitivo**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend) que determina como cada primitiva é mesclada com a superfície de destino.</span><span class="sxs-lookup"><span data-stu-id="962fa-149">Starting in Windows 8, the device context has a [**primitive blend mode**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend) that determines how each primitive is blended with the target surface.</span></span> <span data-ttu-id="962fa-150">Esse modo também se aplica a camadas quando você chama o método [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) .</span><span class="sxs-lookup"><span data-stu-id="962fa-150">This mode also applies to layers when you call the [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) method.</span></span>

<span data-ttu-id="962fa-151">Por exemplo, se você estiver usando uma camada para cortar primitivos com transparência, defina o modo de [**\_ \_ \_ cópia d2d1 PRIMITIVE Blend**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend) no contexto do dispositivo para obter os resultados apropriados.</span><span class="sxs-lookup"><span data-stu-id="962fa-151">For example, if you are using a layer to clip primitives with transparency set the [**D2D1\_PRIMITIVE\_BLEND\_COPY**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend) mode on the device context for proper results.</span></span> <span data-ttu-id="962fa-152">O modo de cópia torna o contexto de dispositivo linear interpolarmente todos os quatro canais de cores, incluindo o canal alfa, de cada pixel com o conteúdo da superfície de destino, de acordo com a máscara geométrica da camada.</span><span class="sxs-lookup"><span data-stu-id="962fa-152">The copy mode makes the device context linear interpolate all 4 color channels, including the alpha channel, of each pixel with the contents of the target surface according to the geometric mask of the layer.</span></span>

### <a name="interoperation"></a><span data-ttu-id="962fa-153">Interoperação</span><span class="sxs-lookup"><span data-stu-id="962fa-153">Interoperation</span></span>

<span data-ttu-id="962fa-154">a partir do Windows 8, o Direct2D dá suporte à interoperação com Direct3D e GDI, enquanto uma camada ou um clipe é enviado por push.</span><span class="sxs-lookup"><span data-stu-id="962fa-154">Starting in Windows 8, Direct2D supports interoperation with Direct3D and GDI while a layer or clip is pushed.</span></span> <span data-ttu-id="962fa-155">Você chama [**ID2D1GdiInteropRenderTarget:: GetDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc) enquanto uma camada é enviada por push para interoperar com GDI.</span><span class="sxs-lookup"><span data-stu-id="962fa-155">You call [**ID2D1GdiInteropRenderTarget::GetDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc) while a layer is pushed to interoperate with GDI.</span></span> <span data-ttu-id="962fa-156">Você chama [**ID2D1DeviceContext:: flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) e, em seguida, renderiza para a superfície subjacente para interoperar com o Direct3D.</span><span class="sxs-lookup"><span data-stu-id="962fa-156">You call [**ID2D1DeviceContext::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) and then render to the underlying surface to interoperate with Direct3D.</span></span> <span data-ttu-id="962fa-157">É sua responsabilidade renderizar dentro da camada ou do clipe com Direct3D ou GDI.</span><span class="sxs-lookup"><span data-stu-id="962fa-157">It is your responsibility to render inside the layer or clip with Direct3D or GDI.</span></span> <span data-ttu-id="962fa-158">Se você tentar renderizar fora da camada ou cortar, os resultados serão indefinidos.</span><span class="sxs-lookup"><span data-stu-id="962fa-158">If you try to render outside the layer or clip the results are undefined.</span></span>

## <a name="creating-layers"></a><span data-ttu-id="962fa-159">Criando camadas</span><span class="sxs-lookup"><span data-stu-id="962fa-159">Creating Layers</span></span>

<span data-ttu-id="962fa-160">Trabalhar com camadas requer familiaridade com os métodos [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)), [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer))e [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) , e a estrutura [**de \_ \_ parâmetros de camada d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) , que contém um conjunto de dados paramétricos que definem como a camada pode ser usada.</span><span class="sxs-lookup"><span data-stu-id="962fa-160">Working with layers requires familiarity with the [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)), [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)), and [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) methods, and the [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structure, which contains a set of parametric data that defines how the layer can be used.</span></span> <span data-ttu-id="962fa-161">A lista a seguir descreve os métodos e a estrutura.</span><span class="sxs-lookup"><span data-stu-id="962fa-161">The following list describes the methods and structure.</span></span>

-   <span data-ttu-id="962fa-162">Chame o método [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) para criar um recurso de camada.</span><span class="sxs-lookup"><span data-stu-id="962fa-162">Call the [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) method to create a layer resource.</span></span>
    > [!Note]  
    > <span data-ttu-id="962fa-163">a partir do Windows 8, você pode ignorar a chamada do método [**createlayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) e, em seguida, passar NULL para o método [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) na interface [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="962fa-163">Starting in Windows 8, you can skip calling the [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) method and then pass NULL to the [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) method on the [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) interface.</span></span> <span data-ttu-id="962fa-164">isso é mais simples e permite Direct2D gerenciar automaticamente o recurso de camada e compartilhar recursos entre camadas e grafos de efeito.</span><span class="sxs-lookup"><span data-stu-id="962fa-164">This is simpler and allows Direct2D to automatically manage the layer resource and share resources between layers and effect graphs.</span></span>

     

-   <span data-ttu-id="962fa-165">Depois que o destino de renderização começou a desenhar (depois de seu método [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) ter sido chamado), você pode usar o método [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) .</span><span class="sxs-lookup"><span data-stu-id="962fa-165">After render target has begun drawing (after its [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) method has been called), you can use the [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) method.</span></span> <span data-ttu-id="962fa-166">O método **PushLayer** adiciona a camada especificada ao destino de renderização, para que o destino receba todas as operações de desenho subsequentes até que [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) seja chamado.</span><span class="sxs-lookup"><span data-stu-id="962fa-166">The **PushLayer** method adds the specified layer to the render target, so that the target receives all subsequent drawing operations until [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) is called.</span></span> <span data-ttu-id="962fa-167">Esse método usa um objeto [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) retornado chamando [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) e um *layerparameters* na estrutura de [**\_ \_ parâmetros da camada d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) .</span><span class="sxs-lookup"><span data-stu-id="962fa-167">This method takes an [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) object returned by calling [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) and an *layerParameters* in the [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structure.</span></span> <span data-ttu-id="962fa-168">A tabela a seguir descreve os campos da estrutura.</span><span class="sxs-lookup"><span data-stu-id="962fa-168">The following table describes the fields of the structure.</span></span> 

    | <span data-ttu-id="962fa-169">Campo</span><span class="sxs-lookup"><span data-stu-id="962fa-169">Field</span></span>                 | <span data-ttu-id="962fa-170">Descrição</span><span class="sxs-lookup"><span data-stu-id="962fa-170">Description</span></span>|
    |-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="962fa-171">**contentBounds**</span><span class="sxs-lookup"><span data-stu-id="962fa-171">**contentBounds**</span></span>     | <span data-ttu-id="962fa-172">Os limites de conteúdo da camada.</span><span class="sxs-lookup"><span data-stu-id="962fa-172">The content bounds of the layer.</span></span> <span data-ttu-id="962fa-173">O conteúdo não será renderizado fora desses limites.</span><span class="sxs-lookup"><span data-stu-id="962fa-173">Content won't render outside these bounds.</span></span> <span data-ttu-id="962fa-174">O padrão desse parâmetro é [**InfiniteRect**](/windows/desktop/api/d2d1Helper/nf-d2d1helper-infiniterect).</span><span class="sxs-lookup"><span data-stu-id="962fa-174">This parameter defaults to [**InfiniteRect**](/windows/desktop/api/d2d1Helper/nf-d2d1helper-infiniterect).</span></span> <span data-ttu-id="962fa-175">Quando o valor padrão é usado, os limites de conteúdo são efetivamente utilizados para serem os limites do destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="962fa-175">When the default value is used, the content bounds are effectively taken to be the bounds of the render target.</span></span> |
    | <span data-ttu-id="962fa-176">**geometricMask**</span><span class="sxs-lookup"><span data-stu-id="962fa-176">**geometricMask**</span></span>     | <span data-ttu-id="962fa-177">Adicional A área, definida por um [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry), para o qual a camada deve ser recortada.</span><span class="sxs-lookup"><span data-stu-id="962fa-177">(Optional) The area, defined by an [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry), to which the layer should be clipped.</span></span> <span data-ttu-id="962fa-178">Defina como **NULL** se a camada não deve ser recortada em uma geometria.</span><span class="sxs-lookup"><span data-stu-id="962fa-178">Set to **NULL** if the layer shouldn't be clipped to a geometry.</span></span> |
    | <span data-ttu-id="962fa-179">**maskAntialiasMode**</span><span class="sxs-lookup"><span data-stu-id="962fa-179">**maskAntialiasMode**</span></span> | <span data-ttu-id="962fa-180">Um valor que especifica o modo de suavização para a máscara geométrica especificada pelo campo **geometricMask** .</span><span class="sxs-lookup"><span data-stu-id="962fa-180">A value that specifies the antialiasing mode for the geometric mask specified by the **geometricMask** field.</span></span> |
    | <span data-ttu-id="962fa-181">**maskTransform**</span><span class="sxs-lookup"><span data-stu-id="962fa-181">**maskTransform**</span></span>     | <span data-ttu-id="962fa-182">Um valor que especifica a transformação que é aplicada à máscara geométrica ao compor a camada.</span><span class="sxs-lookup"><span data-stu-id="962fa-182">A value that specifies the transform that is applied to the geometric mask when composing the layer.</span></span> <span data-ttu-id="962fa-183">Isso é relativo à transformação mundial.</span><span class="sxs-lookup"><span data-stu-id="962fa-183">This is relative to the world transform.</span></span>  |
    | <span data-ttu-id="962fa-184">**opacidade**</span><span class="sxs-lookup"><span data-stu-id="962fa-184">**opacity**</span></span>           | <span data-ttu-id="962fa-185">O valor de opacidade da camada.</span><span class="sxs-lookup"><span data-stu-id="962fa-185">The opacity value of the layer.</span></span> <span data-ttu-id="962fa-186">A opacidade de cada recurso na camada é multiplicada por esse valor durante a composição para o destino.</span><span class="sxs-lookup"><span data-stu-id="962fa-186">The opacity of each resource in the layer is multiplied with this value when compositing to the target.</span></span>  |
    | <span data-ttu-id="962fa-187">**opacityBrush**</span><span class="sxs-lookup"><span data-stu-id="962fa-187">**opacityBrush**</span></span>      | <span data-ttu-id="962fa-188">Adicional Um pincel que é usado para modificar a opacidade da camada.</span><span class="sxs-lookup"><span data-stu-id="962fa-188">(Optional) A brush that is used to modify the opacity of the layer.</span></span> <span data-ttu-id="962fa-189">O pincel é mapeado para a camada e o canal alfa de cada pixel de pincel mapeado é multiplicado em relação ao pixel de camada correspondente.</span><span class="sxs-lookup"><span data-stu-id="962fa-189">The brush is mapped to the layer, and the alpha channel of each mapped brush pixel is multiplied against the corresponding layer pixel.</span></span> <span data-ttu-id="962fa-190">Defina como **NULL** se a camada não tiver uma máscara de opacidade.</span><span class="sxs-lookup"><span data-stu-id="962fa-190">Set to **NULL** if the layer shouldn't have an opacity mask.</span></span>   |
    | <span data-ttu-id="962fa-191">**camadaoptions**</span><span class="sxs-lookup"><span data-stu-id="962fa-191">**layerOptions**</span></span>      | <span data-ttu-id="962fa-192">Um valor que especifica se a camada pretende renderizar o texto com anti-aliasing ClearType.</span><span class="sxs-lookup"><span data-stu-id="962fa-192">A value that specifies whether the layer intends to render text with ClearType antialiasing.</span></span> <span data-ttu-id="962fa-193">O padrão desse parâmetro é off.</span><span class="sxs-lookup"><span data-stu-id="962fa-193">This parameter defaults to off.</span></span> <span data-ttu-id="962fa-194">Ativá-lo permite que o ClearType funcione corretamente, mas resulta em uma velocidade de renderização um pouco mais lenta.</span><span class="sxs-lookup"><span data-stu-id="962fa-194">Turning it on enables ClearType to work correctly, but it results in slightly slower rendering speed.</span></span>    |

    

     

    > [!Note]  
    > <span data-ttu-id="962fa-195">a partir do Windows 8, não é possível renderizar com ClearType em uma camada, de modo que o parâmetro de **camadaoptions** sempre deve ser definido como [**opções de \_ camada D2D1 \_ \_ nenhum**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_layer_options)</span><span class="sxs-lookup"><span data-stu-id="962fa-195">Starting in Windows 8, you cannot render with ClearType in a layer, so the **layerOptions** parameter should always be set to [**D2D1\_LAYER\_OPTIONS\_NONE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_layer_options)</span></span>

     

    <span data-ttu-id="962fa-196">para sua conveniência, Direct2D fornece o método [**D2D1:: layerparameters**](/windows/desktop/api/d2d1helper/nf-d2d1helper-layerparameters) para ajudá-lo a criar estruturas de [**\_ \_ parâmetros de camada D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) .</span><span class="sxs-lookup"><span data-stu-id="962fa-196">For convenience, Direct2D provides the [**D2D1::LayerParameters**](/windows/desktop/api/d2d1helper/nf-d2d1helper-layerparameters) method to help you create [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structures.</span></span>

-   <span data-ttu-id="962fa-197">Para compor o conteúdo da camada no destino de renderização, chame o método [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) .</span><span class="sxs-lookup"><span data-stu-id="962fa-197">To composite the contents of the layer into the render target, call the [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) method.</span></span> <span data-ttu-id="962fa-198">Você deve chamar o método **PopLayer** antes de chamar o método [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) .</span><span class="sxs-lookup"><span data-stu-id="962fa-198">You must call the **PopLayer** method before you call the [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method.</span></span>

<span data-ttu-id="962fa-199">O exemplo a seguir mostra como usar [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)), [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer))e [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer).</span><span class="sxs-lookup"><span data-stu-id="962fa-199">The following example shows how to use [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)), [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)), and [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer).</span></span> <span data-ttu-id="962fa-200">Todos os campos na estrutura de [**\_ \_ parâmetros de camada d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) são definidos como seus padrões, exceto **opacityBrush**, que é definido como um [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush).</span><span class="sxs-lookup"><span data-stu-id="962fa-200">All fields in the [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structure are set to their defaults, except **opacityBrush**, which is set to an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush).</span></span>


```C++
// Create a layer.
ID2D1Layer *pLayer = NULL;
hr = pRT->CreateLayer(NULL, &pLayer);

if (SUCCEEDED(hr))
{
    pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 250));

    // Push the layer with the content bounds.
    pRT->PushLayer(
        D2D1::LayerParameters(
            D2D1::InfiniteRect(),
            NULL,
            D2D1_ANTIALIAS_MODE_PER_PRIMITIVE,
            D2D1::IdentityMatrix(),
            1.0,
            m_pRadialGradientBrush,
            D2D1_LAYER_OPTIONS_NONE),
        pLayer
        );

    pRT->DrawBitmap(m_pBambooBitmap, D2D1::RectF(0, 0, 190, 127));

    pRT->FillRectangle(
        D2D1::RectF(25.f, 25.f, 50.f, 50.f), 
        m_pSolidColorBrush
        );
    pRT->FillRectangle(
        D2D1::RectF(50.f, 50.f, 75.f, 75.f),
        m_pSolidColorBrush
        ); 
    pRT->FillRectangle(
        D2D1::RectF(75.f, 75.f, 100.f, 100.f),
        m_pSolidColorBrush
        );    
 
    pRT->PopLayer();
}
SafeRelease(&pLayer);
```



<span data-ttu-id="962fa-201">O código foi omitido neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="962fa-201">Code has been omitted from this example.</span></span>

<span data-ttu-id="962fa-202">Observe que quando você chama [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) e [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer), certifique-se de que cada **PushLayer** tenha uma chamada **PopLayer** correspondente.</span><span class="sxs-lookup"><span data-stu-id="962fa-202">Note that when you call [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) and [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer), ensure that each **PushLayer** has a matching **PopLayer** call.</span></span> <span data-ttu-id="962fa-203">Se houver mais chamadas **PopLayer** que chamadas **PushLayer** , o destino de renderização será colocado em um estado de erro.</span><span class="sxs-lookup"><span data-stu-id="962fa-203">If there are more **PopLayer** calls than **PushLayer** calls, the render target is placed into an error state.</span></span> <span data-ttu-id="962fa-204">Se a [**liberação**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) for chamada antes que todas as camadas pendentes sejam retiradas, o destino de renderização será colocado em um estado de erro e retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="962fa-204">If [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) is called before all outstanding layers are popped, the render target is placed into an error state and returns an error.</span></span> <span data-ttu-id="962fa-205">Para limpar o estado de erro, use [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).</span><span class="sxs-lookup"><span data-stu-id="962fa-205">To clear the error state, use [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).</span></span>

## <a name="content-bounds"></a><span data-ttu-id="962fa-206">Limites de conteúdo</span><span class="sxs-lookup"><span data-stu-id="962fa-206">Content Bounds</span></span>

<span data-ttu-id="962fa-207">O **contentBounds** define o limite de o que deve ser desenhado para a camada.</span><span class="sxs-lookup"><span data-stu-id="962fa-207">The **contentBounds** sets the limit of what is to be drawn to the layer.</span></span> <span data-ttu-id="962fa-208">Somente as coisas dentro dos limites de conteúdo são compostas de volta ao destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="962fa-208">Only those things within the content bounds are composited back to the render target.</span></span>

<span data-ttu-id="962fa-209">O exemplo a seguir mostra como especificar **contentBounds** para que a imagem original seja recortada para o conteúdo associado ao canto superior esquerdo em (10, 108) e no canto inferior direito em (121, 177).</span><span class="sxs-lookup"><span data-stu-id="962fa-209">The example that follows shows how to specify **contentBounds** so that the original image is clipped to the content bounds with the upper-left corner at (10, 108) and the lower-right corner at (121, 177).</span></span> <span data-ttu-id="962fa-210">A ilustração a seguir mostra a imagem original e o resultado de recortar a imagem para os limites de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="962fa-210">The following illustration shows the original image and the result of clipping the image to the content bounds.</span></span>

![ilustração de limites de conteúdo em uma imagem original e a imagem recortada resultante](images/layers-contentbounds.png)


```C++
HRESULT DemoApp::RenderWithLayerWithContentBounds(ID2D1RenderTarget *pRT)
{
    
    HRESULT hr = S_OK;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 0));

        // Push the layer with the content bounds.
        pRT->PushLayer(
            D2D1::LayerParameters(D2D1::RectF(10, 108, 121, 177)),
            pLayer
            );

        pRT->DrawBitmap(m_pWaterBitmap, D2D1::RectF(0, 0, 128, 192));
        pRT->PopLayer();
    }

    SafeRelease(&pLayer);

    return hr;
    
}
```



<span data-ttu-id="962fa-212">O código foi omitido neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="962fa-212">Code has been omitted from this example.</span></span>

> [!Note]
>
> <span data-ttu-id="962fa-213">A imagem recortada resultante será ainda afetada se você especificar um **geometricMask**.</span><span class="sxs-lookup"><span data-stu-id="962fa-213">The resulting clipped image is further affected if you specify a **geometricMask**.</span></span> <span data-ttu-id="962fa-214">Consulte a seção [máscaras geométricas](#geometric-masks) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="962fa-214">See the [Geometric Masks](#geometric-masks) section for more information.</span></span>

 

## <a name="geometric-masks"></a><span data-ttu-id="962fa-215">Máscaras geométricas</span><span class="sxs-lookup"><span data-stu-id="962fa-215">Geometric Masks</span></span>

<span data-ttu-id="962fa-216">Uma máscara geométrica é um clipe ou um recorte, definido por um objeto [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) , que mascara uma camada quando ela é desenhada por um destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="962fa-216">A geometric mask is a clip or a cutout, defined by an [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) object, that masks a layer when it is drawn by a render target.</span></span> <span data-ttu-id="962fa-217">Você pode usar o campo **geometricMask** da estrutura [**de \_ \_ parâmetros de camada d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) para mascarar os resultados em uma geometria.</span><span class="sxs-lookup"><span data-stu-id="962fa-217">You can use the **geometricMask** field of the [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structure to mask the results to a geometry.</span></span> <span data-ttu-id="962fa-218">Por exemplo, se você quiser exibir uma imagem mascarada por uma letra de bloco "A", você pode primeiro criar uma geometria representando a letra "A" e usar essa geometria como uma máscara geométrica para uma camada.</span><span class="sxs-lookup"><span data-stu-id="962fa-218">For example, if you want to display an image masked by a block letter "A", you can first create a geometry representing the block letter "A" and use that geometry as a geometric mask for a layer.</span></span> <span data-ttu-id="962fa-219">Em seguida, depois de enviar a camada por push, você pode desenhar a imagem.</span><span class="sxs-lookup"><span data-stu-id="962fa-219">Then, after pushing the layer, you can draw the image.</span></span> <span data-ttu-id="962fa-220">A retirada dos resultados da camada na imagem que está sendo recortada para a forma "A" da letra de bloco.</span><span class="sxs-lookup"><span data-stu-id="962fa-220">Popping the layer results in the image being clipped to the block letter "A" shape.</span></span>

<span data-ttu-id="962fa-221">O exemplo a seguir mostra como criar um [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) contendo uma forma de uma montanha e, em seguida, passar a geometria do caminho para o [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)).</span><span class="sxs-lookup"><span data-stu-id="962fa-221">The example that follows shows how to create an [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) containing a shape of a mountain and then pass the path geometry to the [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)).</span></span> <span data-ttu-id="962fa-222">Em seguida, ele desenha um bitmap e quadrados.</span><span class="sxs-lookup"><span data-stu-id="962fa-222">It then draws a bitmap and squares.</span></span> <span data-ttu-id="962fa-223">Se houver apenas um bitmap na camada a ser renderizado, use [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) com um pincel de bitmap clamped para obter eficiência.</span><span class="sxs-lookup"><span data-stu-id="962fa-223">If there is only a bitmap in the layer to render, use [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) with a clamped bitmap brush for efficiency.</span></span> <span data-ttu-id="962fa-224">A ilustração a seguir mostra a saída do exemplo.</span><span class="sxs-lookup"><span data-stu-id="962fa-224">The following illustration shows the output from the example.</span></span>

![ilustração de uma imagem de uma folha e a imagem resultante após a aplicação de uma máscara geométrica de uma montanha](images/layers-bitmapmask.png)

<span data-ttu-id="962fa-226">O primeiro exemplo define a geometria a ser usada como uma máscara.</span><span class="sxs-lookup"><span data-stu-id="962fa-226">The first example defines the geometry to be used as a mask.</span></span>


```C++
hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometry);
    
if(SUCCEEDED(hr))
{
    ID2D1GeometrySink *pSink = NULL;
    // Write to the path geometry using the geometry sink.
    hr = m_pPathGeometry->Open(&pSink);

    if (SUCCEEDED(hr))
    {
        pSink->SetFillMode(D2D1_FILL_MODE_WINDING);
        pSink->BeginFigure(
            D2D1::Point2F(0, 90),
            D2D1_FIGURE_BEGIN_FILLED
            );

        D2D1_POINT_2F points[7] = {
           D2D1::Point2F(35, 30),
           D2D1::Point2F(50, 50),
           D2D1::Point2F(70, 45),
           D2D1::Point2F(105, 90),
           D2D1::Point2F(130, 90),
           D2D1::Point2F(150, 60),
           D2D1::Point2F(170, 90)
           };

        pSink->AddLines(points, 7);
        pSink->EndFigure(D2D1_FIGURE_END_CLOSED);
        hr = pSink->Close();
    }
    SafeRelease(&pSink);
       }
```



<span data-ttu-id="962fa-227">O exemplo a seguir usa a geometria como uma máscara para a camada.</span><span class="sxs-lookup"><span data-stu-id="962fa-227">The next example uses the geometry as a mask for the layer.</span></span>


```C++
HRESULT DemoApp::RenderWithLayerWithGeometricMask(ID2D1RenderTarget *pRT)
{
    
    HRESULT hr;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 450));

        pRT->PushLayer(
            D2D1::LayerParameters(D2D1::InfiniteRect(), m_pPathGeometry),
            pLayer
            );

        pRT->DrawBitmap(m_pLeafBitmap, D2D1::RectF(0, 0, 198, 132));

        pRT->FillRectangle(
            D2D1::RectF(50.f, 50.f, 75.f, 75.f), 
            m_pSolidColorBrush
            ); 
        pRT->FillRectangle(
            D2D1::RectF(75.f, 75.f, 100.f, 100.f),
            m_pSolidColorBrush
            );        

        pRT->PopLayer();
    }

    SafeRelease(&pLayer);

    return hr;
    
}
```



<span data-ttu-id="962fa-228">O código foi omitido neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="962fa-228">Code has been omitted from this example.</span></span>

> [!Note]
>
> <span data-ttu-id="962fa-229">Em geral, se você especificar um **geometricMask**, poderá usar o valor padrão, [**InfiniteRect**](/windows/desktop/api/d2d1Helper/nf-d2d1helper-infiniterect), para o **contentBounds**.</span><span class="sxs-lookup"><span data-stu-id="962fa-229">In general, if you specify a **geometricMask**, you can use the default value, [**InfiniteRect**](/windows/desktop/api/d2d1Helper/nf-d2d1helper-infiniterect), for the **contentBounds**.</span></span>
>
> <span data-ttu-id="962fa-230">Se **contentBounds** for nulo e **GEOMETRICMASK** for não nulo, os limites de conteúdo serão efetivamente os limites da máscara geométrica depois que a transformação mask for aplicada.</span><span class="sxs-lookup"><span data-stu-id="962fa-230">If **contentBounds** is NULL, and **geometricMask** is non-NULL, then the content bounds are effectively the bounds of the geometric mask after the mask transform is applied.</span></span>
>
> <span data-ttu-id="962fa-231">Se **contentBounds** não for nulo e **GEOMETRICMASK** for não nulo, a máscara geométrica transformada será efetivamente recortada em relação aos limites de conteúdo e os limites de conteúdo serão considerados infinitos.</span><span class="sxs-lookup"><span data-stu-id="962fa-231">If **contentBounds** is non-NULL, and **geometricMask** is non-NULL, then the transformed geometric mask is effectively clipped against content bounds and the content bounds are assumed to be infinite.</span></span>

 

## <a name="opacity-masks"></a><span data-ttu-id="962fa-232">Máscaras de opacidade</span><span class="sxs-lookup"><span data-stu-id="962fa-232">Opacity Masks</span></span>

<span data-ttu-id="962fa-233">Uma máscara de opacidade é uma máscara, descrita por um pincel ou bitmap, que é aplicada a outro objeto para tornar esse objeto parcial ou completamente transparente.</span><span class="sxs-lookup"><span data-stu-id="962fa-233">An opacity mask is a mask, described by a brush or bitmap, that is applied to another object to make that object partially or completely transparent.</span></span> <span data-ttu-id="962fa-234">Ele permite o uso do canal alfa de um pincel a ser usado como uma máscara de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="962fa-234">It allows the use of the alpha channel of a brush to be used as a content mask.</span></span> <span data-ttu-id="962fa-235">Por exemplo, você pode definir um pincel de gradiente radial que varia de opaco para transparente para criar um efeito de Vignette.</span><span class="sxs-lookup"><span data-stu-id="962fa-235">For example, you can define a radial gradient brush that varies from opaque to transparent to create a vignette effect.</span></span>

<span data-ttu-id="962fa-236">O exemplo a seguir usa um [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) (*m \_ pRadialGradientBrush*) como uma máscara de opacidade.</span><span class="sxs-lookup"><span data-stu-id="962fa-236">The example that follows uses an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) (*m\_pRadialGradientBrush*) as an opacity mask.</span></span> <span data-ttu-id="962fa-237">Em seguida, ele desenha um bitmap e quadrados.</span><span class="sxs-lookup"><span data-stu-id="962fa-237">It then draws a bitmap and squares.</span></span> <span data-ttu-id="962fa-238">Se houver apenas um bitmap na camada a ser renderizado, use [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) com um pincel de bitmap clamped para obter eficiência.</span><span class="sxs-lookup"><span data-stu-id="962fa-238">If there is only a bitmap in the layer to render, use [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) with a clamped bitmap brush for efficiency.</span></span> <span data-ttu-id="962fa-239">A ilustração a seguir mostra a saída deste exemplo.</span><span class="sxs-lookup"><span data-stu-id="962fa-239">The following illustration shows the output from this example.</span></span>

![ilustração de uma imagem de árvores e a imagem resultante depois que uma máscara de opacidade é aplicada](images/layers-opacitymask.png)


```C++
HRESULT DemoApp::RenderWithLayerWithOpacityMask(ID2D1RenderTarget *pRT)
{   

    HRESULT hr = S_OK;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 250));

        // Push the layer with the content bounds.
        pRT->PushLayer(
            D2D1::LayerParameters(
                D2D1::InfiniteRect(),
                NULL,
                D2D1_ANTIALIAS_MODE_PER_PRIMITIVE,
                D2D1::IdentityMatrix(),
                1.0,
                m_pRadialGradientBrush,
                D2D1_LAYER_OPTIONS_NONE),
            pLayer
            );

        pRT->DrawBitmap(m_pBambooBitmap, D2D1::RectF(0, 0, 190, 127));

        pRT->FillRectangle(
            D2D1::RectF(25.f, 25.f, 50.f, 50.f), 
            m_pSolidColorBrush
            );
        pRT->FillRectangle(
            D2D1::RectF(50.f, 50.f, 75.f, 75.f),
            m_pSolidColorBrush
            ); 
        pRT->FillRectangle(
            D2D1::RectF(75.f, 75.f, 100.f, 100.f),
            m_pSolidColorBrush
            );    
 
        pRT->PopLayer();
    }
    SafeRelease(&pLayer);
   
    return hr;
    
}
```



<span data-ttu-id="962fa-241">O código foi omitido neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="962fa-241">Code has been omitted from this example.</span></span>

> [!Note]  
> <span data-ttu-id="962fa-242">Este exemplo usa uma camada para aplicar uma máscara de opacidade a um único objeto para manter o exemplo o mais simples possível.</span><span class="sxs-lookup"><span data-stu-id="962fa-242">This example uses a layer to apply an opacity mask to a single object to keep the example as simple as possible.</span></span> <span data-ttu-id="962fa-243">Ao aplicar uma máscara de opacidade a um único objeto, seu mais eficiente é usar os métodos [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) ou [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) , em vez de uma camada.</span><span class="sxs-lookup"><span data-stu-id="962fa-243">When applying an opacity mask to a single object, its more efficient to use the [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) or [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) methods, rather than a layer.</span></span>

 

<span data-ttu-id="962fa-244">Para obter instruções sobre como aplicar uma máscara de opacidade sem usar uma camada, consulte a [visão geral das máscaras de opacidade](opacity-masks-overview.md).</span><span class="sxs-lookup"><span data-stu-id="962fa-244">For instructions on how to apply an opacity mask without using a layer, see the [Opacity Masks Overview](opacity-masks-overview.md).</span></span>

## <a name="alternatives-to-layers"></a><span data-ttu-id="962fa-245">Alternativas para camadas</span><span class="sxs-lookup"><span data-stu-id="962fa-245">Alternatives to Layers</span></span>

<span data-ttu-id="962fa-246">Como mencionado anteriormente, o número excessivo de camadas pode afetar negativamente o desempenho do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="962fa-246">As mentioned earlier, excessive number of layers can adversely affect the performance of your application.</span></span> <span data-ttu-id="962fa-247">Para melhorar o desempenho, evite usar camadas sempre que possível; em vez disso, use suas alternativas.</span><span class="sxs-lookup"><span data-stu-id="962fa-247">To improve performance, avoid using layers whenever possible; instead use their alternatives.</span></span> <span data-ttu-id="962fa-248">O exemplo de código a seguir mostra como usar [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f_d2d1_antialias_mode)) e [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) para recortar uma região, como uma alternativa ao uso de uma camada com limites de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="962fa-248">The following code example shows how to use [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f_d2d1_antialias_mode)) and [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) to clip a region, as an alternative to using a layer with content bounds.</span></span>


```C++
pRT->PushAxisAlignedClip(
    D2D1::RectF(20, 20, 100, 100),
    D2D1_ANTIALIAS_MODE_PER_PRIMITIVE
    );

pRT->FillRectangle(D2D1::RectF(0, 0, 200, 133), m_pOriginalBitmapBrush);
pRT->PopAxisAlignedClip();
```



<span data-ttu-id="962fa-249">Da mesma forma, use [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) com um pincel de bitmap clamped como uma alternativa ao uso de uma camada com uma máscara de opacidade quando houver apenas um conteúdo na camada a ser renderizado, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="962fa-249">Similarly, use [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) with a clamped bitmap brush as an alternative to using a layer with an opacity mask when there is only one content in the layer to render, as shown in the following example.</span></span>


```C++
        m_pRenderTarget->FillGeometry(
            m_pRectGeo, 
            m_pLinearFadeFlowersBitmapBrush, 
            m_pLinearGradientBrush
            );
```



<span data-ttu-id="962fa-250">Como alternativa ao uso de uma camada com uma máscara geométrica, considere usar uma máscara de bitmap para recortar uma região, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="962fa-250">As an alternative to using a layer with a geometric mask, consider using a bitmap mask to clip a region, as shown in the following example.</span></span>


```C++
// D2D1_ANTIALIAS_MODE_ALIASED must be set for FillOpacityMask
// to function properly.
m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_ALIASED);

m_pRenderTarget->FillOpacityMask(
    m_pBitmapMask,
    m_pOriginalBitmapBrush,
    D2D1_OPACITY_MASK_CONTENT_GRAPHICS,
    &rcBrushRect,
    NULL
    );

m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_PER_PRIMITIVE);

```



<span data-ttu-id="962fa-251">Por fim, se você quiser aplicar a opacidade a um único primitivo, deverá multiplicar a opacidade na cor do pincel e, em seguida, renderizar o primitivo.</span><span class="sxs-lookup"><span data-stu-id="962fa-251">Lastly, if you want to apply opacity to a single primitive, you should multiply the opacity into the into the brush color and then render the primitive.</span></span> <span data-ttu-id="962fa-252">Você não precisa de uma camada ou bitmap de máscara de opacidade.</span><span class="sxs-lookup"><span data-stu-id="962fa-252">You do not need a layer or an opacity mask bitmap.</span></span>


```C++
float opacity = 0.9f;

ID2D1SolidColorBrush *pBrush = NULL;
hr = pCompatibleRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF(0.93f, 0.94f, 0.96f, 1.0f * opacity)),
    &pBrush
    );

m_pRenderTarget->FillRectangle(
    D2D1::RectF(50.0f, 50.0f, 75.0f, 75.0f), 
    pBrush
    ); 
```



## <a name="clipping-an-arbitrary-shape"></a><span data-ttu-id="962fa-253">Recortando uma forma arbitrária</span><span class="sxs-lookup"><span data-stu-id="962fa-253">Clipping an arbitrary shape</span></span>

<span data-ttu-id="962fa-254">A figura aqui mostra o resultado da aplicação de um clipe a uma imagem.</span><span class="sxs-lookup"><span data-stu-id="962fa-254">The figure here shows the result of applying a clip to an image.</span></span>

![uma imagem que mostra um exemplo de uma imagem antes e depois de um clipe.](images/clip.png)

<span data-ttu-id="962fa-256">Você pode obter esse resultado usando camadas com uma máscara de geometria ou o método [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) com um pincel de opacidade.</span><span class="sxs-lookup"><span data-stu-id="962fa-256">You can get this result by using layers with a geometry mask or the [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method with an opacity brush.</span></span>

<span data-ttu-id="962fa-257">Aqui está um exemplo que usa uma camada:</span><span class="sxs-lookup"><span data-stu-id="962fa-257">Here's an example that uses a layer:</span></span>


```C++
// Call PushLayer() and pass in the clipping geometry.
m_d2dContext->PushLayer(
    D2D1::LayerParameters(
        boundsRect,
        geometricMask));
```



<span data-ttu-id="962fa-258">Aqui está um exemplo que usa o método [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) :</span><span class="sxs-lookup"><span data-stu-id="962fa-258">Here's an example that uses the [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method:</span></span>


```C++
// Create an opacity bitmap and render content.
m_d2dContext->CreateBitmap(size, nullptr, 0,
    D2D1::BitmapProperties(
        D2D1_BITMAP_OPTIONS_TARGET,
        D2D1::PixelFormat(
            DXGI_FORMAT_A8_UNORM,
            D2D1_ALPHA_MODE_PREMULTIPLIED),
        dpiX, dpiY),
    &opacityBitmap);

m_d2dContext->SetTarget(opacityBitmap.Get());
m_d2dContext->BeginDraw();
…
m_d2dContext->EndDraw();

// Create an opacity brush from the opacity bitmap.
m_d2dContext->CreateBitmapBrush(opacityBitmap.Get(),
    D2D1::BitmapBrushProperties(),
    D2D1::BrushProperties(),
    &bitmapBrush);

// Call the FillGeometry method and pass in the clip geometry and the opacity brush
m_d2dContext->FillGeometry( 
    clipGeometry.Get(),
    brush.Get(),
    opacityBrush.Get()); 
```



<span data-ttu-id="962fa-259">Neste exemplo de código, ao chamar o método PushLayer, você não passa uma camada de aplicativo criado.</span><span class="sxs-lookup"><span data-stu-id="962fa-259">In this code example, when you call the PushLayer method, you don't pass in an app created layer.</span></span> <span data-ttu-id="962fa-260">Direct2D cria uma camada para você.</span><span class="sxs-lookup"><span data-stu-id="962fa-260">Direct2D creates a layer for you.</span></span> <span data-ttu-id="962fa-261">Direct2D é capaz de gerenciar a alocação e a destruição desse recurso sem qualquer envolvimento do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="962fa-261">Direct2D is able to manage the allocation and destruction of this resource without any involvement from the app.</span></span> <span data-ttu-id="962fa-262">isso permite que Direct2D reutilize as camadas internamente e aplique otimizações de gerenciamento de recursos.</span><span class="sxs-lookup"><span data-stu-id="962fa-262">This allows Direct2D to reuse layers internally and apply resource management optimizations.</span></span>

> [!Note]  
> <span data-ttu-id="962fa-263">em Windows 8 muitas otimizações foram feitas no uso de camadas e recomendamos que você tente usar APIs de camada em vez de [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) sempre que possível.</span><span class="sxs-lookup"><span data-stu-id="962fa-263">In Windows 8 many optimizations have been made to the usage of layers and we recommend you try using layer APIs instead of [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) whenever possible.</span></span>

 

### <a name="axis-aligned-clips"></a><span data-ttu-id="962fa-264">Clipes alinhados ao eixo</span><span class="sxs-lookup"><span data-stu-id="962fa-264">Axis aligned clips</span></span>

<span data-ttu-id="962fa-265">Se a região a ser recortada estiver alinhada ao eixo da superfície de desenho, em vez de arbitrária.</span><span class="sxs-lookup"><span data-stu-id="962fa-265">If the region to be clipped is aligned to the axis of the drawing surface, instead of arbitrary.</span></span> <span data-ttu-id="962fa-266">Esse caso é adequado para usar um retângulo de clipe em vez de uma camada.</span><span class="sxs-lookup"><span data-stu-id="962fa-266">This case is suited for using a clip rectangle instead of a layer.</span></span> <span data-ttu-id="962fa-267">O lucro de desempenho é mais para geometria com alias do que a geometria de suavização de serrilhado.</span><span class="sxs-lookup"><span data-stu-id="962fa-267">The performance gain is more for aliased geometry than antialiased geometry.</span></span> <span data-ttu-id="962fa-268">Para obter mais informações sobre clipes alinhados por eixo, consulte o tópico [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) .</span><span class="sxs-lookup"><span data-stu-id="962fa-268">For more info on axis aligned clips, see the [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) topic.</span></span>

## <a name="related-topics"></a><span data-ttu-id="962fa-269">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="962fa-269">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="962fa-270">Direct2D Referência</span><span class="sxs-lookup"><span data-stu-id="962fa-270">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 