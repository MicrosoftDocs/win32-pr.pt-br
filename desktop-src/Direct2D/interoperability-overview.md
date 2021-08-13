---
title: Visão geral sobre interoperabilidade
description: Resume as diferentes tecnologias que você pode usar com Direct2D.
ms.assetid: 41f3b908-d218-4a47-bfc3-6a37d38ca26a
keywords:
- interoperação Direct2D, GDI
- interoperação Direct2D, GDI+
- Direct2D, interoperabilidade
- interoperação Direct2D, DirectWrite
- interoperabilidade, Direct2D
- interoperabilidade, Direct3D
- Graphics Device Interface (GDI)
- GDI (Graphics Device Interface)
- interoperabilidade, Graphics Device Interface (GDI)
- interoperabilidade, GDI+
- interoperabilidade DirectWrite
- interoperabilidade, DirectWrite
- Windows Imaging Component (WIC)
- WIC (componente de Windows Imaging)
- interoperabilidade, componente do Windows Imaging (WIC)
- Direct2D, interoperação de WIC
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 35567b461815d28a5fc00b2cc4049f5c81b61c6e8030f477e93efbc8a5d580e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119385316"
---
# <a name="interoperability-overview"></a>Visão geral sobre interoperabilidade

um dos principais recursos do Direct2D é permitir a interoperabilidade entre Direct2D e outras plataformas de renderização para que os desenvolvedores possam usar os pontos fortes específicos de cada plataforma sem serem forçados a comprometeções escolhendo uma plataforma para todas as necessidades. este tópico resume as diferentes plataformas com as quais Direct2D é interoperável. Ele contém as seguintes seções:

-   [Interoperabilidade GDI](#gdi-interoperability)
-   [GDI+ Interoperabilidade](#gdi-interoperability)
-   [Interoperabilidade do Direct3D](#direct3d-interoperability)
-   [DirectWrite Interoperabilidade](#directwrite-interoperability)
-   [Windows Interoperabilidade do componente de geração de imagens (WIC)](#windows-imaging-component-wic-interoperability)
-   [Tópicos relacionados](#related-topics)

o diagrama a seguir resume as diferentes plataformas com as quais Direct2D é interoperável e lista alguns métodos e interfaces que fornecem interoperabilidade.

![diagrama de plataformas com as quais o Direct2D interopera, incluindo Direct3D 10,1, DirectWrite, WIC, GDI+ e GDI](images/direct2dinterop.png)

## <a name="gdi-interoperability"></a>Interoperabilidade GDI

Direct2D habilita a interoperabilidade bidirecional com GDI. você pode usar um [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) para gravar o conteúdo do Direct2D em um [controlador de domínio](/windows/desktop/gdi/device-contexts) GDI ou pode usar o [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) para obter uma representação de controlador de domínio de um destino de renderização.

para obter mais informações e exemplos, consulte a [visão geral de interoperabilidade Direct2D e GDI](direct2d-and-gdi-interoperation-overview.md).

## <a name="gdi-interoperability"></a>GDI+ Interoperabilidade

você pode usar GDI+ com Direct2D da mesma maneira que o GDI. você pode usar um [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) para gravar o conteúdo do Direct2D no mesmo controlador de domínio que o conteúdo do GDI+. essa abordagem permite que você comece a adicionar Direct2D conteúdo aos aplicativos que são renderizados principalmente usando GDI+.

você também pode usar um [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) para fornecer acesso a um controlador de domínio GDI que grava usando Direct2D e, em seguida, usar o método [**FromHDC**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fromhdc(inhdc)) para criar um objeto. essa abordagem é útil para aplicativos que são renderizados principalmente com Direct2D, mas têm um modelo de extensibilidade ou outro conteúdo herdado que requer a capacidade de renderizar com GDI+.

## <a name="direct3d-interoperability"></a>Interoperabilidade do Direct3D

Direct2D pode usar um destino de renderização de superfície DXGI (criado pelo método [**CreateDxgiSurfaceRender**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) ) para gravar em um [IDXGISurface](/windows/win32/api/dxgi/nn-dxgi-idxgisurface). essa ação permite que você adicione planos de fundo e interfaces 2d a cenas 3d e use Direct2D conteúdo como uma textura para um modelo 3d. Direct2D também pode pegar um [IDXGISurface](/windows/win32/api/dxgi/nn-dxgi-idxgisurface) e usar o método [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) para criar uma representação de bitmap.

para obter mais informações e exemplos, consulte a [visão geral de interoperabilidade Direct2D e Direct3D](direct2d-and-direct3d-interoperation-overview.md).

## <a name="directwrite-interoperability"></a>DirectWrite Interoperabilidade

o Direct2D é totalmente integrado ao DirectWrite. Direct2D torna mais fácil renderizar DirectWrite conteúdo fornecendo os métodos [**DrawText**](id2d1rendertarget-drawtext.md), [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)e [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) .

## <a name="windows-imaging-component-wic-interoperability"></a>Windows Interoperabilidade do componente de geração de imagens (WIC)

Direct2D fornece os métodos [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md), [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap)e [**CreateWicBitmapRenderTarget**](id2d1factory-createwicbitmaprendertarget.md) para manipular os bitmaps do WIC.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[visão geral de interoperabilidade Direct2D e GDI](direct2d-and-gdi-interoperation-overview.md)
</dt> <dt>

[Visão geral de interoperabilidade entre Direct2D e Direct3D](direct2d-and-direct3d-interoperation-overview.md)
</dt> </dl>

 

 