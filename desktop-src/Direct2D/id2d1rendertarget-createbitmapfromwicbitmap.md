---
title: Métodos ID2D1RenderTarget CreateBitmapFromWicBitmap
description: Cria um ID2D1Bitmap copiando o bitmap do Microsoft Windows Imaging Component (WIC) especificado.
ms.assetid: 463fc2f9-8ec6-47e8-8d48-a9015616e656
keywords:
- Métodos CreateBitmapFromWicBitmap Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 23ad055beab9f24c39f032a3e28456c231480c68
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105775645"
---
# <a name="id2d1rendertargetcreatebitmapfromwicbitmap-methods"></a>Métodos ID2D1RenderTarget:: CreateBitmapFromWicBitmap

Cria um [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) copiando o bitmap do Microsoft Windows Imaging Component (WIC) especificado.

### <a name="overload-list"></a>Lista de sobrecargas



| Método                                                                                                                                                                                                              | Descrição                                                                                                                         |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateBitmapFromWicBitmap (IWICBitmapSource \* , ID2D1Bitmap \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapfromwicbitmap(iwicbitmapsource_id2d1bitmap))                                                       | Cria um [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) copiando o bitmap do Microsoft Windows Imaging Component (WIC) especificado.<br/>  |
| [**CreateBitmapFromWicBitmap (IWICBitmapSource \* , \_ Propriedades de BITMAP d2d1 \_&, ID2D1Bitmap \* \* )**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties1__id2d1bitmap1))  | Cria um [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) copiando o bitmap do Microsoft Windows Imaging Component (WIC) especificado.<br/> |
| [**CreateBitmapFromWicBitmap (IWICBitmapSource \* , \_ Propriedades de bitmap d2d1 \_ \* , ID2D1Bitmap \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties_id2d1bitmap)) | Cria um [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) copiando o bitmap do Microsoft Windows Imaging Component (WIC) especificado.<br/> |



## <a name="remarks"></a>Comentários

Antes que Direct2D possa carregar uma imagem de WIC, ela deve ser convertida em um formato de pixel e modo alfa com suporte. Para obter uma lista de formatos de pixel e modos alfa com suporte, consulte [formatos de pixel com suporte e modos alfa](supported-pixel-formats-and-alpha-modes.md).

## <a name="examples"></a>Exemplos

Para obter exemplos, consulte [como carregar um bitmap de um arquivo](how-to-load-a-direct2d-bitmap-from-a-file.md) e [como carregar um bitmap de um recurso](how-to-load-a-bitmap-from-a-resource.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)
</dt> <dt>

[Como carregar um bitmap de um arquivo](how-to-load-a-direct2d-bitmap-from-a-file.md)
</dt> <dt>

[Formatos de pixel e modos alfa com suporte](supported-pixel-formats-and-alpha-modes.md)
</dt> </dl>

 

