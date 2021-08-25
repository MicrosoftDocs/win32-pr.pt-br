---
title: O D2D usando o D3D11on12
description: O exemplo D3D1211on12 demonstra como renderizar conteúdo D2D em conteúdo D3D12 compartilhando recursos entre um dispositivo baseado em 11 e um dispositivo baseado em 12.
ms.assetid: FAEF1412-053C-4B5F-80FA-85396C2586B4
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a84f935ba49df4910aa729c39ae6ac0ce08f3810bf3b0cd75752bbe4c00e9ef1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858007"
---
# <a name="d2d-using-d3d11on12"></a>O D2D usando o D3D11on12

O exemplo **D3D1211on12** demonstra como renderizar conteúdo D2D em conteúdo D3D12 compartilhando recursos entre um dispositivo baseado em 11 e um dispositivo baseado em 12.

-   [Criar um ID3D11On12Device](#create-an-id3d11on12device)
-   [Criar uma fábrica D2D](#create-a-d2d-factory)
-   [Criar um destino de renderização para D2D](#create-a-render-target-for-d2d)
-   [Criar objetos de texto D2D básicos](#create-basic-d2d-text-objects)
-   [Atualizando o loop de renderização principal](#updating-the-main-render-loop)
-   [Executar o exemplo](#run-the-sample)
-   [Tópicos relacionados](#related-topics)

## <a name="create-an-id3d11on12device"></a>Criar um ID3D11On12Device

A primeira etapa é criar um [**ID3D11On12Device**](/windows/desktop/api/d3d11on12/nn-d3d11on12-id3d11on12device) após a criação do [**ID3D12Device,**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device) que envolve a criação de [**um ID3D11Device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) que é envolvido em torno de **ID3D12Device** por meio da API [**D3D11On12CreateDevice**](/windows/desktop/api/d3d11on12/nf-d3d11on12-d3d11on12createdevice). Essa API também utiliza, entre outros parâmetros, [**um ID3D12CommandQueue**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue) para que o dispositivo 11On12 possa enviar seus comandos. Depois que **ID3D11Device** for criado, você poderá consultar a interface **ID3D11On12Device** dela. Esse é o objeto de dispositivo primário que será usado para configurar o D2D.

No método **LoadPipeline,** configure os dispositivos.

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



| Fluxo de chamada                                              | Parâmetros |
|--------------------------------------------------------|------------|
| [**ID3D11Device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device)            |            |
| [**D3D11On12CreateDevice**](/windows/desktop/api/d3d11on12/nf-d3d11on12-d3d11on12createdevice) |            |



 

## <a name="create-a-d2d-factory"></a>Criar uma fábrica D2D

Agora que temos um dispositivo 11On12, o usamos para criar um dispositivo e uma fábrica D2D, assim como normalmente seria feito com D3D11.

Adicione ao **método LoadAssets.**

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



| Fluxo de chamada                                                                        | Parâmetros                                                   |
|----------------------------------------------------------------------------------|--------------------------------------------------------------|
| [**OPÇÕES DE CONTEXTO DO DISPOSITIVO D2D1 \_ \_ \_**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_device_context_options)     |                                                              |
| [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory)                              | [**TIPO DE FÁBRICA D2D1 \_ \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_factory_type)        |
| [**IDXGIDevice**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice)                                      |                                                              |
| [**ID2D1Factory3::CreateDevice**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1factory3-createdevice)           |                                                              |
| [**ID2D1Device::CreateDeviceContext**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1device-createdevicecontext) |                                                              |
| [**DWriteCreateFactory**](/windows/desktop/api/dwrite/nf-dwrite-dwritecreatefactory)                       | [**TIPO DE \_ FÁBRICA DWRITE \_**](/windows/desktop/api/dwrite/ne-dwrite-dwrite_factory_type) |



 

## <a name="create-a-render-target-for-d2d"></a>Criar um destino de renderização para D2D

D3D12 possui a cadeia de permuta, portanto, se quisermos renderizar para o buffer de fundo usando nosso dispositivo 11On12 (conteúdo D2D), precisamos criar recursos empacotados do tipo [**ID3D11Resource**](/windows/desktop/api/d3d11/nn-d3d11-id3d11resource) dos buffers de fundo do tipo [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource). Isso vincula **a ID3D12Resource** a uma interface baseada em D3D11 para que ela possa ser usada com o dispositivo 11On12. Depois de termos um recurso empacotado, podemos criar uma superfície de destino de renderização para a renderização do D2D, também no **método LoadAssets.**

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
<th>Fluxo de chamada</th>
<th>Parâmetros</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi"><strong>ID2D1Factory::GetDesktopDpi</strong></a></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_bitmap_properties1"><strong>D2D1_BITMAP_PROPERTIES1</strong></a></td>
<td><dl><a href="/windows/desktop/api/d2d1_1helper/nf-d2d1_1helper-bitmapproperties1"><strong>BitmapProperties1</strong></a><br />
[<strong>D2D1_BITMAP_OPTIONS</strong>] (/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_bitmap_options)<br />
[<strong>PixelFormat</strong>] (/windows/desktop/api/d2d1helper/nf-d2d1helper-pixelformat)<br />
[<strong>DXGI_FORMAT</strong>] (/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)<br />
[<strong>D2D1_ALPHA_MODE</strong>] (/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode)<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></td>
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>GetCPUDescriptorHandleForHeapStart</strong></a></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer"><strong>IDXGISwapChain::GetBuffer</strong></a></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrendertargetview"><strong>CreateRenderTargetView</strong></a></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d11on12/ns-d3d11on12-d3d11_resource_flags"><strong>D3D11_RESOURCE_FLAGS</strong></a></td>
<td><a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_bind_flag"><strong>D3D11_BIND_FLAG</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-createwrappedresource"><strong>CreateWrappedResource</strong></a></td>
<td><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/dxgi/nn-dxgi-idxgisurface"><strong>IDXGISurface</strong></a></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1__id2d1bitmap1)"><strong>ID2D1DeviceContext::CreateBitmapFromDxgiSurface</strong></a></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommandallocator"><strong>CreateCommandAllocator</strong></a></td>
<td><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type"><strong>D3D12_COMMAND_LIST_TYPE</strong></a></td>
</tr>
</tbody>
</table>



 

## <a name="create-basic-d2d-text-objects"></a>Criar objetos de texto D2D básicos

Agora temos um [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device) para renderizar o conteúdo 3D, um [**ID2D1Device**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1device) que é compartilhado com nosso dispositivo 12 por meio de [**um ID3D11On12Device**](/windows/desktop/api/d3d11on12/nn-d3d11on12-id3d11on12device) – que podemos usar para renderizar o conteúdo 2D – e ambos são configurados para renderizar na mesma cadeia de permuta. Este exemplo simplesmente usa o dispositivo D2D para renderizar texto na cena 3D, semelhante a como os jogos renderizam sua interface do usuário. Para isso, precisamos criar alguns objetos D2D básicos, ainda no **método LoadAssets.**

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



| Fluxo de chamada                                                                                           | Parâmetros                                                                 |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [**ID2D1RenderTarget::CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush))    | [**ColorF**](/windows/desktop/api/d2d1helper/nl-d2d1helper-colorf)                                              |
| [**IDWriteFactory::CreateTextFormat**](/windows/desktop/api/dwrite/nf-dwrite-idwritefactory-createtextformat)                 | [**PESO DA \_ FONTE DWRITE \_**](/windows/desktop/api/dwrite/ne-dwrite-dwrite_font_weight)                 |
| [**IDWriteTextFormat::SetTextAlignment**](/windows/desktop/api/dwrite/nf-dwrite-idwritetextformat-settextalignment)           | [**ALINHAMENTO DE TEXTO \_ \_ DWRITE**](/windows/desktop/api/dwrite/ne-dwrite-dwrite_text_alignment)           |
| [**IDWriteTextFormat::SetParagraphAlignment**](/windows/desktop/api/dwrite/nf-dwrite-idwritetextformat-setparagraphalignment) | [**ALINHAMENTO DE PARÁGRAFO \_ \_ DWRITE**](/windows/desktop/api/dwrite/ne-dwrite-dwrite_paragraph_alignment) |



 

## <a name="updating-the-main-render-loop"></a>Atualizando o loop de renderização principal

Agora que a inicialização do exemplo foi concluída, podemos passar para o loop de renderização principal.

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



| Fluxo de chamada                                                              | Parâmetros |
|------------------------------------------------------------------------|------------|
| [**ID3D12CommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandlist)                         |            |
| [**ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)  |            |
| [**IDXGISwapChain1::Present1**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1) |            |



 

A única novidade em nosso loop de renderização é a **chamada renderui,** que usará D2D para renderizar nossa interface do usuário. Observe que executamos todas as nossas listas de comandos D3D12 primeiro para renderizar nossa cena 3D e, em seguida, renderizamos nossa interface do usuário sobre isso. Antes de nos adémos **na RenderUI**, devemos ver uma alteração em **PopulateCommandLists.** Em outros exemplos, normalmente colocamos uma barreira de recursos na lista de comandos antes de a fechar para fazer a transição do buffer de fundo do estado de destino de renderização para o estado atual. No entanto, neste exemplo, removemos essa barreira de recursos, pois ainda precisamos renderizar para os buffers de fundo com D2D. Observe que, quando criamos nossos recursos empacotados do buffer de fundo, especificamos o estado de destino de renderização como o estado "IN" e o estado atual como o estado "OUT".

**A RenderUI** é bastante direta em termos de uso de D2D. Definimos nosso destino de renderização e renderizamos nosso texto. No entanto, antes de usar qualquer recurso empacotado em um dispositivo 11On12, como nossos destinos de renderização de buffer de fundo, devemos chamar a API [**AcquireWrappedResources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-acquirewrappedresources) no dispositivo 11On12. Após a renderização, chamamos a API [**ReleaseWrappedResources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-releasewrappedresources) no dispositivo 11On12. Ao chamar **ReleaseWrappedResources,** incorremos em uma barreira de recursos nos bastidores que fará a transição do recurso especificado para o estado "OUT" especificado no momento da criação. Em nosso caso, esse é o estado atual. Por fim, para enviar todos os nossos comandos executados no dispositivo 11On12 para o [**ID3D12CommandQueue**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue)compartilhado, devemos chamar [**Flush**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-flush) no [**ID3D11DeviceContext**](/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext).

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



| Fluxo de chamada                                                                                                                                                                                 | Parâmetros                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| [**D2D1 \_ TAMANHO \_ F**](/windows/desktop/Direct2D/d2d1-size-f)                                                                                                                                                 |                                       |
| [**D2D1 \_ RECT \_ F**](/windows/desktop/Direct2D/d2d1-rect-f)                                                                                                                                                 | [**RectF**](/windows/desktop/api/d2d1helper/nf-d2d1helper-rectf)           |
| [**AcquireWrappedResources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-acquirewrappedresources)                                                                                                               |                                       |
| [**ID2D1DeviceContext::SetTarget**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-settarget)                                                                                                                |                                       |
| [**ID2D1RenderTarget::BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw)                                                                                                                  |                                       |
| [**ID2D1RenderTarget::SetTransform**](/windows/desktop/Direct2D/id2d1rendertarget-settransform)                                                                                                            | [**Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) |
| [**ID2D1RenderTarget::D rawTextW**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) |                                       |
| [**ID2D1RenderTarget::EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw)                                                                                                                      |                                       |
| [**ReleaseWrappedResources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-releasewrappedresources)                                                                                                               |                                       |
| [**ID3D11DeviceContext::Flush**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-flush)                                                                                                                    |                                       |



 

## <a name="run-the-sample"></a>Execute o exemplo

![a saída final do exemplo 11 em 12](images/11on12image.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia detalhado do código D3D12](d3d12-code-walk-throughs.md)
</dt> <dt>

[Direct3D 11 on 12](direct3d-11-on-12.md)
</dt> <dt>

[Interoperabilidade do Direct3D 12](direct3d-12-interop.md)
</dt> <dt>

[Referência 11on12](direct3d-11on12-reference.md)
</dt> </dl>

 

 