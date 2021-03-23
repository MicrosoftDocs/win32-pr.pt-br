---
title: D2D usando D3D11on12
description: O exemplo D3D1211on12 demonstra como renderizar conteúdo D2D sobre conteúdo D3D12 compartilhando recursos entre um dispositivo baseado em 11 e um dispositivo baseado em 12.
ms.assetid: FAEF1412-053C-4B5F-80FA-85396C2586B4
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d18399b85499787f74dab725d562b6a299878b35
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "104548331"
---
# <a name="d2d-using-d3d11on12"></a><span data-ttu-id="39a23-103">D2D usando D3D11on12</span><span class="sxs-lookup"><span data-stu-id="39a23-103">D2D using D3D11on12</span></span>

<span data-ttu-id="39a23-104">O exemplo **D3D1211on12** demonstra como renderizar conteúdo D2D sobre conteúdo D3D12 compartilhando recursos entre um dispositivo baseado em 11 e um dispositivo baseado em 12.</span><span class="sxs-lookup"><span data-stu-id="39a23-104">The **D3D1211on12** sample demonstrates how to render D2D content over D3D12 content by sharing resources between an 11 based device and a 12 based device.</span></span>

-   [<span data-ttu-id="39a23-105">Criar um ID3D11On12Device</span><span class="sxs-lookup"><span data-stu-id="39a23-105">Create an ID3D11On12Device</span></span>](#create-an-id3d11on12device)
-   [<span data-ttu-id="39a23-106">Criar uma fábrica D2D</span><span class="sxs-lookup"><span data-stu-id="39a23-106">Create a D2D factory</span></span>](#create-a-d2d-factory)
-   [<span data-ttu-id="39a23-107">Criar um destino de renderização para D2D</span><span class="sxs-lookup"><span data-stu-id="39a23-107">Create a render target for D2D</span></span>](#create-a-render-target-for-d2d)
-   [<span data-ttu-id="39a23-108">Criar objetos de texto D2D básicos</span><span class="sxs-lookup"><span data-stu-id="39a23-108">Create basic D2D text objects</span></span>](#create-basic-d2d-text-objects)
-   [<span data-ttu-id="39a23-109">Atualizando o loop de renderização principal</span><span class="sxs-lookup"><span data-stu-id="39a23-109">Updating the main render loop</span></span>](#updating-the-main-render-loop)
-   [<span data-ttu-id="39a23-110">Execute o exemplo</span><span class="sxs-lookup"><span data-stu-id="39a23-110">Run the sample</span></span>](#run-the-sample)
-   [<span data-ttu-id="39a23-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="39a23-111">Related topics</span></span>](#related-topics)

## <a name="create-an-id3d11on12device"></a><span data-ttu-id="39a23-112">Criar um ID3D11On12Device</span><span class="sxs-lookup"><span data-stu-id="39a23-112">Create an ID3D11On12Device</span></span>

<span data-ttu-id="39a23-113">A primeira etapa é criar um [**ID3D11On12Device**](/windows/desktop/api/d3d11on12/nn-d3d11on12-id3d11on12device) após a criação do [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device) , que envolve a criação de um [**ID3D11Device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) que é disposto em torno do **ID3D12Device** por meio da API [**D3D11On12CreateDevice**](/windows/desktop/api/d3d11on12/nf-d3d11on12-d3d11on12createdevice).</span><span class="sxs-lookup"><span data-stu-id="39a23-113">The first step is to create an [**ID3D11On12Device**](/windows/desktop/api/d3d11on12/nn-d3d11on12-id3d11on12device) after the [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device) has been created, which involves creating an [**ID3D11Device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) that is wrapped around the **ID3D12Device** via the API [**D3D11On12CreateDevice**](/windows/desktop/api/d3d11on12/nf-d3d11on12-d3d11on12createdevice).</span></span> <span data-ttu-id="39a23-114">Essa API também leva em conta, entre outros parâmetros, um [**ID3D12CommandQueue**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue) para que o dispositivo 11On12 possa enviar seus comandos.</span><span class="sxs-lookup"><span data-stu-id="39a23-114">This API also takes in, among other parameters, an [**ID3D12CommandQueue**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue) so that the 11On12 device can submit its commands.</span></span> <span data-ttu-id="39a23-115">Depois que o **ID3D11Device** for criado, você poderá consultar a interface **ID3D11On12Device** a partir dele.</span><span class="sxs-lookup"><span data-stu-id="39a23-115">After the **ID3D11Device** is created, you can query the **ID3D11On12Device** interface from it.</span></span> <span data-ttu-id="39a23-116">Este é o objeto de dispositivo primário que será usado para configurar o D2D.</span><span class="sxs-lookup"><span data-stu-id="39a23-116">This is the primary device object that will be used to set up D2D.</span></span>

<span data-ttu-id="39a23-117">No método **LoadPipe** , configure os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="39a23-117">In the **LoadPipeline** method, setup the devices.</span></span>

``` syntax
 // Create an 11 device wrapped around the 12 device and share
    // 12's command queue.
    ComPtr<ID3D11Device> d3d11Device;
    ThrowIfFailed(D3D11On12CreateDevice(
        m_d3d12Device.Get(),
        d3d11DeviceFlags,
        nullptr,
        0,
        reinterpret_cast<IUnknown**>(m_commandQueue.GetAddressOf()),
        1,
        0,
        &d3d11Device,
        &m_d3d11DeviceContext,
        nullptr
        ));

    // Query the 11On12 device from the 11 device.
    ThrowIfFailed(d3d11Device.As(&m_d3d11On12Device));
```



| <span data-ttu-id="39a23-118">Fluxo de chamadas</span><span class="sxs-lookup"><span data-stu-id="39a23-118">Call flow</span></span>                                              | <span data-ttu-id="39a23-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="39a23-119">Parameters</span></span> |
|--------------------------------------------------------|------------|
| [<span data-ttu-id="39a23-120">**ID3D11Device**</span><span class="sxs-lookup"><span data-stu-id="39a23-120">**ID3D11Device**</span></span>](/windows/desktop/api/d3d11/nn-d3d11-id3d11device)            |            |
| [<span data-ttu-id="39a23-121">**D3D11On12CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="39a23-121">**D3D11On12CreateDevice**</span></span>](/windows/desktop/api/d3d11on12/nf-d3d11on12-d3d11on12createdevice) |            |



 

## <a name="create-a-d2d-factory"></a><span data-ttu-id="39a23-122">Criar uma fábrica D2D</span><span class="sxs-lookup"><span data-stu-id="39a23-122">Create a D2D factory</span></span>

<span data-ttu-id="39a23-123">Agora que temos um dispositivo 11On12, usamos-o para criar uma fábrica e um dispositivo do D2D da mesma forma que normalmente faria com o D3D11.</span><span class="sxs-lookup"><span data-stu-id="39a23-123">Now that we have an 11On12 device, we use it to create a D2D factory and device just as it would normally be done with D3D11.</span></span>

<span data-ttu-id="39a23-124">Adicione ao método **Loadassets** .</span><span class="sxs-lookup"><span data-stu-id="39a23-124">Add to the **LoadAssets** method.</span></span>

``` syntax
 // Create D2D/DWrite components.
    {
        D2D1_DEVICE_CONTEXT_OPTIONS deviceOptions = D2D1_DEVICE_CONTEXT_OPTIONS_NONE;
        ThrowIfFailed(D2D1CreateFactory(D2D1_FACTORY_TYPE_SINGLE_THREADED, __uuidof(ID2D1Factory3), &d2dFactoryOptions, &m_d2dFactory));
        ComPtr<IDXGIDevice> dxgiDevice;
        ThrowIfFailed(m_d3d11On12Device.As(&dxgiDevice));
        ThrowIfFailed(m_d2dFactory->CreateDevice(dxgiDevice.Get(), &m_d2dDevice));
        ThrowIfFailed(m_d2dDevice->CreateDeviceContext(deviceOptions, &m_d2dDeviceContext));
        ThrowIfFailed(DWriteCreateFactory(DWRITE_FACTORY_TYPE_SHARED, __uuidof(IDWriteFactory), &m_dWriteFactory));
    }
```



| <span data-ttu-id="39a23-125">Fluxo de chamadas</span><span class="sxs-lookup"><span data-stu-id="39a23-125">Call flow</span></span>                                                                        | <span data-ttu-id="39a23-126">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="39a23-126">Parameters</span></span>                                                   |
|----------------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="39a23-127">**\_Opções de \_ contexto de dispositivo d2d1 \_**</span><span class="sxs-lookup"><span data-stu-id="39a23-127">**D2D1\_DEVICE\_CONTEXT\_OPTIONS**</span></span>](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_device_context_options)     |                                                              |
| [<span data-ttu-id="39a23-128">**D2D1CreateFactory**</span><span class="sxs-lookup"><span data-stu-id="39a23-128">**D2D1CreateFactory**</span></span>](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory)                              | [<span data-ttu-id="39a23-129">**\_Tipo de fábrica d2d1 \_**</span><span class="sxs-lookup"><span data-stu-id="39a23-129">**D2D1\_FACTORY\_TYPE**</span></span>](/windows/desktop/api/d2d1/ne-d2d1-d2d1_factory_type)        |
| [<span data-ttu-id="39a23-130">**IDXGIDevice**</span><span class="sxs-lookup"><span data-stu-id="39a23-130">**IDXGIDevice**</span></span>](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice)                                      |                                                              |
| [<span data-ttu-id="39a23-131">**ID2D1Factory3:: CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="39a23-131">**ID2D1Factory3::CreateDevice**</span></span>](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1factory3-createdevice)           |                                                              |
| [<span data-ttu-id="39a23-132">**ID2D1Device::CreateDeviceContext**</span><span class="sxs-lookup"><span data-stu-id="39a23-132">**ID2D1Device::CreateDeviceContext**</span></span>](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1device-createdevicecontext) |                                                              |
| [<span data-ttu-id="39a23-133">**DWriteCreateFactory**</span><span class="sxs-lookup"><span data-stu-id="39a23-133">**DWriteCreateFactory**</span></span>](/windows/desktop/api/dwrite/nf-dwrite-dwritecreatefactory)                       | [<span data-ttu-id="39a23-134">**\_tipo de fábrica DWRITE \_**</span><span class="sxs-lookup"><span data-stu-id="39a23-134">**DWRITE\_FACTORY\_TYPE**</span></span>](/windows/desktop/api/dwrite/ne-dwrite-dwrite_factory_type) |



 

## <a name="create-a-render-target-for-d2d"></a><span data-ttu-id="39a23-135">Criar um destino de renderização para D2D</span><span class="sxs-lookup"><span data-stu-id="39a23-135">Create a render target for D2D</span></span>

<span data-ttu-id="39a23-136">D3D12 possui a cadeia de permuta; portanto, se quisermos renderizar para o buffer de fundo usando nosso dispositivo 11On12 (D2D Content), precisamos criar recursos encapsulados do tipo [**ID3D11Resource**](/windows/desktop/api/d3d11/nn-d3d11-id3d11resource) dos buffers de fundo do tipo [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span><span class="sxs-lookup"><span data-stu-id="39a23-136">D3D12 owns the swap chain, so if we want to render to the back buffer using our 11On12 device (D2D content), then we need to create wrapped resources of type [**ID3D11Resource**](/windows/desktop/api/d3d11/nn-d3d11-id3d11resource) from the back buffers of type [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span></span> <span data-ttu-id="39a23-137">Isso vincula o **ID3D12Resource** a uma interface baseada em D3D11 para que ele possa ser usado com o dispositivo 11On12.</span><span class="sxs-lookup"><span data-stu-id="39a23-137">This links the **ID3D12Resource** with a D3D11 based interface so that it can be used with the 11On12 device.</span></span> <span data-ttu-id="39a23-138">Depois de termos um recurso encapsulado, podemos criar uma superfície de destino de renderização para D2D para renderizar, também no método **Loadassets** .</span><span class="sxs-lookup"><span data-stu-id="39a23-138">After we have a wrapped resource, we can then create a render target surface for D2D to render to, also in the **LoadAssets** method.</span></span>

``` syntax
 // Query the desktop's dpi settings, which will be used to create
    // D2D's render targets.
    float dpiX;
    float dpiY;
    m_d2dFactory->GetDesktopDpi(&dpiX, &dpiY);
    D2D1_BITMAP_PROPERTIES1 bitmapProperties = D2D1::BitmapProperties1(
        D2D1_BITMAP_OPTIONS_TARGET | D2D1_BITMAP_OPTIONS_CANNOT_DRAW,
        D2D1::PixelFormat(DXGI_FORMAT_UNKNOWN, D2D1_ALPHA_MODE_PREMULTIPLIED),
        dpiX,
        dpiY
        );  

    // Create frame resources.
    {
        CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart());

        // Create a RTV, D2D render target, and a command allocator for each frame.
        for (UINT n = 0; n < FrameCount; n++)
        {
            ThrowIfFailed(m_swapChain->GetBuffer(n, IID_PPV_ARGS(&m_renderTargets[n])));
            m_d3d12Device->CreateRenderTargetView(m_renderTargets[n].Get(), nullptr, rtvHandle);

            // Create a wrapped 11On12 resource of this back buffer. Since we are 
            // rendering all D3D12 content first and then all D2D content, we specify 
            // the In resource state as RENDER_TARGET - because D3D12 will have last 
            // used it in this state - and the Out resource state as PRESENT. When 
            // ReleaseWrappedResources() is called on the 11On12 device, the resource 
            // will be transitioned to the PRESENT state.
            D3D11_RESOURCE_FLAGS d3d11Flags = { D3D11_BIND_RENDER_TARGET };
            ThrowIfFailed(m_d3d11On12Device->CreateWrappedResource(
                m_renderTargets[n].Get(),
                &d3d11Flags,
                D3D12_RESOURCE_STATE_RENDER_TARGET,
                D3D12_RESOURCE_STATE_PRESENT,
                IID_PPV_ARGS(&m_wrappedBackBuffers[n])
                ));

            // Create a render target for D2D to draw directly to this back buffer.
            ComPtr<IDXGISurface> surface;
            ThrowIfFailed(m_wrappedBackBuffers[n].As(&surface));
            ThrowIfFailed(m_d2dDeviceContext->CreateBitmapFromDxgiSurface(
                surface.Get(),
                &bitmapProperties,
                &m_d2dRenderTargets[n]
                ));

            rtvHandle.Offset(1, m_rtvDescriptorSize);

            ThrowIfFailed(m_d3d12Device->CreateCommandAllocator(D3D12_COMMAND_LIST_TYPE_DIRECT, IID_PPV_ARGS(&m_commandAllocators[n])));
        }
    }
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="39a23-139">Fluxo de chamadas</span><span class="sxs-lookup"><span data-stu-id="39a23-139">Call flow</span></span></th>
<th><span data-ttu-id="39a23-140">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="39a23-140">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="39a23-141"><a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi"><strong>ID2D1Factory::GetDesktopDpi</strong></a></span><span class="sxs-lookup"><span data-stu-id="39a23-141"><a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi"><strong>ID2D1Factory::GetDesktopDpi</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="39a23-142"><a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_bitmap_properties1"><strong>D2D1_BITMAP_PROPERTIES1</strong></a></span><span class="sxs-lookup"><span data-stu-id="39a23-142"><a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_bitmap_properties1"><strong>D2D1_BITMAP_PROPERTIES1</strong></a></span></span></td>
<td><dl><span data-ttu-id="39a23-143"><a href="/windows/desktop/api/d2d1_1helper/nf-d2d1_1helper-bitmapproperties1"><strong>BitmapProperties1</strong></a></span><span class="sxs-lookup"><span data-stu-id="39a23-143"><a href="/windows/desktop/api/d2d1_1helper/nf-d2d1_1helper-bitmapproperties1"><strong>BitmapProperties1</strong></a></span></span><br />
<span data-ttu-id="39a23-144">[<strong>D2D1_BITMAP_OPTIONS</strong>] (/Windows/Desktop/API/d2d1_1/ne-d2d1_1-d2d1_bitmap_options)</span><span class="sxs-lookup"><span data-stu-id="39a23-144">[<strong>D2D1_BITMAP_OPTIONS</strong>](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_bitmap_options)</span></span><br />
<span data-ttu-id="39a23-145">[<strong>PixelFormat</strong>] (/windows/desktop/api/d2d1helper/nf-d2d1helper-pixelformat)</span><span class="sxs-lookup"><span data-stu-id="39a23-145">[<strong>PixelFormat</strong>](/windows/desktop/api/d2d1helper/nf-d2d1helper-pixelformat)</span></span><br />
<span data-ttu-id="39a23-146">[<strong>DXGI_FORMAT</strong>] (/Windows/Desktop/API/dxgiformat/ne-dxgiformat-dxgi_format)</span><span class="sxs-lookup"><span data-stu-id="39a23-146">[<strong>DXGI_FORMAT</strong>](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)</span></span><br />
<span data-ttu-id="39a23-147">[<strong>D2D1_ALPHA_MODE</strong>] (/Windows/Desktop/API/dcommon/ne-dcommon-d2d1_alpha_mode)</span><span class="sxs-lookup"><span data-stu-id="39a23-147">[<strong>D2D1_ALPHA_MODE</strong>](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode)</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="39a23-148"><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="39a23-148"><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></span></span></td>
<td><span data-ttu-id="39a23-149"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>GetCPUDescriptorHandleForHeapStart</strong></a></span><span class="sxs-lookup"><span data-stu-id="39a23-149"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>GetCPUDescriptorHandleForHeapStart</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="39a23-150"><a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer"><strong>IDXGISwapChain::GetBuffer</strong></a></span><span class="sxs-lookup"><span data-stu-id="39a23-150"><a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer"><strong>IDXGISwapChain::GetBuffer</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="39a23-151"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrendertargetview"><strong>CreateRenderTargetView</strong></a></span><span class="sxs-lookup"><span data-stu-id="39a23-151"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrendertargetview"><strong>CreateRenderTargetView</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="39a23-152"><a href="/windows/desktop/api/d3d11on12/ns-d3d11on12-d3d11_resource_flags"><strong>D3D11_RESOURCE_FLAGS</strong></a></span><span class="sxs-lookup"><span data-stu-id="39a23-152"><a href="/windows/desktop/api/d3d11on12/ns-d3d11on12-d3d11_resource_flags"><strong>D3D11_RESOURCE_FLAGS</strong></a></span></span></td>
<td><span data-ttu-id="39a23-153"><a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_bind_flag"><strong>D3D11_BIND_FLAG</strong></a></span><span class="sxs-lookup"><span data-stu-id="39a23-153"><a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_bind_flag"><strong>D3D11_BIND_FLAG</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="39a23-154"><a href="/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-createwrappedresource"><strong>CreateWrappedResource</strong></a></span><span class="sxs-lookup"><span data-stu-id="39a23-154"><a href="/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-createwrappedresource"><strong>CreateWrappedResource</strong></a></span></span></td>
<td><span data-ttu-id="39a23-155"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span><span class="sxs-lookup"><span data-stu-id="39a23-155"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="39a23-156"><a href="/windows/desktop/api/dxgi/nn-dxgi-idxgisurface"><strong>IDXGISurface</strong></a></span><span class="sxs-lookup"><span data-stu-id="39a23-156"><a href="/windows/desktop/api/dxgi/nn-dxgi-idxgisurface"><strong>IDXGISurface</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="39a23-157"><a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1__id2d1bitmap1)"><strong>ID2D1DeviceContext:: CreateBitmapFromDxgiSurface</strong></a></span><span class="sxs-lookup"><span data-stu-id="39a23-157"><a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1__id2d1bitmap1)"><strong>ID2D1DeviceContext::CreateBitmapFromDxgiSurface</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="39a23-158"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommandallocator"><strong>CreateCommandAllocator</strong></a></span><span class="sxs-lookup"><span data-stu-id="39a23-158"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommandallocator"><strong>CreateCommandAllocator</strong></a></span></span></td>
<td><span data-ttu-id="39a23-159"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type"><strong>D3D12_COMMAND_LIST_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="39a23-159"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type"><strong>D3D12_COMMAND_LIST_TYPE</strong></a></span></span></td>
</tr>
</tbody>
</table>



 

## <a name="create-basic-d2d-text-objects"></a><span data-ttu-id="39a23-160">Criar objetos de texto D2D básicos</span><span class="sxs-lookup"><span data-stu-id="39a23-160">Create basic D2D text objects</span></span>

<span data-ttu-id="39a23-161">Agora temos um [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device) para renderizar o conteúdo 3D, um [**ID2D1Device**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1device) que é compartilhado com o nosso dispositivo por meio de um [**ID3D11On12Device**](/windows/desktop/api/d3d11on12/nn-d3d11on12-id3d11on12device) , que podemos usar para renderizar conteúdo 2D – e eles estão configurados para renderizar para a mesma cadeia de permuta.</span><span class="sxs-lookup"><span data-stu-id="39a23-161">Now we have an [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device) to render 3D content, an [**ID2D1Device**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1device) that is shared with our 12 device via an [**ID3D11On12Device**](/windows/desktop/api/d3d11on12/nn-d3d11on12-id3d11on12device) - which we can use to render 2D content - and they are both configured to render to the same swap chain.</span></span> <span data-ttu-id="39a23-162">Este exemplo simplesmente usa o dispositivo D2D para renderizar texto pela cena 3D, semelhante a como os jogos renderizam sua interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="39a23-162">This sample simply uses the D2D device to render text over the 3D scene, similar to how games render their UI.</span></span> <span data-ttu-id="39a23-163">Para isso, precisamos criar alguns objetos D2D básicos, ainda no método **Loadassets** .</span><span class="sxs-lookup"><span data-stu-id="39a23-163">For that, we need to create some basic D2D objects, still in the **LoadAssets** method.</span></span>

``` syntax
 // Create D2D/DWrite objects for rendering text.
    {
        ThrowIfFailed(m_d2dDeviceContext->CreateSolidColorBrush(D2D1::ColorF(D2D1::ColorF::Black), &m_textBrush));
        ThrowIfFailed(m_dWriteFactory->CreateTextFormat(
            L"Verdana",
            NULL,
            DWRITE_FONT_WEIGHT_NORMAL,
            DWRITE_FONT_STYLE_NORMAL,
            DWRITE_FONT_STRETCH_NORMAL,
            50,
            L"en-us",
            &m_textFormat
            ));
        ThrowIfFailed(m_textFormat->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER));
        ThrowIfFailed(m_textFormat->SetParagraphAlignment(DWRITE_PARAGRAPH_ALIGNMENT_CENTER));
    }
```



| <span data-ttu-id="39a23-164">Fluxo de chamadas</span><span class="sxs-lookup"><span data-stu-id="39a23-164">Call flow</span></span>                                                                                           | <span data-ttu-id="39a23-165">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="39a23-165">Parameters</span></span>                                                                 |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="39a23-166">[**ID2D1RenderTarget:: CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush))</span><span class="sxs-lookup"><span data-stu-id="39a23-166">[**ID2D1RenderTarget::CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush))</span></span>    | [<span data-ttu-id="39a23-167">**ColorF**</span><span class="sxs-lookup"><span data-stu-id="39a23-167">**ColorF**</span></span>](/windows/desktop/api/d2d1helper/nl-d2d1helper-colorf)                                              |
| [<span data-ttu-id="39a23-168">**IDWriteFactory:: CreateTextFormat**</span><span class="sxs-lookup"><span data-stu-id="39a23-168">**IDWriteFactory::CreateTextFormat**</span></span>](/windows/desktop/api/dwrite/nf-dwrite-idwritefactory-createtextformat)                 | [<span data-ttu-id="39a23-169">**\_espessura da fonte DWRITE \_**</span><span class="sxs-lookup"><span data-stu-id="39a23-169">**DWRITE\_FONT\_WEIGHT**</span></span>](/windows/desktop/api/dwrite/ne-dwrite-dwrite_font_weight)                 |
| [<span data-ttu-id="39a23-170">**IDWriteTextFormat:: SetTextAlign**</span><span class="sxs-lookup"><span data-stu-id="39a23-170">**IDWriteTextFormat::SetTextAlignment**</span></span>](/windows/desktop/api/dwrite/nf-dwrite-idwritetextformat-settextalignment)           | [<span data-ttu-id="39a23-171">**\_alinhamento de texto DWRITE \_**</span><span class="sxs-lookup"><span data-stu-id="39a23-171">**DWRITE\_TEXT\_ALIGNMENT**</span></span>](/windows/desktop/api/dwrite/ne-dwrite-dwrite_text_alignment)           |
| [<span data-ttu-id="39a23-172">**IDWriteTextFormat::SetParagraphAlignment**</span><span class="sxs-lookup"><span data-stu-id="39a23-172">**IDWriteTextFormat::SetParagraphAlignment**</span></span>](/windows/desktop/api/dwrite/nf-dwrite-idwritetextformat-setparagraphalignment) | [<span data-ttu-id="39a23-173">**\_alinhamento de parágrafo DWRITE \_**</span><span class="sxs-lookup"><span data-stu-id="39a23-173">**DWRITE\_PARAGRAPH\_ALIGNMENT**</span></span>](/windows/desktop/api/dwrite/ne-dwrite-dwrite_paragraph_alignment) |



 

## <a name="updating-the-main-render-loop"></a><span data-ttu-id="39a23-174">Atualizando o loop de renderização principal</span><span class="sxs-lookup"><span data-stu-id="39a23-174">Updating the main render loop</span></span>

<span data-ttu-id="39a23-175">Agora que a inicialização do exemplo está completa, podemos passar para o loop de renderização principal.</span><span class="sxs-lookup"><span data-stu-id="39a23-175">Now that the initialization of the sample is complete, we can move on to the main render loop.</span></span>

``` syntax
// Render the scene.
void D3D1211on12::OnRender()
{
    // Record all the commands we need to render the scene into the command list.
    PopulateCommandList();

    // Execute the command list.
    ID3D12CommandList* ppCommandLists[] = { m_commandList.Get() };
    m_commandQueue->ExecuteCommandLists(_countof(ppCommandLists), ppCommandLists);

    RenderUI();

    // Present the frame.
    ThrowIfFailed(m_swapChain->Present(0, 0));

    MoveToNextFrame();
}
```



| <span data-ttu-id="39a23-176">Fluxo de chamadas</span><span class="sxs-lookup"><span data-stu-id="39a23-176">Call flow</span></span>                                                              | <span data-ttu-id="39a23-177">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="39a23-177">Parameters</span></span> |
|------------------------------------------------------------------------|------------|
| [<span data-ttu-id="39a23-178">**ID3D12CommandList**</span><span class="sxs-lookup"><span data-stu-id="39a23-178">**ID3D12CommandList**</span></span>](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandlist)                         |            |
| [<span data-ttu-id="39a23-179">**ExecuteCommandLists**</span><span class="sxs-lookup"><span data-stu-id="39a23-179">**ExecuteCommandLists**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)  |            |
| [<span data-ttu-id="39a23-180">**IDXGISwapChain1::Present1**</span><span class="sxs-lookup"><span data-stu-id="39a23-180">**IDXGISwapChain1::Present1**</span></span>](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1) |            |



 

<span data-ttu-id="39a23-181">A única novidade em nosso loop de processamento é a chamada **RenderUI** , que usará D2D para renderizar nossa interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="39a23-181">The only thing new to our render loop is the **RenderUI** call, which will use D2D to render our UI.</span></span> <span data-ttu-id="39a23-182">Observe que executamos todas as nossas listas de comandos D3D12 primeiro para renderizar nossa cena 3D e, em seguida, renderizamos nossa interface do usuário sobre isso.</span><span class="sxs-lookup"><span data-stu-id="39a23-182">Notice that we execute all of our D3D12 command lists first to render our 3D scene, and then we render our UI on top of that.</span></span> <span data-ttu-id="39a23-183">Antes de nos aprofundarmos no **RenderUI**, devemos examinar uma alteração em **PopulateCommandLists**.</span><span class="sxs-lookup"><span data-stu-id="39a23-183">Before we dive into **RenderUI**, we must look at a change to **PopulateCommandLists**.</span></span> <span data-ttu-id="39a23-184">Em outros exemplos, normalmente colocamos uma barreira de recurso na lista de comandos antes de fechá-la para fazer a transição do buffer de fundo do estado de destino de renderização para o estado atual.</span><span class="sxs-lookup"><span data-stu-id="39a23-184">In other samples we commonly put a resource barrier on the command list prior to closing it to transition the back buffer from the render target state to the present state.</span></span> <span data-ttu-id="39a23-185">No entanto, neste exemplo, removemos essa barreira de recurso, porque ainda precisamos renderizar para os buffers de fundo com D2D.</span><span class="sxs-lookup"><span data-stu-id="39a23-185">However, in this sample we remove that resource barrier, because we still need to render to the back buffers with D2D.</span></span> <span data-ttu-id="39a23-186">Observe que, quando criamos nossos recursos encapsulados do buffer de fundo, especificamos o estado de destino de renderização como o estado "IN" e o estado atual como o estado "OUT".</span><span class="sxs-lookup"><span data-stu-id="39a23-186">Note that when we created our wrapped resources of the back buffer that we specified the render target state as the “IN” state and the present state as the “OUT” state.</span></span>

<span data-ttu-id="39a23-187">O **RenderUI** é bastante direto em termos de uso de D2D.</span><span class="sxs-lookup"><span data-stu-id="39a23-187">**RenderUI** is fairly straight-forward in terms of D2D usage.</span></span> <span data-ttu-id="39a23-188">Definimos nosso destino de renderização e renderizamos nosso texto.</span><span class="sxs-lookup"><span data-stu-id="39a23-188">We set our render target and render our text.</span></span> <span data-ttu-id="39a23-189">No entanto, antes de usar qualquer recurso encapsulado em um dispositivo 11On12, como nosso buffer de retorno de destino, devemos chamar a API [**AcquireWrappedResources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-acquirewrappedresources) no dispositivo 11On12.</span><span class="sxs-lookup"><span data-stu-id="39a23-189">However, before using any wrapped resources on an 11On12 device, such as our back buffer render targets, we must call the [**AcquireWrappedResources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-acquirewrappedresources) API on the 11On12 device.</span></span> <span data-ttu-id="39a23-190">Após a renderização, chamamos a API [**ReleaseWrappedResources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-releasewrappedresources) no dispositivo 11On12.</span><span class="sxs-lookup"><span data-stu-id="39a23-190">After rendering we call the [**ReleaseWrappedResources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-releasewrappedresources) API on the 11On12 device.</span></span> <span data-ttu-id="39a23-191">Ao chamar **ReleaseWrappedResources** , incorremos em uma barreira de recursos em segundo plano que fará a transição do recurso especificado para o estado "out" especificado no momento da criação.</span><span class="sxs-lookup"><span data-stu-id="39a23-191">By calling **ReleaseWrappedResources** we incur a resource barrier behind the scenes that will transition the specified resource to the “OUT” state specified at creation time.</span></span> <span data-ttu-id="39a23-192">Em nosso caso, esse é o estado atual.</span><span class="sxs-lookup"><span data-stu-id="39a23-192">In our case, this is the present state.</span></span> <span data-ttu-id="39a23-193">Por fim, para enviar todos os nossos comandos executados no dispositivo 11On12 para o [**ID3D12CommandQueue**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue)compartilhado, devemos chamar [**flush**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-flush) no [**ID3D11DeviceContext**](/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext).</span><span class="sxs-lookup"><span data-stu-id="39a23-193">Finally, in order to submit all of our commands performed on the 11On12 device to the shared [**ID3D12CommandQueue**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue), we must call [**Flush**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-flush) on the [**ID3D11DeviceContext**](/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext).</span></span>

``` syntax
// Render text over D3D12 using D2D via the 11On12 device.
void D3D1211on12::RenderUI()
{
    D2D1_SIZE_F rtSize = m_d2dRenderTargets[m_frameIndex]->GetSize();
    D2D1_RECT_F textRect = D2D1::RectF(0, 0, rtSize.width, rtSize.height);
    static const WCHAR text[] = L"11On12";

    // Acquire our wrapped render target resource for the current back buffer.
    m_d3d11On12Device->AcquireWrappedResources(m_wrappedBackBuffers[m_frameIndex].GetAddressOf(), 1);

    // Render text directly to the back buffer.
    m_d2dDeviceContext->SetTarget(m_d2dRenderTargets[m_frameIndex].Get());
    m_d2dDeviceContext->BeginDraw();
    m_d2dDeviceContext->SetTransform(D2D1::Matrix3x2F::Identity());
    m_d2dDeviceContext->DrawTextW(
        text,
        _countof(text) - 1,
        m_textFormat.Get(),
        &textRect,
        m_textBrush.Get()
        );
    ThrowIfFailed(m_d2dDeviceContext->EndDraw());

    // Release our wrapped render target resource. Releasing 
    // transitions the back buffer resource to the state specified
    // as the OutState when the wrapped resource was created.
    m_d3d11On12Device->ReleaseWrappedResources(m_wrappedBackBuffers[m_frameIndex].GetAddressOf(), 1);

    // Flush to submit the 11 command list to the shared command queue.
    m_d3d11DeviceContext->Flush();
}
```



| <span data-ttu-id="39a23-194">Fluxo de chamadas</span><span class="sxs-lookup"><span data-stu-id="39a23-194">Call flow</span></span>                                                                                                                                                                                 | <span data-ttu-id="39a23-195">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="39a23-195">Parameters</span></span>                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| [<span data-ttu-id="39a23-196">**D2D1 \_ tamanho \_ F**</span><span class="sxs-lookup"><span data-stu-id="39a23-196">**D2D1\_SIZE\_F**</span></span>](/windows/desktop/Direct2D/d2d1-size-f)                                                                                                                                                 |                                       |
| [<span data-ttu-id="39a23-197">**D2D1 \_ Rect \_ F**</span><span class="sxs-lookup"><span data-stu-id="39a23-197">**D2D1\_RECT\_F**</span></span>](/windows/desktop/Direct2D/d2d1-rect-f)                                                                                                                                                 | [<span data-ttu-id="39a23-198">**RectF**</span><span class="sxs-lookup"><span data-stu-id="39a23-198">**RectF**</span></span>](/windows/desktop/api/d2d1helper/nf-d2d1helper-rectf)           |
| [<span data-ttu-id="39a23-199">**AcquireWrappedResources**</span><span class="sxs-lookup"><span data-stu-id="39a23-199">**AcquireWrappedResources**</span></span>](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-acquirewrappedresources)                                                                                                               |                                       |
| [<span data-ttu-id="39a23-200">**ID2D1DeviceContext:: SetTarget**</span><span class="sxs-lookup"><span data-stu-id="39a23-200">**ID2D1DeviceContext::SetTarget**</span></span>](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-settarget)                                                                                                                |                                       |
| [<span data-ttu-id="39a23-201">**ID2D1RenderTarget:: BeginDraw**</span><span class="sxs-lookup"><span data-stu-id="39a23-201">**ID2D1RenderTarget::BeginDraw**</span></span>](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw)                                                                                                                  |                                       |
| [<span data-ttu-id="39a23-202">**ID2D1RenderTarget:: SetTransform**</span><span class="sxs-lookup"><span data-stu-id="39a23-202">**ID2D1RenderTarget::SetTransform**</span></span>](/windows/desktop/Direct2D/id2d1rendertarget-settransform)                                                                                                            | [<span data-ttu-id="39a23-203">**Matrix3x2F**</span><span class="sxs-lookup"><span data-stu-id="39a23-203">**Matrix3x2F**</span></span>](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) |
| <span data-ttu-id="39a23-204">[**ID2D1RenderTarget::D rawTextW**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))</span><span class="sxs-lookup"><span data-stu-id="39a23-204">[**ID2D1RenderTarget::DrawTextW**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))</span></span> |                                       |
| [<span data-ttu-id="39a23-205">**ID2D1RenderTarget:: EndDraw**</span><span class="sxs-lookup"><span data-stu-id="39a23-205">**ID2D1RenderTarget::EndDraw**</span></span>](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw)                                                                                                                      |                                       |
| [<span data-ttu-id="39a23-206">**ReleaseWrappedResources**</span><span class="sxs-lookup"><span data-stu-id="39a23-206">**ReleaseWrappedResources**</span></span>](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-releasewrappedresources)                                                                                                               |                                       |
| [<span data-ttu-id="39a23-207">**ID3D11DeviceContext:: flush**</span><span class="sxs-lookup"><span data-stu-id="39a23-207">**ID3D11DeviceContext::Flush**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-flush)                                                                                                                    |                                       |



 

## <a name="run-the-sample"></a><span data-ttu-id="39a23-208">Execute o exemplo</span><span class="sxs-lookup"><span data-stu-id="39a23-208">Run the sample</span></span>

![a saída final do 11 no exemplo de 12](images/11on12image.png)

## <a name="related-topics"></a><span data-ttu-id="39a23-210">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="39a23-210">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39a23-211">Instruções passo a passo de código do D3D12</span><span class="sxs-lookup"><span data-stu-id="39a23-211">D3D12 Code Walk-Throughs</span></span>](d3d12-code-walk-throughs.md)
</dt> <dt>

[<span data-ttu-id="39a23-212">Direct3D 11 on 12</span><span class="sxs-lookup"><span data-stu-id="39a23-212">Direct3D 11 on 12</span></span>](direct3d-11-on-12.md)
</dt> <dt>

[<span data-ttu-id="39a23-213">Interoperabilidade do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="39a23-213">Direct3D 12 Interop</span></span>](direct3d-12-interop.md)
</dt> <dt>

[<span data-ttu-id="39a23-214">Referência de 11on12</span><span class="sxs-lookup"><span data-stu-id="39a23-214">11on12 Reference</span></span>](direct3d-11on12-reference.md)
</dt> </dl>

 

 