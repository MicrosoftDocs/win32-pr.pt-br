---
title: D2D1_MATRIX_3X2_F (D2d1. h)
description: Representa uma matriz 3 por 2.
ms.assetid: f05d7555-6482-4eea-950f-7b443892cc1f
keywords:
- D2D1_MATRIX_3X2_F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: beb252e35508c48570c96f251205fc8a54755687
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105759153"
---
# <a name="d2d1_matrix_3x2_f"></a>D2D1 \_ matriz \_ 3x2 \_ F

Representa uma matriz 3 por 2.


```C++
typedef D2D_MATRIX_3X2_F D2D1_MATRIX_3X2_F;
```



## <a name="remarks"></a>Comentários

**D2d1 \_ MATRIZ \_ 3x2** é um novo nome para a estrutura [**D2D \_ Matrix \_ 3x2 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) . Para obter uma lista de campos fornecidos pela matriz, consulte [**D2D \_ Matrix \_ 3x2 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f).

Para simplificar as operações comuns de matriz, o Direct2D fornece a classe [**d2d1:: Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f) , que é derivada da estrutura [**\_ \_ 3x2 da matriz d2d1**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) . A classe **Matrix3x2F** fornece um conjunto de métodos auxiliares para executar tarefas comuns, como a criação de uma translação ou matriz de distorção.

## <a name="examples"></a>Exemplos

O exemplo a seguir usa o método [**d2d1:: Matrix3x2F:: Rotation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation) para criar uma matriz de rotação que gira um quadrado no sentido horário 45 graus sobre o centro do quadrado e passa a matriz para o método [**SetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)) do destino render (*m \_ pRenderTarget*).

A ilustração a seguir mostra o efeito de aplicar a transformação de rotação anterior ao quadrado. O quadrado original é um contorno pontilhado e o quadrado girado é uma estrutura de tópicos sólida.

![ilustração de um quadrado girado no sentido horário 45 graus sobre o centro do quadrado original](images/rotate-ovw.png)


```C++
    // Create a rectangle.
    D2D1_RECT_F rectangle = D2D1::Rect(438.0f, 301.5f, 498.0f, 361.5f);

    // Draw the rectangle.
    m_pRenderTarget->DrawRectangle(
        rectangle,
        m_pOriginalShapeBrush,
        1.0f,
        m_pStrokeStyleDash
        );

    // Apply the rotation transform to the render target.
    m_pRenderTarget->SetTransform(
        D2D1::Matrix3x2F::Rotation(
            45.0f,
            D2D1::Point2F(468.0f, 331.5f))
        );

    // Fill the rectangle.
    m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);

    // Draw the transformed rectangle.
    m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);

```



O código foi omitido neste exemplo. Para obter mais informações sobre transformações, consulte a [Visão geral das transformações](direct2d-transforms-overview.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7, Windows Vista com SP2 e atualização de plataforma para aplicativos UWP do Windows Vista \[ Desktop apps \|\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2, Windows Server 2008 com SP2 e atualização de plataforma para aplicativos de aplicativos de desktop do Windows Server 2008 \[ \| UWP\]<br/> |
| Número mínimo de telefone com suporte<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]<br/>                                                  |
| parâmetro<br/>                   | <dl> <dt>D2d1. h</dt> </dl>                                                        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**D2D1::Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f)
</dt> <dt>

[Visão geral das transformações](direct2d-transforms-overview.md)
</dt> <dt>

[Como girar um objeto](how-to-rotate.md)
</dt> <dt>

[Como dimensionar um objeto](how-to-scale.md)
</dt> <dt>

[Como distorcer um objeto](how-to-skew.md)
</dt> <dt>

[Como converter um objeto](how-to-translate.md)
</dt> <dt>

[**D2D \_ matriz \_ 3x2 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f)
</dt> </dl>

 

