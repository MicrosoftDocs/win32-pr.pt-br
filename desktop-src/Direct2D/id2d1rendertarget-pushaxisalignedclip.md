---
title: Métodos ID2D1RenderTarget PushAxisAlignedClip (D2d1 \_ 1. h)
description: Especifica um retângulo para o qual todas as operações de desenho subsequentes são recortadas.
ms.assetid: 8b777425-07b1-4494-889a-0c947fb61315
keywords:
- Direct2D métodos de PushAxisAlignedClip
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 3ce76db0608ccd79ecd8ea1be716f8cbdf4313f95bfdda9cfac7b63474e3f412
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873986"
---
# <a name="id2d1rendertargetpushaxisalignedclip-methods"></a>ID2D1RenderTarget: métodos de ushAxisAlignedClip de:P

Especifica um retângulo para o qual todas as operações de desenho subsequentes são recortadas.

### <a name="overload-list"></a>Lista de sobrecargas



| Método                                                                                                                                         | Descrição                                                                               |
|:-----------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [**PushAxisAlignedClip (D2D1 \_ Rect \_ F&, d2d1 \_ modo AntiAlias \_ )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))  | Especifica um retângulo para o qual todas as operações de desenho subsequentes são recortadas. <br/> |
| [**PushAxisAlignedClip (D2D1 \_ Rect \_ F \* , d2d1 \_ modo AntiAlias \_ )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) | Especifica um retângulo para o qual todas as operações de desenho subsequentes são recortadas. <br/> |



## <a name="remarks"></a>Comentários

Um par [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) e [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) pode ocorrer ao contrário ou dentro de um [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) e [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer), mas não pode se sobrepor. Por exemplo, a sequência de **PushAxisAlignedClip**, [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)), **PopLayer**, **PopAxisAlignedClip** é válida, mas a sequência de **PushAxisAlignedClip**, **PushLayer**, **PopAxisAlignedClip**, **PopLayer** é inválida.

Esse método não retornará um código de erro se ele falhar. Para determinar se uma operação de desenho (como **PushAxisAlignedClip**) falhou, verifique o resultado retornado pelos métodos [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) ou [**ID2D1RenderTarget:: flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .

## <a name="examples"></a>Exemplos

Para obter um exemplo, consulte [como recortar com um Axis-Aligned clip Rectangle](how-to-clip-with-axis-aligned-rects.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D2d1 \_ 1. h (inclui D2d1. h)</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D2d1. lib</dt> </dl>                   |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl>                   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

�

�
