---
title: Visão geral da interoperabilidade do Direct2D e da GDI
description: Descreve como usar o Direct2D e o GDI juntos.
ms.assetid: 182df2dc-2574-4d8f-a7e1-30d70da1740a
keywords:
- Interoperação Direct2D, GDI
- Direct2D, interoperabilidade
- interoperabilidade, Direct2D
- Graphics Device Interface (GDI)
- GDI (Graphics Device Interface)
- interoperabilidade, Graphics Device Interface (GDI)
- Direct3D, interoperabilidade
- Interoperação do Direct3D, Direct2D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 991d94b4460e9130b3353be38d5f749511434eb6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641690"
---
# <a name="direct2d-and-gdi-interoperability-overview"></a>Visão geral da interoperabilidade do Direct2D e da GDI

Este tópico descreve como usar o Direct2D e o [GDI](/windows/desktop/gdi/windows-gdi) juntos. Há duas maneiras de combinar Direct2D com GDI: você pode gravar o conteúdo GDI em um destino de renderização compatível com GDI Direct2D ou pode gravar o conteúdo de Direct2D em um [controlador de domínio de dispositivo GDI (DC)](/windows/desktop/gdi/device-contexts).

Este tópico inclui as seções a seguir.

-   [Pré-requisitos](#prerequisites)
-   [Desenhar conteúdo de Direct2D para um contexto de dispositivo GDI](#draw-direct2d-content-to-a-gdi-device-context)
-   [ID2D1DCRenderTargets, transformações GDI e compilações de idiomas da direita para a esquerda do Windows](#id2d1dcrendertargets-gdi-transforms-and-right-to-left-language-builds-of-windows)
-   [Desenhar conteúdo GDI para um Direct2D GDI-Compatible destino de renderização](#draw-gdi-content-to-a-direct2d-gdi-compatible-render-target)
-   [Tópicos relacionados](#related-topics)

## <a name="prerequisites"></a>Pré-requisitos

Esta visão geral pressupõe que você esteja familiarizado com as operações básicas de desenho Direct2D. Para obter um tutorial, consulte o guia de [início rápido do Direct2D](direct2d-quickstart.md). Ele também pressupõe que você esteja familiarizado com as operações de desenho do GDI.

## <a name="draw-direct2d-content-to-a-gdi-device-context"></a>Desenhar conteúdo de Direct2D para um contexto de dispositivo GDI

Para desenhar o conteúdo do Direct2D em um controlador de domínio GDI, use um [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget). Para criar um destino de renderização de DC, use o método [**ID2D1Factory:: CreateDCRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdcrendertarget) . Esse método usa dois parâmetros.

O primeiro parâmetro, uma estrutura de [**\_ Propriedades de \_ destino \_ de renderização d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) , especifica a RENDERIZAÇÃO, comunicação remota, DPI, formato de pixel e informações de uso. Para habilitar o destino de renderização do controlador de domínio para trabalhar com o GDI, defina o formato DXGI para o [ \_ formato dxgi \_ B8G8R8A8 \_ UNORM](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) e o modo alfa para [**d2d1 modo alfa, \_ \_ \_ premultiplicado**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) ou **d2d1 \_ \_ modo alfa \_ ignore**.

O segundo parâmetro é o endereço do ponteiro que recebe a referência de destino de renderização de DC.

O código a seguir cria um destino de renderização de DC.


```C++
// Create a DC render target.
D2D1_RENDER_TARGET_PROPERTIES props = D2D1::RenderTargetProperties(
    D2D1_RENDER_TARGET_TYPE_DEFAULT,
    D2D1::PixelFormat(
        DXGI_FORMAT_B8G8R8A8_UNORM,
        D2D1_ALPHA_MODE_IGNORE),
    0,
    0,
    D2D1_RENDER_TARGET_USAGE_NONE,
    D2D1_FEATURE_LEVEL_DEFAULT
    );

hr = m_pD2DFactory->CreateDCRenderTarget(&props, &m_pDCRT);
```



No código anterior, *m \_ pD2DFactory* é um ponteiro para um [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)e *m \_ pDCRT* é um ponteiro para um [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget).

Antes de poder renderizar com o destino de renderização do DC, você deve usar seu método [**BindDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1dcrendertarget-binddc) para associá-lo a um controlador de domínio GDI. Você faz isso sempre que usar um controlador de domínio diferente ou o tamanho da área que deseja desenhar para alterações.

O método [**BindDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1dcrendertarget-binddc) usa dois parâmetros, *HDC* e *pSubRect*. O parâmetro *HDC* fornece um identificador para o contexto do dispositivo que recebe a saída do destino render. O parâmetro *pSubRect* é um retângulo que descreve a parte do contexto do dispositivo para o qual o conteúdo é renderizado. O destino de renderização do DC atualiza seu tamanho para corresponder à área de contexto do dispositivo descrita por *pSubRect*, caso ele mude de tamanho.

O código a seguir associa um controlador de domínio a um destino de renderização de DC.


```C++
HRESULT DemoApp::OnRender(const PAINTSTRUCT &ps)
{


// Get the dimensions of the client drawing area.
GetClientRect(m_hwnd, &rc);
```



<span codelanguage="ManagedCPlusPlus"></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>// Bind the DC to the DC render target.
hr = m_pDCRT->BindDC(ps.hdc, &rc);</code></pre></td>
</tr>
</tbody>
</table>



Depois de associar o destino de renderização de DC a um DC, você pode usá-lo para desenhar. O código a seguir desenha o conteúdo Direct2D e GDI usando um DC.


```C++
HRESULT DemoApp::OnRender(const PAINTSTRUCT &ps)
{

    HRESULT hr;
    RECT rc;

    // Get the dimensions of the client drawing area.
    GetClientRect(m_hwnd, &rc);

    //
    // Draw the pie chart with Direct2D.
    //

    // Create the DC render target.
    hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        // Bind the DC to the DC render target.
        hr = m_pDCRT->BindDC(ps.hdc, &rc);

        m_pDCRT->BeginDraw();

        m_pDCRT->SetTransform(D2D1::Matrix3x2F::Identity());

        m_pDCRT->Clear(D2D1::ColorF(D2D1::ColorF::White));

        m_pDCRT->DrawEllipse(
            D2D1::Ellipse(
                D2D1::Point2F(150.0f, 150.0f),
                100.0f,
                100.0f),
            m_pBlackBrush,
            3.0
            );

        m_pDCRT->DrawLine(
            D2D1::Point2F(150.0f, 150.0f),
            D2D1::Point2F(
                (150.0f + 100.0f * 0.15425f),
                (150.0f - 100.0f * 0.988f)),
            m_pBlackBrush,
            3.0
            );

        m_pDCRT->DrawLine(
            D2D1::Point2F(150.0f, 150.0f),
            D2D1::Point2F(
                (150.0f + 100.0f * 0.525f),
                (150.0f + 100.0f * 0.8509f)),
            m_pBlackBrush,
            3.0
            );

        m_pDCRT->DrawLine(
            D2D1::Point2F(150.0f, 150.0f),
            D2D1::Point2F(
                (150.0f - 100.0f * 0.988f),
                (150.0f - 100.0f * 0.15425f)),
            m_pBlackBrush,
            3.0
            );

        hr = m_pDCRT->EndDraw();
        if (SUCCEEDED(hr))
        {
            //
            // Draw the pie chart with GDI.
            //

            // Save the original object.
            HGDIOBJ original = NULL;
            original = SelectObject(
                ps.hdc,
                GetStockObject(DC_PEN)
                );

            HPEN blackPen = CreatePen(PS_SOLID, 3, 0);
            SelectObject(ps.hdc, blackPen);

            Ellipse(ps.hdc, 300, 50, 500, 250);

            POINT pntArray1[2];
            pntArray1[0].x = 400;
            pntArray1[0].y = 150;
            pntArray1[1].x = static_cast<LONG>(400 + 100 * 0.15425);
            pntArray1[1].y = static_cast<LONG>(150 - 100 * 0.9885);

            POINT pntArray2[2];
            pntArray2[0].x = 400;
            pntArray2[0].y = 150;
            pntArray2[1].x = static_cast<LONG>(400 + 100 * 0.525);
            pntArray2[1].y = static_cast<LONG>(150 + 100 * 0.8509);


            POINT pntArray3[2];
            pntArray3[0].x = 400;
            pntArray3[0].y = 150;
            pntArray3[1].x = static_cast<LONG>(400 - 100 * 0.988);
            pntArray3[1].y = static_cast<LONG>(150 - 100 * 0.15425);

            Polyline(ps.hdc, pntArray1, 2);
            Polyline(ps.hdc, pntArray2, 2);
            Polyline(ps.hdc, pntArray3, 2);

            DeleteObject(blackPen);

            // Restore the original object.
            SelectObject(ps.hdc, original);
        }
    }

    if (hr == D2DERR_RECREATE_TARGET)
    {
        hr = S_OK;
        DiscardDeviceResources();
    }

    return hr;
}
```



Esse código produz saídas conforme mostrado na ilustração a seguir (os textos explicativos foram adicionados para realçar a diferença entre a renderização Direct2D e GDI).

![ilustração de dois gráficos circulares renderizados com Direct2D e GDI](images/gdiinteropcallout.png)

## <a name="id2d1dcrendertargets-gdi-transforms-and-right-to-left-language-builds-of-windows"></a>ID2D1DCRenderTargets, transformações GDI e compilações de idiomas da direita para a esquerda do Windows

Quando você usa um [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget), ele processa o conteúdo de Direct2D para um bitmap interno e, em seguida, renderiza o bitmap para o controlador de domínio com GDI.

É possível que o GDI aplique uma transformação GDI (por meio do método [**SetWorldTransform**](/windows/desktop/api/wingdi/nf-wingdi-setworldtransform) ) ou outro efeito ao mesmo DC usado pelo destino de renderização; nesse caso, a GDI transforma o bitmap produzido por Direct2D. Usar uma transformação GDI para transformar o conteúdo Direct2D tem o potencial de degradar a qualidade visual da saída, pois você está transformando um bitmap para o qual o posicionamento de anti-aliasing e subpixel já foi calculado.

Por exemplo, suponha que você use o destino de renderização para desenhar uma cena que contém geometria e texto com suavização de alias. Se você usar uma transformação GDI para aplicar uma transformação de escala ao controlador de domínio e dimensionar a cena para que ela seja 10 vezes maior, você verá as bordas denteadas e de pixelização. (Se, no entanto, você aplicou uma transformação semelhante usando Direct2D, a qualidade visual da cena não seria degradada.)

Em alguns casos, pode não ser óbvio que a GDI está executando processamento adicional que pode prejudicar a qualidade do conteúdo do Direct2D. Por exemplo, em uma compilação da direita para a esquerda (RTL) do Windows, o conteúdo renderizado por um [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) pode ser horizontalmente invertido quando o GDI o copia para seu destino. Se o conteúdo é realmente invertido depende das configurações atuais do controlador de domínio.

Dependendo do tipo de conteúdo que está sendo renderizado, talvez você queira impedir a inversão. Se o conteúdo de Direct2D incluir texto ClearType, essa inversão diminuirá a qualidade do texto.

Você pode controlar o comportamento de renderização RTL usando a função GDI [**SetLayout**](/windows/desktop/api/wingdi/nf-wingdi-setlayout) . Para evitar o espelhamento, chame a função GDI **SetLayout** e especifique **\_ BITMAPORIENTATIONPRESERVED de layout** como o único valor para o segundo parâmetro (não o combine com **\_ DPE de layout**), conforme mostrado no exemplo a seguir:


```C++
SetLayout(m_hwnd, LAYOUT_BITMAPORIENTATIONPRESERVED);
```



## <a name="draw-gdi-content-to-a-direct2d-gdi-compatible-render-target"></a>Desenhar conteúdo GDI para um Direct2D GDI-Compatible destino de renderização

A seção anterior descreve como gravar o conteúdo do Direct2D em um controlador de domínio GDI. Você também pode gravar conteúdo GDI em um destino de renderização compatível com GDI Direct2D. Essa abordagem é útil para aplicativos que principalmente renderizam com Direct2D, mas têm um modelo de extensibilidade ou outro conteúdo herdado que requer a capacidade de renderizar com o GDI.

Para renderizar o conteúdo GDI para um destino de renderização compatível com GDI Direct2D, use um [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget), que fornece acesso a um contexto de dispositivo que pode aceitar chamadas de desenho do GDI. Ao contrário de outras interfaces, um objeto **ID2D1GdiInteropRenderTarget** não é criado diretamente. Em vez disso, use o método [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) de uma instância de destino de renderização existente. O código a seguir mostra como fazer isso:


```C++
        D2D1_RENDER_TARGET_PROPERTIES rtProps = D2D1::RenderTargetProperties();
        rtProps.usage =  D2D1_RENDER_TARGET_USAGE_GDI_COMPATIBLE;

        // Create a GDI compatible Hwnd render target.
        hr = m_pD2DFactory->CreateHwndRenderTarget(
            rtProps,
            D2D1::HwndRenderTargetProperties(m_hwnd, size),
            &m_pRenderTarget
            );


        if (SUCCEEDED(hr))
        {
            hr = m_pRenderTarget->QueryInterface(__uuidof(ID2D1GdiInteropRenderTarget), (void**)&m_pGDIRT); 
        }
```



No código anterior, *m \_ pD2DFactory* é um ponteiro para um [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)e *m \_ pGDIRT* é um ponteiro para um [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget).

Observe que o sinalizador compatível com o [**uso de destino do d2d1 \_ \_ \_ \_ \_ render**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_usage) é especificado ao criar o destino de renderização compatível com GDI do HWND. Se um formato de pixel for necessário, use o [ \_ formato dxgi \_ B8G8R8A8 \_ UNORM](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format). Se um modo alfa for necessário, use o modo [**\_ alfa d2d1 \_ \_ bimultiplicado**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) ou o **\_ modo alfa d2d1 \_ \_ ignore**.

Observe que o método [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sempre tem sucesso. Para testar se os métodos da interface [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) funcionarão para um determinado destino de renderização, crie uma [**d2d1 de \_ \_ \_ Propriedades de destino de renderização**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) que especifica a compatibilidade GDI e o formato de pixel apropriado e, em seguida, chame o método [**IsSupported**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-issupported(constd2d1_render_target_properties)) de destino de renderização para ver se o destino de renderização é compatível com GDI.

O exemplo a seguir mostra como desenhar um gráfico de pizza (conteúdo GDI) para o destino de renderização compatível com GDI do HWND.


```C++
        HDC hDC = NULL;
        hr = m_pGDIRT->GetDC(D2D1_DC_INITIALIZE_MODE_COPY, &hDC);

        if (SUCCEEDED(hr))
        {
            // Draw the pie chart to the GDI render target associated with the Hwnd render target.
            HGDIOBJ original = NULL;
            original = SelectObject(
                hDC,
                GetStockObject(DC_PEN)
                );

            HPEN blackPen = CreatePen(PS_SOLID, 3, 0);
            SelectObject(hDC, blackPen);

            Ellipse(hDC, 300, 50, 500, 250);

            POINT pntArray1[2];
            pntArray1[0].x = 400;
            pntArray1[0].y = 150;
            pntArray1[1].x = static_cast<LONG>(400 + 100 * 0.15425);
            pntArray1[1].y = static_cast<LONG>(150 - 100 * 0.9885);

            POINT pntArray2[2];
            pntArray2[0].x = 400;
            pntArray2[0].y = 150;
            pntArray2[1].x = static_cast<LONG>(400 + 100 * 0.525);
            pntArray2[1].y = static_cast<LONG>(150 + 100 * 0.8509);

            POINT pntArray3[2];
            pntArray3[0].x = 400;
            pntArray3[0].y = 150;
            pntArray3[1].x = static_cast<LONG>(400 - 100 * 0.988);
            pntArray3[1].y = static_cast<LONG>(150 - 100 * 0.15425);

            Polyline(hDC, pntArray1, 2);
            Polyline(hDC, pntArray2, 2);
            Polyline(hDC, pntArray3, 2);

            DeleteObject(blackPen);

            // Restore the original object.
            SelectObject(hDC, original);

            m_pGDIRT->ReleaseDC(NULL);
        }

```



O código gera gráficos, conforme mostrado na ilustração a seguir com textos explicativos para destacar a diferença de qualidade de renderização. O gráfico de pizza à direita (conteúdo GDI) reduziu a qualidade de renderização do que o gráfico de pizza à esquerda (conteúdo de Direct2D). Isso ocorre porque o Direct2D é capaz de renderizar com anti-aliasing

![ilustração de dois gráficos circulares renderizados em um destino de renderização compatível com GDI do Direct2D](images/gdicontentind2d.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ID2D1Factory::CreateDCRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdcrendertarget)
</dt> <dt>

[**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget)
</dt> <dt>

[**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget)
</dt> <dt>

[**\_Propriedades de \_ destino de renderização d2d1 \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties)
</dt> <dt>

[Contextos de dispositivo GDI](/windows/desktop/gdi/device-contexts)
</dt> <dt>

[SDK DO GDI](/windows/desktop/gdi/windows-gdi)
</dt> </dl>

 

 