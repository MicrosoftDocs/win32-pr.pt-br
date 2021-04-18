---
title: Métodos ID2D1RenderTarget FillOpacityMask
description: Aplica a máscara de opacidade descrita pelo bitmap especificado a um pincel e usa esse pincel para pintar uma região do destino de renderização.
ms.assetid: a5e56d8a-2929-4f7b-b1c4-fb358c202721
keywords:
- Métodos FillOpacityMask Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: e988994b849c193725dfdd75773f22a63fed6754
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749277"
---
# <a name="id2d1rendertargetfillopacitymask-methods"></a>Métodos ID2D1RenderTarget:: FillOpacityMask

Aplica a máscara de opacidade descrita pelo bitmap especificado a um pincel e usa esse pincel para pintar uma região do destino de renderização.

### <a name="overload-list"></a>Lista de sobrecargas



| Método                                                                                                                                                                                                                          | Descrição                                                                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [**FillOpacityMask (ID2D1Bitmap \* , ID2D1Brush \* , d2d1 \_ OPACITY \_ \_ CONTENT, D2D \_ Rect \_ f&, D2D \_ Rect \_ f&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_))       | Aplica a máscara de opacidade descrita pelo bitmap especificado a um pincel e usa esse pincel para pintar uma região do destino de renderização. <br/> |
| [**FillOpacityMask (ID2D1Bitmap \* , ID2D1Brush \* , d2d1 \_ de \_ máscara de opacidade \_ , D2D \_ Rect f \_ \* , D2D \_ Rect \_ f \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f_constd2d1_rect_f)) | Aplica a máscara de opacidade descrita pelo bitmap especificado a um pincel e usa esse pincel para pintar uma região do destino de renderização. <br/> |



## <a name="remarks"></a>Comentários

Para que esse método funcione corretamente, o destino de renderização deve usar o modo de anti-aliasing com [**\_ \_ \_ ALIAS do modo AntiAlias d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_antialias_mode) . Você pode definir o modo de suavização chamando o método [**ID2D1RenderTarget:: SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) .

Esse método não retornará um código de erro se ele falhar. Para determinar se uma operação de desenho (como **FillOpacityMask**) falhou, verifique o resultado retornado pelos métodos [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) ou [**ID2D1RenderTarget:: flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

 

