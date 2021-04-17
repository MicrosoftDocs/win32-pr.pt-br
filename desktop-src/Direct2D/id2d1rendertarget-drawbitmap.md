---
title: Métodos ID2D1RenderTarget DrawBitmap
description: Desenha o ID2D1Bitmap especificado.
ms.assetid: 241df698-ca5e-4d94-902a-a9e140820c14
keywords:
- Métodos DrawBitmap Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: d82bbf557d7e53f06f614afbba578de40c789953
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812857"
---
# <a name="id2d1rendertargetdrawbitmap-methods"></a>ID2D1RenderTarget: métodos de rawBitmap de:D

Desenha o [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)especificado.

### <a name="overload-list"></a>Lista de sobrecargas



| Método                                                                                                                                                                                                                       | Descrição                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**DrawBitmap (ID2D1Bitmap \* , d2d1 \_ rect \_ f&, float, d2d1 \_ bitmap \_ do \_ modo de interpolação, d2d1 \_ Rect \_ f&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f_))   | Desenha o bitmap especificado depois de dimensioná-lo para o tamanho do retângulo especificado. <br/> |
| [**DrawBitmap (ID2D1Bitmap \* , d2d1 \_ rect \_ f&, float, d2d1 \_ bitmap \_ \_ modo de interpolação, d2d1 \_ Rect \_ f \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f))  | Desenha o bitmap especificado depois de dimensioná-lo para o tamanho do retângulo especificado. <br/> |
| [**DrawBitmap (ID2D1Bitmap \* , d2d1 \_ Rect \_ f \* , float, d2d1 \_ bitmap \_ do \_ modo de interpolação, d2d1 \_ Rect \_ f \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f_float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f)) | Desenha o bitmap especificado depois de dimensioná-lo para o tamanho do retângulo especificado. <br/> |



## <a name="remarks"></a>Comentários

Esse método não retornará um código de erro se ele falhar. Para determinar se uma operação de desenho (como **DrawBitmap**) falhou, verifique o resultado retornado pelos métodos [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) ou [**ID2D1RenderTarget:: flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .

## <a name="examples"></a>Exemplos

Para obter um exemplo, consulte [como desenhar um bitmap](how-to-draw-a-bitmap.md). Para obter um exemplo que mostra como carregar um bitmap de um recurso ou arquivo, consulte [como carregar um bitmap de um recurso](how-to-load-a-bitmap-from-a-resource.md) e [como carregar um bitmap de um arquivo](how-to-load-a-direct2d-bitmap-from-a-file.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[Como desenhar um bitmap](how-to-draw-a-bitmap.md)
</dt> <dt>

[Como carregar um bitmap de um recurso](how-to-load-a-bitmap-from-a-resource.md)
</dt> <dt>

[Como carregar um bitmap de um arquivo](how-to-load-a-direct2d-bitmap-from-a-file.md)
</dt> </dl>

 

