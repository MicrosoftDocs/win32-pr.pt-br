---
title: Compartilhamento de superfície entre APIs gráficas do Windows
description: Este tópico fornece uma visão geral técnica da interoperabilidade usando o compartilhamento de superfície entre APIs gráficas do Windows, incluindo Direct3D 11, Direct2D, DirectWrite, Direct3D 10 e Direct3D 9Ex.
ms.assetid: 65abf33e-3d15-42ff-99bd-674f24da773e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1032cb1cf9b16280088f00e79e7e59bb7f1510b1
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343611"
---
# <a name="surface-sharing-between-windows-graphics-apis"></a><span data-ttu-id="67973-103">Compartilhamento de superfície entre APIs gráficas do Windows</span><span class="sxs-lookup"><span data-stu-id="67973-103">Surface sharing between Windows graphics APIs</span></span>

<span data-ttu-id="67973-104">Este tópico fornece uma visão geral técnica da interoperabilidade usando o compartilhamento de superfície entre APIs gráficas do Windows, incluindo Direct3D 11, Direct2D, DirectWrite, Direct3D 10 e Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="67973-104">This topic provides a technical overview of interoperability using surface sharing between Windows graphics APIs, including Direct3D 11, Direct2D, DirectWrite, Direct3D 10, and Direct3D 9Ex.</span></span> <span data-ttu-id="67973-105">Se você já tiver um conhecimento prático dessas APIs, este documento poderá ajudá-lo a usar várias APIs para renderizar na mesma superfície em um aplicativo projetado para os sistemas operacionais Windows 7 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="67973-105">If you already have a working knowledge of these APIs, this paper can help you use multiple APIs to render to the same surface in an application designed for the Windows 7 or Windows Vista operating systems.</span></span> <span data-ttu-id="67973-106">Este tópico também fornece diretrizes de melhores práticas e ponteiros para recursos adicionais.</span><span class="sxs-lookup"><span data-stu-id="67973-106">This topic also provides best practice guidelines and pointers to additional resources.</span></span>

> [!Note]  
> <span data-ttu-id="67973-107">Para interoperabilidade direct2D e DirectWrite no runtime do DirectX 11.1, você pode usar os contextos de dispositivo e dispositivos [direct2D](/windows/desktop/Direct2D/devices-and-device-contexts) para renderizar diretamente para dispositivos Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="67973-107">For Direct2D and DirectWrite interoperability on the DirectX 11.1 runtime, you can use [Direct2D devices and device contexts](/windows/desktop/Direct2D/devices-and-device-contexts) to render directly to Direct3D 11 devices.</span></span>

 

<span data-ttu-id="67973-108">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="67973-108">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="67973-109">Introdução</span><span class="sxs-lookup"><span data-stu-id="67973-109">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="67973-110">Visão geral da interoperabilidade de API</span><span class="sxs-lookup"><span data-stu-id="67973-110">API Interoperability Overview</span></span>](#api-interoperability-overview)
-   [<span data-ttu-id="67973-111">Cenários de interoperabilidade</span><span class="sxs-lookup"><span data-stu-id="67973-111">Interoperability Scenarios</span></span>](#interoperability-scenarios)
    -   [<span data-ttu-id="67973-112">Compartilhamento de dispositivo do Direct3D 10.1 com Direct2D</span><span class="sxs-lookup"><span data-stu-id="67973-112">Direct3D 10.1 Device Sharing with Direct2D</span></span>](#direct3d-101-device-sharing-with-direct2d)
    -   [<span data-ttu-id="67973-113">Superfícies compartilhadas sincronizadas do DXGI 1.1</span><span class="sxs-lookup"><span data-stu-id="67973-113">DXGI 1.1 Synchronized Shared Surfaces</span></span>](#dxgi-11-synchronized-shared-surfaces)
    -   [<span data-ttu-id="67973-114">Interoperabilidade entre o Direct3D 9Ex e as APIs baseadas em DXGI</span><span class="sxs-lookup"><span data-stu-id="67973-114">Interoperability between Direct3D 9Ex and DXGI based APIs</span></span>](#interoperability-between-direct3d-9ex-and-dxgi-based-apis)
-   [<span data-ttu-id="67973-115">Conclusão</span><span class="sxs-lookup"><span data-stu-id="67973-115">Conclusion</span></span>](#conclusion)

## <a name="introduction"></a><span data-ttu-id="67973-116">Introdução</span><span class="sxs-lookup"><span data-stu-id="67973-116">Introduction</span></span>

<span data-ttu-id="67973-117">Neste documento, a interoperabilidade da API de gráficos do Windows refere-se ao compartilhamento da mesma superfície de renderização por APIs diferentes.</span><span class="sxs-lookup"><span data-stu-id="67973-117">In this document, Windows graphics API interoperability refers to the sharing of the same rendering surface by different APIs.</span></span> <span data-ttu-id="67973-118">Esse tipo de interoperabilidade permite que os aplicativos criem exibições atraentes aproveitando várias APIs gráficas do Windows e facilitando a migração para novas tecnologias mantendo a compatibilidade com as APIs existentes.</span><span class="sxs-lookup"><span data-stu-id="67973-118">This kind of interoperability enables applications to create compelling displays by leveraging multiple Windows graphics APIs, and to ease migration to new technologies by maintaining compatibility with existing APIs.</span></span>

<span data-ttu-id="67973-119">No Windows 7 (e Windows Vista SP2 com Windows 7 Interop Pack, Vista 7IP), as APIs de renderização de gráficos são Direct3D 11, Direct2D, Direct3D 10.1, Direct3D 10.0, Direct3D 9Ex, Direct3D 9c e APIs direct3D anteriores, bem como GDI e GDI+.</span><span class="sxs-lookup"><span data-stu-id="67973-119">In Windows 7 (and Windows Vista SP2 with Windows 7 Interop Pack, Vista 7IP), the graphics rendering APIs are Direct3D 11, Direct2D, Direct3D 10.1, Direct3D 10.0, Direct3D 9Ex, Direct3D 9c and earlier Direct3D APIs, as well GDI and GDI+.</span></span> <span data-ttu-id="67973-120">Windows Imaging Component (WIC) e DirectWrite são tecnologias relacionadas para processamento de imagem e o Direct2D executa a renderização de texto.</span><span class="sxs-lookup"><span data-stu-id="67973-120">Windows Imaging Component (WIC) and DirectWrite are related technologies for image processing, and Direct2D performs text rendering.</span></span> <span data-ttu-id="67973-121">A DXVA (API de Aceleração de Vídeo) do DirectX, baseada em Direct3D 9c e Direct3D 9Ex, é usada para processamento de vídeo.</span><span class="sxs-lookup"><span data-stu-id="67973-121">DirectX Video Acceleration API (DXVA), based on Direct3D 9c and Direct3D 9Ex, is used for video processing.</span></span>

<span data-ttu-id="67973-122">À medida que as APIs de gráficos do Windows evoluem para serem baseadas em Direct3D, a Microsoft está investindo mais esforço na garantia de interoperabilidade entre as APIs.</span><span class="sxs-lookup"><span data-stu-id="67973-122">As Windows graphics APIs evolve towards being Direct3D-based, Microsoft is investing more effort in ensuring interoperability across APIs.</span></span> <span data-ttu-id="67973-123">APIs do Direct3D e APIs de nível mais alto desenvolvidas com base em APIs do Direct3D também fornecem suporte quando necessário para a compatibilidade de ponte com APIs mais antigas.</span><span class="sxs-lookup"><span data-stu-id="67973-123">Newly developed Direct3D APIs and higher level APIs based on Direct3D APIs also provide support where needed for bridging compatibility with older APIs.</span></span> <span data-ttu-id="67973-124">Para ilustrar, os aplicativos Direct2D podem usar o Direct3D 10,1 compartilhando um dispositivo Direct3D 10,1.</span><span class="sxs-lookup"><span data-stu-id="67973-124">To illustrate, Direct2D applications can use Direct3D 10.1 by sharing a Direct3D 10.1 device.</span></span> <span data-ttu-id="67973-125">Além disso, as APIs do Direct3D 11, Direct2D e Direct3D 10,1 podem aproveitar a (infraestrutura de gráficos do DirectX) 1,1, que permite superfícies compartilhadas sincronizadas que dão suporte total à interoperabilidade entre essas APIs.</span><span class="sxs-lookup"><span data-stu-id="67973-125">Also, Direct3D 11, Direct2D, and Direct3D 10.1 APIs can all take advantage of DirectX Graphics Infrastructure (DXGI) 1.1, which enables synchronized shared surfaces that fully support interoperability among these APIs.</span></span> <span data-ttu-id="67973-126">As APIs baseadas em DXGI 1,1 interoperam com GDI e com GDI+ por associação, obtendo o contexto do dispositivo GDI de uma superfície do DXGI 1,1.</span><span class="sxs-lookup"><span data-stu-id="67973-126">DXGI 1.1-based APIs interoperate with GDI, and with GDI+ by association, by obtaining the GDI device context from a DXGI 1.1 surface.</span></span> <span data-ttu-id="67973-127">Para obter mais informações, consulte a documentação de interoperabilidade de DXGI e GDI disponível no MSDN.</span><span class="sxs-lookup"><span data-stu-id="67973-127">For more information, see the DXGI and GDI interoperability documentation available on MSDN.</span></span>

<span data-ttu-id="67973-128">O compartilhamento de superfície não sincronizado tem suporte do tempo de execução do Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="67973-128">Unsynchronized surface sharing is supported by the Direct3D 9Ex runtime.</span></span> <span data-ttu-id="67973-129">Os aplicativos de vídeo baseados em DXVA podem usar o auxiliar de interoperabilidade do Direct3D 9Ex e DXGI para a interoperabilidade de DXVA baseada em Direct3D 9Ex com o Direct3D 11 para o sombreador de computação ou podem interoperar com Direct2D para controles 2D ou renderização de texto.</span><span class="sxs-lookup"><span data-stu-id="67973-129">DXVA-based video applications can use the Direct3D 9Ex and DXGI interoperability helper for Direct3D 9Ex-based DXVA interoperability with Direct3D 11 for compute shader, or can interoperate with Direct2D for 2D controls or text rendering.</span></span> <span data-ttu-id="67973-130">O WIC e o DirectWrite também interoperam com GDI, Direct2D e por associação, outras APIs do Direct3D.</span><span class="sxs-lookup"><span data-stu-id="67973-130">WIC and DirectWrite also interoperate with GDI, Direct2D, and by association, other Direct3D APIs.</span></span>

<span data-ttu-id="67973-131">O Direct3D 10,0, o Direct3D 9c e os tempos de execução do Direct3D mais antigos não oferecem suporte a superfícies compartilhadas.</span><span class="sxs-lookup"><span data-stu-id="67973-131">Direct3D 10.0, Direct3D 9c, and older Direct3D runtimes do not support shared surfaces.</span></span> <span data-ttu-id="67973-132">As cópias de memória do sistema continuarão sendo usadas para interoperabilidade com APIs baseadas em GDI ou DXGI.</span><span class="sxs-lookup"><span data-stu-id="67973-132">System memory copies will continue to be used for interoperability with GDI or DXGI-based APIs.</span></span>

<span data-ttu-id="67973-133">Observe que os cenários de interoperabilidade neste documento referem-se a várias APIs de gráficos Renderizando em uma superfície de renderização compartilhada, em vez de na mesma janela do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="67973-133">Note that the interoperability scenarios within this document refer to multiple graphics APIs rendering to a shared rendering surface, rather than to the same application window.</span></span> <span data-ttu-id="67973-134">A sincronização de APIs separadas que visam superfícies diferentes que são compostas na mesma janela está fora do escopo deste documento.</span><span class="sxs-lookup"><span data-stu-id="67973-134">Synchronization for separate APIs targeting different surfaces that are then composited onto the same window is outside the scope of this paper.</span></span>

## <a name="api-interoperability-overview"></a><span data-ttu-id="67973-135">Visão geral da interoperabilidade de API</span><span class="sxs-lookup"><span data-stu-id="67973-135">API Interoperability Overview</span></span>

<span data-ttu-id="67973-136">A interoperabilidade do compartilhamento de superfície de APIs de gráficos do Windows pode ser descrita em termos de cenários de API para API e a funcionalidade de interoperabilidade correspondente.</span><span class="sxs-lookup"><span data-stu-id="67973-136">Surface sharing interoperability of Windows graphics APIs can be described in terms of API-to-API scenarios and the corresponding interoperability functionality.</span></span> <span data-ttu-id="67973-137">A partir do Windows 7 e a partir do Windows Vista SP2 com 7IP, novas APIs e runtimes associados incluem Direct2D e tecnologias relacionadas: Direct3D 11 e DXGI 1.1.</span><span class="sxs-lookup"><span data-stu-id="67973-137">As of Windows 7 and beginning with Windows Vista SP2 with 7IP, new APIs and associated runtimes include Direct2D and related technologies: Direct3D 11 and DXGI 1.1.</span></span> <span data-ttu-id="67973-138">O desempenho da GDI também foi aprimorado no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="67973-138">GDI performance was also improved in Windows 7.</span></span> <span data-ttu-id="67973-139">O Direct3D 10.1 foi introduzido no Windows Vista SP1.</span><span class="sxs-lookup"><span data-stu-id="67973-139">Direct3D 10.1 was introduced in Windows Vista SP1.</span></span> <span data-ttu-id="67973-140">O diagrama a seguir mostra o suporte à interoperabilidade entre APIs.</span><span class="sxs-lookup"><span data-stu-id="67973-140">The following diagram shows the interoperability support between APIs.</span></span>

![diagrama de suporte de interoperabilidade entre apis gráficas do Windows](images/surface-sharing-interoperability.png)

<span data-ttu-id="67973-142">Neste diagrama, as setas mostram cenários de interoperabilidade nos quais a mesma superfície pode ser acessível pelas APIs conectadas.</span><span class="sxs-lookup"><span data-stu-id="67973-142">In this diagram, arrows show interoperability scenarios in which the same surface can be accessible by the connected APIs.</span></span> <span data-ttu-id="67973-143">As setas azuis indicam mecanismos de interoperabilidade introduzidos no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="67973-143">Blue arrows indicate interoperability mechanisms introduced in Windows Vista.</span></span> <span data-ttu-id="67973-144">As setas verdes indicam suporte à interoperabilidade para novas APIs ou melhorias que ajudam as APIs mais antigas a interoperar com APIs mais novas.</span><span class="sxs-lookup"><span data-stu-id="67973-144">Green arrows indicate interoperability support for new APIs or improvements that help older APIs to interoperate with newer APIs.</span></span> <span data-ttu-id="67973-145">Por exemplo, as setas verdes representam o compartilhamento de dispositivos, o suporte à superfície compartilhada sincronizada, o auxiliar de sincronização direct3D 9Ex/DXGI e a obtenção de um contexto de dispositivo GDI de uma superfície compatível.</span><span class="sxs-lookup"><span data-stu-id="67973-145">For example, green arrows represent device sharing, synchronized shared surface support, Direct3D 9Ex/DXGI synchronization helper, and obtaining a GDI device context from a compatible surface.</span></span>

## <a name="interoperability-scenarios"></a><span data-ttu-id="67973-146">Cenários de interoperabilidade</span><span class="sxs-lookup"><span data-stu-id="67973-146">Interoperability Scenarios</span></span>

<span data-ttu-id="67973-147">A partir do Windows 7 e do Windows Vista 7IP, as ofertas base das APIs gráficas do Windows oferecem suporte à renderização de várias APIs para a mesma superfície do DXGI 1.1.</span><span class="sxs-lookup"><span data-stu-id="67973-147">As of Windows 7 and Windows Vista 7IP, mainstream offerings from Windows graphics APIs support multiple APIs rendering to the same DXGI 1.1 surface.</span></span>

<span data-ttu-id="67973-148">**Direct3D 11, Direct3D 10.1, Direct2D — Interoperabilidade entre si**</span><span class="sxs-lookup"><span data-stu-id="67973-148">**Direct3D 11, Direct3D 10.1, Direct2D — Interoperability with each other**</span></span>

<span data-ttu-id="67973-149">As APIs Direct3D 11, Direct3D 10.1 e Direct2D (e suas APIs relacionadas, como DirectWrite e WIC) podem interoperar entre si usando o compartilhamento de dispositivos Direct3D 10.1 ou superfícies compartilhadas sincronizadas.</span><span class="sxs-lookup"><span data-stu-id="67973-149">Direct3D 11, Direct3D 10.1 and Direct2D APIs (and its related APIs such as DirectWrite and WIC) can interoperate with each other using either Direct3D 10.1 device sharing or synchronized shared surfaces.</span></span>

### <a name="direct3d-101-device-sharing-with-direct2d"></a><span data-ttu-id="67973-150">Compartilhamento de dispositivo do Direct3D 10.1 com Direct2D</span><span class="sxs-lookup"><span data-stu-id="67973-150">Direct3D 10.1 Device Sharing with Direct2D</span></span>

<span data-ttu-id="67973-151">O compartilhamento de dispositivos entre o Direct2D e o Direct3D 10.1 permite que um aplicativo use ambas as APIs para renderizar de forma direta e eficiente na mesma superfície do DXGI 1.1, usando o mesmo objeto de dispositivo Direct3D subjacente.</span><span class="sxs-lookup"><span data-stu-id="67973-151">Device sharing between Direct2D and Direct3D 10.1 allows an application to use both APIs to seamlessly and efficiently render onto the same DXGI 1.1 surface, using the same underlying Direct3D device object.</span></span> <span data-ttu-id="67973-152">O Direct2D fornece a capacidade de chamar APIs do Direct2D usando um dispositivo Direct3D 10.1 existente, aproveitando o fato de que o Direct2D é criado com base nos runtimes do Direct3D 10.1 e do DXGI 1.1.</span><span class="sxs-lookup"><span data-stu-id="67973-152">Direct2D provides the ability to call Direct2D APIs using an existing Direct3D 10.1 device, leveraging the fact that Direct2D is built on top of Direct3D 10.1 and DXGI 1.1 runtimes.</span></span> <span data-ttu-id="67973-153">Os snippets de código a seguir ilustram como o Direct2D obtém o destino de renderização do dispositivo Direct3D 10.1 de uma superfície DXGI 1.1 associada ao dispositivo.</span><span class="sxs-lookup"><span data-stu-id="67973-153">The following code snippets illustrate how Direct2D obtains the Direct3D 10.1 device render target from a DXGI 1.1 surface associated with the device.</span></span> <span data-ttu-id="67973-154">O destino de renderização do dispositivo Direct3D 10,1 pode executar chamadas de desenho Direct2D entre as APIs BeginDraw e EndDraw.</span><span class="sxs-lookup"><span data-stu-id="67973-154">The Direct3D 10.1 device render target can execute Direct2D drawing calls between BeginDraw and EndDraw APIs.</span></span>


```C++
// Direct3D 10.1 Device and Swapchain creation
HRESULT hr = D3D10CreateDeviceandSwapChain1(
                pAdapter,
                DriverType,
                Software,
                D3D10_CREATE_DEVICE_BGRA_SUPPORT,
                featureLevel,
                D3D10_1_SDK_VERSION,
                pSwapChainDesc,
                &pSwapChain,
                &pDevice
                );

hr = pSwapChain->GetBuffer(
        0,
        __uuidof(IDXGISurface),
        (void **)&pDXGIBackBuffer
        ));

// Direct3D 10.1 API rendering calls
...

hr = D2D1CreateFactory(
        D2D1_FACTORY_TYPE_SINGLE_THREADED,
        &m_spD2DFactory
        ));

pD2DFactory->CreateDxgiSurfaceRenderTarget(
        pDXGIBackBuffer,
        &renderTargetProperties,
        &pD2DBackBufferRenderTarget
        ));
...

pD2DBackBufferRenderTarget->BeginDraw();
//Direct2D API rendering calls
...

pD2DBackBufferRenderTarget->EndDraw();

pSwapChain->Present(0, 0);
```



<span data-ttu-id="67973-155">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="67973-155">**Remarks**</span></span>

-   <span data-ttu-id="67973-156">O dispositivo Direct3D 10,1 associado deve dar suporte ao formato BGRA.</span><span class="sxs-lookup"><span data-stu-id="67973-156">The associated Direct3D 10.1 device must support BGRA format.</span></span> <span data-ttu-id="67973-157">Esse dispositivo foi criado chamando D3D10CreateDevice1 com o parâmetro D3D10 \_ criar \_ dispositivo \_ BGRA \_ suporte.</span><span class="sxs-lookup"><span data-stu-id="67973-157">That device was created by calling D3D10CreateDevice1 with parameter D3D10\_CREATE\_DEVICE\_BGRA\_SUPPORT.</span></span> <span data-ttu-id="67973-158">O formato BGRA tem suporte a partir do nível de recurso 9,1 do Direct3D 10.</span><span class="sxs-lookup"><span data-stu-id="67973-158">BGRA format is supported starting with Direct3D 10 feature level 9.1.</span></span>
-   <span data-ttu-id="67973-159">O aplicativo não deve criar várias ID2D1RenderTargets associando ao mesmo dispositivo Direct3D 10.1.</span><span class="sxs-lookup"><span data-stu-id="67973-159">The application should not create multiple ID2D1RenderTargets associating to the same Direct3D10.1 device.</span></span>
-   <span data-ttu-id="67973-160">Para obter um desempenho ideal, mantenha pelo menos um recurso em todos os momentos, como texturas ou superfícies associadas ao dispositivo.</span><span class="sxs-lookup"><span data-stu-id="67973-160">For optimal performance, keep at least one resource around at all times, such as textures or surfaces associated with the device.</span></span>

<span data-ttu-id="67973-161">O compartilhamento de dispositivo é adequado para uso em processo e de thread único de um dispositivo de renderização compartilhado por APIs de renderização Direct3D 10,1 e Direct2D.</span><span class="sxs-lookup"><span data-stu-id="67973-161">Device sharing is suitable for in-process, single-threaded usage of one rendering device shared by both Direct3D 10.1 and Direct2D rendering APIs.</span></span> <span data-ttu-id="67973-162">As superfícies de compartilhamento sincronizadas permitem o uso de vários threads, em processo e fora do processo de vários dispositivos de renderização usados pelas APIs do Direct3D 10,1, Direct2D e Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="67973-162">Synchronized shared surfaces enable multi-threaded, in-process and out-of-process usage of multiple rendering devices used by Direct3D 10.1, Direct2D and Direct3D 11 APIs.</span></span>

<span data-ttu-id="67973-163">Outro método de interoperabilidade entre Direct3D 10,1 e Direct2D é usando ID3D1RenderTarget:: CreateSharedBitmap, que cria um objeto ID2D1Bitmap de IDXGISurface.</span><span class="sxs-lookup"><span data-stu-id="67973-163">Another method of Direct3D 10.1 and Direct2D interoperability is by using ID3D1RenderTarget::CreateSharedBitmap, which creates an ID2D1Bitmap object from IDXGISurface.</span></span> <span data-ttu-id="67973-164">Você pode escrever uma cena do Direct3D 10.1 no bitmap e renderizá-la com Direct2D.</span><span class="sxs-lookup"><span data-stu-id="67973-164">You can write a Direct3D10.1 scene to the bitmap and render it with Direct2D.</span></span> <span data-ttu-id="67973-165">Para obter mais informações, consulte [método ID2D1RenderTarget:: CreateSharedBitmap](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap).</span><span class="sxs-lookup"><span data-stu-id="67973-165">For more information, see [ID2D1RenderTarget::CreateSharedBitmap Method](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap).</span></span>

### <a name="direct2d-software-rasterization"></a><span data-ttu-id="67973-166">Rasterização de software Direct2D</span><span class="sxs-lookup"><span data-stu-id="67973-166">Direct2D Software Rasterization</span></span>

<span data-ttu-id="67973-167">Não há suporte para o compartilhamento de dispositivos com o Direct3D 10,1 ao usar o processador de software Direct2D, por exemplo, especificando D2D1 \_ \_ renderização de destino \_ \_ forçada de \_ \_ processamento de software em d2d1 \_ renderizar \_ o uso de destino \_ ao criar um destino de renderização Direct2D.</span><span class="sxs-lookup"><span data-stu-id="67973-167">Device sharing with Direct3D 10.1 is not supported when using the Direct2D software renderer, for example, by specifying D2D1\_RENDER\_TARGET\_USAGE\_FORCE\_SOFTWARE\_RENDERING in D2D1\_RENDER\_TARGET\_USAGE when creating a Direct2D render target.</span></span>

<span data-ttu-id="67973-168">O Direct2D pode usar o rasterizador de software WARP10 para compartilhar o dispositivo com o Direct3D 10 ou o Direct3D 11, mas o desempenho diminui significativamente.</span><span class="sxs-lookup"><span data-stu-id="67973-168">Direct2D can use the WARP10 software rasterizer to share device with Direct3D 10 or Direct3D 11, but the performance declines significantly.</span></span>

### <a name="dxgi-11-synchronized-shared-surfaces"></a><span data-ttu-id="67973-169">Superfícies compartilhadas sincronizadas do DXGI 1,1</span><span class="sxs-lookup"><span data-stu-id="67973-169">DXGI 1.1 Synchronized Shared Surfaces</span></span>

<span data-ttu-id="67973-170">As APIs do Direct3D 11, Direct3D 10,1 e Direct2D usam DXGI 1,1, que fornece a funcionalidade para sincronizar a leitura e gravação na mesma superfície de memória de vídeo (DXGISurface1) por dois ou mais dispositivos Direct3D.</span><span class="sxs-lookup"><span data-stu-id="67973-170">Direct3D 11, Direct3D 10.1 and Direct2D APIs all use DXGI 1.1, which provides the functionality to synchronize reading from and writing to the same video memory surface (DXGISurface1) by two or more Direct3D devices.</span></span> <span data-ttu-id="67973-171">Os dispositivos de renderização que usam superfícies compartilhadas sincronizadas podem ser dispositivos Direct3D 10.1 ou Direct3D 11, cada um em execução no mesmo processo ou processos cruzados.</span><span class="sxs-lookup"><span data-stu-id="67973-171">The rendering devices using synchronized shared surfaces can be Direct3D 10.1 or Direct3D 11 devices, each running in the same process or cross-processes.</span></span>

<span data-ttu-id="67973-172">Os aplicativos podem usar superfícies compartilhadas sincronizadas para interoperar entre qualquer dispositivo baseado em DXGI 1.1, como Direct3D 11 e Direct3D 10.1 ou entre Direct3D 11 e Direct2D, obtendo o dispositivo Direct3D 10.1 do objeto de destino de renderização direct2D.</span><span class="sxs-lookup"><span data-stu-id="67973-172">Applications can use synchronized shared surfaces to interoperate between any DXGI 1.1-based devices, such as Direct3D 11 and Direct3D 10.1, or between Direct3D 11 and Direct2D, by obtaining the Direct3D 10.1 device from Direct2D render target object.</span></span>

<span data-ttu-id="67973-173">No Direct3D 10.1 e em APIs posteriores, para usar o DXGI 1.1, verifique se o dispositivo Direct3D foi criado usando um objeto de adaptador DXGI 1.1, que é enumerado do objeto de fábrica DXGI 1.1.</span><span class="sxs-lookup"><span data-stu-id="67973-173">In Direct3D 10.1 and later APIs, to use DXGI 1.1, ensure that the Direct3D device is created using a DXGI 1.1 adapter object, which is enumerated from the DXGI 1.1 factory object.</span></span> <span data-ttu-id="67973-174">Chame CreateDXGIFactory1 para criar o objeto IDXGIFactory1 e EnumAdapters1 para enumerar o objeto IDXGIAdapter1.</span><span class="sxs-lookup"><span data-stu-id="67973-174">Call CreateDXGIFactory1 to create the IDXGIFactory1 object, and EnumAdapters1 to enumerate the IDXGIAdapter1 object.</span></span> <span data-ttu-id="67973-175">O objeto IDXGIAdapter1 precisa ser passado como parte da chamada D3D10CreateDevice ou D3D10CreateDeviceAndSwapChain.</span><span class="sxs-lookup"><span data-stu-id="67973-175">The IDXGIAdapter1 object needs to be passed in as part of D3D10CreateDevice or D3D10CreateDeviceAndSwapChain call.</span></span> <span data-ttu-id="67973-176">Para obter mais informações sobre AS APIs do DXGI 1.1, consulte o Guia de Programação [para DXGI.](https://msdn.microsoft.com/library/ee418147(VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="67973-176">For more information on DXGI 1.1 APIs, please refer to the [Programming Guide for DXGI](https://msdn.microsoft.com/library/ee418147(VS.85).aspx).</span></span>

### <a name="apis"></a><span data-ttu-id="67973-177">APIs</span><span class="sxs-lookup"><span data-stu-id="67973-177">APIs</span></span>

<span data-ttu-id="67973-178">**D3D10 \_ RESOURCE \_ MISC \_ SHARED \_ KEYEDMUTEX**</span><span class="sxs-lookup"><span data-stu-id="67973-178">**D3D10\_RESOURCE\_MISC\_SHARED\_KEYEDMUTEX**</span></span>  
<span data-ttu-id="67973-179">Ao criar o recurso compartilhado sincronizado, de definido D3D10 \_ RESOURCE \_ MISC \_ SHARED KEYEDMUTEX no SINALIZADOR MISC de RECURSOS \_ D3D10. \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="67973-179">When creating the synchronized shared resource, set D3D10\_RESOURCE\_MISC\_SHARED\_KEYEDMUTEX in D3D10\_RESOURCE\_MISC\_FLAG.</span></span>  


```C++
typedef enum D3D10_RESOURCE_MISC_FLAG {
    D3D10_RESOURCE_MISC_GENERATE_MIPS      = 0x1L,
    D3D10_RESOURCE_MISC_SHARED             = 0x2L,
    D3D10_RESOURCE_MISC_TEXTURECUBE        = 0x4L,
    D3D10_RESOURCE_MISC_SHARED_KEYEDMUTEX  = 0x10L,
    D3D10_RESOURCE_MISC_GDI_COMPATIBLE     = 0x20L,
}   D3D10_RESOURCE_MISC_FLAG;
```



<span data-ttu-id="67973-180">**D3D10 \_ RESOURCE \_ MISC \_ SHARED \_ KEYEDMUTEX**</span><span class="sxs-lookup"><span data-stu-id="67973-180">**D3D10\_RESOURCE\_MISC\_SHARED\_KEYEDMUTEX**</span></span>  
<span data-ttu-id="67973-181">Permite que o recurso criado seja sincronizado usando as APIs IDXGIKeyedMutex::AcquireSync e ReleaseSync.</span><span class="sxs-lookup"><span data-stu-id="67973-181">Enables the resource created to be synchronized using the IDXGIKeyedMutex::AcquireSync and ReleaseSync APIs.</span></span> <span data-ttu-id="67973-182">As APIs direct3D 10.1 de criação de recursos a seguir que levam um parâmetro D3D10 RESOURCE MISC FLAG foram estendidas para dar suporte ao \_ \_ novo \_ sinalizador.</span><span class="sxs-lookup"><span data-stu-id="67973-182">The following resource creation Direct3D 10.1 APIs that all take a D3D10\_RESOURCE\_MISC\_FLAG parameter have been extended to support the new flag.</span></span>  

-   <span data-ttu-id="67973-183">ID3D10Device1::CreateTexture1D</span><span class="sxs-lookup"><span data-stu-id="67973-183">ID3D10Device1::CreateTexture1D</span></span>
-   <span data-ttu-id="67973-184">ID3D10Device1::CreateTexture2D</span><span class="sxs-lookup"><span data-stu-id="67973-184">ID3D10Device1::CreateTexture2D</span></span>
-   <span data-ttu-id="67973-185">ID3D10Device1::CreateTexture3D</span><span class="sxs-lookup"><span data-stu-id="67973-185">ID3D10Device1::CreateTexture3D</span></span>
-   <span data-ttu-id="67973-186">ID3D10Device1::CreateBuffer</span><span class="sxs-lookup"><span data-stu-id="67973-186">ID3D10Device1::CreateBuffer</span></span>

  
<span data-ttu-id="67973-187">Se qualquer uma das funções listadas for chamada com o sinalizador D3D10 RESOURCE MISC SHARED KEYEDMUTEX definido, a interface retornada poderá ser consultada para uma \_ \_ interface \_ \_ IDXGIKeyedMutex, que implementa APIs AcquireSync e ReleaseSync para sincronizar o acesso à superfície.</span><span class="sxs-lookup"><span data-stu-id="67973-187">If any of the listed functions are called with the D3D10\_RESOURCE\_MISC\_SHARED\_KEYEDMUTEX flag set, the interface returned can be queried for an IDXGIKeyedMutex interface, which implements AcquireSync and ReleaseSync APIs to synchronize access to the surface.</span></span> <span data-ttu-id="67973-188">O dispositivo que cria a superfície e qualquer outro dispositivo que abra a superfície (usando OpenSharedResource) é necessário para chamar IDXGIKeyedMutex:: AcquireSync antes de qualquer comando de renderização na superfície e IDXGIKeyedMutex:: ReleaseSync quando a renderização é concluída.</span><span class="sxs-lookup"><span data-stu-id="67973-188">The device creating the surface and any other device opening the surface (using OpenSharedResource) is required to call IDXGIKeyedMutex::AcquireSync before any rendering commands to the surface, and IDXGIKeyedMutex::ReleaseSync when it is done rendering.</span></span>  
<span data-ttu-id="67973-189">Os dispositivos WARP e REF não dão suporte a recursos compartilhados.</span><span class="sxs-lookup"><span data-stu-id="67973-189">WARP and REF devices do not support shared resources.</span></span> <span data-ttu-id="67973-190">A tentativa de criar um recurso com esse sinalizador em um dispositivo WARP ou REF fará com que o método Create retorne um \_ código de erro E OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="67973-190">Attempting to create a resource with this flag on either a WARP or REF device will cause the create method to return an E\_OUTOFMEMORY error code.</span></span>  
<span data-ttu-id="67973-191">**INTERFACE IDXGIKEYEDMUTEX**</span><span class="sxs-lookup"><span data-stu-id="67973-191">**IDXGIKEYEDMUTEX INTERFACE**</span></span>  
<span data-ttu-id="67973-192">Uma nova interface no DXGI 1,1, IDXGIKeyedMutex, representa um mutex com chave, que permite o acesso exclusivo a um recurso compartilhado que é usado por vários dispositivos.</span><span class="sxs-lookup"><span data-stu-id="67973-192">A new interface in DXGI 1.1, IDXGIKeyedMutex, represents a keyed mutex, which allows exclusive access to a shared resource that is used by multiple devices.</span></span> <span data-ttu-id="67973-193">Para obter a documentação de referência sobre essa interface e seus dois métodos, AcquireSync e ReleaseSync, consulte [IDXGIKeyedMutex](https://msdn.microsoft.com/library/ee421920(VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="67973-193">For reference documentation about this interface and its two methods, AcquireSync and ReleaseSync, see [IDXGIKeyedMutex](https://msdn.microsoft.com/library/ee421920(VS.85).aspx).</span></span>  
</dl>

### <a name="sample-synchronized-surface-sharing-between-two-direct3d-101-devices"></a><span data-ttu-id="67973-194">Exemplo: compartilhamento de superfície sincronizado entre dois dispositivos Direct3D 10,1</span><span class="sxs-lookup"><span data-stu-id="67973-194">Sample: Synchronized Surface Sharing Between two Direct3D 10.1 Devices</span></span>

<span data-ttu-id="67973-195">O exemplo a seguir ilustra o compartilhamento de uma superfície entre dois dispositivos Direct3D 10,1.</span><span class="sxs-lookup"><span data-stu-id="67973-195">The example below illustrates sharing a surface between two Direct3D 10.1 devices.</span></span> <span data-ttu-id="67973-196">A superfície compartilhada sincronizada é criada por um dispositivo Direct3D 10.1.</span><span class="sxs-lookup"><span data-stu-id="67973-196">The synchronized shared surface is created by a Direct3D10.1 device.</span></span>


```C++
// Create Sync Shared Surface using Direct3D10.1 Device 1.
D3D10_TEXTURE2D_DESC desc;
ZeroMemory( &desc, sizeof(desc) );
desc.Width = width;
desc.Height = height;
desc.MipLevels = 1;
desc.ArraySize = 1;
// must match swapchain format in order to CopySubresourceRegion.
desc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
desc.SampleDesc.Count = 1;
desc.Usage = D3D10_USAGE_DEFAULT;
// creates 2D texture as a Synchronized Shared Surface.
desc.MiscFlags = D3D10_RESOURCE_MISC_SHARED_KEYEDMUTEX;
desc.BindFlags = D3D10_BIND_RENDER_TARGET | D3D10_BIND_SHADER_RESOURCE;
ID3D10Texture2D* g_pShared = NULL;
g_pd3dDevice1->CreateTexture2D( &desc, NULL, &g_pShared );

// QI IDXGIResource interface to synchronized shared surface.
IDXGIResource* pDXGIResource = NULL;
g_pShared->QueryInterface(__uuidof(IDXGIResource), (LPVOID*) &pDXGIResource);

// obtain handle to IDXGIResource object.
pDXGIResource->GetSharedHandle(&g_hsharedHandle);
pDXGIResource->Release();
if ( !g_hsharedHandle )
    return E_FAIL;

// QI IDXGIKeyedMutex interface of synchronized shared surface's resource handle.
hr = g_pShared->QueryInterface( __uuidof(IDXGIKeyedMutex),
    (LPVOID*)&g_pDXGIKeyedMutex_dev1 );
If ( FAILED( hr ) || ( g_pDXGIKeyedMutex_dev1 == NULL ) )
    return E_FAIL;
```



<span data-ttu-id="67973-197">O mesmo dispositivo Direct3D 10.1 pode obter a superfície compartilhada sincronizada para renderização chamando AcquireSync e, em seguida, liberando a superfície para a renderização do outro dispositivo chamando ReleaseSync.</span><span class="sxs-lookup"><span data-stu-id="67973-197">The same Direct3D10.1 device can obtain the synchronized shared surface for rendering by calling AcquireSync, then releasing the surface for the other device's rendering by calling ReleaseSync.</span></span> <span data-ttu-id="67973-198">Quando não estiver compartilhando a superfície compartilhada sincronizada com qualquer outro dispositivo Direct3D, o criador poderá obter e liberar a superfície compartilhada sincronizada (para iniciar e encerrar a renderização) adquirindo e liberando usando o mesmo valor de chave.</span><span class="sxs-lookup"><span data-stu-id="67973-198">When not sharing the synchronized shared surface with any other Direct3D device, the creator can obtain and release the synchronized shared surface (to start and end rendering) by acquiring and release using the same key value.</span></span>


```C++
// Obtain handle to Sync Shared Surface created by Direct3D10.1 Device 1.
hr = g_pd3dDevice2->OpenSharedResource( g_hsharedHandle,__uuidof(ID3D10Texture2D),
                                        (LPVOID*) &g_pdev2Shared);
if (FAILED (hr))
    return hr;
hr = g_pdev2Shared->QueryInterface( __uuidof(IDXGIKeyedMutex),
                                    (LPVOID*) &g_pDXGIKeyedMutex_dev2);
if( FAILED( hr ) || ( g_pDXGIKeyedMutex_dev2 == NULL ) )
    return E_FAIL;

// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 2.
UINT acqKey = 1;
UINT relKey = 0;
DWORD timeOut = 5;
DWORD result = g_pDXGIKeyedMutex_dev2->AcquireSync(acqKey, timeOut);
if ( result == WAIT_OBJECT_0 )
    // Rendering calls using Device 2.
else
    // Handle unable to acquire shared surface error.
result = g_pDXGIKeyedMutex_dev2->ReleaseSync(relKey));
if (result == WAIT_OBJECT_0)
    return S_OK;
```



<span data-ttu-id="67973-199">O segundo dispositivo Direct3D 10.1 pode obter a superfície compartilhada sincronizada para renderização chamando AcquireSync e, em seguida, liberando a superfície para a renderização do primeiro dispositivo chamando ReleaseSync.</span><span class="sxs-lookup"><span data-stu-id="67973-199">The second Direct3D10.1 device can obtain the synchronized shared surface for rendering by calling AcquireSync, then releasing the surface for the first device's rendering by calling ReleaseSync.</span></span> <span data-ttu-id="67973-200">Observe que o dispositivo 2 é capaz de adquirir a superfície compartilhada sincronizada usando o mesmo valor de chave que aquela especificada na chamada ReleaseSync pelo dispositivo 1.</span><span class="sxs-lookup"><span data-stu-id="67973-200">Note that device 2 is able to acquire the synchronized shared surface using the same key value as the one specified in the ReleaseSync call by device 1.</span></span>


```C++
// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 1.
UINT acqKey = 0;
UINT relKey = 1;
DWORD timeOut = 5;
DWORD result = g_pDXGIKeyedMutex_dev1->AcquireSync(acqKey, timeOut);
if (result == WAIT_OBJECT_0)
    // Rendering calls using Device 1.
else
    // Handle unable to acquire shared surface error.
result = g_pDXGIKeyedMutex_dev1->ReleaseSync(relKey));
if ( result == WAIT_OBJECT_0 )
    return S_OK;
```



<span data-ttu-id="67973-201">Dispositivos adicionais que compartilham a mesma superfície podem assumir a compra e a liberação da superfície usando chaves adicionais, conforme mostrado nas chamadas a seguir.</span><span class="sxs-lookup"><span data-stu-id="67973-201">Additional devices sharing the same surface can take turns acquiring and releasing the surface by using additional keys, as shown in the following calls.</span></span>


```C++
// Within Device 1's process/thread:
// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 1
result = g_pDXGIKeyedMutex_dev1->AcquireSync(0, timeOut);
// Rendering calls using Device 1
...
result = g_pDXGIKeyedMutex_dev1->ReleaseSync(1);
...
////////////////////////////////////////////////////////////////////////////
// Within Device 2's process/thread:
// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 2
result = g_pDXGIKeyedMutex_dev2->AcquireSync(1, timeOut);
// Rendering calls using Device 2
...
result = g_pDXGIKeyedMutex_dev1->ReleaseSync(2);

////////////////////////////////////////////////////////////////////////////
// Within Device 3's process/thread:
// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 3
result = g_pDXGIKeyedMutex_dev1->AcquireSync(2, timeOut);
// Rendering calls using Device 3
...
result = g_pDXGIKeyedMutex_dev1->ReleaseSync(0);
...
```



<span data-ttu-id="67973-202">Observe que um aplicativo do mundo real sempre pode renderizar para uma superfície intermediária que é copiada para a superfície compartilhada para impedir que qualquer dispositivo que aguarda em outro dispositivo que compartilhe a superfície.</span><span class="sxs-lookup"><span data-stu-id="67973-202">Note that a real-world application might always render to an intermediate surface that is then copied into the shared surface to prevent any one device waiting on another device that shares the surface.</span></span>

### <a name="using-synchronized-shared-surfaces-with-direct2d-and-direct3d-11"></a><span data-ttu-id="67973-203">Usando superfícies compartilhadas sincronizadas com Direct2D e Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="67973-203">Using Synchronized Shared Surfaces with Direct2D and Direct3D 11</span></span>

<span data-ttu-id="67973-204">Da mesma forma, para compartilhar entre as APIs direct3D 11 e Direct3D 10.1, uma superfície compartilhada sincronizada pode ser criada a partir de um dispositivo de API e compartilhada com os outros dispositivos de API, dentro ou fora do processo.</span><span class="sxs-lookup"><span data-stu-id="67973-204">Similarly, for sharing between Direct3D 11 and Direct3D 10.1 APIs, a synchronized shared surface can be created from either API device and shared with the other API device(s), in or out of process.</span></span>

<span data-ttu-id="67973-205">Os aplicativos que usam o Direct2D podem compartilhar um dispositivo Direct3D 10.1 e usar uma superfície compartilhada sincronizada para interoperar com o Direct3D 11 ou outros dispositivos Direct3D 10.1, independentemente de pertencerem ao mesmo processo ou processos diferentes.</span><span class="sxs-lookup"><span data-stu-id="67973-205">Applications that use Direct2D can share a Direct3D 10.1 device and use a synchronized shared surface to interoperate with Direct3D 11 or other Direct3D 10.1 devices, whether they belong to the same process or different processes.</span></span> <span data-ttu-id="67973-206">No entanto, para aplicativos de processo único e de thread único, o compartilhamento de dispositivos é o método de interoperabilidade mais eficiente e de alto desempenho entre o Direct2D e o Direct3D 10 ou Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="67973-206">However, for single-process, single-thread applications, device sharing is the most high-performance and efficient method of interoperability between Direct2D and either Direct3D 10 or Direct3D 11.</span></span>

### <a name="software-rasterizer"></a><span data-ttu-id="67973-207">Software Rasterizer</span><span class="sxs-lookup"><span data-stu-id="67973-207">Software Rasterizer</span></span>

<span data-ttu-id="67973-208">Não há suporte para superfícies compartilhadas sincronizadas quando os aplicativos usam os rasterizadores de software Direct3D ou Direct2D, incluindo o rasterizador de referência e o WARP, em vez de usar aceleração de hardware de gráficos.</span><span class="sxs-lookup"><span data-stu-id="67973-208">Synchronized shared surfaces are not supported when applications use the Direct3D or Direct2D software rasterizers, including the reference rasterizer and WARP, instead of using graphics hardware acceleration.</span></span>

### <a name="interoperability-between-direct3d-9ex-and-dxgi-based-apis"></a><span data-ttu-id="67973-209">Interoperabilidade entre o Direct3D 9Ex e as APIs baseadas em DXGI</span><span class="sxs-lookup"><span data-stu-id="67973-209">Interoperability between Direct3D 9Ex and DXGI based APIs</span></span>

<span data-ttu-id="67973-210">As APIs do Direct3D 9Ex incluíam a noção de compartilhamento de superfície para permitir que outras APIs leiam da superfície compartilhada.</span><span class="sxs-lookup"><span data-stu-id="67973-210">Direct3D 9Ex APIs included the notion of surface sharing to allow other APIs to read from the shared surface.</span></span> <span data-ttu-id="67973-211">Para compartilhar a leitura e a escrita em uma superfície compartilhada do Direct3D 9Ex, você deve adicionar a sincronização manual ao próprio aplicativo.</span><span class="sxs-lookup"><span data-stu-id="67973-211">In order to share reading and writing to a Direct3D 9Ex shared surface, you must add manual synchronization to the application itself.</span></span>

### <a name="direct3d-9ex-shared-surfaces-plus-manual-synchronization-helper"></a><span data-ttu-id="67973-212">Direct3D 9Ex Shared Surfaces Plus Manual Synchronization Helper</span><span class="sxs-lookup"><span data-stu-id="67973-212">Direct3D 9Ex Shared Surfaces Plus Manual Synchronization Helper</span></span>

<span data-ttu-id="67973-213">A tarefa mais fundamental na interoperabilidade direct3D 9Ex e Direct3D 10 ou 11 é passar uma única superfície do primeiro dispositivo (dispositivo A) para o segundo (dispositivo B), de forma que, quando o dispositivo B adquire um alça na superfície, a renderização do dispositivo A é garantida como concluída.</span><span class="sxs-lookup"><span data-stu-id="67973-213">The most fundamental task in Direct3D 9Ex and Direct3D 10 or 11 interoperability is passing a single surface from the first device (device A) to the second (device B) such that when device B acquires a handle on the surface, device A's rendering is guaranteed to have completed.</span></span> <span data-ttu-id="67973-214">Portanto, o dispositivo B pode usar essa superfície sem se preocupar.</span><span class="sxs-lookup"><span data-stu-id="67973-214">Therefore, device B can use this surface without worry.</span></span> <span data-ttu-id="67973-215">Isso é muito semelhante ao problema de produtor-consumidor clássico e essa discussão modela o problema dessa maneira.</span><span class="sxs-lookup"><span data-stu-id="67973-215">This is very similar to the classic producer-consumer problem and this discussion models the problem that way.</span></span> <span data-ttu-id="67973-216">O primeiro dispositivo que usa a superfície e, em seguida, o abandona é o produtor (dispositivo A) e o dispositivo que está aguardando inicialmente é o consumidor (dispositivo B).</span><span class="sxs-lookup"><span data-stu-id="67973-216">The first device that uses the surface and then relinquishes it is the producer (Device A), and the device that is initially waiting is the consumer (Device B).</span></span> <span data-ttu-id="67973-217">Qualquer aplicativo do mundo real é mais sofisticado do que isso e encadeará vários blocos de construção de produtor-consumidor para criar a funcionalidade desejada.</span><span class="sxs-lookup"><span data-stu-id="67973-217">Any real-world application is more sophisticated than this, and will chain together multiple producer-consumer building blocks to create the desired functionality.</span></span>

<span data-ttu-id="67973-218">Os blocos de construção produtor-consumidor são implementados no auxiliar usando uma fila de superfícies.</span><span class="sxs-lookup"><span data-stu-id="67973-218">The producer-consumer building blocks are implemented in the helper by using a queue of surfaces.</span></span> <span data-ttu-id="67973-219">As superfícies são enfileiradas pelo produtor e removidas da fila pelo consumidor.</span><span class="sxs-lookup"><span data-stu-id="67973-219">Surfaces are enqueued by the producer and dequeued by the consumer.</span></span> <span data-ttu-id="67973-220">O auxiliar apresenta três interfaces COM: ISurfaceQueue, ISurfaceProducer e ISurfaceConsumer.</span><span class="sxs-lookup"><span data-stu-id="67973-220">The helper introduces three COM interfaces: ISurfaceQueue, ISurfaceProducer, and ISurfaceConsumer.</span></span>

### <a name="high-level-overview-of-helper"></a><span data-ttu-id="67973-221">High-Level visão geral do auxiliar</span><span class="sxs-lookup"><span data-stu-id="67973-221">High-Level Overview of Helper</span></span>

<span data-ttu-id="67973-222">O objeto ISurfaceQueue é o bloco de construção para usar as superfícies compartilhadas.</span><span class="sxs-lookup"><span data-stu-id="67973-222">The ISurfaceQueue object is the building block for using the shared surfaces.</span></span> <span data-ttu-id="67973-223">Ele é criado com um dispositivo Direct3D inicializado e uma descrição para criar um número fixo de superfícies compartilhadas.</span><span class="sxs-lookup"><span data-stu-id="67973-223">It is created with an initialized Direct3D device and a description to create a fixed number of shared surfaces.</span></span> <span data-ttu-id="67973-224">O objeto de fila gerencia a criação de recursos e a abertura de código.</span><span class="sxs-lookup"><span data-stu-id="67973-224">The queue object manages creation of resources and opening of code.</span></span> <span data-ttu-id="67973-225">O número e o tipo de superfícies são fixos; Depois que as superfícies são criadas, o aplicativo não pode adicioná-las ou removê-las.</span><span class="sxs-lookup"><span data-stu-id="67973-225">The number and type of surfaces are fixed; once the surfaces are created, the application cannot add or remove them.</span></span>

<span data-ttu-id="67973-226">Cada instância do objeto ISurfaceQueue fornece um tipo de rua unidirecional que pode ser usada para enviar superfícies do dispositivo de produção para o dispositivo consumidor.</span><span class="sxs-lookup"><span data-stu-id="67973-226">Each instance of the ISurfaceQueue object provides a sort of one-way street that can be used to send surfaces from the producing device to the consuming device.</span></span> <span data-ttu-id="67973-227">Várias ruas unidirecionais podem ser usadas para habilitar cenários de compartilhamento de superfície entre dispositivos de aplicativos específicos.</span><span class="sxs-lookup"><span data-stu-id="67973-227">Multiple such one-way streets can be used to enable surface sharing scenarios between devices of specific applications.</span></span>

<span data-ttu-id="67973-228">**Tempo de vida de criação/objeto**</span><span class="sxs-lookup"><span data-stu-id="67973-228">**Creation/Object Lifetime**</span></span>  
<span data-ttu-id="67973-229">Há duas maneiras de criar o objeto de fila: por meio de CreateSurfaceQueue, ou por meio do método clone de ISurfaceQueue.</span><span class="sxs-lookup"><span data-stu-id="67973-229">There are two ways to create the queue object: through CreateSurfaceQueue, or through the Clone method of ISurfaceQueue.</span></span> <span data-ttu-id="67973-230">Como as interfaces são objetos COM, o gerenciamento de tempo de vida padrão COM é aplicável.</span><span class="sxs-lookup"><span data-stu-id="67973-230">Because the interfaces are COM objects, standard COM lifetime management applies.</span></span>  
<span data-ttu-id="67973-231">**Modelo de produtor/consumidor**</span><span class="sxs-lookup"><span data-stu-id="67973-231">**Producer/Consumer Model**</span></span>  
<span data-ttu-id="67973-232">Enqueue (): o produtor chama essa função para indicar que ela é feita com a superfície, que agora pode ser disponibilizada para outro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="67973-232">Enqueue (): The producer calls this function to indicate it is done with the surface, which can now become available to another device.</span></span> <span data-ttu-id="67973-233">Ao retornar dessa função, o dispositivo produtor não tem mais direitos à superfície e não é seguro continuar a usá-lo.</span><span class="sxs-lookup"><span data-stu-id="67973-233">Upon returning from this function, the producer device no longer has rights to the surface and it is unsafe to continue using it.</span></span>  
<span data-ttu-id="67973-234">Remover da fila (): o dispositivo consumidor chama essa função para obter uma superfície compartilhada.</span><span class="sxs-lookup"><span data-stu-id="67973-234">Dequeue (): The consuming device calls this function to get a shared surface.</span></span> <span data-ttu-id="67973-235">A API garante que todas as superfícies removidas da fila estejam prontas para serem usadas.</span><span class="sxs-lookup"><span data-stu-id="67973-235">The API guarantees that any dequeued surfaces are ready to be used.</span></span>  
<span data-ttu-id="67973-236">**Metadados**</span><span class="sxs-lookup"><span data-stu-id="67973-236">**Metadata**</span></span>  
<span data-ttu-id="67973-237">A API dá suporte à associação de metadados com as superfícies compartilhadas.</span><span class="sxs-lookup"><span data-stu-id="67973-237">The API supports associating metadata with the shared surfaces.</span></span>  
<span data-ttu-id="67973-238">Enqueue() tem a opção de especificar metadados adicionais que serão passados para o dispositivo consumidor.</span><span class="sxs-lookup"><span data-stu-id="67973-238">Enqueue() has the option of specifying additional metadata that will be passed to the consuming device.</span></span> <span data-ttu-id="67973-239">Os metadados devem ser menores que um máximo conhecido no momento da criação.</span><span class="sxs-lookup"><span data-stu-id="67973-239">The metadata must be less than a maximum known at creation time.</span></span>  
<span data-ttu-id="67973-240">Opcionalmente, Dequeue() pode passar um buffer e um ponteiro para o tamanho do buffer.</span><span class="sxs-lookup"><span data-stu-id="67973-240">Dequeue() can optionally pass a buffer and a pointer to the size of the buffer.</span></span> <span data-ttu-id="67973-241">A fila preenche o buffer com os metadados da chamada enfileirada correspondente.</span><span class="sxs-lookup"><span data-stu-id="67973-241">The queue fills in the buffer with the metadata from the corresponding Enqueue call.</span></span>  
<span data-ttu-id="67973-242">**Clonar**</span><span class="sxs-lookup"><span data-stu-id="67973-242">**Cloning**</span></span>  
<span data-ttu-id="67973-243">Cada objeto ISurfaceQueue resolve uma sincronização única.</span><span class="sxs-lookup"><span data-stu-id="67973-243">Each ISurfaceQueue object solves a one-way synchronization.</span></span> <span data-ttu-id="67973-244">Presumimos que a grande maioria dos aplicativos que usam essa API usará um sistema fechado.</span><span class="sxs-lookup"><span data-stu-id="67973-244">We assume that the vast majority of applications using this API will use a closed system.</span></span> <span data-ttu-id="67973-245">O sistema fechado mais simples com dois dispositivos enviando superfícies para frente e para trás requer duas filas.</span><span class="sxs-lookup"><span data-stu-id="67973-245">The simplest closed system with two devices sending surfaces back and forth requires two queues.</span></span> <span data-ttu-id="67973-246">O objeto ISurfaceQueue tem um método Clone() para tornar possível criar várias filas que fazem parte do mesmo pipeline maior.</span><span class="sxs-lookup"><span data-stu-id="67973-246">The ISurfaceQueue object has a Clone() method to make it possible to create multiple queues that are all part of the same larger pipeline.</span></span>  
<span data-ttu-id="67973-247">Clone cria um novo objeto ISurfaceQueue de um existente e compartilha todos os recursos abertos entre eles.</span><span class="sxs-lookup"><span data-stu-id="67973-247">Clone creates a new ISurfaceQueue object from an existing one, and shares all the opened resources between them.</span></span> <span data-ttu-id="67973-248">O objeto resultante tem exatamente as mesmas superfícies que a fila de origem.</span><span class="sxs-lookup"><span data-stu-id="67973-248">The resulting object has exactly the same surfaces as the source queue.</span></span> <span data-ttu-id="67973-249">As filas clonadas podem ter tamanhos de metadados diferentes entre si.</span><span class="sxs-lookup"><span data-stu-id="67973-249">Cloned queues can have different metadata sizes from each other.</span></span>  
<span data-ttu-id="67973-250">**Surfaces**</span><span class="sxs-lookup"><span data-stu-id="67973-250">**Surfaces**</span></span>  
<span data-ttu-id="67973-251">O ISurfaceQueue assume a responsabilidade de criar e gerenciar suas superfícies.</span><span class="sxs-lookup"><span data-stu-id="67973-251">The ISurfaceQueue takes responsibility for creating and managing its surfaces.</span></span> <span data-ttu-id="67973-252">Não é válido enquete superfícies arbitrárias.</span><span class="sxs-lookup"><span data-stu-id="67973-252">It is not valid to enqueue arbitrary surfaces.</span></span> <span data-ttu-id="67973-253">Além disso, uma superfície deve ter apenas um "proprietário" ativo.</span><span class="sxs-lookup"><span data-stu-id="67973-253">Furthermore, a surface should only have one active "owner."</span></span> <span data-ttu-id="67973-254">Ele deve estar em uma fila específica ou ser usado por um dispositivo específico.</span><span class="sxs-lookup"><span data-stu-id="67973-254">It should either be on a specific queue or being used by a specific device.</span></span> <span data-ttu-id="67973-255">Não é válido ter em várias filas ou para que os dispositivos continuem usando a superfície depois que ela for enfilfilada.</span><span class="sxs-lookup"><span data-stu-id="67973-255">It is not valid to have it on multiple queues or for devices to continue using the surface after it is enqueued.</span></span>  
</dl>

### <a name="api-details"></a><span data-ttu-id="67973-256">Detalhes da API</span><span class="sxs-lookup"><span data-stu-id="67973-256">API Details</span></span>

### <a name="isurfacequeue"></a><span data-ttu-id="67973-257">IsurfaceQueue</span><span class="sxs-lookup"><span data-stu-id="67973-257">IsurfaceQueue</span></span>

<span data-ttu-id="67973-258">A fila é responsável por criar e manter os recursos compartilhados.</span><span class="sxs-lookup"><span data-stu-id="67973-258">The queue is responsible for creating and maintaining the shared resources.</span></span> <span data-ttu-id="67973-259">Ele também fornece a funcionalidade para encadear várias filas usando clone.</span><span class="sxs-lookup"><span data-stu-id="67973-259">It also provides the functionality to chain multiple queues using Clone.</span></span> <span data-ttu-id="67973-260">A fila tem métodos que abrem o dispositivo de produção e um dispositivo de consumo.</span><span class="sxs-lookup"><span data-stu-id="67973-260">The queue has methods that open the producing device and a consuming device.</span></span> <span data-ttu-id="67973-261">Somente um de cada pode ser aberto a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="67973-261">Only one of each can be opened at any time.</span></span>

<span data-ttu-id="67973-262">A fila expõe as seguintes APIs:</span><span class="sxs-lookup"><span data-stu-id="67973-262">The queue exposes the following APIs:</span></span>



| <span data-ttu-id="67973-263">API</span><span class="sxs-lookup"><span data-stu-id="67973-263">API</span></span>                            | <span data-ttu-id="67973-264">Descrição</span><span class="sxs-lookup"><span data-stu-id="67973-264">Description</span></span>                                                                                 |
|-----------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="67973-265">CreateSurfaceQueue</span><span class="sxs-lookup"><span data-stu-id="67973-265">CreateSurfaceQueue</span></span>          | <span data-ttu-id="67973-266">Cria um objeto ISurfaceQueue (a fila "raiz").</span><span class="sxs-lookup"><span data-stu-id="67973-266">Creates an ISurfaceQueue object (the "root" queue).</span></span>                              |
| <span data-ttu-id="67973-267">ISurfaceQueue::OpenConsumer</span><span class="sxs-lookup"><span data-stu-id="67973-267">ISurfaceQueue::OpenConsumer</span></span> | <span data-ttu-id="67973-268">Retorna uma interface para o dispositivo consumidor a ser removido da fila.</span><span class="sxs-lookup"><span data-stu-id="67973-268">Returns an interface for the consuming device to dequeue.</span></span>                        |
| <span data-ttu-id="67973-269">ISurfaceQueue::OpenProducer</span><span class="sxs-lookup"><span data-stu-id="67973-269">ISurfaceQueue::OpenProducer</span></span> | <span data-ttu-id="67973-270">Retorna uma interface para o dispositivo de produção a ser enfileirado.</span><span class="sxs-lookup"><span data-stu-id="67973-270">Returns an interface for the producing device to enqueue.</span></span>                        |
| <span data-ttu-id="67973-271">ISurfaceQueue:: clone</span><span class="sxs-lookup"><span data-stu-id="67973-271">ISurfaceQueue::Clone</span></span>        | <span data-ttu-id="67973-272">Cria um objeto ISurfaceQueue que compartilha superfícies com o objeto de fila raiz.</span><span class="sxs-lookup"><span data-stu-id="67973-272">Creates an ISurfaceQueue object that shares surfaces with the root queue object.</span></span> |



 

<span data-ttu-id="67973-273">**CreateSurfaceQueue**</span><span class="sxs-lookup"><span data-stu-id="67973-273">**CreateSurfaceQueue**</span></span>  


```C++
typedef struct SURFACE_QUEUE_DESC {
  UINT            Width;
  UINT            Height;
  DXGI_FORMAT     Format;
  UINT            NumSurfaces;
  UINT            MetaDataSize;
  DWORD           Flags;
} SURFACE_QUEUE_DESC;
```



<span data-ttu-id="67973-274">**Membros**</span><span class="sxs-lookup"><span data-stu-id="67973-274">**Members**</span></span>  

<span data-ttu-id="67973-275">**Largura**, **altura**  das dimensões das superfícies compartilhadas.</span><span class="sxs-lookup"><span data-stu-id="67973-275">**Width**, **Height**  The dimensions of the shared surfaces.</span></span> <span data-ttu-id="67973-276">Todas as superfícies compartilhadas devem ter as mesmas dimensões.</span><span class="sxs-lookup"><span data-stu-id="67973-276">All shared surfaces must have the same dimensions.</span></span>  
<span data-ttu-id="67973-277">**Formato** O formato das superfícies compartilhadas.</span><span class="sxs-lookup"><span data-stu-id="67973-277">**Format** The format of the shared surfaces.</span></span> <span data-ttu-id="67973-278">Todas as superfícies compartilhadas devem ter o mesmo formato.</span><span class="sxs-lookup"><span data-stu-id="67973-278">All shared surfaces must have the same format.</span></span> <span data-ttu-id="67973-279">Os formatos válidos dependem dos dispositivos que serão usados, pois diferentes pares de dispositivos podem compartilhar tipos de formato diferentes.</span><span class="sxs-lookup"><span data-stu-id="67973-279">The valid formats depend on the devices that will be used, because different pairs of devices can share different format types.</span></span>  
<span data-ttu-id="67973-280">**NumSurfaces**  O número de superfícies que fazem parte da fila.</span><span class="sxs-lookup"><span data-stu-id="67973-280">**NumSurfaces**  The number of surfaces that are part of the queue.</span></span> <span data-ttu-id="67973-281">Este é um número fixo.</span><span class="sxs-lookup"><span data-stu-id="67973-281">This is a fixed number.</span></span>  
 <span data-ttu-id="67973-282">**MetaDataSize**  O tamanho máximo do buffer de metadados.</span><span class="sxs-lookup"><span data-stu-id="67973-282">**MetaDataSize**  The maximum size of the metadata buffer.</span></span>  
<span data-ttu-id="67973-283">**Sinalizadores**  Sinalizadores para controlar o comportamento da fila.</span><span class="sxs-lookup"><span data-stu-id="67973-283">**Flags**  Flags to control the behavior of the queue.</span></span> <span data-ttu-id="67973-284">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="67973-284">See Remarks.</span></span>  



```C++
HRESULT CreateSurfaceQueue(
  [in]   SURFACE_QUEUE_DESC *pDesc,
  [in]   IUnknown *pDevice,
  [out]  IDXGIXSurfaceQueue **ppQueue
);
```



<span data-ttu-id="67973-285">**Parâmetros**</span><span class="sxs-lookup"><span data-stu-id="67973-285">**Parameters**</span></span>

 <span data-ttu-id="67973-286">*pDesc* \[ em \]  A descrição da fila de superfície compartilhada a ser criada.</span><span class="sxs-lookup"><span data-stu-id="67973-286">*pDesc* \[in\]  The description of the shared surface queue to be created.</span></span>  

 <span data-ttu-id="67973-287">*pDevice* \[ em \]  O dispositivo que deve ser usado para criar as superfícies compartilhadas.</span><span class="sxs-lookup"><span data-stu-id="67973-287">*pDevice* \[in\]  The device that should be used to create the shared surfaces.</span></span> <span data-ttu-id="67973-288">Esse é um parâmetro explícito devido a um recurso no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="67973-288">This is an explicit parameter because of a feature in Windows Vista.</span></span> <span data-ttu-id="67973-289">Para superfícies compartilhadas entre o Direct3D 9 e o Direct3D 10, as superfícies devem ser criadas com o Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="67973-289">For surfaces shared between Direct3D 9 and Direct3D 10, the surfaces must be created with Direct3D 9.</span></span>  

 <span data-ttu-id="67973-290">*ppQueue* \[ out \]  No retorno, contém um ponteiro para o objeto ISurfaceQueue.</span><span class="sxs-lookup"><span data-stu-id="67973-290">*ppQueue* \[out\]  On return, contains a pointer to the ISurfaceQueue object.</span></span>  


<span data-ttu-id="67973-291">**Valores de retorno**</span><span class="sxs-lookup"><span data-stu-id="67973-291">**Return Values**</span></span>

<span data-ttu-id="67973-292">Se *pDevice não for* capaz de compartilhar recursos, essa função retornará DXGI ERROR INVALID \_ \_ \_ CALL.</span><span class="sxs-lookup"><span data-stu-id="67973-292">If *pDevice* is not capable of sharing resources, this function returns DXGI\_ERROR\_INVALID\_CALL.</span></span> <span data-ttu-id="67973-293">Essa função cria os recursos.</span><span class="sxs-lookup"><span data-stu-id="67973-293">This function creates the resources.</span></span> <span data-ttu-id="67973-294">Se falhar, ele retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="67973-294">If it fails, it returns an error.</span></span> <span data-ttu-id="67973-295">Se for bem-sucedido, ele retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="67973-295">If it succeeds, it returns S\_OK.</span></span>

<span data-ttu-id="67973-296">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="67973-296">**Remarks**</span></span>

<span data-ttu-id="67973-297">A criação do objeto de fila também cria todas as superfícies.</span><span class="sxs-lookup"><span data-stu-id="67973-297">Creating the queue object also creates all of the surfaces.</span></span> <span data-ttu-id="67973-298">Todas as superfícies são assumidas como destinos de renderização 2D e serão criadas com os sinalizadores D3D10 BIND RENDER RENDER TARGET e \_ \_ \_ D3D10 BIND SHADER RESOURCE definidos (ou os sinalizadores equivalentes para os \_ \_ diferentes \_ runtimes).</span><span class="sxs-lookup"><span data-stu-id="67973-298">All surfaces are assumed to be 2D render targets and will be created with the D3D10\_BIND\_RENDER\_TARGET and D3D10\_BIND\_SHADER\_RESOURCE flags set (or the equivalent flags for the different runtimes).</span></span>

<span data-ttu-id="67973-299">O desenvolvedor pode especificar um sinalizador que indica se a fila será acessada por vários threads.</span><span class="sxs-lookup"><span data-stu-id="67973-299">The developer can specify a flag that indicates whether the queue will be accessed by multiple threads.</span></span> <span data-ttu-id="67973-300">Se nenhum sinalizador for definido (**Sinalizadores** == 0), a fila será usada por vários threads.</span><span class="sxs-lookup"><span data-stu-id="67973-300">If no flags are set (**Flags** == 0), the queue will be used by multiple threads.</span></span> <span data-ttu-id="67973-301">O desenvolvedor pode especificar o acesso thread único, que desliga o código de sincronização e fornece uma melhoria de desempenho para esses casos.</span><span class="sxs-lookup"><span data-stu-id="67973-301">The developer can specify single threaded access, which turns off the synchronization code and provides a performance improvement for those cases.</span></span> <span data-ttu-id="67973-302">Cada fila clonada tem seu próprio sinalizador, portanto, é possível que filas diferentes no sistema tenham controles de sincronização diferentes.</span><span class="sxs-lookup"><span data-stu-id="67973-302">Each cloned queue has its own flag, so it is possible for different queues in the system to have different synchronization controls.</span></span>

 <span data-ttu-id="67973-303">**Abrir um produtor**</span><span class="sxs-lookup"><span data-stu-id="67973-303">**Open a Producer**</span></span>  


```C++
HRESULT OpenProducer(
  [in]   IUnknown *pDevice,
  [out]  IDXGIXSurfaceProducer **ppProducer
);
```



<span data-ttu-id="67973-304">**Parâmetros**</span><span class="sxs-lookup"><span data-stu-id="67973-304">**Parameters**</span></span>  

<span data-ttu-id="67973-305">*pDevice* \[ Em\]</span><span class="sxs-lookup"><span data-stu-id="67973-305">*pDevice* \[in\]</span></span>  

<span data-ttu-id="67973-306">O dispositivo de produtor que enfiloca superfícies na fila da superfície.</span><span class="sxs-lookup"><span data-stu-id="67973-306">The producer device that enqueues surfaces onto the surface queue.</span></span> 

<span data-ttu-id="67973-307">*ppProducer* \[ out \] retorna um objeto para a interface do produtor.</span><span class="sxs-lookup"><span data-stu-id="67973-307">*ppProducer* \[out\] Returns an object to the producer interface.</span></span>  


<span data-ttu-id="67973-308">**Valores de retorno**</span><span class="sxs-lookup"><span data-stu-id="67973-308">**Return Values**</span></span>

<span data-ttu-id="67973-309">Se o dispositivo não for capaz de compartilhar superfícies, retorna a \_ chamada de erro dxgi \_ inválido \_ .</span><span class="sxs-lookup"><span data-stu-id="67973-309">If the device is not capable of sharing surfaces, returns DXGI\_ERROR\_INVALID\_CALL.</span></span>

<span data-ttu-id="67973-310">**Abrir um consumidor**</span><span class="sxs-lookup"><span data-stu-id="67973-310">**Open a Consumer**</span></span>  


```C++
HRESULT OpenConsumer(
  [in]   IUnknown *pDevice,
  [out]  IDXGIXSurfaceConsumer **ppConsumer
);
```



<span data-ttu-id="67973-311">**Parâmetros**</span><span class="sxs-lookup"><span data-stu-id="67973-311">**Parameters**</span></span>  
 <span data-ttu-id="67973-312">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="67973-312">*pDevice* \[in\]</span></span>  
 <span data-ttu-id="67973-313">O dispositivo de consumidor que recoloca as superfícies da fila de superfície.</span><span class="sxs-lookup"><span data-stu-id="67973-313">The consumer device that dequeues surfaces from the surface queue.</span></span> 
 <span data-ttu-id="67973-314">*ppConsumer* \[ out \]  retorna um objeto para a interface do consumidor.</span><span class="sxs-lookup"><span data-stu-id="67973-314">*ppConsumer* \[out\]  Returns an object to the consumer interface.</span></span>  


<span data-ttu-id="67973-315">**Valores de retorno**</span><span class="sxs-lookup"><span data-stu-id="67973-315">**Return Values**</span></span>

<span data-ttu-id="67973-316">Se o dispositivo não for capaz de compartilhar superfícies, retorna a \_ chamada de erro dxgi \_ inválido \_ .</span><span class="sxs-lookup"><span data-stu-id="67973-316">If the device is not capable of sharing surfaces, returns DXGI\_ERROR\_INVALID\_CALL.</span></span>

<span data-ttu-id="67973-317">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="67973-317">**Remarks**</span></span>

<span data-ttu-id="67973-318">Essa função abre todas as superfícies na fila para o dispositivo de entrada e as armazena em cache.</span><span class="sxs-lookup"><span data-stu-id="67973-318">This function opens all of the surfaces in the queue for the input device and caches them.</span></span> <span data-ttu-id="67973-319">As chamadas subsequentes para remover a fila simplesmente vão para o cache e não precisam reabrir as superfícies a cada vez.</span><span class="sxs-lookup"><span data-stu-id="67973-319">Subsequent calls to Dequeue will simply go to the cache and not have to reopen the surfaces each time.</span></span>



### <a name="cloning-an-idxgixsurfacequeue"></a><span data-ttu-id="67973-320">Clonando um IDXGIXSurfaceQueue</span><span class="sxs-lookup"><span data-stu-id="67973-320">Cloning an IDXGIXSurfaceQueue</span></span>




```C++
typedef struct SHARED_SURFACE_QUEUE_CLONE_DESC {
  UINT         MetaDataSize;
  DWORD        Flags;
} SHARED_SURFACE_QUEUE_CLONE_DESC;
```



<span data-ttu-id="67973-321">**Os membros** **MetaDataSize** e **flags** têm o mesmo comportamento que eles fazem para o CreateSurfaceQueue.</span><span class="sxs-lookup"><span data-stu-id="67973-321">**Members** **MetaDataSize** and **Flags** have the same behavior as they do for CreateSurfaceQueue.</span></span>  



```C++
HRESULT Clone(
  [in]   SHARED_SURFACE_QUEUE_CLONE_DESC *pDesc,
  [out]  IDXGIXSurfaceQueue **ppQueue
);
```



<span data-ttu-id="67973-322">**Parâmetros**</span><span class="sxs-lookup"><span data-stu-id="67973-322">**Parameters**</span></span>

<span data-ttu-id="67973-323">*pDesc* \[ em \] uma struct que fornece uma descrição do objeto de clonagem a ser criado.</span><span class="sxs-lookup"><span data-stu-id="67973-323">*pDesc* \[in\] A struct that provides a description of the Clone object to be created.</span></span> <span data-ttu-id="67973-324">Esse parâmetro deve ser inicializado.</span><span class="sxs-lookup"><span data-stu-id="67973-324">This parameter should be initialized.</span></span>  
<span data-ttu-id="67973-325">*ppQueue* \[ out \] retorna o objeto Initialized.</span><span class="sxs-lookup"><span data-stu-id="67973-325">*ppQueue* \[out\] Returns the initialized object.</span></span>  
</dl>

<span data-ttu-id="67973-326">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="67973-326">**Remarks**</span></span>

<span data-ttu-id="67973-327">Você pode clonar de qualquer objeto de fila existente, mesmo que não seja a raiz.</span><span class="sxs-lookup"><span data-stu-id="67973-327">You can clone from any existing queue object, even if it is not the root.</span></span>  
</dl>

### <a name="idxgixsurfaceconsumer"></a><span data-ttu-id="67973-328">IDXGIXSurfaceConsumer</span><span class="sxs-lookup"><span data-stu-id="67973-328">IDXGIXSurfaceConsumer</span></span>

<dl>


```C++
HRESULT Dequeue(
  [in]      REFIID    id,
  [out]     void      **ppSurface,
  [in,out]  void      *pBuffer,
  [in,out]  UINT      *pBufferSize,
  [in]      DWORD     dwTimeout
);
```



<span data-ttu-id="67973-329">**Parâmetros**</span><span class="sxs-lookup"><span data-stu-id="67973-329">**Parameters**</span></span>  
<span data-ttu-id="67973-330">*ID* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="67973-330">*id* \[in\]</span></span>  
<span data-ttu-id="67973-331">O REFIID de uma superfície 2D do dispositivo de consumo.</span><span class="sxs-lookup"><span data-stu-id="67973-331">The REFIID of a 2D surface of the consuming device.</span></span>  

-   <span data-ttu-id="67973-332">Para um IDirect3DDevice9, o REFIID deve ser \_ \_ uuidof (IDirect3DTexture9).</span><span class="sxs-lookup"><span data-stu-id="67973-332">For a IDirect3DDevice9, the REFIID should be \_\_uuidof(IDirect3DTexture9).</span></span>
-   <span data-ttu-id="67973-333">Para um ID3D10Device, o REFIID deve ser \_ \_ uuidof (ID3D10Texture2D).</span><span class="sxs-lookup"><span data-stu-id="67973-333">For a ID3D10Device, the REFIID should be \_\_uuidof(ID3D10Texture2D).</span></span>
-   <span data-ttu-id="67973-334">Para um ID3D11Device, o REFIID deve ser \_ \_ uuidof(ID3D11Texture2D).</span><span class="sxs-lookup"><span data-stu-id="67973-334">For a ID3D11Device, the REFIID should be \_\_uuidof(ID3D11Texture2D).</span></span>

<span data-ttu-id="67973-335">*ppSurface* \[ out \] Retorna um ponteiro para a superfície.</span><span class="sxs-lookup"><span data-stu-id="67973-335">*ppSurface* \[out\] Returns a pointer to the surface.</span></span>  
<span data-ttu-id="67973-336">*pBuffer* \[ in, out Um parâmetro opcional e, se não FOR NULL, no retorno, conterão os metadados que foram passados \] na chamada de enquete correspondente. </span><span class="sxs-lookup"><span data-stu-id="67973-336">*pBuffer* \[in, out\] An optional parameter and if not **NULL**, on return, contains the metadata that was passed in on the corresponding enqueue call.</span></span>  
<span data-ttu-id="67973-337">*pBufferSize* \[ in, out \] O tamanho de *pBuffer*, em bytes.</span><span class="sxs-lookup"><span data-stu-id="67973-337">*pBufferSize* \[in, out\] The size of *pBuffer*, in bytes.</span></span> <span data-ttu-id="67973-338">Retorna o número de bytes retornados em *pBuffer.*</span><span class="sxs-lookup"><span data-stu-id="67973-338">Returns the number of bytes returned in *pBuffer*.</span></span> <span data-ttu-id="67973-339">Se a chamada de enquete não forneceu metadados, *pBuffer* será definido como 0.</span><span class="sxs-lookup"><span data-stu-id="67973-339">If the enqueue call did not provide metadata, *pBuffer* is set to 0.</span></span>  
<span data-ttu-id="67973-340">*dwTimeout* \[ em \] Especifica um valor de tempoout.</span><span class="sxs-lookup"><span data-stu-id="67973-340">*dwTimeout* \[in\] Specifies a timeout value.</span></span> <span data-ttu-id="67973-341">Confira os Comentários para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="67973-341">See the Remarks for more detail.</span></span>  
</dl>

<span data-ttu-id="67973-342">**Valores de retorno**</span><span class="sxs-lookup"><span data-stu-id="67973-342">**Return Values**</span></span>

<span data-ttu-id="67973-343">Essa função poderá retornar WAIT TIMEOUT se um valor de tempoout for especificado e a função não retornar \_ antes do valor de tempo-máximo.</span><span class="sxs-lookup"><span data-stu-id="67973-343">This function can return WAIT\_TIMEOUT if a timeout value is specified and the function does not return before the time out value.</span></span> <span data-ttu-id="67973-344">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="67973-344">See Remarks.</span></span> <span data-ttu-id="67973-345">Se nenhuma superfície estiver disponível, a função retornará com *ppSurface* definido como **NULL,** *pBufferSize* definido como 0 e o valor de retorno será 0x80070120 (WIN32 \_ TO \_ HRESULT(WAIT \_ TIMEOUT)).</span><span class="sxs-lookup"><span data-stu-id="67973-345">If no surfaces are available, the function returns with *ppSurface* set to **NULL**, *pBufferSize* set to 0 and the return value is 0x80070120 (WIN32\_TO\_HRESULT(WAIT\_TIMEOUT)).</span></span>  
</dl>

<span data-ttu-id="67973-346">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="67973-346">**Remarks**</span></span>

<span data-ttu-id="67973-347">Essa API poderá bloquear se a fila estiver vazia.</span><span class="sxs-lookup"><span data-stu-id="67973-347">This API can block if the queue is empty.</span></span> <span data-ttu-id="67973-348">O *parâmetro dwTimeout* funciona de forma idêntica às APIs de sincronização do Windows, como WaitForSingleObject.</span><span class="sxs-lookup"><span data-stu-id="67973-348">The *dwTimeout* parameter works identically to the Windows synchronization APIs, such as WaitForSingleObject.</span></span> <span data-ttu-id="67973-349">Para o comportamento sem bloqueio, use um tempoout de 0.</span><span class="sxs-lookup"><span data-stu-id="67973-349">For non-blocking behavior, use a timeout of 0.</span></span>  
</dl>

### <a name="isurfaceproducer"></a><span data-ttu-id="67973-350">ISurfaceProducer</span><span class="sxs-lookup"><span data-stu-id="67973-350">ISurfaceProducer</span></span>

<span data-ttu-id="67973-351">Essa interface fornece dois métodos que permitem que o aplicativo enquete superfícies.</span><span class="sxs-lookup"><span data-stu-id="67973-351">This interface provides two methods that allow the app to enqueue surfaces.</span></span> <span data-ttu-id="67973-352">Depois que uma superfície é ensuada, o ponteiro de superfície não é mais válido e não é seguro de usar.</span><span class="sxs-lookup"><span data-stu-id="67973-352">After a surface is enqueued, the surface pointer is no longer valid and is not safe to use.</span></span> <span data-ttu-id="67973-353">A única ação que o aplicativo deve executar com o ponteiro é liberá-lo.</span><span class="sxs-lookup"><span data-stu-id="67973-353">The only action that the application should perform with the pointer is to release it.</span></span>



| <span data-ttu-id="67973-354">Método</span><span class="sxs-lookup"><span data-stu-id="67973-354">Method</span></span>                          | <span data-ttu-id="67973-355">Descrição</span><span class="sxs-lookup"><span data-stu-id="67973-355">Description</span></span>                                                                                                                                                      |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67973-356">ISurfaceProducer::Enqueue</span><span class="sxs-lookup"><span data-stu-id="67973-356">ISurfaceProducer::Enqueue</span></span> | <span data-ttu-id="67973-357">Enfilra uma superfície para o objeto de fila.</span><span class="sxs-lookup"><span data-stu-id="67973-357">Enqueues a surface to the queue object.</span></span> <span data-ttu-id="67973-358">Depois que essa chamada for concluída, o produtor será concluído com a superfície e a superfície estará pronta para outro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="67973-358">After this call completes, the producer is done with the surface and the surface is ready for another device.</span></span> |
| <span data-ttu-id="67973-359">ISurfaceProducer:: flush</span><span class="sxs-lookup"><span data-stu-id="67973-359">ISurfaceProducer::Flush</span></span>   | <span data-ttu-id="67973-360">Usado se os aplicativos tiverem um comportamento não bloqueado.</span><span class="sxs-lookup"><span data-stu-id="67973-360">Used if the applications should have non-blocking behavior.</span></span> <span data-ttu-id="67973-361">Consulte Comentários para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="67973-361">See Remarks for details.</span></span>                                                                  |



 

<span data-ttu-id="67973-362">**Enfileirar**</span><span class="sxs-lookup"><span data-stu-id="67973-362">**Enqueue**</span></span>  


```C++
HRESULT Enqueue(
  [in]  IUnknown *pSurface,
  [in]  void *pBuffer,
  [in]  UINT BufferSize,
  [in]  DWORD Flags
);
```



<span data-ttu-id="67973-363">**Parâmetros**</span><span class="sxs-lookup"><span data-stu-id="67973-363">**Parameters**</span></span>  
<span data-ttu-id="67973-364">*pSurface* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="67973-364">*pSurface* \[in\]</span></span>  
<span data-ttu-id="67973-365">A superfície do dispositivo de produção que precisa ser enfileirado.</span><span class="sxs-lookup"><span data-stu-id="67973-365">The surface of the producing device that needs to be enqueued.</span></span> <span data-ttu-id="67973-366">Essa superfície deve ser uma superfície removida da fila da mesma rede de fila.</span><span class="sxs-lookup"><span data-stu-id="67973-366">This surface must be a dequeued surface from the same queue network.</span></span> <span data-ttu-id="67973-367">*pBuffer* \[ em \] um parâmetro opcional, que é usado para transmitir metadados.</span><span class="sxs-lookup"><span data-stu-id="67973-367">*pBuffer* \[in\] An optional parameter, which is used to pass in metadata.</span></span> <span data-ttu-id="67973-368">Ele deve apontar para os dados que serão passados para a chamada de remoção da fila.</span><span class="sxs-lookup"><span data-stu-id="67973-368">It should point to the data that will be passed on to the dequeue call.</span></span>  
<span data-ttu-id="67973-369">*BufferSize* \[ no \] tamanho de *pBuffer*, em bytes.</span><span class="sxs-lookup"><span data-stu-id="67973-369">*BufferSize* \[in\] The size of *pBuffer*, in bytes.</span></span>  
<span data-ttu-id="67973-370">*Sinalizadores* \[ de em \] um parâmetro opcional que controla o comportamento dessa função.</span><span class="sxs-lookup"><span data-stu-id="67973-370">*Flags* \[in\] An optional parameter that controls the behavior of this function.</span></span> <span data-ttu-id="67973-371">O único sinalizador é o \_ sinalizador da fila de superfície \_ \_ \_ não \_ aguardar.</span><span class="sxs-lookup"><span data-stu-id="67973-371">The only flag is SURFACE\_QUEUE\_FLAG\_ DO\_NOT\_WAIT.</span></span> <span data-ttu-id="67973-372">Consulte os comentários para liberação.</span><span class="sxs-lookup"><span data-stu-id="67973-372">See the Remarks for Flush.</span></span> <span data-ttu-id="67973-373">Se nenhum sinalizador for passado (*flags* = = 0), o comportamento de bloqueio padrão será usado.</span><span class="sxs-lookup"><span data-stu-id="67973-373">If no flag is passed (*Flags* == 0), then the default blocking behavior is used.</span></span>  
</dl>

<span data-ttu-id="67973-374">**Valores de retorno**</span><span class="sxs-lookup"><span data-stu-id="67973-374">**Return Values**</span></span>

<span data-ttu-id="67973-375">Essa função pode retornar \_ um erro \_ dxgi \_ ainda \_ está desenhando se um sinalizador de fila de superfície \_ \_ \_ \_ não \_ aguardar é usado.</span><span class="sxs-lookup"><span data-stu-id="67973-375">This function can return DXGI\_ERROR\_WAS\_STILL\_DRAWING if a SURFACE\_QUEUE\_FLAG\_DO\_NOT\_WAIT flag is used.</span></span>  
</dl>

<span data-ttu-id="67973-376">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="67973-376">**Remarks**</span></span>

-   <span data-ttu-id="67973-377">Essa função coloca a superfície na fila.</span><span class="sxs-lookup"><span data-stu-id="67973-377">This function puts the surface on the queue.</span></span> <span data-ttu-id="67973-378">Se o aplicativo não especificar o sinalizador de fila de superfície não \_ \_ \_ \_ \_ esperar, essa função está bloqueando e fará uma sincronização de GPU-CPU para garantir que toda a renderização na superfície enfileirada seja concluída.</span><span class="sxs-lookup"><span data-stu-id="67973-378">If the application does not specify SURFACE\_QUEUE\_FLAG\_DO\_NOT\_WAIT, this function is blocking and will do a GPU-CPU synchronization to assure that all the rendering on the enqueued surface is complete.</span></span> <span data-ttu-id="67973-379">Se essa função for realizada com sucesso, uma superfície estará disponível para remoção da fila.</span><span class="sxs-lookup"><span data-stu-id="67973-379">If this function succeeds, a surface will be available for dequeue.</span></span> <span data-ttu-id="67973-380">Se você quiser um comportamento sem bloqueio, use o \_ sinalizador não \_ aguardar.</span><span class="sxs-lookup"><span data-stu-id="67973-380">If you want non-blocking behavior, use the DO\_NOT\_WAIT flag.</span></span> <span data-ttu-id="67973-381">Consulte flush () para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="67973-381">See Flush() for details.</span></span>
-   <span data-ttu-id="67973-382">De acordo COM as regras de contagem de referência COM, a superfície retornada pela remoção será AddRef () para que o aplicativo não precise fazer isso.</span><span class="sxs-lookup"><span data-stu-id="67973-382">As per the COM reference counting rules, the surface returned by Dequeue will be AddRef() so the application does not need to do this.</span></span> <span data-ttu-id="67973-383">Depois de chamar enqueue, o aplicativo deve liberar a superfície porque não está mais usando-a.</span><span class="sxs-lookup"><span data-stu-id="67973-383">After calling Enqueue, the application must Release the surface because they are no longer using it.</span></span>

<span data-ttu-id="67973-384">**Liberar**</span><span class="sxs-lookup"><span data-stu-id="67973-384">**Flush**</span></span>  


```C++
HRESULT Flush(
  [in]  DWORD Flags,
  [out] UINT *nSurfaces
);
```



<span data-ttu-id="67973-385">**Parâmetros**</span><span class="sxs-lookup"><span data-stu-id="67973-385">**Parameters**</span></span>  
<span data-ttu-id="67973-386">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="67973-386">*Flags* \[in\]</span></span>  
<span data-ttu-id="67973-387">O único sinalizador é SURFACE \_ QUEUE \_ FLAG NÃO \_ \_ \_ WAIT.</span><span class="sxs-lookup"><span data-stu-id="67973-387">The only flag is SURFACE\_QUEUE\_FLAG\_ DO\_NOT\_WAIT.</span></span> <span data-ttu-id="67973-388">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="67973-388">See Remarks.</span></span> <span data-ttu-id="67973-389">*nSurfaces* \[ out \] Retorna o número de superfícies que ainda estão pendentes e não foram liberados.</span><span class="sxs-lookup"><span data-stu-id="67973-389">*nSurfaces* \[out\] Returns the number of surfaces that are still pending and not flushed.</span></span>  
</dl>

<span data-ttu-id="67973-390">**Valores de retorno**</span><span class="sxs-lookup"><span data-stu-id="67973-390">**Return Values**</span></span>

<span data-ttu-id="67973-391">Essa função poderá retornar ERRO DXGI AINDA ESTAVA DESENHANDO se o sinalizador \_ SURFACE QUEUE NÃO WAIT \_ for \_ \_ \_ \_ \_ \_ \_ usado.</span><span class="sxs-lookup"><span data-stu-id="67973-391">This function can return DXGI\_ERROR\_WAS\_STILL\_DRAWING if the SURFACE\_QUEUE\_FLAG\_DO\_NOT\_WAIT flag is used.</span></span> <span data-ttu-id="67973-392">Essa função retornará S \_ OK se alguma superfície tiver sido liberado com êxito.</span><span class="sxs-lookup"><span data-stu-id="67973-392">This function returns S\_OK if any surfaces were successfully flushed.</span></span> <span data-ttu-id="67973-393">Essa função retornará ERRO DXGI \_ \_ AINDA ESTAVA \_ \_ DESENHANDO somente se nenhuma superfície tiver sido liberado.</span><span class="sxs-lookup"><span data-stu-id="67973-393">This function returns DXGI\_ERROR\_WAS\_STILL\_DRAWING only if no surfaces were flushed.</span></span> <span data-ttu-id="67973-394">Juntos, o valor de retorno *e nSurfaces* indicam ao aplicativo qual trabalho foi feito e se algum trabalho é deixado para fazer.</span><span class="sxs-lookup"><span data-stu-id="67973-394">Together, the return value and *nSurfaces* indicate to the application what work has been done and if any work is left to do.</span></span>  
</dl>

<span data-ttu-id="67973-395">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="67973-395">**Remarks**</span></span>

<span data-ttu-id="67973-396">A liberação só será significativa se a chamada anterior à enquete tiver usado o sinalizador NÃO WAIT; caso contrário, ela \_ \_ será não operada.</span><span class="sxs-lookup"><span data-stu-id="67973-396">Flush is meaningful only if the previous call to enqueue used the DO\_NOT\_WAIT flag; otherwise, it will be a no-op.</span></span> <span data-ttu-id="67973-397">Se a chamada à enquete tiver usado o sinalizador NÃO WAIT, a enquete retornará imediatamente e a \_ \_ sincronização gpu-CPU não será garantida.</span><span class="sxs-lookup"><span data-stu-id="67973-397">If the call to enqueue used the DO\_NOT\_WAIT flag, enqueue returns immediately and the GPU-CPU synchronization is not guaranteed.</span></span> <span data-ttu-id="67973-398">A superfície ainda é considerada enqueixada, o dispositivo de produção não pode continuar a usá-la, mas não está disponível para a desaquete.</span><span class="sxs-lookup"><span data-stu-id="67973-398">The surface is still considered enqueued, the producing device cannot continue using it, but it is not available for dequeue.</span></span> <span data-ttu-id="67973-399">Para tentar fazer commit da superfície para o desembaixo, Flush deve ser chamado.</span><span class="sxs-lookup"><span data-stu-id="67973-399">In order to try to commit the surface for dequeue, Flush must be called.</span></span> <span data-ttu-id="67973-400">A liberação tenta fazer commit de todas as superfícies que estão ensuadas no momento.</span><span class="sxs-lookup"><span data-stu-id="67973-400">Flush attempts to commit all of the surfaces that are currently enqueued.</span></span> <span data-ttu-id="67973-401">Se nenhum sinalizador for passado para Liberação, ele bloqueará e limpará toda a fila, preparando todas as superfícies para a desfileiramento.</span><span class="sxs-lookup"><span data-stu-id="67973-401">If no flag is passed to Flush, it will block and clear out the entire queue, readying all surfaces in it for dequeue.</span></span> <span data-ttu-id="67973-402">Se o sinalizador NÃO AGUARDAR for usado, a fila verificará as superfícies para ver se alguma delas está pronta; essa etapa não \_ \_ está bloqueando.</span><span class="sxs-lookup"><span data-stu-id="67973-402">If the DO\_NOT\_WAIT flag is used, the queue will check the surfaces to see if any of them are ready; this step is non-blocking.</span></span> <span data-ttu-id="67973-403">As superfícies que finalizaram a sincronização GPU-CPU estarão prontas para o dispositivo de consumidor.</span><span class="sxs-lookup"><span data-stu-id="67973-403">Surfaces that have finished the GPU-CPU sync will be ready for the consumer device.</span></span> <span data-ttu-id="67973-404">Superfícies que ainda estão pendentes não serão afetadas.</span><span class="sxs-lookup"><span data-stu-id="67973-404">Surfaces that are still pending will be unaffected.</span></span> <span data-ttu-id="67973-405">A função retorna o número de superfícies que ainda precisam ser liberados.</span><span class="sxs-lookup"><span data-stu-id="67973-405">The function returns the number of surfaces that still need to be flushed.</span></span>

> [!Note]  
> <span data-ttu-id="67973-406">A liberação não quebrará a semântica da fila.</span><span class="sxs-lookup"><span data-stu-id="67973-406">Flush will not break the queue semantics.</span></span> <span data-ttu-id="67973-407">A API garante que as superfícies ensuadas primeiro serão comprometidas antes que as superfícies sejam ensuadas posteriormente, independentemente de quando ocorrer a sincronização GPU-CPU.</span><span class="sxs-lookup"><span data-stu-id="67973-407">The API guarantees that surfaces enqueued first will be committed before surfaces enqueued later, regardless of when the GPU-CPU sync happens.</span></span>

 

  
</dl>

### <a name="direct3d-9ex-and-dxgi-interop-helper-how-to-use"></a><span data-ttu-id="67973-408">Auxiliar de interop do Direct3D 9Ex e DXGI: Como usar</span><span class="sxs-lookup"><span data-stu-id="67973-408">Direct3D 9Ex and DXGI Interop Helper: How To Use</span></span>

<span data-ttu-id="67973-409">Esperamos que a maioria dos casos de uso envolva dois dispositivos que compartilham várias superfícies.</span><span class="sxs-lookup"><span data-stu-id="67973-409">We expect most of the usage cases to involve two devices sharing a number of surfaces.</span></span> <span data-ttu-id="67973-410">Como esse também é o cenário mais simples, este documento detalha como usar as APIs para atingir essa meta, discute uma variação sem bloqueio e termina com uma breve seção sobre a inicialização de três dispositivos.</span><span class="sxs-lookup"><span data-stu-id="67973-410">Because this also happens to be the simplest scenario, this paper details how to use the APIs to achieve this goal, discusses a non-blocking variation, and ends with a brief section about initializing for three devices.</span></span>

### <a name="two-devices"></a><span data-ttu-id="67973-411">Dois dispositivos</span><span class="sxs-lookup"><span data-stu-id="67973-411">Two Devices</span></span>

<span data-ttu-id="67973-412">O aplicativo de exemplo que usa esse auxiliar pode usar o Direct3D 9Ex e o Direct3D 11 juntos.</span><span class="sxs-lookup"><span data-stu-id="67973-412">The example application that uses this helper can use Direct3D 9Ex and Direct3D 11 together.</span></span> <span data-ttu-id="67973-413">O aplicativo pode processar o conteúdo com ambos os dispositivos e apresentar o conteúdo usando o Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="67973-413">The application can process content with both devices, and present content using Direct3D 9.</span></span> <span data-ttu-id="67973-414">O processamento pode significar a renderização de conteúdo, a decodificação de vídeo, a execução de sombreadores de computação e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="67973-414">Processing could mean rendering content, decoding video, running compute shaders, and so on.</span></span> <span data-ttu-id="67973-415">Para cada quadro, o aplicativo será processado primeiro com o Direct3D 11, depois o processo com o Direct3D 9 e, finalmente, presente com o Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="67973-415">For every frame, the application will first process with Direct3D 11, then process with Direct3D 9, and finally present with Direct3D 9.</span></span> <span data-ttu-id="67973-416">Além disso, o processamento com o Direct3D 11 produzirá alguns metadados que o Direct3D 9 presente precisará consumir.</span><span class="sxs-lookup"><span data-stu-id="67973-416">Furthermore, the processing with Direct3D 11 will produce some metadata that the Direct3D 9 present will need to consume.</span></span> <span data-ttu-id="67973-417">Esta seção aborda o uso do auxiliar em três partes que correspondem a esta sequência: inicialização, loop principal e limpeza.</span><span class="sxs-lookup"><span data-stu-id="67973-417">This section covers the helper usage in three parts that correspond to this sequence: Initialization, Main Loop, and Cleanup.</span></span>

<span data-ttu-id="67973-418">**Inicialização**</span><span class="sxs-lookup"><span data-stu-id="67973-418">**Initialization**</span></span>  
<span data-ttu-id="67973-419">A inicialização envolve as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="67973-419">Initialization involves the following steps:</span></span>  

1.  <span data-ttu-id="67973-420">Inicialize ambos os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="67973-420">Initialize both devices.</span></span>
2.  <span data-ttu-id="67973-421">Crie a fila raiz: m \_ 11to9Queue.</span><span class="sxs-lookup"><span data-stu-id="67973-421">Create the Root Queue: m\_11to9Queue.</span></span>
3.  <span data-ttu-id="67973-422">Clone da fila raiz: m \_ 9to11Queue.</span><span class="sxs-lookup"><span data-stu-id="67973-422">Clone from the Root Queue: m\_9to11Queue.</span></span>
4.  <span data-ttu-id="67973-423">Chame OpenProducer/OpenConsumer em ambas as filas.</span><span class="sxs-lookup"><span data-stu-id="67973-423">Call OpenProducer/OpenConsumer on both queues.</span></span>

<span data-ttu-id="67973-424">Os nomes de fila usam os números 9 e 11 para indicar qual API é o produtor e qual é a *_fila_* consumidor: **m \_** do _produtor_*_para_* o _consumidor_.</span><span class="sxs-lookup"><span data-stu-id="67973-424">The queue names use the numbers 9 and 11 to indicate which API is the producer and which is the consumer: **m\_**_producer_*_to_*_consumer_*_Queue_*.</span></span> <span data-ttu-id="67973-425">Da mesma forma, m \_ 11to9Queue indica uma fila para a qual o dispositivo Direct3D 11 produz superfícies que o dispositivo Direct3D 9 consome.</span><span class="sxs-lookup"><span data-stu-id="67973-425">Accordingly, m\_11to9Queue indicates a queue for which the Direct3D 11 device produces surfaces that the Direct3D 9 device consumes.</span></span> <span data-ttu-id="67973-426">Da mesma forma, m \_ 9to11Queue indica uma fila para a qual o Direct3D 9 produz superfícies que o Direct3D 11 consome.</span><span class="sxs-lookup"><span data-stu-id="67973-426">Similarly, m\_9to11Queue indicates a queue for which Direct3D 9 produces surfaces that Direct3D 11 consumes.</span></span>  
<span data-ttu-id="67973-427">A fila raiz está inicialmente cheia e todas as filas clonadas estão vazias inicialmente.</span><span class="sxs-lookup"><span data-stu-id="67973-427">The Root queue is initially full and all cloned queues are initially empty.</span></span> <span data-ttu-id="67973-428">Isso não deve ser um problema para o aplicativo, exceto para o primeiro ciclo de enfileiramentos e remoção de filas e a disponibilidade dos metadados.</span><span class="sxs-lookup"><span data-stu-id="67973-428">This should not be a problem for the application except for the first cycle of the Enqueues and Dequeues and the availability of metadata.</span></span> <span data-ttu-id="67973-429">Se uma remoção da fila solicitar metadados, mas nenhum tiver sido definido (porque nada está lá inicialmente ou o enfileiramento não definiu nada), a remoção da fila verá que nenhum metadado foi recebido.</span><span class="sxs-lookup"><span data-stu-id="67973-429">If a dequeue asks for metadata but none was set (either because nothing is there initially or the enqueue did not set anything), dequeue sees that no metadata was received.</span></span>  

1.  <span data-ttu-id="67973-430">**Inicialize ambos os dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="67973-430">**Initialize Both Devices.**</span></span>  
    ```C++
    m_pD3D9Device = InitializeD3D9ExDevice();
    m_pD3D11Device = InitializeD3D11Device();
    ```

    

2.  <span data-ttu-id="67973-431">**Crie a Fila Raiz.**</span><span class="sxs-lookup"><span data-stu-id="67973-431">**Create the Root Queue.**</span></span>  
    <span data-ttu-id="67973-432">Essa etapa também cria as superfícies.</span><span class="sxs-lookup"><span data-stu-id="67973-432">This step also creates the surfaces.</span></span> <span data-ttu-id="67973-433">Restrições de tamanho e formato são idênticas à criação de qualquer recurso compartilhado.</span><span class="sxs-lookup"><span data-stu-id="67973-433">Size and format restrictions are identical to creating any shared resource.</span></span> <span data-ttu-id="67973-434">O tamanho do buffer de metadados é fixo no momento da criação e, nesse caso, passaremos apenas uma UINT.</span><span class="sxs-lookup"><span data-stu-id="67973-434">The size of the metadata buffer is fixed at create time, and in this case, we'll just be passing a UINT.</span></span>  
    <span data-ttu-id="67973-435">A fila deve ser criada com um número fixo de superfícies.</span><span class="sxs-lookup"><span data-stu-id="67973-435">The queue must be created with a fixed number of surfaces.</span></span> <span data-ttu-id="67973-436">O desempenho variará dependendo do cenário.</span><span class="sxs-lookup"><span data-stu-id="67973-436">Performance will vary depending on the scenario.</span></span> <span data-ttu-id="67973-437">Ter várias superfícies aumenta as chances de que os dispositivos estão ocupados.</span><span class="sxs-lookup"><span data-stu-id="67973-437">Having multiple surfaces increases the chances that devices are busy.</span></span> <span data-ttu-id="67973-438">Por exemplo, se houver apenas uma superfície, não haverá paralelização entre os dois dispositivos.</span><span class="sxs-lookup"><span data-stu-id="67973-438">For example, if there is only one surface, then there will be no parallelization between the two devices.</span></span> <span data-ttu-id="67973-439">Por outro lado, aumentar o número de superfícies aumenta o espaço de memória, o que pode prejudicar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="67973-439">On the other hand, increasing the number of surfaces increases the memory footprint, which can degrade performance.</span></span> <span data-ttu-id="67973-440">Este exemplo usa duas superfícies.</span><span class="sxs-lookup"><span data-stu-id="67973-440">This example uses two surfaces.</span></span>  
    ```C++
    SURFACE_QUEUE_DESC Desc;
    Desc.Width        = 640;
    Desc.Height       = 480;
    Desc.Format       = DXGI_FORMAT_R16G16B16A16_FLOAT;
    Desc.NumSurfaces  = 2;
    Desc.MetaDataSize = sizeof(UINT);
    Desc.Flags        = 0;

    CreateSurfaceQueue(&Desc, m_pD3D9Device, &m_11to9Queue);
    ```

    

3.  <span data-ttu-id="67973-441">**Clone a fila raiz.**</span><span class="sxs-lookup"><span data-stu-id="67973-441">**Clone the Root Queue.**</span></span>  
    <span data-ttu-id="67973-442">Cada fila clonada deve usar as mesmas superfícies, mas pode ter diferentes tamanhos de buffer de metadados e sinalizadores diferentes.</span><span class="sxs-lookup"><span data-stu-id="67973-442">Each cloned queue must use the same surfaces but can have different metadata buffer sizes and different flags.</span></span> <span data-ttu-id="67973-443">Nesse caso, não há metadados do Direct3D 9 para o Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="67973-443">In this case, there is no metadata from Direct3D 9 to Direct3D 11.</span></span>  
    ```C++
    SURFACE_QUEUE_CLONE_DESC Desc;
    Desc.MetaDataSize = 0;
    Desc.Flags        = 0;

    m_11to9Queue->Clone(&Desc, &m_9to11Queue);
    ```

    

4.  <span data-ttu-id="67973-444">**Abra os Dispositivos de Produtor e Consumidor.**</span><span class="sxs-lookup"><span data-stu-id="67973-444">**Open the Producer and Consumer Devices.**</span></span>  
    <span data-ttu-id="67973-445">O aplicativo deve executar essa etapa antes de chamar Enqueue e Dequeue.</span><span class="sxs-lookup"><span data-stu-id="67973-445">The application must perform this step before calling Enqueue and Dequeue.</span></span> <span data-ttu-id="67973-446">Abrir um produtor e consumidor retorna interfaces que contêm as APIs de enqueue/dequeue.</span><span class="sxs-lookup"><span data-stu-id="67973-446">Opening a producer and consumer returns interfaces which contain the enqueue/dequeue APIs.</span></span>  
    ```C++
    // Open for m_p9to11Queue.
    m_p9to11Queue->OpenProducer(m_pD3D9Device, &m_pD3D9Producer);
    m_p9to11Queue->OpenConsumer(m_pD3D11Device, &m_pD3D11Consumer);

    // Open for m_p11to9Queue.
    m_p11to9Queue->OpenProducer(m_pD3D11Device, &m_pD3D11Producer);
    m_p11to9Queue->OpenConsumer(m_pD3D9Device, &m_pD3D9Consumer);
    ```

    

<span data-ttu-id="67973-447">**Loop Principal**</span><span class="sxs-lookup"><span data-stu-id="67973-447">**Main Loop**</span></span>  
<span data-ttu-id="67973-448">O uso da fila é modelado após o problema de produtor/consumidor clássico.</span><span class="sxs-lookup"><span data-stu-id="67973-448">The usage of the queue is modeled after the classical producer/consumer problem.</span></span> <span data-ttu-id="67973-449">Pense nisso de uma perspectiva por dispositivo.</span><span class="sxs-lookup"><span data-stu-id="67973-449">Think of this from a per-device perspective.</span></span> <span data-ttu-id="67973-450">Cada dispositivo deve executar estas etapas: desfileirar para obter uma superfície de sua fila de consumo, processar na superfície e enfileirar em sua fila de produção.</span><span class="sxs-lookup"><span data-stu-id="67973-450">Each device must perform these steps: dequeue to get a surface from its consuming queue, process on the surface, and then enqueue onto its producing queue.</span></span> <span data-ttu-id="67973-451">Para o dispositivo Direct3D 11, o uso do Direct3D 9 é quase idêntico.</span><span class="sxs-lookup"><span data-stu-id="67973-451">For the Direct3D 11 device, the Direct3D 9 usage is almost identical.</span></span>  


```C++
// Direct3D 9 Device.
IDirect3DTexture9* pTexture9 = NULL;
REFIID             surfaceID9 = _uuidof(IDirect3DTexture9);
UINT               metaData;
UINT               metaDataSize;
while (!done)
{
    // Dequeue surface.
    m_pD3D9Consumer->Dequeue(surfaceID9, (void**)&pSurface9,
                             &metaData, &metaDataSize, INFINITE);

    // Process the surface.
    ProcessD3D9(pSurface9);

    // Present the surface using the meta data.
    PresentD3D9(pSurface9, metaData, metaDataSize);

    // Enqueue surface.
    m_pD3D9Producer->Enqueue(pSurface9, NULL, 0, 0);
}
```



<span data-ttu-id="67973-452">**Limpando**</span><span class="sxs-lookup"><span data-stu-id="67973-452">**Cleaning Up**</span></span>  
<span data-ttu-id="67973-453">Esta etapa é muito simples.</span><span class="sxs-lookup"><span data-stu-id="67973-453">This step is very straightforward.</span></span> <span data-ttu-id="67973-454">Além das etapas normais para limpar as APIs do Direct3D, o aplicativo deve liberar as interfaces COM de retorno.</span><span class="sxs-lookup"><span data-stu-id="67973-454">In addition to the normal steps for cleaning up Direct3D APIs, the application must release the return COM interfaces.</span></span>  


```C++
m_pD3D9Producer->Release();
m_pD3D9Consumer->Release();
m_pD3D11Producer->Release();
m_pD3D11Consumer->Release();
m_p9to11Queue->Release();
m_p11to9Queue->Release();
```



</dl>

### <a name="non-blocking-use"></a><span data-ttu-id="67973-455">Uso sem bloqueio</span><span class="sxs-lookup"><span data-stu-id="67973-455">Non-Blocking Use</span></span>

<span data-ttu-id="67973-456">O exemplo anterior faz sentido para um caso de uso multithread, no qual cada dispositivo tem seu próprio thread.</span><span class="sxs-lookup"><span data-stu-id="67973-456">The previous example makes sense for a multithreaded usage case in which each device has its own thread.</span></span> <span data-ttu-id="67973-457">O exemplo usa as versões de bloqueio das APIs: infinito para tempo limite e nenhum sinalizador para enfileirar.</span><span class="sxs-lookup"><span data-stu-id="67973-457">The example uses the blocking versions of the APIs: INFINITE for timeout, and no flag to enqueue.</span></span> <span data-ttu-id="67973-458">Se você quiser usar o auxiliar em uma forma sem bloqueio, precisará fazer apenas algumas alterações.</span><span class="sxs-lookup"><span data-stu-id="67973-458">If you want to use the helper in a non-blocking way, you need to make only a few changes.</span></span> <span data-ttu-id="67973-459">Esta seção mostra o uso sem bloqueio com ambos os dispositivos em um thread.</span><span class="sxs-lookup"><span data-stu-id="67973-459">This section shows non-blocking use with both devices on one thread.</span></span>

<span data-ttu-id="67973-460">**Inicialização**</span><span class="sxs-lookup"><span data-stu-id="67973-460">**Initialization**</span></span>  
<span data-ttu-id="67973-461">A inicialização é idêntica, exceto pelos sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="67973-461">Initialization is identical except for the flags.</span></span> <span data-ttu-id="67973-462">Como o aplicativo é de thread único, use esse sinalizador para a criação.</span><span class="sxs-lookup"><span data-stu-id="67973-462">Because the application is single-threaded, use that flag for creation.</span></span> <span data-ttu-id="67973-463">Isso desativa um pouco do código de sincronização, o que potencialmente melhora o desempenho.</span><span class="sxs-lookup"><span data-stu-id="67973-463">This turns off some of the synchronization code, which potentially improves performance.</span></span>  


```C++
SURFACE_QUEUE_DESC Desc;
Desc.Width        = 640;
Desc.Height       = 480;
Desc.Format       = DXGI_FORMAT_R16G16B16A16_FLOAT;
Desc.NumSurfaces  = 2;
Desc.MetaDataSize = sizeof(UINT);
Desc.Flags        = SURFACE_QUEUE_FLAG_SINGLE_THREADED;

CreateSurfaceQueue(&Desc, m_pD3D9Device, &m_11to9Queue);
```




```C++
SURFACE_QUEUE_CLONE_DESC Desc;
Desc.MetaDataSize = 0;
Desc.Flags        = SURFACE_QUEUE_FLAG_SINGLE_THREADED;

m_11to9Queue->Clone(&Desc, &m_9to11Queue);
```



<span data-ttu-id="67973-464">Abrir os dispositivos produtor e consumidor é o mesmo que no exemplo de bloqueio.</span><span class="sxs-lookup"><span data-stu-id="67973-464">Opening the producer and consumer devices are the same as in the blocking example.</span></span>  
<span data-ttu-id="67973-465">**Usando a fila**</span><span class="sxs-lookup"><span data-stu-id="67973-465">**Using the Queue**</span></span>  
<span data-ttu-id="67973-466">Há várias maneiras de usar a fila em um modo sem bloqueio com várias características de desempenho.</span><span class="sxs-lookup"><span data-stu-id="67973-466">There are many ways of using the queue in a non-blocking fashion with various performance characteristics.</span></span> <span data-ttu-id="67973-467">O exemplo a seguir é simples, mas tem baixo desempenho devido à rotação e sondagem excessivas.</span><span class="sxs-lookup"><span data-stu-id="67973-467">The following example is simple but has poor performance due to excessive spinning and polling.</span></span> <span data-ttu-id="67973-468">Apesar desses problemas, o exemplo mostra como usar o auxiliar.</span><span class="sxs-lookup"><span data-stu-id="67973-468">Despite these problems, the example shows how to use the helper.</span></span> <span data-ttu-id="67973-469">A abordagem é constantemente se sentar em um loop e remover da fila, processar, enfileirar e liberar.</span><span class="sxs-lookup"><span data-stu-id="67973-469">The approach is to constantly sit in a loop and dequeue, process, enqueue, and flush.</span></span> <span data-ttu-id="67973-470">Se qualquer uma das etapas falhar porque o recurso não está disponível, o aplicativo simplesmente tentará novamente o loop seguinte.</span><span class="sxs-lookup"><span data-stu-id="67973-470">If any of the steps fail because the resource is not available, the application simply tries again the next loop.</span></span>  


```C++
// Direct3D 11 Device.
ID3D11Texture2D* pSurface11 = NULL;
REFIID           surfaceID11 = __uuidof(ID3D11Texture2D);
UINT             metaData;
while (!done)
{
    //
    // D3D11 Portion.
    //

    // Dequeue surface.
    hr = m_pD3D11Consumer->Dequeue(surfaceID11,
                                   (void**)&pSurface11,
                                   NULL, 0, 0);
    // Only continue if we got a surface.
    if (SUCCEEDED(hr))
    {
        // Process the surface and return some meta data.
        ProcessD3D11(pSurface11, &metaData);

        // Enqueue surface.
        m_pD3D11Producer->Enqueue(pSurface11, &metaData,
                                  sizeof(UINT),
                                  SURFACE_QUEUE_FLAG_DO_NOT_WAIT);
    }
    // Flush the queue to check if any surfaces completed.
    m_pD3D11Producer->Flush(NULL,SURFACE_QUEUE_FLAG_DO_NOT_WAIT);

    //
    // Do the same with the Direct3D 9 Device.
    //

    // Dequeue surface.
    hr = m_pD3D9Consumer->Dequeue(surfaceID9,
                                  (void**)&pSurface9,
                                  &metaData,
                                  &metaDataSize, 0);
    // Only continue if we got a surface.
    if (SUCCEEDED(hr)))
    {
        // Process the surface.
        ProcessD3D9(pSurface9);

        // Present the surface using the meta data.
        PresentD3D9(pSurface9, metaData, metaDataSize);

        // Enqueue surface.
        m_pD3D9Producer->Enqueue(pSurface9, NULL, 0,
                                 SURFACE_QUEUE_FLAG_DO_NOT_WAIT);
    }
    // Flush the queue to check if any surfaces completed.
    m_pD3D9Producer->Flush(NULL,SURFACE_QUEUE_FLAG_DO_NOT_WAIT);
}
```



<span data-ttu-id="67973-471">Uma solução mais complexa poderia verificar o valor de retorno de enfileirar e liberar para determinar se a liberação é necessária.</span><span class="sxs-lookup"><span data-stu-id="67973-471">A more complex solution could check the return value from enqueue and from flush to determine if flushing is necessary.</span></span>  
</dl>

### <a name="three-devices"></a><span data-ttu-id="67973-472">Três dispositivos</span><span class="sxs-lookup"><span data-stu-id="67973-472">Three Devices</span></span>

<span data-ttu-id="67973-473">Estender os exemplos anteriores para abranger vários dispositivos é simples.</span><span class="sxs-lookup"><span data-stu-id="67973-473">Extending the previous examples to cover multiple devices is straightforward.</span></span> <span data-ttu-id="67973-474">O código a seguir executa a inicialização.</span><span class="sxs-lookup"><span data-stu-id="67973-474">The following code performs the initialization.</span></span> <span data-ttu-id="67973-475">Depois que os objetos Produtor/Consumidor foram criados, o código para usá-los é o mesmo.</span><span class="sxs-lookup"><span data-stu-id="67973-475">After the Producer/Consumer objects have been created, the code to use them is the same.</span></span> <span data-ttu-id="67973-476">Este exemplo tem três dispositivos e, portanto, três filas.</span><span class="sxs-lookup"><span data-stu-id="67973-476">This example has three devices and therefore three queues.</span></span> <span data-ttu-id="67973-477">As superfícies fluem do Direct3D 9 para o Direct3D 10 para o Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="67973-477">Surfaces flow from Direct3D 9 to Direct3D 10 to Direct3D 11.</span></span>


```C++
SURFACE_QUEUE_DESC Desc;
Desc.Width        = 640;
Desc.Height       = 480;
Desc.Format       = DXGI_FORMAT_R16G16B16A16_FLOAT;
Desc.NumSurfaces  = 2;
Desc.MetaDataSize = sizeof(UINT);
Desc.Flags        = 0;

SURFACE_QUEUE_CLONE_DESC Desc;
Desc.MetaDataSize = 0;
Desc.Flags        = 0;

CreateSurfaceQueue(&Desc, m_pD3D9Device, &m_11to9Queue);
m_11to9Queue->Clone(&Desc, &m_9to10Queue);
m_11to9Queue->Clone(&Desc, &m_10to11Queue);
```



<span data-ttu-id="67973-478">Conforme mencionado anteriormente, a clonagem funciona da mesma maneira, independentemente de qual fila seja clonada.</span><span class="sxs-lookup"><span data-stu-id="67973-478">As mentioned earlier, cloning works the same way, no matter which queue is cloned.</span></span> <span data-ttu-id="67973-479">Por exemplo, a segunda chamada clonar poderia ter sido fora do objeto m \_ 9to10Queue.</span><span class="sxs-lookup"><span data-stu-id="67973-479">For example, the second Clone call could have been off of the m\_9to10Queue object.</span></span>


```C++
// Open for m_p9to10Queue.
m_p9to10Queue->OpenProducer(m_pD3D9Device, &m_pD3D9Producer);
m_p9to10Queue->OpenConsumer(m_pD3D10Device, &m_pD3D10Consumer);

// Open for m_p10to11Queue.
m_p10to11Queue->OpenProducer(m_pD3D10Device, &m_pD3D10Producer);
m_p10to11Queue->OpenConsumer(m_pD3D11Device, &m_pD3D11Consumer);

// Open for m_p11to9Queue.
m_p11to9Queue->OpenProducer(m_pD3D11Device, &m_pD3D11Producer);
m_p11to9Queue->OpenConsumer(m_pD3D9Device, &m_pD3D9Consumer);
```



## <a name="conclusion"></a><span data-ttu-id="67973-480">Conclusão</span><span class="sxs-lookup"><span data-stu-id="67973-480">Conclusion</span></span>

<span data-ttu-id="67973-481">Você pode criar soluções que usam interoperabilidade para empregar o poder de várias APIs do DirectX.</span><span class="sxs-lookup"><span data-stu-id="67973-481">You can create solutions that use interoperability to employ the power of multiple DirectX APIs.</span></span> <span data-ttu-id="67973-482">A interoperabilidade da API de gráficos do Windows agora oferece um DXGI 1.1 do Common Surface Management Runtime.</span><span class="sxs-lookup"><span data-stu-id="67973-482">Windows graphics API interoperability now offers a common surface management runtime DXGI 1.1.</span></span> <span data-ttu-id="67973-483">Esse runtime permite o suporte ao compartilhamento de superfície sincronizado em APIs recém-desenvolvidas, como Direct3D 11, Direct3D 10.1 e Direct2D.</span><span class="sxs-lookup"><span data-stu-id="67973-483">This runtime enables synchronized surface sharing support within newly developed APIs, such as Direct3D 11, Direct3D 10.1 and Direct2D.</span></span> <span data-ttu-id="67973-484">Melhorias de interoperabilidade entre novas APIs e APIs existentes auxiliam na migração de aplicativos e na compatibilidade com compatibilidade com backward.</span><span class="sxs-lookup"><span data-stu-id="67973-484">Interoperability improvements between new APIs and existing APIs aid application migration and backward compatibility.</span></span> <span data-ttu-id="67973-485">As APIs de consumidor do Direct3D 9Ex e DXGI 1.1 podem interoperar, conforme mostrado com o mecanismo de sincronização fornecido por meio do código auxiliar de exemplo na Galeria de Códigos do MSDN.</span><span class="sxs-lookup"><span data-stu-id="67973-485">Direct3D 9Ex and DXGI 1.1 consumer APIs can interoperate, as shown with the synchronization mechanism provided through sample helper code on MSDN Code Gallery.</span></span>

 

 