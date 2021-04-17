---
title: Métodos ID2D1RenderTarget CreateBitmapBrush
description: Cria um ID2D1BitmapBrush a partir do bitmap especificado.
ms.assetid: 7f6ef07e-4271-4605-aced-f191a0fe65af
keywords:
- Métodos CreateBitmapBrush Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: fcd512393a3f037cd3def40d4aa55003d9fddcef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755401"
---
# <a name="id2d1rendertargetcreatebitmapbrush-methods"></a>Métodos ID2D1RenderTarget:: CreateBitmapBrush

Cria um [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) a partir do bitmap especificado.

### <a name="overload-list"></a>Lista de sobrecargas



| Método                                                                                                                                                                                                                                                               | Descrição                                                                                                                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateBitmapBrush (ID2D1Bitmap \* , \_ Propriedades de pincel de BITMAP d2d1 \_ \_&, \_ Propriedades de pincel d2d1 \_&, ID2D1BitmapBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties_id2d1bitmap))   | Cria um [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) a partir do bitmap especificado.<br/>                                                                                                    |
| [**CreateBitmapBrush (ID2D1Bitmap \* , \_ Propriedades de pincel de bitmap d2d1 \_ \_ \* , \_ \_ Propriedades \* de pincel de d2d1, ID2D1BitmapBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapbrush(id2d1bitmap_constd2d1_bitmap_brush_properties_constd2d1_brush_properties_id2d1bitmapbrush)) | Cria um [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) a partir do bitmap especificado.<br/>                                                                                                    |
| [**CreateBitmapBrush (ID2D1Bitmap \* , ID2D1BitmapBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapbrush(id2d1bitmap_id2d1bitmapbrush))                                                                                                                        | Cria um [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) a partir do bitmap especificado. O pincel usa os valores padrão para seu modo de extensão, modo de interpolação, opacidade e transformação.<br/> |
| [**CreateBitmapBrush (ID2D1Bitmap \* , \_ Propriedades de pincel de BITMAP d2d1 \_ \_&, ID2D1BitmapBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapbrush(id2d1bitmap_constd2d1_bitmap_brush_properties__id2d1bitmapbrush))                                                      | Cria um [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) a partir do bitmap especificado. O pincel usa os valores padrão para sua opacidade e transformação.<br/>                                   |



## <a name="examples"></a>Exemplos

Para ver um exemplo que mostra como pintar uma área com um pincel de bitmap, consulte [como criar um pincel de bitmap](how-to-create-a-bitmap-brush.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[Como criar um pincel de bitmap](how-to-create-a-bitmap-brush.md)
</dt> <dt>

[Visão geral de pincéis](direct2d-brushes-overview.md)
</dt> </dl>

 

