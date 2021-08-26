---
title: Métodos ID2D1RenderTarget CreateBitmapBrush
description: Cria um ID2D1BitmapBrush do bitmap especificado.
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
ms.openlocfilehash: 411ae2dd81fce88bec5d6a3717fe79d942de84f060c53a90b83cae461d6a49de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053086"
---
# <a name="id2d1rendertargetcreatebitmapbrush-methods"></a>Métodos ID2D1RenderTarget::CreateBitmapBrush

Cria um [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) do bitmap especificado.

### <a name="overload-list"></a>Lista de sobrecargas



| Método                                                                                                                                                                                                                                                               | Descrição                                                                                                                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateBitmapBrush(ID2D1Bitmap,D2D1 \* \_ BITMAP \_ BRUSH PROPERTIES \_&,D2D1 \_ BRUSH PROPERTIES \_&,ID2D1BitmapBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties_id2d1bitmap))   | Cria um [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) do bitmap especificado.<br/>                                                                                                    |
| [**CreateBitmapBrush(ID2D1Bitmap, \* D2D1 \_ BITMAP \_ BRUSH PROPERTIES \_ \* ,D2D1 \_ BRUSH PROPERTIES \_ \* ,ID2D1BitmapBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapbrush(id2d1bitmap_constd2d1_bitmap_brush_properties_constd2d1_brush_properties_id2d1bitmapbrush)) | Cria um [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) do bitmap especificado.<br/>                                                                                                    |
| [**CreateBitmapBrush(ID2D1Bitmap, \* ID2D1BitmapBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapbrush(id2d1bitmap_id2d1bitmapbrush))                                                                                                                        | Cria um [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) do bitmap especificado. O pincel usa os valores padrão para seu modo de extensão, modo de interpolação, opacidade e transformação.<br/> |
| [**CreateBitmapBrush(ID2D1Bitmap, \* D2D1 \_ BITMAP \_ BRUSH PROPERTIES \_&,ID2D1BitmapBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapbrush(id2d1bitmap_constd2d1_bitmap_brush_properties__id2d1bitmapbrush))                                                      | Cria um [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) do bitmap especificado. O pincel usa os valores padrão para sua opacidade e transformação.<br/>                                   |



## <a name="examples"></a>Exemplos

Para ver um exemplo mostrando como pintar uma área com um pincel de bitmap, consulte [How to Create a Bitmap Brush](how-to-create-a-bitmap-brush.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>D2d1.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[Como criar um pincel de bitmap](how-to-create-a-bitmap-brush.md)
</dt> <dt>

[Visão geral de pincéis](direct2d-brushes-overview.md)
</dt> </dl>

 

