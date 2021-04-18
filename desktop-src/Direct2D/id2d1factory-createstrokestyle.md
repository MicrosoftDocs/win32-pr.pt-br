---
title: Métodos CreateStrokeStyle ID2D1Factory
description: Cria um ID2D1StrokeStyle que descreve a extremidade inicial, o padrão de tracejado e outros recursos de um traço.
ms.assetid: cc7bd68b-a6eb-4d05-b331-032ce80f375c
keywords:
- Métodos CreateStrokeStyle Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 09a578cafe6795bbf742d9dac114365d6e850586
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779565"
---
# <a name="id2d1factorycreatestrokestyle-methods"></a>Métodos ID2D1Factory:: CreateStrokeStyle

Cria um [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) que descreve a extremidade inicial, o padrão de tracejado e outros recursos de um traço.

### <a name="overload-list"></a>Lista de sobrecargas



| Método                                                                                                                                                                                                  | Descrição                                                                                                                                |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateStrokeStyle ( \_ Propriedades de estilo de traço D2D1 \_ \_&, float \* , uint, ID2D1StrokeStyle \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createstrokestyle(constd2d1_stroke_style_properties__constfloat_uint32_id2d1strokestyle))  | Cria um [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) que descreve a extremidade inicial, o padrão de tracejado e outros recursos de um traço.<br/> |
| [**CreateStrokeStyle ( \_ \_ \_ Propriedades de estilo de traço d2d1 \* , float \* , uint, ID2D1StrokeStyle \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createstrokestyle(constd2d1_stroke_style_properties_constfloat_uint32_id2d1strokestyle)) | Cria um [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) que descreve a extremidade inicial, o padrão de tracejado e outros recursos de um traço.<br/> |



## <a name="examples"></a>Exemplos

O exemplo a seguir cria um traço que usa um padrão de traço personalizado.


```C++
// Dash array for dashStyle D2D1_DASH_STYLE_CUSTOM
float dashes[] = {1.0f, 2.0f, 2.0f, 3.0f, 2.0f, 2.0f};

// Stroke Style with Dash Style -- Custom
if (SUCCEEDED(hr))
{
    hr = m_pD2DFactory->CreateStrokeStyle(
        D2D1::StrokeStyleProperties(
            D2D1_CAP_STYLE_FLAT,
            D2D1_CAP_STYLE_FLAT,
            D2D1_CAP_STYLE_ROUND,
            D2D1_LINE_JOIN_MITER,
            10.0f,
            D2D1_DASH_STYLE_CUSTOM,
            0.0f),
        dashes,
        ARRAYSIZE(dashes),
        &m_pStrokeStyleCustomOffsetZero
        );
}
```



O exemplo a seguir usa o estilo de traço ao desenhar uma linha.


```C++
m_pRenderTarget->DrawLine(
    D2D1::Point2F(0, 310),
    D2D1::Point2F(200, 310),
    m_pCornflowerBlueBrush,
    10.0f,
    m_pStrokeStyleCustomOffsetZero
    );
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
</dt> </dl>

 

