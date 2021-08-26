---
title: Métodos SetTransform de ID2D1Brush (D2d1 \_ 1. h)
description: Define a transformação aplicada ao pincel.
ms.assetid: 57afadc1-88c9-4a5b-a83f-63c4c69182a7
keywords:
- Métodos SetTransform Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: a5a30d4051303667402fdd1143f5a813d7515223c8093a5913294e6dd1722273
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918027"
---
# <a name="id2d1brushsettransform-methods"></a>Métodos ID2D1Brush:: SetTransform

Define a transformação aplicada ao pincel.

### <a name="overload-list"></a>Lista de sobrecargas



| Método                                                                                       | Descrição                                              |
|:---------------------------------------------------------------------------------------------|:---------------------------------------------------------|
| [**SetTransform (D2D1 \_ Matrix \_ 3X2 \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_))  | Define a transformação aplicada ao pincel.<br/> |
| [**SetTransform ( \_ matriz d2d1 \_ 3x2 \_ F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f)) | Define a transformação aplicada ao pincel.<br/> |



## <a name="remarks"></a>Comentários

Quando você pinta com um pincel, ele pinta no espaço de coordenadas do destino de renderização. Os pincéis não se posicionam automaticamente para se alinharem com o objeto que está sendo pintado; Por padrão, eles começam a pintar na origem (0, 0) do destino de renderização.

Você pode "mover" o gradiente definido por um [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) para uma área de destino definindo seu ponto de partida e ponto de extremidade. Da mesma forma, você pode mover o gradiente definido por um [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) alterando seu centro e raios.

Para alinhar o conteúdo de um [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) à área que está sendo pintada, você pode usar o método **SetTransform** para converter o bitmap no local desejado. Essa transformação afeta apenas o pincel; Ele não afeta nenhum outro conteúdo desenhado pelo destino de renderização.

As ilustrações a seguir mostram o efeito de usar um [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) para preencher um retângulo localizado em (100, 100). A ilustração na ilustração à esquerda mostra o resultado do preenchimento do retângulo sem transformar o pincel: o bitmap é desenhado na origem do destino do processamento. Como resultado, apenas uma parte do bitmap é exibida no retângulo.

A ilustração à direita mostra o resultado da transformação do [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) para que seu conteúdo seja deslocado 50 pixels para a direita e 50 pixels para baixo. O bitmap agora preenche o retângulo.

![ilustração de dois quadrados, um pintado com um bitmap sem um pincel transformado e um pintado com um pincel transformado](images/brushes-ovw-transform.png)

## <a name="examples"></a>Exemplos

Os exemplos de código a seguir mostram como criar a transformação mostrada no diagrama à direita na ilustração anterior. Primeiro, aplique uma tradução ao [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), movendo o pincel 50 pixels para o eixo x e 50 pixels para baixo ao longo do eixo y. Em seguida, use o **ID2D1BitmapBrush** para preencher o retângulo que tem o canto superior esquerdo em (100, 100) e no canto inferior direito em (200, 200).


```C++
// Create the bitmap to be used by the bitmap brush.
if (SUCCEEDED(hr))
{
    hr = LoadResourceBitmap(
        m_pRenderTarget,
        m_pWICFactory,
        L"FERN",
        L"Image",
        &amp;m_pBitmap
        );
   
}
```




```C++
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pBitmap,
        &amp;m_pBitmapBrush
        );
}
```




```C++
D2D1_RECT_F rcTransformedBrushRect = D2D1::RectF(100, 100, 200, 200);



 // Demonstrate the effect of transforming a bitmap brush.
 m_pBitmapBrush->SetTransform(
     D2D1::Matrix3x2F::Translation(D2D1::SizeF(50,50))
     );

 // To see the content of the rcTransformedBrushRect, comment
 // out this statement.
 m_pRenderTarget->FillRectangle(
     &rcTransformedBrushRect, 
     m_pBitmapBrush
     );

 m_pRenderTarget-&gt;DrawRectangle(rcTransformedBrushRect, m_pBlackBrush, 1, NULL);
```





## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D2d1 \_ 1. h (inclui D2d1. h)</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D2d1. lib</dt> </dl>                   |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl>                   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral de pincéis](direct2d-brushes-overview.md)
</dt> <dt>

[**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush)
</dt> </dl>

�

�
