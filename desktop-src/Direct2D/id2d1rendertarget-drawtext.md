---
title: Métodos DrawText ID2D1RenderTarget
description: Desenha o texto especificado usando as informações de formato fornecidas por um objeto IDWriteTextFormat.
ms.assetid: 7cda7854-f9df-48d3-bc62-6aaee769e6f9
keywords:
- Métodos DrawText Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 430607b09795be249a05398b1bfb749e9be45ae517c6374e001a4c3042bf316f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874186"
---
# <a name="id2d1rendertargetdrawtext-methods"></a>Métodos ID2D1RenderTarget::D rawText

Desenha o texto especificado usando as informações de formato fornecidas por [**um objeto IDWriteTextFormat.**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat)

### <a name="overload-list"></a>Lista de sobrecargas



| Método                                                                                                                                                                                                                                                                               | Descrição                                                                                                                                     |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DrawText(WCHAR, \* IDWriteTextFormat, \* D2D1 \_ RECT \_ F&,ID2D1Brush \* ,D2D1 OPÇÕES DE TEXTO DE DESENHO, MÉTODO DE MEDIÇÃO \_ DE TEXTO \_ \_ DWRITE) \_ \_ \_**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))  | Desenha o texto especificado usando as informações de formato fornecidas por [**um objeto IDWriteTextFormat.**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat)<br/>  |
| [**DrawText(WCHAR, \* IDWriteTextFormat, \* D2D1 \_ RECT \_ \* F, ID2D1Brush \* , D2D1 \_ OPÇÕES \_ \_ \_ \_ \_ DE TEXTO DE DESENHO, MÉTODO DE MEDIÇÃO DE TEXTO DWRITE)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f_id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) | Desenha o texto especificado usando as informações de formato fornecidas por [**um objeto IDWriteTextFormat.**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) <br/> |



## <a name="remarks"></a>Comentários

Para desenhar texto com Direct2D, use o método [**ID2D1RenderTarget::D rawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) para texto que tenha um único formato ou o método [**ID2D1RenderTarget::D rawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) quando precisar de vários formatos, recursos avançados do OpenType ou testes de acerto. Esses métodos usam a API DirectWrite para fornecer exibição de texto de alta qualidade.

Esse método não retornará um código de erro se ele falhar. Para determinar se uma operação de desenho (como **DrawText**) falhou, verifique o resultado retornado pelos métodos [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) ou [**ID2D1RenderTarget::Flush.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush)

## <a name="examples"></a>Exemplos

Para ver um exemplo, [consulte Como desenhar texto.](how-to--draw-text.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>D2d1.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat)
</dt> <dt>

[Como desenhar texto](how-to--draw-text.md)
</dt> <dt>

[Formatação de texto e visão geral de layout](/windows/desktop/DirectWrite/text-formatting-and-layout)
</dt> </dl>

 

