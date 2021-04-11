---
title: Visão geral sobre interoperabilidade
description: Resume as diferentes tecnologias que você pode usar com o Direct2D.
ms.assetid: 41f3b908-d218-4a47-bfc3-6a37d38ca26a
keywords:
- Interoperação Direct2D, GDI
- Interoperação Direct2D, GDI+
- Direct2D, interoperabilidade
- Direct2D, DirectWrite interoperation
- interoperabilidade, Direct2D
- interoperabilidade, Direct3D
- Graphics Device Interface (GDI)
- GDI (Graphics Device Interface)
- interoperabilidade, Graphics Device Interface (GDI)
- interoperabilidade, GDI+
- Interoperabilidade do DirectWrite
- interoperabilidade, DirectWrite
- Windows Imaging Component (WIC)
- WIC (Windows Imaging Component)
- interoperabilidade, Windows Imaging Component (WIC)
- Direct2D, interoperação de WIC
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 6f56c570a837a541bac9467477d4f6009bda019e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366187"
---
# <a name="interoperability-overview"></a>Visão geral sobre interoperabilidade

Um dos principais recursos do Direct2D's é permitir a interoperabilidade entre Direct2D e outras plataformas de renderização para que os desenvolvedores possam usar os pontos fortes específicos de cada plataforma sem serem forçados a comprometeções escolhendo uma plataforma para todas as necessidades. Este tópico resume as diferentes plataformas com as quais o Direct2D é interoperável. Ele contém as seguintes seções:

-   [Interoperabilidade GDI](#gdi-interoperability)
-   [Interoperabilidade de GDI+](#gdi-interoperability)
-   [Interoperabilidade do Direct3D](#direct3d-interoperability)
-   [Interoperabilidade do DirectWrite](#directwrite-interoperability)
-   [Interoperabilidade do Windows Imaging Component (WIC)](#windows-imaging-component-wic-interoperability)
-   [Tópicos relacionados](#related-topics)

O diagrama a seguir resume as diferentes plataformas com as quais o Direct2D é interoperável e lista alguns métodos e interfaces que fornecem interoperabilidade.

![diagrama de plataformas com as quais o Direct2D interopera, incluindo Direct3D 10,1, DirectWrite, WIC, GDI+ e GDI](images/direct2dinterop.png)

## <a name="gdi-interoperability"></a>Interoperabilidade GDI

O Direct2D habilita a interoperabilidade bidirecional com GDI. Você pode usar um [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) para gravar o conteúdo do Direct2D em um DC ( [contexto de dispositivo](/windows/desktop/gdi/device-contexts) GDI) ou pode usar o [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) para obter uma representação de DC de um destino de renderização.

Para obter mais informações e exemplos, consulte a [visão geral de interoperabilidade Direct2D e GDI](direct2d-and-gdi-interoperation-overview.md).

## <a name="gdi-interoperability"></a>Interoperabilidade de GDI+

Você pode usar o GDI+ com Direct2D da mesma maneira que o GDI. Você pode usar um [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) para gravar o conteúdo do Direct2D no mesmo controlador de domínio que o seu conteúdo GDI+. Essa abordagem permite que você comece a adicionar conteúdo Direct2D a aplicativos que são renderizados principalmente usando o GDI+.

Você também pode usar um [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) para fornecer acesso a um controlador de domínio GDI que grava usando Direct2D e, em seguida, usar o método [**FromHDC**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fromhdc(inhdc)) para criar um objeto. Essa abordagem é útil para aplicativos que são renderizados principalmente com Direct2D, mas têm um modelo de extensibilidade ou outro conteúdo herdado que requer a capacidade de renderizar com o GDI+.

## <a name="direct3d-interoperability"></a>Interoperabilidade do Direct3D

Direct2D pode usar um destino de renderização de superfície DXGI (criado pelo método [**CreateDxgiSurfaceRender**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) ) para gravar em um [IDXGISurface](/windows/win32/api/dxgi/nn-dxgi-idxgisurface). Essa ação permite que você adicione planos de fundo e interfaces 2D a cenas 3D e use o conteúdo Direct2D como uma textura para um modelo 3D. Direct2D também pode pegar um [IDXGISurface](/windows/win32/api/dxgi/nn-dxgi-idxgisurface) e usar o método [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) para criar uma representação de bitmap.

Para obter mais informações e exemplos, consulte a [visão geral de interoperabilidade do Direct2D e do Direct3D](direct2d-and-direct3d-interoperation-overview.md).

## <a name="directwrite-interoperability"></a>Interoperabilidade do DirectWrite

O Direct2D está totalmente integrado ao DirectWrite. O Direct2D facilita a renderização do conteúdo do DirectWrite fornecendo os métodos [**DrawText**](id2d1rendertarget-drawtext.md), [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)e [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) .

## <a name="windows-imaging-component-wic-interoperability"></a>Interoperabilidade do Windows Imaging Component (WIC)

O Direct2D fornece os métodos [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md), [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap)e [**CreateWicBitmapRenderTarget**](id2d1factory-createwicbitmaprendertarget.md) para manipular bitmaps de WIC.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral da interoperabilidade do Direct2D e da GDI](direct2d-and-gdi-interoperation-overview.md)
</dt> <dt>

[Visão geral de interoperabilidade entre Direct2D e Direct3D](direct2d-and-direct3d-interoperation-overview.md)
</dt> </dl>

 

 