---
title: Métodos ID2D1RenderTarget PushLayer (D2d1 \_ 1. h)
description: Adiciona a camada especificada ao destino de renderização para que ele receba todas as operações de desenho subsequentes até que PopLayer seja chamado.
ms.assetid: 9336662c-e94e-40ba-adbe-066d704958bc
keywords:
- Métodos PushLayer Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 6a5609192162ae0b0c0e2af8f1b84429d8710509
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796278"
---
# <a name="id2d1rendertargetpushlayer-methods"></a>ID2D1RenderTarget: métodos de ushLayer de:P

Adiciona a camada especificada ao destino de renderização para que ele receba todas as operações de desenho subsequentes até que [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) seja chamado.

### <a name="overload-list"></a>Lista de sobrecargas



| Método                                                                                                                            | Descrição                                                                                                                                                                     |
|:----------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PushLayer ( \_ parâmetros de camada D2D1 \_&, ID2D1Layer \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer))  | Adiciona a camada especificada ao destino de renderização para que ele receba todas as operações de desenho subsequentes até que [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) seja chamado. <br/> |
| [**PushLayer ( \_ parâmetros da camada d2d1 \_ \* , ID2D1Layer \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters_id2d1layer)) | Adiciona a camada especificada ao destino de renderização para que ele receba todas as operações de desenho subsequentes até que [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) seja chamado. <br/> |



## <a name="remarks"></a>Comentários

O método [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) permite que um chamador comece a redirecionar a renderização para uma camada. Todas as operações de renderização são válidas em uma camada. O local da camada é afetado pelo conjunto de transformação mundial no destino de renderização.

Cada **PushLayer** deve ter uma chamada [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) correspondente. Se houver mais chamadas **PopLayer** que chamadas **PushLayer** , o destino de renderização será colocado em um estado de erro. Se a [**liberação**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) for chamada antes que todas as camadas pendentes sejam retiradas, o destino de renderização será colocado em um estado de erro e um erro será retornado. O estado de erro pode ser limpo por uma chamada para [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).

Um recurso [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) específico pode estar ativo apenas uma vez. Em outras palavras, você não pode chamar um método [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) e, em seguida, seguir imediatamente com outro método **PushLayer** com o mesmo recurso de camada. Em vez disso, você deve chamar o segundo método **PushLayer** com recursos de camada diferentes.

Para obter um exemplo, consulte [como cortar uma região com camadas](how-to-clip-with-layers.md).

Esse método não retornará um código de erro se ele falhar. Para determinar se uma operação de desenho (como **PushLayer**) falhou, verifique o resultado retornado pelos métodos [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) ou [**ID2D1RenderTarget:: flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .

## <a name="examples"></a>Exemplos

O exemplo a seguir usa uma camada para recortar um bitmap para uma máscara geométrica. Para obter o exemplo completo, consulte [como recortar para uma máscara geométrica](how-to-clip-with-layers.md).


```C++
HRESULT DemoApp::RenderWithLayer(ID2D1RenderTarget *pRT)
{
    HRESULT hr = S_OK;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &amp;pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(350, 50));

        // Push the layer with the geometric mask.
        pRT->PushLayer(
            D2D1::LayerParameters(D2D1::InfiniteRect(), m_pPathGeometry),
            pLayer
            );
            
  
        pRT->DrawBitmap(m_pOrigBitmap, D2D1::RectF(0, 0, 200, 133));
        pRT->FillRectangle(D2D1::RectF(0.f, 0.f, 25.f, 25.f), m_pSolidColorBrush);  
        pRT->FillRectangle(D2D1::RectF(25.f, 25.f, 50.f, 50.f), m_pSolidColorBrush);
        pRT->FillRectangle(D2D1::RectF(50.f, 50.f, 75.f, 75.f), m_pSolidColorBrush); 
        pRT->FillRectangle(D2D1::RectF(75.f, 75.f, 100.f, 100.f), m_pSolidColorBrush);    
        pRT->FillRectangle(D2D1::RectF(100.f, 100.f, 125.f, 125.f), m_pSolidColorBrush); 
        pRT->FillRectangle(D2D1::RectF(125.f, 125.f, 150.f, 150.f), m_pSolidColorBrush);    
        

        pRT->PopLayer();
    }

    SafeRelease(&amp;pLayer);

    return hr;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D2d1 \_ 1. h (inclui D2d1. h)</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D2d1. lib</dt> </dl>                   |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl>                   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[Visão geral de camadas](direct2d-layers-overview.md)
</dt> </dl>

�

�
