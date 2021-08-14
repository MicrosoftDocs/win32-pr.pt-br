---
title: Métodos CreateLinearGradientBrush ID2D1RenderTarget (D2d1. h)
description: Cria um objeto ID2D1LinearGradientBrush para áreas de pintura com um gradiente linear.
ms.assetid: dc07113f-ff93-4b0f-8328-02dd481dccb0
keywords:
- Métodos CreateLinearGradientBrush Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 74e3ba102b24b330f176189a66eae7ac9cd74ece194900f3d8997675bf486641
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966866"
---
# <a name="id2d1rendertargetcreatelineargradientbrush-methods"></a>Métodos ID2D1RenderTarget:: CreateLinearGradientBrush

Cria um objeto [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) para áreas de pintura com um gradiente linear.

### <a name="overload-list"></a>Lista de sobrecargas



| Método                                                                                                                                                                                                                       | Descrição                                                                                                                                                                      |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateLinearGradientBrush ( \_ Propriedades de \_ pincel de gradiente LINEAR d2d1 \_ \_&, ID2D1GradientStopCollection \* , ID2D1LinearGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush))                            | Cria um [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) que contém as interrupções de gradiente especificadas, não tem transformação e tem uma opacidade base de 1,0. <br/> |
| [**CreateLinearGradientBrush (D2D1 \_ , \_ Propriedades de pincel de gradiente linear \_ \_&, \_ Propriedades de pincel d2d1 \_&, ID2D1GradientStopCollection \* , ID2D1LinearGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush))   | Cria um [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) que contém as interrupções de gradiente especificadas e tem a transformação especificada e a opacidade base. <br/> |
| [**CreateLinearGradientBrush ( \_ Propriedades de \_ pincel de gradiente linear d2d1 \_ \_ \* , \_ Propriedades de pincel d2d1 \_ \* , ID2D1GradientStopCollection \* , ID2D1LinearGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) | Cria um [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) que contém as interrupções de gradiente especificadas e tem a transformação especificada e a opacidade base. <br/> |



## <a name="examples"></a>Exemplos

Para obter um exemplo que mostra como criar uma coleção de parada de gradiente e usá-la para definir um gradiente linear, consulte [como criar um pincel de gradiente linear](how-to-create-a-linear-gradient-brush.md).

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

[**CreateGradientStopCollection**](id2d1rendertarget-creategradientstopcollection.md)
</dt> <dt>

[**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection)
</dt> <dt>

[**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)
</dt> <dt>

[**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)
</dt> <dt>

[Como criar um pincel de gradiente linear](how-to-create-a-linear-gradient-brush.md)
</dt> <dt>

[Visão geral de pincéis](direct2d-brushes-overview.md)
</dt> </dl>

�

�
