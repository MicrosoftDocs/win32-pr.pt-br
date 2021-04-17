---
title: Métodos ID2D1Factory CreateHwndRenderTarget (D2d1. h)
description: Cria um ID2D1HwndRenderTarget, um destino de renderização que é renderizado para uma janela.
ms.assetid: 3b55b1b0-a423-40dc-9581-c1fbe8134ca5
keywords:
- Métodos CreateHwndRenderTarget Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 984de8aea923c5b90d05fb79bc0c9edc319fb4bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747426"
---
# <a name="id2d1factorycreatehwndrendertarget-methods"></a>Métodos ID2D1Factory:: CreateHwndRenderTarget

Cria um [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)), um destino de renderização que é renderizado para uma janela.

### <a name="overload-list"></a>Lista de sobrecargas



| Método                                                                                                                                                                                                                                                                              | Descrição                                                                                                             |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**CreateHwndRenderTarget (D2D1 \_ render \_ Propriedades de destino \_ \* , \_ d2d1 \_ HWND \_ process \_ Propriedades \* de destino, ID2D1HwndRenderTarget \* \* )**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) | Cria um [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)), um destino de renderização que é renderizado para uma janela.<br/> |
| [**CreateHwndRenderTarget ( \_ Propriedades de destino de RENDERIZAÇÃO D2D1 \_ \_&, d2d1 \_ HWND de renderização de propriedades de \_ \_ destino \_&, ID2D1HwndRenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createhwndrendertarget(constd2d1_render_target_properties__constd2d1_hwnd_render_target_properties__id2d1hwndrendertarget))   | Cria um [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)), um destino de renderização que é renderizado para uma janela.<br/> |



## <a name="remarks"></a>Comentários

Quando você cria um destino de renderização e a aceleração de hardware está disponível, você aloca recursos na GPU do computador. Ao criar um destino de renderização uma vez e mantê-lo o mais longo possível, você obterá benefícios de desempenho. Seu aplicativo deve criar destinos de renderização uma vez e mantê-los durante a vida útil do aplicativo ou até que o erro de [**\_ \_ destino de recriação de D2DERR**](direct2d-error-codes.md) seja recebido. Quando receber esse erro, você precisará recriar o destino de renderização (e todos os recursos que ele criou).

## <a name="examples"></a>Exemplos

O exemplo a seguir cria um [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)).


```C++
RECT rc;
GetClientRect(m_hwnd, &rc);

D2D1_SIZE_U size = D2D1::SizeU(
    rc.right - rc.left,
    rc.bottom - rc.top
    );

// Create a Direct2D render target.
hr = m_pD2DFactory->CreateHwndRenderTarget(
    D2D1::RenderTargetProperties(),
    D2D1::HwndRenderTargetProperties(m_hwnd, size),
    &m_pRenderTarget
    );
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D2d1. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
</dt> </dl>
