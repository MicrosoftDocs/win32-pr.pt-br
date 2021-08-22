---
description: Descreve como usar sobreposições de hardware no Direct3D 9.
ms.assetid: fa9d5bf5-4c0f-471a-b639-d329b0cd89a4
title: Suporte à sobreposição de hardware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f537c91bc217344206c0a23cf5ca8a14254a9c983e4ae550e96457bbb055e5d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600396"
---
# <a name="hardware-overlay-support"></a>Suporte à sobreposição de hardware

Uma sobreposição de hardware é uma área dedicada de memória de vídeo que pode ser sobrepassada na superfície primária. Nenhuma cópia é executada quando a sobreposição é exibida. A operação de sobreposição é executada em hardware, sem modificar os dados na superfície primária.

O uso de sobreposições de hardware para reprodução de vídeo era comum em versões anteriores do Windows, pois as sobreposições são eficientes para conteúdo de vídeo com uma alta taxa de quadros. A partir do Windows 7, o Direct3D 9 dá suporte a sobreposições de hardware. Esse suporte destina-se principalmente à reprodução de vídeo e difere em alguns aspectos das APIs do DirectDraw anteriores:

-   A sobreposição não pode ser reduzida, espelhada ou desinteressada.
-   Não há suporte para chaves de cor de origem e combinação alfa.
-   As sobreposições poderão ser estendidas se o hardware de sobreposição for compatível com ele. Caso contrário, não há suporte para alongamento. Na prática, nem todos os drivers gráficos suportam alongamento.
-   Cada dispositivo dá suporte a no máximo uma sobreposição.
-   A sobreposição é executada usando uma chave de cor de destino, mas o runtime do Direct3D seleciona automaticamente a cor e desenha o retângulo de destino. O Direct3D rastreia automaticamente a posição da janela e atualiza a posição de sobreposição sempre que **o PresentEx** é chamado.

### <a name="creating-a-hardware-overlay-surface"></a>Criando uma superfície de sobreposição de hardware

Para consultar o suporte à sobreposição, chame **IDirect3D9::GetDeviceCaps.** Se o driver for compatível com a sobreposição de hardware, o sinalizador **\_ OVERLAY D3DCAPS** será definido no **D3DCAPS9. Membro Caps.**

Para descobrir se há suporte para um formato de sobreposição específico para um determinado modo de exibição, chame [**IDirect3D9ExOverlayExtension::CheckDeviceOverlayType**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9exoverlayextension-checkdeviceoverlaytype).

Para criar a sobreposição, chame **IDirect3D9Ex::CreateDeviceEx** e especifique o efeito de troca **\_ OVERLAY D3DSWAPEFFECT.** O buffer de fundo pode usar um formato não RGB se o hardware dá suporte a ele.

As superfícies de sobreposição têm as seguintes limitações:

-   O aplicativo não pode criar mais de uma cadeia de troca de sobreposição.
-   A sobreposição deve ser usada no modo em janelas. Ele não pode ser usado no modo de tela inteira.
-   O efeito de troca de sobreposição deve ser usado com a interface **IDirect3DDevice9Ex.** Não há suporte para **IDirect3DDevice9.**
-   Não é possível usar multisampling.
-   Não há suporte para os sinalizadores **\_ FLIPRESTART** **D3DPRESENTIANOTFLIP \_** e D3DPRESENT.
-   As estatísticas de apresentação não estão disponíveis para a superfície de sobreposição.

Se o hardware não dá suporte ao alongamento, é recomendável criar uma cadeia de permuta tão grande quanto o modo de exibição, para que a janela possa ser re dimensionada para qualquer dimensão. Recriar a cadeia de permuta não é uma maneira ideal de lidar com o re tamanho da janela, pois pode causar artefatos de renderização graves. Além disso, devido à maneira como a GPU gerencia a memória de sobreposição, recriar a cadeia de permuta pode fazer com que um aplicativo ficar sem memória de vídeo.

### <a name="new-d3dpresent_parameters-flags"></a>Novos sinalizadores de PARÂMETROS D3DPRESENT \_

Os **sinalizadores D3DPRESENT \_ PARAMETERS** a seguir são definidos para criar sobreposições.



| Sinalizador                                      | Descrição                                                                                                                                                                        |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **D3DPRESENTFLAG \_ OVERLAY \_ LIMITEDRGB**   | O intervalo RGB é de 16 a 235. O padrão é de 0 a 255. <br/> Requer a **funcionalidade D3DOVERLAYCAPS \_ LIMITEDRANGERGB.**<br/>                                                 |
| **SOBREPOSIÇÃO DE D3DPRESENTFLAG \_ \_ YCbCr \_ BT709** | As cores YUV usam a definição BT.709. O padrão é BT.601. <br/> Requer a **funcionalidade D3DOVERLAYCAPS \_ YCbCr \_ BT709.**<br/>                                      |
| **SOBREPOSIÇÃO DE D3DPRESENTFLAG \_ \_ YCbCrcbCrcbYCC \_** | Saída dos dados usando YCbCr estendido (sempreYCC).<br/> Requer a **funcionalidade D3DOVERLAYCAPS \_ YCbCr \_ BT601cbYCC \_** ou **D3DOVERLAYCAPS \_ YCbCr \_ BT709cbYCC. \_**<br/> |



 

### <a name="using-hardware-overlays"></a>Usando sobreposições de hardware

Para exibir a superfície de sobreposição, o aplicativo chama **IDirect3DDevice9Ex::P resentEx.** O runtime do Direct3D desenha automaticamente a chave de cor de destino.

Os **sinalizadores PresentEx** a seguir são definidos para sobreposições.



| Sinalizador                              | Descrição                                                                                                                                                                                                                                                                           |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **D3DPRESENT \_ UPDATECOLORKEY**    | De definir esse sinalizador se Gerenciador de Janelas da Área de Trabalho (DWM) estiver desabilitada. Esse sinalizador faz com que o Direct3D redesenhar a chave de cor.<br/> Se a DWM estiver habilitada, esse sinalizador não será necessário, pois o Direct3D desenha a chave de cor uma vez na superfície que a DWM usa para redirecionamento.<br/> |
| **D3DPRESENT \_ HIDEOVERLAY**       | Oculta a sobreposição.                                                                                                                                                                                                                                                                    |
| **D3DPRESENT \_ UPDATEOVERLAYONLY** | Atualiza a sobreposição sem alterar o conteúdo.<br/> Esse sinalizador será útil se a janela se mover enquanto o vídeo estiver em pausa.<br/>                                                                                                                                           |



 

Um aplicativo deve estar preparado para lidar com os seguintes casos:

-   Se outro aplicativo estiver usando a sobreposição, **PresentEx** **retornará D3DERR \_ NOTAVAILABLE.**
-   Se a janela for movida para outro monitor, o aplicativo deverá recriar a cadeia de permuta. Caso contrário, se o aplicativo chamar **PresentEx** para exibir a sobreposição em um monitor diferente, **PresentEx** **retornará D3DERR \_ INVALIDDEVICE**.
-   Se o modo de exibição mudar, o Direct3D tentará restaurar a sobreposição. Se o novo modo não for compatível com a sobreposição, **PresentEx** **retornará D3DERR \_ UNSUPPORTEDOVERLAY**.

### <a name="example-code"></a>Código de exemplo

O exemplo a seguir mostra como criar uma superfície de sobreposição.


```C++
const UINT VIDEO_WIDTH = 256;
const UINT VIDEO_HEIGHT = 256;

HRESULT CreateHWOverlay(
    HWND hwnd, 
    IDirect3D9Ex *pD3D, 
    IDirect3DDevice9Ex **ppDevice
    )
{
    *ppDevice = NULL;

    D3DCAPS9                caps;
    ZeroMemory(&caps, sizeof(caps));

    HRESULT hr = pD3D->GetDeviceCaps(
        D3DADAPTER_DEFAULT,
        D3DDEVTYPE_HAL,
        &caps
        );

    if (FAILED(hr))
    {
        return hr;
    }

    // Check if overlay is supported.
    if (!(caps.Caps & D3DCAPS_OVERLAY))
    {
        return D3DERR_UNSUPPORTEDOVERLAY;
    }

    D3DOVERLAYCAPS          overlayCaps = { 0 };

    IDirect3DDevice9Ex           *pDevice = NULL;
    IDirect3D9ExOverlayExtension *pOverlay = NULL;

    // Check specific overlay capabilities.
    hr = pD3D->QueryInterface(IID_PPV_ARGS(&pOverlay));

    if (SUCCEEDED(hr))
    {
        hr = pOverlay->CheckDeviceOverlayType(
            D3DADAPTER_DEFAULT,
            D3DDEVTYPE_HAL,
            VIDEO_WIDTH,
            VIDEO_HEIGHT,
            D3DFMT_X8R8G8B8,
            NULL,
            D3DDISPLAYROTATION_IDENTITY,
            &overlayCaps
            );
    }

    // Create the overlay.
    if (SUCCEEDED(hr))
    {

        DWORD flags =   D3DCREATE_FPU_PRESERVE | 
                        D3DCREATE_MULTITHREADED | 
                        D3DCREATE_SOFTWARE_VERTEXPROCESSING;

        
        D3DPRESENT_PARAMETERS   pp = { 0 };

        pp.BackBufferWidth = overlayCaps.MaxOverlayDisplayWidth;
        pp.BackBufferHeight = overlayCaps.MaxOverlayDisplayHeight;
        pp.BackBufferFormat = D3DFMT_X8R8G8B8;
        pp.SwapEffect = D3DSWAPEFFECT_OVERLAY;
        pp.hDeviceWindow = hwnd;
        pp.Windowed = TRUE;
        pp.Flags = D3DPRESENTFLAG_VIDEO;
        pp.FullScreen_RefreshRateInHz = D3DPRESENT_RATE_DEFAULT;
        pp.PresentationInterval       = D3DPRESENT_INTERVAL_ONE;

        hr = pD3D->CreateDeviceEx(D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL,
            NULL, flags, &pp, NULL, &pDevice);
    }

    if (SUCCEEDED(hr))
    {
        (*ppDevice) = pDevice;
        (*ppDevice)->AddRef();
    }

    SafeRelease(&pD3D);
    SafeRelease(&pDevice);
    SafeRelease(&pOverlay);
    return hr;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[APIs de vídeo do Direct3D](direct3d-video-apis.md)
</dt> </dl>

 

 




