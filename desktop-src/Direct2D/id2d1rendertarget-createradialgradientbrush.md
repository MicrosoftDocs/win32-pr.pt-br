---
title: Métodos ID2D1RenderTarget CreateRadialGradientBrush (D2d1.h)
description: Cria um objeto ID2D1RadialGradientBrush que pode ser usado para pintar áreas com um gradiente radial.
ms.assetid: 985a4c1b-d29b-46ed-bc55-6dcd313718a8
keywords:
- Métodos CreateRadialGradientBrush Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: b32c384e55f8c6ac17551c290c36e1130c05d5939fd5cf56116410ddac37320f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108816"
---
# <a name="id2d1rendertargetcreateradialgradientbrush-methods"></a>Métodos ID2D1RenderTarget::CreateRadialGradientBrush

Cria um [**objeto ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) que pode ser usado para pintar áreas com um gradiente radial.

### <a name="overload-list"></a>Lista de sobrecargas



| Método                                                                                                                                                                                                                       | Descrição                                                                                                                                                                      |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateRadialGradientBrush(D2D1 \_ RADIAL GRADIENT BRUSH PROPERTIES \_ \_ \_&,ID2D1GradientStopCollection \* , ID2D1RadialGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush))                            | Cria [**um ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) que contém as paradas de gradiente especificadas, não tem nenhuma transformação e tem uma opacidade base de 1.0. <br/> |
| [**CreateRadialGradientBrush(D2D1 \_ RADIAL GRADIENT BRUSH PROPERTIES \_ \_ \_&,D2D1 \_ BRUSH PROPERTIES \_&,ID2D1GradientStopCollection \* ,ID2D1RadialGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush))   | Cria [**um ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) que contém as paradas de gradiente especificadas e tem a transformação e a opacidade base especificadas. <br/> |
| [**CreateRadialGradientBrush(D2D1 \_ RADIAL GRADIENT BRUSH PROPERTIES \_ \_ \_ \* ,D2D1 \_ BRUSH PROPERTIES \_ \* ,ID2D1GradientStopCollection \* , ID2D1RadialGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush)) | Cria [**um ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) que contém as paradas de gradiente especificadas e tem a transformação e a opacidade base especificadas. <br/> |



## <a name="examples"></a>Exemplos

Para ver um exemplo, [consulte How to Create a Radial Gradient Brush](how-to-create-a-radial-gradient-brush.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D2d1.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D2d1.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[Como criar um pincel de gradiente radial](how-to-create-a-radial-gradient-brush.md)
</dt> <dt>

[Visão geral de pincéis](direct2d-brushes-overview.md)
</dt> </dl>

�

�
