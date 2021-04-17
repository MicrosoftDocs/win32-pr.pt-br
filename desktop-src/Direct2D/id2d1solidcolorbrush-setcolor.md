---
title: Métodos setColor ID2D1SolidColorBrush
description: Especifica a cor deste pincel de cor sólida.
ms.assetid: 2900bf72-9641-419c-b0d7-334f14f8a474
keywords:
- Métodos setColor Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 580778135e840a69342ff34ffd8e415883317517
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105775643"
---
# <a name="id2d1solidcolorbrushsetcolor-methods"></a>Métodos ID2D1SolidColorBrush:: setColor

Especifica a cor deste pincel de cor sólida.

### <a name="overload-list"></a>Lista de sobrecargas



| Método                                                                          | Descrição                                                |
|:--------------------------------------------------------------------------------|:-----------------------------------------------------------|
| [**SetColor (D2D1 de \_ cor \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1solidcolorbrush-setcolor(constd2d1_color_f_))  | Especifica a cor deste pincel de cor sólida. <br/> |
| [**SetColor (D2D1 \_ cor \_ F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1solidcolorbrush-setcolor(constd2d1_color_f)) | Especifica a cor deste pincel de cor sólida. <br/> |



## <a name="remarks"></a>Comentários

Para ajudar a criar cores, o Direct2D fornece a classe [**colorf**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) . Ele oferece vários métodos auxiliares para a criação de cores e fornece um conjunto ou cores predefinidas.

## <a name="examples"></a>Exemplos

O código a seguir mostra como usar esse método.


```C++
        m_pSolidColorBrush->SetColor(
            D2D1::ColorF(
                0.0f,
                intensity,
                1.0f - intensity
                ));

        hr = m_pRealization->Fill(
                m_pRT,
                m_pSolidColorBrush,
                m_useRealizations ?
                    REALIZATION_RENDER_MODE_DEFAULT :
                    REALIZATION_RENDER_MODE_FORCE_UNREALIZED
                );
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)
</dt> </dl>

 

