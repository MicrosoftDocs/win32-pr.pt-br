---
title: Métodos ID2D1RenderTarget Clear
description: Limpa a área de desenho para a cor especificada.
ms.assetid: 3bfec923-17fc-479a-a760-9baab2ff3a56
keywords:
- Limpar métodos Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 4e4e0c9843752af0799901537c5ee6d682d895a5ada22843ad2c406e9bda32b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928946"
---
# <a name="id2d1rendertargetclear-methods"></a>Métodos ID2D1RenderTarget::Clear

Limpa a área de desenho para a cor especificada.

### <a name="overload-list"></a>Lista de sobrecargas



| Método                                                                 | Descrição                                                 |
|:-----------------------------------------------------------------------|:------------------------------------------------------------|
| [**Clear(D2D1 \_ COLOR \_ F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-clear(constd2d1_color_f)) | Limpa a área de desenho para a cor especificada. <br/> |
| [**Clear(D2D1 \_ COLOR \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-clear(constd2d1_color_f_))  | Limpa a área de desenho para a cor especificada. <br/> |



## <a name="remarks"></a>Comentários

Direct2D interpreta *clearColor* como alfa reta (não pré-ultido). Se o modo alfa do destino de renderização for [**D2D1 \_ MODO ALFA \_ \_ IGNORAR**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode), o canal alfa de *clearColor* será ignorado e substituído por 1.0f (totalmente opaco).

Se o destino de renderização tiver um clipe ativo (especificado por [**PushAxisAlignedClip),**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))o comando clear só será aplicado à área dentro da região do clipe.

## <a name="examples"></a>Exemplos

O exemplo a seguir usa o **método Clear** para criar uma plano de fundo em branco antes de renderizar outro conteúdo.


```C++
//  Called whenever the application needs to display the client
//  window. This method writes "Hello, World"
//
//  Note that this function will automatically discard device-specific
//  resources if the Direct3D device disappears during function
//  invocation, and will recreate the resources the next time it's
//  invoked.
//
HRESULT DemoApp::OnRender()
{
    HRESULT hr;

    hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        static const WCHAR sc_helloWorld[] = L"Hello, World!";

        // Retrieve the size of the render target.
        D2D1_SIZE_F renderTargetSize = m_pRenderTarget->GetSize();

        m_pRenderTarget->BeginDraw();

        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

        m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

        m_pRenderTarget->DrawText(
            sc_helloWorld,
            ARRAYSIZE(sc_helloWorld) - 1,
            m_pTextFormat,
            D2D1::RectF(0, 0, renderTargetSize.width, renderTargetSize.height),
            m_pBlackBrush
            );

        hr = m_pRenderTarget->EndDraw();

        if (hr == D2DERR_RECREATE_TARGET)
        {
            hr = S_OK;
            DiscardDeviceResources();
        }
    }

    return hr;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>D2d1.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

 

