---
title: Métodos ID2D1RenderTarget FillEllipse (D2d1. h)
description: Pinta o interior da elipse especificada.
ms.assetid: 149fb303-d2e8-416c-b28f-8bc5f1482ba6
keywords:
- Métodos FillEllipse Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: b8328775d87dd4df0fd015990d31db0751b729bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757904"
---
# <a name="id2d1rendertargetfillellipse-methods"></a>Métodos ID2D1RenderTarget:: FillEllipse

Pinta o interior da elipse especificada.

### <a name="overload-list"></a>Lista de sobrecargas



| Método                                                                                                             | Descrição                                               |
|:-------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------|
| [**FillEllipse (D2D1 \_ ELLIPSE&, ID2D1Brush \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush))  | Pinta o interior da elipse especificada. <br/> |
| [**FillEllipse (D2D1 \_ Ellipse \* , ID2D1Brush \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) | Pinta o interior da elipse especificada. <br/> |



## <a name="remarks"></a>Comentários

Esse método não retornará um código de erro se ele falhar. Para determinar se uma operação de desenho (como **FillEllipse**) falhou, verifique o resultado retornado pelos métodos [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) ou [**ID2D1RenderTarget:: flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .

## <a name="examples"></a>Exemplos

Para obter um exemplo, consulte [como desenhar e preencher uma forma básica](how-to-draw-an-ellipse.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D2d1. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[Como desenhar e preencher uma forma básica](how-to-draw-an-ellipse.md)
</dt> </dl>

�

�
