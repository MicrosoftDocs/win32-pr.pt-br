---
title: Formatos de pixel e modos alfa com suporte
description: Descreve os formatos de pixel e os modos alfa com suporte de cada tipo de destino de renderização.
ms.assetid: 09b1f9c6-1780-4733-ac22-9e8c21466b67
keywords:
- Direct2D, formatos de pixel
- Direct2D, modos alfa
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 9a3777cac7cc0a258002d1475fb7b1c6dd2546ca
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104084992"
---
# <a name="supported-pixel-formats-and-alpha-modes"></a>Formatos de pixel e modos alfa com suporte

Este tópico descreve os formatos de pixel e os modos alfa com suporte nas várias partes do Direct2D, incluindo cada tipo de destino de renderização, [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)e [**ID2D1ImageSource**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesource). Ele contém as seguintes seções:

-   [Formatos YUV com suporte para origem de imagem DXGI](#supported-yuv-formats-for-dxgi-image-source)
-   [Especificando um formato de pixel para um destino de renderização](#specifying-a-pixel-format-for-a-render-target)
-   [Formatos com suporte para ID2D1HwndRenderTarget](#supported-formats-for-id2d1hwndrendertarget)
-   [Formatos com suporte para ID2D1DeviceContext](#supported-formats-for-id2d1devicecontext)
-   [Formatos com suporte para destino de renderização compatível](#supported-formats-for-compatible-render-target)
-   [Formatos com suporte para destino de renderização da superfície DXGI](#supported-formats-for-dxgi-surface-render-target)
-   [Formatos com suporte para destino de renderização de bitmap do WIC](#supported-formats-for-wic-bitmap-render-target)
-   [Formatos com suporte para ID2D1DCRenderTarget](#supported-formats-for-id2d1dcrendertarget)
-   [Especificando um formato de pixel para um ID2D1Bitmap](#specifying-a-pixel-format-for-an-id2d1bitmap)
    -   [Formatos de WIC com suporte](#supported-wic-formats)
-   [Usando um formato sem suporte](#using-an-unsupported-format)
-   [Sobre os modos alfa](#about-alpha-modes)
    -   [Sobre os modos precalculados e alfabéticos retos](#about-premultiplied-and-straight-alpha-modes)
    -   [As diferenças entre alfa e premultiplicado Alpha](#the-differences-between-straight-and-premultiplied-alpha)
    -   [Modo alfa para destinos de renderização](#alpha-mode-for-render-targets)
    -   [Modos de ClearType e de modo alfa](#cleartype-and-alpha-modes)
-   [Tópicos relacionados](#related-topics)

## <a name="supported-yuv-formats-for-dxgi-image-source"></a>Formatos YUV com suporte para origem de imagem DXGI

Um [**ID2D1ImageSource**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesource) é um provedor abstrato de pixels. Ele pode ser instanciado a partir de um WIC ([**CreateImageSourceFromWic**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromwic(iwicbitmapsource_id2d1imagesourcefromwic)) ou [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) ([**CreateImageSourceFromDxgi**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromdxgi)).

[**ID2D1ImageSourceFromWic**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic) dá suporte ao mesmo conjunto de formatos de pixel e modos alfa como [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).

Além do acima, um [**ID2D1ImageSource**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesource) que é instanciado do [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) também dá suporte a alguns formatos de pixel YUV, incluindo dados de planar divididos em várias superfícies. Consulte [**CreateImageSourceFromDxgi**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromdxgi) para obter mais informações sobre os requisitos para cada formato de pixel.



| Formatar                    |
|---------------------------|
| \_AYUV de formato dxgi \_        |
| \_NV12 de formato dxgi \_        |
| \_YUY2 de formato dxgi \_        |
| \_P208 de formato dxgi \_        |
| \_V208 de formato dxgi \_        |
| \_V408 de formato dxgi \_        |
| \_UNORM de \_ R8 de formato dxgi \_   |
| \_Formato dxgi \_ R8G8 \_ UNORM |



 

## <a name="specifying-a-pixel-format-for-a-render-target"></a>Especificando um formato de pixel para um destino de renderização

Ao criar um destino de renderização, você deve especificar seu formato de pixel. Para especificar o formato de pixel, use uma estrutura de [**\_ \_ formato de pixel d2d1**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format) para definir o membro **PixelFormat** de uma estrutura de propriedades de [**\_ \_ destino \_ de renderização d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) . Em seguida, você passa essa estrutura para o método Create apropriado, como [**ID2D1Factory:: CreateHwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)).

A estrutura de [**\_ \_ formato de pixel d2d1**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format) tem dois campos:

-   **formato**, um valor de [ \_ formato dxgi](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) que descreve o tamanho e a organização dos canais em cada pixel e
-   **alfa**, um valor de [**\_ \_ modo alfa d2d1**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) que descreve como as informações de Alfa são interpretadas.

O exemplo a seguir cria uma estrutura de [**\_ \_ formato de pixel d2d1**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format) e a usa para especificar o formato de pixel e o modo alfa de um [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget).


```C++
RECT rc;
GetClientRect(m_hwnd, &rc);

D2D1_SIZE_U size = D2D1::SizeU(
    rc.right - rc.left,
    rc.bottom - rc.top
    );

// Create a pixel format and initial its format
// and alphaMode fields.
D2D1_PIXEL_FORMAT pixelFormat = D2D1::PixelFormat(
    DXGI_FORMAT_B8G8R8A8_UNORM,
    D2D1_ALPHA_MODE_IGNORE
    );

D2D1_RENDER_TARGET_PROPERTIES props = D2D1::RenderTargetProperties();
props.pixelFormat = pixelFormat;

// Create a Direct2D render target.
hr = m_pD2DFactory->CreateHwndRenderTarget(
    props,
    D2D1::HwndRenderTargetProperties(m_hwnd, size),
    &m_pRT
    );

```



Destinos de renderização diferentes dão suporte a combinações de formato alfa e formatos diferentes. As seções a seguir listam as combinações de formato e alfa com suporte de cada destino de renderização.

## <a name="supported-formats-for-id2d1hwndrendertarget"></a>Formatos com suporte para ID2D1HwndRenderTarget

Os formatos com suporte para um [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) dependem se eles são renderizados usando hardware ou software, ou se o Direct2D manipula o modo de renderização automaticamente por padrão.

> [!Note]  
> Recomendamos que você use [**o \_ formato dxgi \_ B8G8R8A8 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) como o formato de pixel para melhorar o desempenho. Isso é particularmente útil para destinos de renderização de software. Os destinos de formato BGRA têm melhores formatos de RGBA.

 

Quando você cria um [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget), você usa a estrutura de [**\_ Propriedades de \_ destino \_ d2d1 render**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) para especificar opções de renderização. As opções incluem o formato de pixel, conforme observado na seção anterior. O campo tipo dessa estrutura permite que você especifique se o destino de renderização é renderizado para hardware ou software, ou se Direct2D deve determinar automaticamente o modo de renderização.

Para habilitar o Direct2D para determinar se o destino de renderização usa a renderização de hardware ou software, use a configuração [**padrão de tipo de \_ destino de renderização \_ \_ \_ d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) .

A tabela a seguir lista os formatos com suporte para objetos [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) que são criados usando a configuração padrão de tipo de [**destino de \_ renderização \_ \_ \_ d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) .



| Formatar                        | Modo alfa                       |
|-------------------------------|----------------------------------|
| \_Formato dxgi \_ B8G8R8A8 \_ UNORM | Modo alfa D2D1 pré- \_ \_ \_ multiplicado |
| \_Formato dxgi \_ B8G8R8A8 \_ UNORM | \_ \_ Ignorar modo alfa \_ d2d1        |
| \_Formato dxgi \_ B8G8R8A8 \_ UNORM | \_Modo alfa \_ d2d1 \_ desconhecido       |
| \_formato dxgi \_ desconhecido         | Modo alfa D2D1 pré- \_ \_ \_ multiplicado |
| \_formato dxgi \_ desconhecido         | \_ \_ Ignorar modo alfa \_ d2d1        |
| \_formato dxgi \_ desconhecido         | \_Modo alfa \_ d2d1 \_ desconhecido       |



 

Para forçar um destino de renderização a usar a renderização de hardware, use a configuração de [**\_ hardware do tipo de \_ destino \_ \_ d2d1 render**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) . A tabela a seguir lista os formatos com suporte para objetos [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) que usam explicitamente a renderização de hardware.



| Formatar                        | Modo alfa                       |
|-------------------------------|----------------------------------|
| \_Formato dxgi \_ B8G8R8A8 \_ UNORM | Modo alfa D2D1 pré- \_ \_ \_ multiplicado |
| \_Formato dxgi \_ B8G8R8A8 \_ UNORM | \_ \_ Ignorar modo alfa \_ d2d1        |
| \_Formato dxgi \_ B8G8R8A8 \_ UNORM | \_Modo alfa \_ d2d1 \_ desconhecido       |
| \_Formato dxgi \_ R8G8B8A8 \_ UNORM | Modo alfa D2D1 pré- \_ \_ \_ multiplicado |
| \_Formato dxgi \_ R8G8B8A8 \_ UNORM | \_ \_ Ignorar modo alfa \_ d2d1        |
| \_Formato dxgi \_ R8G8B8A8 \_ UNORM | \_Modo alfa \_ d2d1 \_ desconhecido       |
| \_formato dxgi \_ desconhecido         | Modo alfa D2D1 pré- \_ \_ \_ multiplicado |
| \_formato dxgi \_ desconhecido         | \_ \_ Ignorar modo alfa \_ d2d1        |
| \_formato dxgi \_ desconhecido         | \_Modo alfa \_ d2d1 \_ desconhecido       |



 

Para forçar um destino de renderização a usar a renderização de software, use a configuração de [**\_ software do tipo de \_ destino \_ \_ d2d1 render**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) . A tabela a seguir lista os formatos com suporte para objetos [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) que usam explicitamente a renderização de software.



| Formatar                        | Modo alfa                       |
|-------------------------------|----------------------------------|
| \_Formato dxgi \_ B8G8R8A8 \_ UNORM | Modo alfa D2D1 pré- \_ \_ \_ multiplicado |
| \_Formato dxgi \_ B8G8R8A8 \_ UNORM | \_ \_ Ignorar modo alfa \_ d2d1        |
| \_Formato dxgi \_ B8G8R8A8 \_ UNORM | \_Modo alfa \_ d2d1 \_ desconhecido       |
| \_formato dxgi \_ desconhecido         | Modo alfa D2D1 pré- \_ \_ \_ multiplicado |
| \_formato dxgi \_ desconhecido         | \_ \_ Ignorar modo alfa \_ d2d1        |
| \_formato dxgi \_ desconhecido         | \_Modo alfa \_ d2d1 \_ desconhecido       |



 

Independentemente de o [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) ser acelerado por hardware, o [formato \_ \_ desconhecido do formato dxgi](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) usa o [formato de dxgi \_ \_ B8G8R8A8](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) por padrão e o modo alfa do [**\_ \_ modo \_**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) alfa do d2d1 usa **d2d1 modo alfa \_ \_ \_ ignorar** por padrão.

## <a name="supported-formats-for-id2d1devicecontext"></a>Formatos com suporte para ID2D1DeviceContext

A partir do Windows 8, o [**contexto do dispositivo**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) aproveita mais os [**formatos de alta cor do Direct3D**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) , como:

-   \_Formato dxgi \_ B8G8R8A8 \_ UNORM \_ sRGB
-   \_Formato dxgi \_ R8G8B8A8 \_ UNORM \_ sRGB
-   \_Formato dxgi \_ R16G16B16A16 \_ UNORM
-   \_ \_ Float R16G16B16A16 de formato dxgi \_
-   \_ \_ Float R32G32B32A32 de formato dxgi \_

Use o método [**ID2D1DeviceContext:: IsDxgiFormatSupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isdxgiformatsupported) para ver se um formato funciona em um determinado contexto de dispositivo. Esses formatos também podem funcionar em um [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget).

Esses formatos são além dos formatos suportados pela interface [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) no Windows 7. Confira [dispositivos e contextos de dispositivo](devices-and-device-contexts.md) para obter mais informações.

## <a name="supported-formats-for-compatible-render-target"></a>Formatos com suporte para destino de renderização compatível

Um destino de renderização compatível (um [**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget) que é criado por um dos métodos [**ID2D1RenderTarget:: CreateCompatibleRenderTarget**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) ) herda os formatos com suporte e os modos alfa do destino de renderização que o criou. Um destino de renderização compatível também dá suporte ao seguinte formato e combinações de modo alfa, independentemente de qual seu pai dá suporte.



| Formatar                  | Modo alfa                       |
|-------------------------|----------------------------------|
| \_Formato dxgi \_ a8 \_ UNORM | Modo alfa D2D1 pré- \_ \_ \_ multiplicado |
| \_Formato dxgi \_ a8 \_ UNORM | \_Modo alfa \_ d2d1 \_ reto      |
| \_formato dxgi \_ desconhecido   | \_Modo alfa \_ d2d1 \_ desconhecido       |



 

O formato de [formato de dxgi \_ \_ desconhecido](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) usa o formato de destino de renderização pai por padrão e o modo alfa do [**\_ \_ modo \_ alfa d2d1**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) usa o **modo alfa d2d1 \_ \_ \_ precalculado** por padrão.

## <a name="supported-formats-for-dxgi-surface-render-target"></a>Formatos com suporte para destino de renderização da superfície DXGI

Um destino de renderização DXGI é um [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) que é criado por um dos métodos [**ID2D1Factory:: CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) . Ele dá suporte ao seguinte formato e combinações de modo alfa.



| Formatar                        | Modo alfa                       |
|-------------------------------|----------------------------------|
| \_Formato dxgi \_ B8G8R8A8 \_ UNORM | Modo alfa D2D1 pré- \_ \_ \_ multiplicado |
| \_Formato dxgi \_ B8G8R8A8 \_ UNORM | \_ \_ Ignorar modo alfa \_ d2d1        |
| \_Formato dxgi \_ R8G8B8A8 \_ UNORM | Modo alfa D2D1 pré- \_ \_ \_ multiplicado |
| \_Formato dxgi \_ R8G8B8A8 \_ UNORM | \_ \_ Ignorar modo alfa \_ d2d1        |
| \_Formato dxgi \_ a8 \_ UNORM       | Modo alfa D2D1 pré- \_ \_ \_ multiplicado |
| \_Formato dxgi \_ a8 \_ UNORM       | \_Modo alfa \_ d2d1 \_ reto      |
| \_formato dxgi \_ desconhecido         | Modo alfa D2D1 pré- \_ \_ \_ multiplicado |
| \_formato dxgi \_ desconhecido         | \_ \_ Ignorar modo alfa \_ d2d1        |



 

> [!Note]  
> O formato deve corresponder ao formato da superfície DXGI à qual o destino de renderização de superfície DXGI é desenhado.

 

O [formato \_ \_ desconhecido formato dxgi](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) usa o formato de superfície DXGI por padrão. Não use o modo alfa do [**\_ modo alfa do d2d1 \_ \_ desconhecido**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) com um destino de renderização da superfície DXGI. Ele não tem valor padrão e fará com que a criação de destino de renderização de superfície DXGI falhe.

## <a name="supported-formats-for-wic-bitmap-render-target"></a>Formatos com suporte para destino de renderização de bitmap do WIC

Um destino de renderização de bitmap do WIC é um [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) que é criado por um dos métodos [**ID2D1Factory:: CreateWicBitmapRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties_id2d1rendertarget)) . Ele dá suporte ao seguinte formato e combinações de modo alfa.



| Formatar                        | Modo alfa                       |
|-------------------------------|----------------------------------|
| \_Formato dxgi \_ B8G8R8A8 \_ UNORM | Modo alfa D2D1 pré- \_ \_ \_ multiplicado |
| \_Formato dxgi \_ B8G8R8A8 \_ UNORM | \_ \_ Ignorar modo alfa \_ d2d1        |
| \_Formato dxgi \_ B8G8R8A8 \_ UNORM | \_Modo alfa \_ d2d1 \_ desconhecido       |
| \_Formato dxgi \_ a8 \_ UNORM       | Modo alfa D2D1 pré- \_ \_ \_ multiplicado |
| \_Formato dxgi \_ a8 \_ UNORM       | \_Modo alfa \_ d2d1 \_ reto      |
| \_Formato dxgi \_ a8 \_ UNORM       | \_Modo alfa \_ d2d1 \_ desconhecido       |
| \_formato dxgi \_ desconhecido         | Modo alfa D2D1 pré- \_ \_ \_ multiplicado |
| \_formato dxgi \_ desconhecido         | \_ \_ Ignorar modo alfa \_ d2d1        |
| \_formato dxgi \_ desconhecido         | \_Modo alfa \_ d2d1 \_ desconhecido       |



 

O formato de pixel do destino de bitmap do WIC deve corresponder ao formato de pixel do bitmap do WIC.

O [formato \_ \_ desconhecido formato dxgi](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) usa o formato de bitmap do WIC por padrão e o modo alfa do [**\_ \_ modo \_ alfa d2d1**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) usa o modo alfa do bitmap do WIC por padrão.

## <a name="supported-formats-for-id2d1dcrendertarget"></a>Formatos com suporte para ID2D1DCRenderTarget

Um [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) dá suporte ao seguinte formato e combinações de modo alfa.



| Formatar                        | Modo alfa                       |
|-------------------------------|----------------------------------|
| \_Formato dxgi \_ B8G8R8A8 \_ UNORM | Modo alfa D2D1 pré- \_ \_ \_ multiplicado |
| \_Formato dxgi \_ B8G8R8A8 \_ UNORM | \_ \_ Ignorar modo alfa \_ d2d1        |



 

Não use o formato [de \_ formato \_ de dxgi desconhecido](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ou o modo alfa do [**\_ \_ modo \_ alfa do d2d1**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) com um [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget). Ele não tem valor padrão e fará com que a criação de **ID2D1DCRenderTarget** falhe.

## <a name="specifying-a-pixel-format-for-an-id2d1bitmap"></a>Especificando um formato de pixel para um ID2D1Bitmap

Em geral, os objetos [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) dão suporte aos seguintes formatos e modos alfa (com algumas restrições, descritas nos parágrafos que se seguem.)



| Formatar                                                      | Modo alfa                       |
|-------------------------------------------------------------|----------------------------------|
| \_Formato dxgi \_ B8G8R8A8 \_ UNORM                               | Modo alfa D2D1 pré- \_ \_ \_ multiplicado |
| \_Formato dxgi \_ B8G8R8A8 \_ UNORM                               | \_ \_ Ignorar modo alfa \_ d2d1        |
| \_Formato dxgi \_ B8G8R8A8 \_ UNORM                               | \_Modo alfa \_ d2d1 \_ desconhecido       |
| \_Formato dxgi \_ a8 \_ UNORM                                     | Modo alfa D2D1 pré- \_ \_ \_ multiplicado |
| \_Formato dxgi \_ a8 \_ UNORM                                     | \_Modo alfa \_ d2d1 \_ reto      |
| \_Formato dxgi \_ a8 \_ UNORM                                     | \_Modo alfa \_ d2d1 \_ desconhecido       |
| \_formato dxgi \_ desconhecido                                       | Modo alfa D2D1 pré- \_ \_ \_ multiplicado |
| \_formato dxgi \_ desconhecido                                       | \_ \_ Ignorar modo alfa \_ d2d1        |
| \_formato dxgi \_ desconhecido                                       | \_Modo alfa \_ d2d1 \_ desconhecido       |
| \_Formato dxgi \_ B8G8R8X8 \_ UNORM (Windows 8.1 e posterior, somente) | \_ \_ Ignorar modo alfa \_ d2d1        |
| \_Formato dxgi \_ BC1 \_ UNORM (Windows 8.1 e posterior, somente)      | Modo alfa D2D1 pré- \_ \_ \_ multiplicado |
| \_Formato dxgi \_ BC1 \_ UNORM (Windows 8.1 e posterior, somente)      | \_ \_ Ignorar modo alfa \_ d2d1        |
| \_Formato dxgi \_ BC1 \_ UNORM (Windows 8.1 e posterior, somente)      | \_Modo alfa \_ d2d1 \_ desconhecido       |
| \_Formato dxgi \_ BC2 \_ UNORM (Windows 8.1 e posterior, somente)      | Modo alfa D2D1 pré- \_ \_ \_ multiplicado |
| \_Formato dxgi \_ BC2 \_ UNORM (Windows 8.1 e posterior, somente)      | \_ \_ Ignorar modo alfa \_ d2d1        |
| \_Formato dxgi \_ BC2 \_ UNORM (Windows 8.1 e posterior, somente)      | \_Modo alfa \_ d2d1 \_ desconhecido       |
| \_Formato dxgi \_ BC3 \_ UNORM (Windows 8.1 e posterior, somente)      | Modo alfa D2D1 pré- \_ \_ \_ multiplicado |
| \_Formato dxgi \_ BC3 \_ UNORM (Windows 8.1 e posterior, somente)      | \_ \_ Ignorar modo alfa \_ d2d1        |
| \_Formato dxgi \_ BC3 \_ UNORM (Windows 8.1 e posterior, somente)      | \_Modo alfa \_ d2d1 \_ desconhecido       |



 

Quando você usa o método [**ID2D1RenderTarget:: CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) , usa o campo **PixelFormat** de uma estrutura [**de \_ \_ Propriedades de bitmap d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_bitmap_properties) para especificar o formato de pixel do novo destino de renderização. Ele deve corresponder ao formato de pixel da origem [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) .

Ao usar o método [**CreateBitmapFromWicBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties__id2d1bitmap)) , você usa o campo **PixelFormat** de uma estrutura [**de \_ \_ Propriedades de bitmap d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_bitmap_properties) (em vez do membro **PixelFormat** de uma estrutura de propriedades de [**\_ destino de renderização \_ \_ d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) ) para especificar o formato de pixel do novo destino de renderização. Ele deve corresponder ao formato de pixel da origem do bitmap do WIC.

> [!Note]  
> Para obter mais informações sobre o suporte para formatos de pixel BCn (Block compacted), consulte [Bloquear compactação](block-compression.md).

 

### <a name="supported-wic-formats"></a>Formatos de WIC com suporte

Quando você usa o método [**CreateBitmapFromWicBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties__id2d1bitmap)) para criar um bitmap de um bitmap do WIC, ou quando você usa o método [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) com um [**IWICBITMAPLOCK**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmaplock), a origem do WIC deve estar em um formato com suporte pelo Direct2D.



| Formato do WIC                     | Formato DXGI correspondente     | Modo alfa correspondente                                        |
|--------------------------------|-------------------------------|-----------------------------------------------------------------|
| \_WICPIXELFORMAT8BPPALPHA GUID  | \_Formato dxgi \_ a8 \_ UNORM       | Modo alfa do \_ modo Alpha d2d1 \_ \_ reto ou d2d1 \_ \_ \_ bimultiplicado |
| \_WICPIXELFORMAT32BPPPRGBA GUID | \_Formato dxgi \_ R8G8B8A8 \_ UNORM | D2D1 \_ modo \_ alfa \_ bimultiplicado ou d2d1 \_ \_ modo alfa \_ ignorado   |
| \_WICPIXELFORMAT32BPPBGR GUID   | \_Formato dxgi \_ B8G8R8A8 \_ UNORM | \_ \_ Ignorar modo alfa \_ d2d1                                       |
| \_WICPIXELFORMAT32BPPPBGRA GUID | \_Formato dxgi \_ B8G8R8A8 \_ UNORM | Modo alfa D2D1 pré- \_ \_ \_ multiplicado                                |



 

Para obter um exemplo que mostra como converter um bitmap do WIC em um formato com suporte, consulte [como carregar um bitmap de um arquivo](how-to-load-a-direct2d-bitmap-from-a-file.md).

## <a name="using-an-unsupported-format"></a>Usando um formato sem suporte

O uso de qualquer combinação diferente dos formatos de pixel e dos modos alfa listados nas tabelas anteriores resulta em um [**\_ \_ \_ formato de pixel sem suporte D2DERR**](direct2d-error-codes.md) ou um erro **E \_ INVALIDARG** .

## <a name="about-alpha-modes"></a>Sobre os modos alfa

### <a name="about-premultiplied-and-straight-alpha-modes"></a>Sobre os modos precalculados e alfabéticos retos

A enumeração do [**\_ \_ modo alfa do d2d1**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) indica se o canal alfa usa alfa (Alpha), Straight Alpha ou deve ser ignorado e considerado opaco. Com o Straight Alpha, o canal alfa indica um valor que corresponde ao quão transparente é a cor.

As cores são sempre tratadas como alfa lineares por comandos de desenho Direct2D e pincéis, independentemente do formato de destino.

Com o alfa premultiplicado, cada canal de cor é dimensionado pelo valor alfa. Normalmente, nenhum valor de canal de cor é maior que o valor do canal alfa. Se um valor de canal de cor em um formato previamente multiplicado for maior que o canal alfa, a combinação de código-fonte padrão em matemática cria um Blend aditivo.

O valor do canal alfa em si é o mesmo em alfa e bimultiplicated Alpha.

### <a name="the-differences-between-straight-and-premultiplied-alpha"></a>As diferenças entre alfa e premultiplicado Alpha

Ao descrever uma cor RGBA usando alfa linear, o valor alfa da cor é armazenado no canal alfa. Por exemplo, para descrever uma cor vermelha que seja 60% opaca, use os seguintes valores: (255, 0, 0, 255 \* 0,6) = (255, 0, 0, 153). O valor 255 indica vermelho completo e 153 (que é 60% de 255) indica que a cor deve ter uma opacidade de 60 por cento.

Ao descrever uma cor RGBA usando alfa contramultiplicado, cada cor é multiplicada pelo valor alfa: (255 \* 0,6, 0 \* 0,6, 0 \* 0,6, 255 \* 0,6) = (153, 0, 0, 153).

Independentemente do modo alfa do destino de renderização, os [**valores \_ \_ F de cor d2d1**](d2d1-color-f.md) são sempre interpretados como alfa retos. Por exemplo, ao especificar a cor de um [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) para uso com um destino de renderização que usa o modo alfa multiplicado, especifique a cor da mesma forma que faria se o destino de renderização fosse usado diretamente alfa. Quando você pinta com o pincel, o Direct2D converte a cor para o formato de destino para você.

### <a name="alpha-mode-for-render-targets"></a>Modo alfa para destinos de renderização

Independentemente da configuração do modo alfa, o conteúdo de um destino de renderização dá suporte à transparência. Por exemplo, se você desenhar um retângulo vermelho transparente por parte com um destino de renderização com um modo alfa [**do \_ \_ modo alfa \_ d2d1**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode), o retângulo aparecerá rosa (se o plano de fundo for branco).

Se você desenhar um retângulo vermelho transparente por parte quando o modo alfa for [**d2d1 \_ \_ modo alfa \_ multiplicado**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode), o retângulo aparecerá rosa (supondo que o plano de fundo é branco) e você poderá vê-lo para qualquer coisa que esteja atrás do destino de renderização. Isso é útil quando você usa um [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) para processar em uma janela transparente ou quando você usa um destino de renderização compatível (um renderizador direcionado criado pelo método [**CreateCompatibleRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) ) para criar um bitmap com suporte para transparência.

### <a name="cleartype-and-alpha-modes"></a>Modos de ClearType e de modo alfa

Se você especificar um modo alfa diferente de [**d2d1 \_ \_ modo alfa \_ ignorar**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) para um destino de renderização, o modo de suavização de texto será alterado automaticamente do [**\_ \_ \_ modo AntiAlias de texto d2d1 ClearType**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_text_antialias_mode) para o **modo de \_ AntiAlias de texto d2d1 em \_ escala de \_ cinza**. (Quando você especifica um modo alfa de **\_ modo alfa \_ d2d1 \_ desconhecido**, o Direct2D define o alfa para você, dependendo do tipo de destino de renderização.)

Você pode usar o método [**SetTextAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settextantialiasmode) para alterar o modo de suavização de texto de volta para o [**\_ \_ \_ modo AntiAlias de texto d2d1 ClearType**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_text_antialias_mode), mas renderizar texto ClearType para uma superfície transparente pode criar resultados imprevisíveis. Se você quiser renderizar texto ClearType para um destino de renderização transparente, recomendamos que você use uma das duas técnicas a seguir.

-   Use o método [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f_d2d1_antialias_mode)) para recortar o destino de renderização para a área em que o texto será renderizado, em seguida, chame o método [**Clear**](id2d1rendertarget-clear.md) e especifique uma cor opaca e, em seguida, processe o texto.
-   Use [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f_id2d1brush_float_id2d1strokestyle)) para desenhar um retângulo opaco por trás da área em que o texto será renderizado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**\_Formato de pixel d2d1 \_**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format)
</dt> <dt>

[**\_Modo alfa \_ d2d1**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode)
</dt> <dt>

[\_formato dxgi](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)
</dt> </dl>

 

 