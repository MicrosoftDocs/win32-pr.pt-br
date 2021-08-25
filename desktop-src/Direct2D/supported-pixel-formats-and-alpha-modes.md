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
ms.openlocfilehash: d5b260741cae6aebb447a11692f03dad6e35498a19f33221aa77ac8a8507144a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119917156"
---
# <a name="supported-pixel-formats-and-alpha-modes"></a>Formatos de pixel e modos alfa com suporte

este tópico descreve os formatos de pixel e os modos alfa com suporte nas várias partes do Direct2D, incluindo cada tipo de destino de renderização, [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)e [**ID2D1ImageSource**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesource). Ele contém as seguintes seções:

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

os formatos com suporte para um [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) dependem se ele é renderizado por meio de hardware ou software, ou se Direct2D manipula o modo de renderização automaticamente por padrão.

> [!Note]  
> Recomendamos que você use [**o \_ formato dxgi \_ B8G8R8A8 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) como o formato de pixel para melhorar o desempenho. Isso é particularmente útil para destinos de renderização de software. Os destinos de formato BGRA têm melhores formatos de RGBA.

 

Quando você cria um [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget), você usa a estrutura de [**\_ Propriedades de \_ destino \_ d2d1 render**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) para especificar opções de renderização. As opções incluem o formato de pixel, conforme observado na seção anterior. o campo tipo dessa estrutura permite que você especifique se o destino de renderização é renderizado em hardware ou software, ou se Direct2D deve determinar automaticamente o modo de renderização.

para habilitar Direct2D para determinar se o destino de renderização usa renderização de hardware ou software, use a configuração [**\_ padrão do tipo de \_ destino \_ \_ D2D1 render**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) .

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
| \_Formato dxgi \_ B8G8R8A8 \_ UNORM | D2D1 \_ MODO \_ ALFA \_ PRÉ-ULTADO |
| DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM | D2D1 \_ MODO \_ ALFA \_ IGNORAR        |
| DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM | MODO ALFA D2D1 \_ \_ \_ DESCONHECIDO       |
| FORMATO DXGI \_ \_ DESCONHECIDO         | D2D1 \_ MODO \_ ALFA \_ PRÉ-ULTADO |
| FORMATO DXGI \_ \_ DESCONHECIDO         | D2D1 \_ MODO \_ ALFA \_ IGNORAR        |
| FORMATO DXGI \_ \_ DESCONHECIDO         | MODO ALFA D2D1 \_ \_ \_ DESCONHECIDO       |



 

Independentemente de o [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) ser acelerado por hardware, o formato [DXGI \_ FORMAT \_ UNKNOWN](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) usa [DXGI \_ FORMAT \_ B8G8R8A8](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) por padrão e o modo alfa DESCONHECIDO do MODO [**\_ ALFA \_ \_ D2D1**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) usa **D2D1 \_ ALPHA MODE \_ \_ IGNORE** por padrão.

## <a name="supported-formats-for-id2d1devicecontext"></a>Formatos com suporte para ID2D1DeviceContext

Começando com Windows 8 [**o contexto do dispositivo**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) aproveita mais os formatos de cor alta do [**Direct3D,**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) como:

-   FORMATO DXGI \_ \_ B8G8R8A8 \_ UNORM \_ SRGB
-   FORMATO DXGI \_ \_ R8G8B8A8 \_ UNORM \_ SRGB
-   DXGI \_ FORMAT \_ R16G16B16A16 \_ UNORM
-   DXGI \_ FORMAT \_ R16G16B16A16 \_ FLOAT
-   DXGI \_ FORMAT \_ R32G32B32A32 \_ FLOAT

Use o [**método ID2D1DeviceContext::IsDxgiFormatSupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isdxgiformatsupported) para ver se um formato funciona em um contexto de dispositivo específico. Esses formatos também podem funcionar em [**um ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget).

Esses formatos são além dos formatos com suporte da interface [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) no Windows 7. Consulte [Dispositivos e contextos de dispositivo](devices-and-device-contexts.md) para obter mais informações.

## <a name="supported-formats-for-compatible-render-target"></a>Formatos com suporte para destino de renderização compatível

Um destino de renderização compatível [**(um ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget) criado por um dos métodos [**ID2D1RenderTarget::CreateCompatibleRenderTarget)**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) herda os formatos com suporte e os modos alfa do destino de renderização que o criou. Um destino de renderização compatível também dá suporte às combinações de formato e modo alfa a seguir, independentemente do que seu pai dá suporte.



| Formatar                  | Modo alfa                       |
|-------------------------|----------------------------------|
| FORMATO DXGI \_ \_ A8 \_ UNORM | D2D1 \_ MODO \_ ALFA \_ PRÉ-ULTADO |
| FORMATO DXGI \_ \_ A8 \_ UNORM | MODO ALFA D2D1 \_ \_ \_ RETA      |
| FORMATO DXGI \_ \_ DESCONHECIDO   | MODO ALFA D2D1 \_ \_ \_ DESCONHECIDO       |



 

O [formato DESCONHECIDO FORMATO DXGI \_ \_](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) usa o formato de destino de renderização pai por padrão e o modo alfa DESCONHECIDO DO MODO [**\_ ALFA \_ \_ D2D1**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) usa O MODO ALFA **D2D1 \_ \_ \_ PREMULTIPLIED** por padrão.

## <a name="supported-formats-for-dxgi-surface-render-target"></a>Formatos com suporte para destino de renderização do DXGI Surface

Um destino de renderização DXGI é um [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) criado por um dos métodos [**ID2D1Factory::CreateDxgiSurfaceRenderTarget.**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) Ele dá suporte às combinações de formato e modo alfa a seguir.



| Formatar                        | Modo alfa                       |
|-------------------------------|----------------------------------|
| DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM | D2D1 \_ MODO \_ ALFA \_ PRÉ-ULTADO |
| DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM | D2D1 \_ MODO \_ ALFA \_ IGNORAR        |
| DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM | D2D1 \_ MODO \_ ALFA \_ PRÉ-ULTADO |
| DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM | D2D1 \_ MODO \_ ALFA \_ IGNORAR        |
| FORMATO DXGI \_ \_ A8 \_ UNORM       | D2D1 \_ MODO \_ ALFA \_ PRÉ-ULTADO |
| FORMATO DXGI \_ \_ A8 \_ UNORM       | MODO ALFA D2D1 \_ \_ \_ RETA      |
| FORMATO DXGI \_ \_ DESCONHECIDO         | D2D1 \_ MODO \_ ALFA \_ PRÉ-ULTADO |
| FORMATO DXGI \_ \_ DESCONHECIDO         | D2D1 \_ MODO \_ ALFA \_ IGNORAR        |



 

> [!Note]  
> O formato deve corresponder ao formato da superfície DXGI ao qual o destino de renderização da superfície DXGI desenha.

 

O [formato DESCONHECIDO FORMATO DXGI \_ \_ ](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) usa o formato de superfície DXGI por padrão. Não use o modo [**alfa DESCONHECIDO do MODO \_ ALFA \_ \_ D2D1**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) com um destino de renderização de superfície DXGI. Ele não tem nenhum valor padrão e fará com que a criação do destino de renderização da superfície DXGI falhe.

## <a name="supported-formats-for-wic-bitmap-render-target"></a>Formatos com suporte para destino de renderização de bitmap WIC

Um destino de renderização de bitmap WIC é um [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) criado por um dos métodos [**ID2D1Factory::CreateWicBitmapRenderTarget.**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties_id2d1rendertarget)) Ele dá suporte às combinações de formato e modo alfa a seguir.



| Formatar                        | Modo alfa                       |
|-------------------------------|----------------------------------|
| DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM | D2D1 \_ MODO \_ ALFA \_ PRÉ-ULTADO |
| DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM | D2D1 \_ MODO \_ ALFA \_ IGNORAR        |
| DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM | MODO ALFA D2D1 \_ \_ \_ DESCONHECIDO       |
| FORMATO DXGI \_ \_ A8 \_ UNORM       | D2D1 \_ MODO \_ ALFA \_ PRÉ-ULTADO |
| FORMATO DXGI \_ \_ A8 \_ UNORM       | MODO ALFA D2D1 \_ \_ \_ RETA      |
| FORMATO DXGI \_ \_ A8 \_ UNORM       | MODO ALFA D2D1 \_ \_ \_ DESCONHECIDO       |
| FORMATO DXGI \_ \_ DESCONHECIDO         | D2D1 \_ MODO \_ ALFA \_ PRÉ-ULTADO |
| FORMATO DXGI \_ \_ DESCONHECIDO         | D2D1 \_ MODO \_ ALFA \_ IGNORAR        |
| FORMATO DXGI \_ \_ DESCONHECIDO         | MODO ALFA D2D1 \_ \_ \_ DESCONHECIDO       |



 

O formato de pixel do destino de bitmap WIC deve corresponder ao formato de pixel do bitmap WIC.

O [formato DESCONHECIDO FORMATO DXGI \_ \_](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) usa o formato de bitmap WIC por padrão e o modo alfa DESCONHECIDO DO MODO [**\_ ALFA \_ \_ D2D1**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) usa o modo alfa de bitmap WIC por padrão.

## <a name="supported-formats-for-id2d1dcrendertarget"></a>Formatos com suporte para ID2D1DCRenderTarget

Um [**ID2D1DCRenderTarget dá**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) suporte às combinações de formato e modo alfa a seguir.



| Formatar                        | Modo alfa                       |
|-------------------------------|----------------------------------|
| DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM | D2D1 \_ MODO \_ ALFA \_ PRÉ-ULTADO |
| DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM | D2D1 \_ MODO \_ ALFA \_ IGNORAR        |



 

Não use o formato [DXGI \_ FORMAT \_ UNKNOWN ou](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) o modo alfa UNKNOWN DO MODO [**\_ ALFA \_ \_ D2D1**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) com um [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget). Ele não tem nenhum valor padrão e fará com que a **criação de ID2D1DCRenderTarget** falhe.

## <a name="specifying-a-pixel-format-for-an-id2d1bitmap"></a>Especificando um formato de pixel para um ID2D1Bitmap

Em geral, [**os objetos ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) suportam os seguintes formatos e modos alfa (com algumas restrições, descritas nos parágrafos a seguir.)



| Formatar                                                      | Modo alfa                       |
|-------------------------------------------------------------|----------------------------------|
| DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM                               | D2D1 \_ MODO \_ ALFA \_ PRÉ-ULTADO |
| DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM                               | D2D1 \_ MODO \_ ALFA \_ IGNORAR        |
| DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM                               | MODO ALFA D2D1 \_ \_ \_ DESCONHECIDO       |
| FORMATO DXGI \_ \_ A8 \_ UNORM                                     | D2D1 \_ MODO \_ ALFA \_ PRÉ-ULTADO |
| FORMATO DXGI \_ \_ A8 \_ UNORM                                     | MODO ALFA D2D1 \_ \_ \_ RETA      |
| FORMATO DXGI \_ \_ A8 \_ UNORM                                     | MODO ALFA D2D1 \_ \_ \_ DESCONHECIDO       |
| FORMATO DXGI \_ \_ DESCONHECIDO                                       | D2D1 \_ MODO \_ ALFA \_ PRÉ-ULTADO |
| FORMATO DXGI \_ \_ DESCONHECIDO                                       | D2D1 \_ MODO \_ ALFA \_ IGNORAR        |
| FORMATO DXGI \_ \_ DESCONHECIDO                                       | MODO ALFA D2D1 \_ \_ \_ DESCONHECIDO       |
| DXGI \_ FORMAT \_ B8G8R8X8 \_ UNORM (Windows 8.1 e posterior, somente) | D2D1 \_ MODO \_ ALFA \_ IGNORAR        |
| FORMATO DXGI \_ \_ BC1 \_ UNORM (Windows 8.1 e posterior, somente)      | D2D1 \_ MODO \_ ALFA \_ PRÉ-ULTADO |
| FORMATO DXGI \_ \_ BC1 \_ UNORM (Windows 8.1 e posterior, somente)      | D2D1 \_ MODO \_ ALFA \_ IGNORAR        |
| FORMATO DXGI \_ \_ BC1 \_ UNORM (Windows 8.1 e posterior, somente)      | MODO ALFA D2D1 \_ \_ \_ DESCONHECIDO       |
| FORMATO DXGI \_ \_ BC2 \_ UNORM (Windows 8.1 e posterior, somente)      | D2D1 \_ MODO \_ ALFA \_ PRÉ-ULTADO |
| FORMATO DXGI \_ \_ BC2 \_ UNORM (Windows 8.1 e posterior, somente)      | D2D1 \_ MODO \_ ALFA \_ IGNORAR        |
| FORMATO DXGI \_ \_ BC2 \_ UNORM (Windows 8.1 e posterior, somente)      | MODO ALFA D2D1 \_ \_ \_ DESCONHECIDO       |
| DXGI \_ FORMAT \_ BC3 \_ UNORM (Windows 8.1 e posterior, somente)      | D2D1 \_ MODO \_ ALFA \_ PRÉ-ULTADO |
| DXGI \_ FORMAT \_ BC3 \_ UNORM (Windows 8.1 e posterior, somente)      | D2D1 \_ MODO \_ ALFA \_ IGNORAR        |
| DXGI \_ FORMAT \_ BC3 \_ UNORM (Windows 8.1 e posterior, somente)      | MODO ALFA D2D1 \_ \_ \_ DESCONHECIDO       |



 

Ao usar o método [**ID2D1RenderTarget::CreateSharedBitmap,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) você usa o **campo pixelFormat** de uma estrutura [**D2D1 \_ BITMAP \_ PROPERTIES**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_bitmap_properties) para especificar o formato de pixel do novo destino de renderização. Ele deve corresponder ao formato de pixel da [**origem ID2D1Bitmap.**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)

Ao usar o método [**CreateBitmapFromWicBitmap,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties__id2d1bitmap)) você usa o campo **pixelFormat** de uma estrutura [**D2D1 \_ BITMAP \_ PROPERTIES**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_bitmap_properties) (em vez do membro **pixelFormat** de uma estrutura DE PROPRIEDADES DE DESTINO RENDERIZAÇÃO [**D2D1) \_ \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) para especificar o formato de pixel do novo destino de renderização. Ele deve corresponder ao formato de pixel da origem do bitmap WIC.

> [!Note]  
> Para obter mais informações sobre o suporte para formatos de pixel compactados em bloco (BCn), consulte [Bloquear compactação](block-compression.md).

 

### <a name="supported-wic-formats"></a>Formatos WIC com suporte

Quando você usa o método [**CreateBitmapFromWicBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties__id2d1bitmap)) para criar um bitmap de um bitmap WIC ou quando você usa o método [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) com [**um IWICBitmapLock**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmaplock), a origem do WIC deve estar em um formato com suporte pelo Direct2D.



| Formato WIC                     | Formato DXGI correspondente     | Modo alfa correspondente                                        |
|--------------------------------|-------------------------------|-----------------------------------------------------------------|
| GUID \_ WICPixelFormat8bppAlpha  | FORMATO DXGI \_ \_ A8 \_ UNORM       | MODO ALFA D2D1 \_ RETA OU MODO ALFA \_ \_ D2D1 \_ \_ \_ PRÉ-ULTIPLIED |
| GUID \_ WICPixelFormat32bppPRGBA | DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM | D2D1 \_ MODO \_ ALFA \_ PREMULTIPLIED ou D2D1 \_ ALPHA MODE \_ \_ IGNORE   |
| GUID \_ WICPixelFormat32bppBGR   | DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM | D2D1 \_ MODO \_ ALFA \_ IGNORAR                                       |
| GUID \_ WICPixelFormat32bppPBGRA | DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM | D2D1 \_ MODO \_ ALFA \_ PRÉ-ULTADO                                |



 

Para ver um exemplo que mostra como converter um bitmap WIC em um formato com suporte, consulte Como carregar um [bitmap de um arquivo](how-to-load-a-direct2d-bitmap-from-a-file.md).

## <a name="using-an-unsupported-format"></a>Usando um formato sem suporte

O uso de qualquer combinação que não seja os formatos de pixel e os modos alfa listados nas tabelas anteriores resulta em um FORMATO DE PIXEL SEM SUPORTE [**D2DERR \_ \_ \_**](direct2d-error-codes.md) ou **um erro E \_ INVALIDARG.**

## <a name="about-alpha-modes"></a>Sobre modos alfa

### <a name="about-premultiplied-and-straight-alpha-modes"></a>Sobre modos alfa diretos e pré-ultidos

A [**enumeração MODO \_ ALFA \_ D2D1**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) indica se o canal alfa usa alfa pré-ultado, alfa reto ou deve ser ignorado e considerado opaco. Com alfa reta, o canal alfa indica um valor que corresponde ao quão transparente uma cor é.

As cores são sempre tratadas como alfa Direct2D desenhando comandos e pincéis, independentemente do formato de destino.

Com alfa pré-ultado, cada canal de cor é dimensionado pelo valor alfa. Normalmente, nenhum valor de canal de cor é maior que o valor do canal alfa. Se um valor de canal de cor em um formato pré-multiplicado for maior que o canal alfa, a matemática de combinação de origem padrão criará uma combinação aditiva.

O valor do próprio canal alfa é o mesmo em alfa reta e pré-multiplicada.

### <a name="the-differences-between-straight-and-premultiplied-alpha"></a>As diferenças entre alfa reto e pré-ultado

Ao descrever uma cor RGBA usando alfa reto, o valor alfa da cor é armazenado no canal alfa. Por exemplo, para descrever uma cor vermelha que seja 60% opaca, use os seguintes valores: (255, 0, 0, 255 \* 0,6) = (255, 0, 0, 153). O valor 255 indica vermelho completo e 153 (que é 60% de 255) indica que a cor deve ter uma opacidade de 60%.

Ao descrever uma cor RGBA usando alfa pré-multiplicado, cada cor é multiplicada pelo valor alfa: (255 \* 0,6, 0 \* 0,6, \* 0 0,6, 255 \* 0,6) = (153, 0, 0, 153).

Independentemente do modo alfa do destino de renderização, os valores [**de D2D1 \_ COLOR \_ F**](d2d1-color-f.md) são sempre interpretados como alfa reto. Por exemplo, ao especificar a cor de [**um ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) para uso com um destino de renderização que usa o modo alfa pré-ultado, especifique a cor como faria se o destino de renderização tivesse usado alfa reto. Quando você pinta com o pincel, Direct2D traduz a cor para o formato de destino para você.

### <a name="alpha-mode-for-render-targets"></a>Modo alfa para destinos de renderização

Independentemente da configuração de modo alfa, o conteúdo de um destino de renderização dá suporte à transparência. Por exemplo, se você desenhar um retângulo vermelho parcialmente transparente com um destino de renderização com um modo alfa [**de D2D1 \_ ALPHA MODE \_ \_ IGNORE**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode), o retângulo será exibido em rosa (se a plano de fundo for branca).

Se você desenhar um retângulo vermelho parcialmente transparente quando o modo alfa for [**D2D1 \_ ALPHA \_ MODE \_ PREMULTIPLIED**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode), o retângulo será exibido em rosa (supondo que a plano de fundo seja branca) e você poderá ver por meio dele o que estiver por trás do destino de renderização. Isso é útil quando você usa um [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) para renderizar em uma janela transparente ou quando você usa um destino de renderização compatível (uma renderização direcionada criada pelo método [**CreateCompatibleRenderTarget)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) para criar um bitmap que dá suporte à transparência.

### <a name="cleartype-and-alpha-modes"></a>Modos ClearType e Alfa

Se você especificar um modo alfa diferente de [**D2D1 \_ ALPHA \_ MODE \_ IGNORE**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) para um destino de renderização, o modo de antialização de texto será automaticamente diferente de [**D2D1 \_ TEXT \_ ANTIALIAS \_ MODE CLEARTYPE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_text_antialias_mode) para **D2D1 \_ TEXT \_ ANTIALIAS \_ MODE GRAYSCALE**. (Quando você especifica um modo alfa de MODO ALFA **D2D1 \_ \_ \_ UNKNOWN,** Direct2D define o alfa para você, dependendo do tipo de destino de renderização.)

Você pode usar o método [**SetTextAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settextantialiasmode) para alterar o modo de antialias de texto de volta para [**D2D1 \_ TEXT \_ ANTIALIAS \_ MODE CLEARTYPE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_text_antialias_mode), mas renderizar texto ClearType para uma superfície transparente pode criar resultados imprevisíveis. Se você quiser renderizar o texto ClearType para um destino de renderização transparente, recomendamos que você use uma das duas técnicas a seguir.

-   Use o [**método PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f_d2d1_antialias_mode)) para cortar o destino de renderização para a área em que o texto será renderizado e, em seguida, chame o método [**Clear**](id2d1rendertarget-clear.md) e especifique uma cor opaca e renderizar o texto.
-   Use [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f_id2d1brush_float_id2d1strokestyle)) para desenhar um retângulo opaco atrás da área em que o texto será renderizado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**FORMATO DE PIXEL D2D1 \_ \_**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format)
</dt> <dt>

[**MODO ALFA \_ D2D1 \_**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode)
</dt> <dt>

[FORMATO \_ DXGI](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)
</dt> </dl>

 

 