---
title: Métodos ID2D1RenderTarget CreateCompatibleRenderTarget (D2d1. h)
description: Cria um novo destino de renderização de bitmap para uso durante o desenho de fora da tela intermediário que é compatível com o destino de renderização atual.
ms.assetid: 4a799a7c-0d2f-460f-99f9-24c6cf7c4537
keywords:
- Métodos CreateCompatibleRenderTarget Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 0f0de8478d2ab3ee2e7142bd0e197053dc58ac2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752921"
---
# <a name="id2d1rendertargetcreatecompatiblerendertarget-methods"></a>Métodos ID2D1RenderTarget:: CreateCompatibleRenderTarget

Cria um novo destino de renderização de bitmap para uso durante o desenho de fora da tela intermediário que é compatível com o destino de renderização atual.

### <a name="overload-list"></a>Lista de sobrecargas



| Método                                                                                                                                                                                                                        | Descrição                                                                                                                                                                                                                                            |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateCompatibleRenderTarget (tamanho de D2D1 \_ \_ F, d2d1 de \_ tamanho \_ U, d2d1 em \_ \_ formato de pixel, d2d1 \_ \_ \_ \_ Opções de destino de renderização compatíveis, ID2D1BitmapRenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(d2d1_size_f_d2d1_size_u_d2d1_pixel_format_d2d1_compatible_render_target_options_id2d1bitmaprendertarget))       | Cria um destino de renderização de bitmap para uso durante o desenho de tela intermediária que é compatível com o destino de renderização atual.<br/>                                                                                                             |
| [**CreateCompatibleRenderTarget (tamanho de D2D1 \_ \_ F \* , d2d1 de \_ tamanho \_ U \* , d2d1 em \_ \_ formato \* de pixel, d2d1 \_ \_ \_ \_ Opções de destino de renderização compatíveis, ID2D1BitmapRenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(d2d1_size_f_d2d1_size_u_d2d1_pixel_format_d2d1_compatible_render_target_options_id2d1bitmaprendertarget)) | Cria um destino de renderização de bitmap para uso durante o desenho de tela intermediária que é compatível com o destino de renderização atual. <br/>                                                                                                            |
| [**CreateCompatibleRenderTarget (ID2D1BitmapRenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget))                                                                                                 | Cria um novo destino de renderização de bitmap para uso durante o desenho de fora da tela intermediário que é compatível com o destino de renderização atual e tem o mesmo tamanho, DPI e formato de pixel (mas não modo alfa) como o destino de renderização atual. <br/>         |
| [**CreateCompatibleRenderTarget (D2D1 \_ tamanho \_ F, ID2D1BitmapRenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(d2d1_size_f_id2d1bitmaprendertarget))                                                                                   | Cria um novo destino de renderização de bitmap para uso durante o desenho de fora da tela intermediário que é compatível com o destino de renderização atual e tem o mesmo formato de pixel (mas não modo alfa) como o destino de renderização atual. <br/>                        |
| [**CreateCompatibleRenderTarget (tamanho de D2D1 \_ \_ F, d2d1 \_ tamanho \_ U, ID2D1BitmapRenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(d2d1_size_f_d2d1_size_u_id2d1bitmaprendertarget))                                                                     | Cria um destino de renderização de bitmap para uso durante o desenho intermediário fora da tela que é compatível com o destino de renderização atual. O novo destino de renderização de bitmap tem o mesmo formato de pixel (mas não o modo alfa) como o destino de renderização atual. <br/> |
| [**CreateCompatibleRenderTarget (tamanho de D2D1 \_ \_ F, d2d1 \_ Size \_ U, d2d1 \_ pixel \_ Format, ID2D1BitmapRenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(d2d1_size_f_d2d1_size_u_d2d1_pixel_format_id2d1bitmaprendertarget))                                                 | Cria um destino de renderização de bitmap para uso durante o desenho de tela intermediária que é compatível com o destino de renderização atual. <br/>                                                                                                            |



## <a name="examples"></a>Exemplos

O exemplo a seguir usa o método **CreateCompatibleRenderTarget** para criar um [**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget) e o usa para desenhar um padrão de grade. O padrão de grade é usado como a origem de um [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).


```C++
HRESULT DemoApp::CreateGridPatternBrush(
    ID2D1RenderTarget *pRenderTarget,
    ID2D1BitmapBrush **ppBitmapBrush
    )
{
    // Create a compatible render target.
    ID2D1BitmapRenderTarget *pCompatibleRenderTarget = NULL;
    HRESULT hr = pRenderTarget->CreateCompatibleRenderTarget(
        D2D1::SizeF(10.0f, 10.0f),
        &amp;pCompatibleRenderTarget
        );
    if (SUCCEEDED(hr))
    {
        // Draw a pattern.
        ID2D1SolidColorBrush *pGridBrush = NULL;
        hr = pCompatibleRenderTarget->CreateSolidColorBrush(
            D2D1::ColorF(D2D1::ColorF(0.93f, 0.94f, 0.96f, 1.0f)),
            &amp;pGridBrush
            );
        if (SUCCEEDED(hr))
        {
            pCompatibleRenderTarget->BeginDraw();
            pCompatibleRenderTarget->FillRectangle(D2D1::RectF(0.0f, 0.0f, 10.0f, 1.0f), pGridBrush);
            pCompatibleRenderTarget->FillRectangle(D2D1::RectF(0.0f, 0.1f, 1.0f, 10.0f), pGridBrush);
            pCompatibleRenderTarget->EndDraw();

            // Retrieve the bitmap from the render target.
            ID2D1Bitmap *pGridBitmap = NULL;
            hr = pCompatibleRenderTarget->GetBitmap(&amp;pGridBitmap);
            if (SUCCEEDED(hr))
            {
                // Choose the tiling mode for the bitmap brush.
                D2D1_BITMAP_BRUSH_PROPERTIES brushProperties =
                    D2D1::BitmapBrushProperties(D2D1_EXTEND_MODE_WRAP, D2D1_EXTEND_MODE_WRAP);

                // Create the bitmap brush.
                hr = m_pRenderTarget->CreateBitmapBrush(pGridBitmap, brushProperties, ppBitmapBrush);

                pGridBitmap->Release();
            }

            pGridBrush->Release();
        }

        pCompatibleRenderTarget->Release();
    }

    return hr;
}
```



O exemplo de código a seguir usa o pincel para pintar um padrão.


```C++
// Paint a grid background.
m_pRenderTarget->FillRectangle(
    D2D1::RectF(0.0f, 0.0f, renderTargetSize.width, renderTargetSize.height),
    m_pGridPatternBitmapBrush
    );
```



O código foi omitido neste exemplo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D2d1. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

�

�
