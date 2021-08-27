---
title: Métodos CreateLayer ID2D1RenderTarget (D2d1. h)
description: Cria um recurso de camada que pode ser usado com esse destino de renderização e seus destinos de renderização compatíveis.
ms.assetid: 074e9ffb-c5f2-4e7b-94c7-d457bf07c0b7
keywords:
- Métodos CreateLayer Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: a351c9e1b4fc36c816e87aeaae79a591bb43768a4e098bf315990fc1e1794fe4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131486"
---
# <a name="id2d1rendertargetcreatelayer-methods"></a>Métodos ID2D1RenderTarget:: CreateLayer

Cria um recurso de camada que pode ser usado com esse destino de renderização e seus destinos de renderização compatíveis.

### <a name="overload-list"></a>Lista de sobrecargas



| Método                                                                                                                 | Descrição                                                                                                                                                    |
|:-----------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateLayer (ID2D1Layer \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer))                                | Cria um recurso de camada que pode ser usado com esse destino de renderização e seus destinos de renderização compatíveis. <br/>                                               |
| [**CreateLayer (D2D1 \_ tamanho \_ F, ID2D1Layer \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(d2d1_size_f_id2d1layer))       | Cria um recurso de camada que pode ser usado com esse destino de renderização e seus destinos de renderização compatíveis. A nova camada tem o tamanho inicial especificado. <br/> |
| [**CreateLayer (D2D1 \_ tamanho \_ F \* , ID2D1Layer \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(d2d1_size_f_id2d1layer)) | Cria um recurso de camada que pode ser usado com esse destino de renderização e seus destinos de renderização compatíveis. A nova camada tem o tamanho inicial especificado. <br/> |



## <a name="remarks"></a>Comentários

A camada é redimensionada automaticamente, conforme necessário.

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
|--------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D2d1. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral de camadas](direct2d-layers-overview.md)
</dt> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

�

�
