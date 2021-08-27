---
title: Métodos ID2D1SvgElement GetAttributeValue
description: Obtém um atributo desse elemento.
ms.assetid: 2f6ca40a-6c78-9c60-c06a-a31f6edf7663
keywords:
- Métodos GetAttributeValue Direct2D
topic_type:
- apiref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
api_location: ''
ms.openlocfilehash: cfc85f2af132c52a95f196aa6e0722b4d75ccc9bc8a4b7a1abb992cc581a6f32
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076846"
---
# <a name="id2d1svgelementgetattributevalue-methods"></a>Métodos ID2D1SvgElement::GetAttributeValue

Obtém um atributo desse elemento.

### <a name="overload-list"></a>Lista de sobrecargas



| Método                                                                                                                     | Descrição                                                                                                                                                 |
|:---------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetAttributeValue(PCWSTR, FLOAT \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_float))                                         | Obtém um atributo desse elemento como um float.<br/>                                                                                                    |
| [**GetAttributeValue(PCWSTR, D2D1 \_ COLOR \_ F \* )**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)                                | Obtém um atributo desse elemento como uma cor.<br/>                                                                                                    |
| [**GetAttributeValue(PCWSTR, REFIID, void \* \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_refiid_void))                                | Obtém um atributo desse elemento como um tipo de interface. <br/>                                                                                         |
| [**GetAttributeValue(PCWSTR, D2D1 \_ FILL \_ MODE \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_fill_mode))                              | Obtém um atributo desse elemento como um modo de preenchimento. Esse método pode ser usado para obter o valor das propriedades de regra de preenchimento ou regra de clipe.<br/>             |
| [**GetAttributeValue(PCWSTR, ID2D1SvgPaint \* \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_id2d1svgpaint))                              | Obtém um atributo desse elemento como uma pintura. Esse método pode ser usado para obter o valor das propriedades de preenchimento ou traço.<br/>                         |
| [**GetAttributeValue(PCWSTR, D2D1 \_ SVG \_ LENGTH \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_length))                            | Obtém um atributo desse elemento como um valor de comprimento.<br/>                                                                                             |
| [**GetAttributeValue(PCWSTR, D2D1 \_ SVG \_ DISPLAY \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_display))                            | Obtém um atributo desse elemento como um valor de exibição. Esse método pode ser usado para obter o valor da propriedade de exibição.<br/>                          |
| [**GetAttributeValue(PCWSTR, D2D1 \_ EXTEND \_ MODE \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_extend_mode))                           | Obtém um atributo desse elemento como um valor de modo de extensão. Esse método pode ser usado para obter o valor de um atributo spreadMethod.<br/>                  |
| [**GetAttributeValue(PCWSTR, D2D1 \_ SVG \_ OVERFLOW \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_overflow))                           | Obtém um atributo desse elemento como um valor de estouro. Esse método pode ser usado para obter o valor da propriedade overflow.<br/>                       |
| [**GetAttributeValue(PCWSTR, D2D1 \_ SVG \_ LINE \_ CAP \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_line_cap))                         | Obtém um atributo desse elemento como um valor de limite de linha. Esse método pode ser usado para obter o valor da propriedade stroke-linecap.<br/>                  |
| [**GetAttributeValue(PCWSTR, D2D1 \_ MATRIX \_ 3X2 \_ F \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_matrix_3x2_f))                         | Obtém um atributo desse elemento como um valor de matriz. Esse método pode ser usado para obter o valor de um atributo transform ou gradientTransform.<br/>     |
| [**GetAttributeValue(PCWSTR, ID2D1SvgPathData \* \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_id2d1svgpathdata))                           | Obtém um atributo desse elemento como dados de caminho. Esse método pode ser usado para obter o valor do atributo d em um elemento path.<br/>                   |
| [**GetAttributeValue(PCWSTR, D2D1 \_ SVG \_ LINE \_ JOIN \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_line_join))                         | Obtém um atributo desse elemento como um valor de junção de linha. Esse método pode ser usado para obter o valor da propriedade stroke-linejoin.<br/>                |
| [**GetAttributeValue(PCWSTR, D2D1 \_ SVG \_ UNIT \_ TYPE \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_unit_type))                        | Obtém um atributo desse elemento como um valor de tipo de unidade. Esse método pode ser usado para obter o valor de um atributo gradientUnits ou clipPathUnits.<br/>  |
| [**GetAttributeValue(PCWSTR, ID2D1SvgAttribute \* \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_id2d1svgattribute))                          | Obtém um atributo desse elemento.<br/>                                                                                                               |
| [**GetAttributeValue(PCWSTR, D2D1 \_ SVG \_ VISIBILITY \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_visibility))                        | Obtém um atributo desse elemento como um valor de visibilidade. Esse método pode ser usado para obter o valor da propriedade de visibilidade.<br/>                    |
| [**GetAttributeValue(PCWSTR, ID2D1SvgRakkeDashArray \* \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_id2d1svgstrokedasharray))                    | Obtém um atributo desse elemento como uma matriz de traços de traço. Esse método pode ser usado para obter o valor da propriedade stroke-dasharray.<br/>             |
| [**GetAttributeValue(PCWSTR, ID2D1SvgPointCollection \* \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_id2d1svgpointcollection))                    | Obtém um atributo desse elemento como pontos. Esse método pode ser usado para obter o valor do atributo points em um elemento de polígono ou polilinha.<br/>  |
| [**GetAttributeValue(PCWSTR, D2D1 \_ SVG \_ PRESERVE ASPECT RATIO \_ \_ \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_preserve_aspect_ratio))           | Obtém um atributo desse elemento como um valor de proporção de preservação. Esse método pode ser usado para obter o valor de um atributo preserveAspectRatio.<br/> |
| [**GetAttributeValue(PCWSTR, D2D1 \_ SVG \_ ATTRIBUTE \_ POD \_ TYPE, void \* , UINT32)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_attribute_pod_type_void_uint32)) | Obtém um atributo desse elemento como um tipo POD.<br/>                                                                                                 |
| [**GetAttributeValue(PCWSTR, D2D1 \_ SVG \_ ATTRIBUTE \_ STRING \_ TYPE, PWSTR, UINT32)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_color_f))  | Obtém um atributo desse elemento como uma cadeia de caracteres. <br/>                                                                                                  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ID2D1SvgElement**](/windows/win32/api/d2d1svg/nn-d2d1svg-id2d1svgelement)
</dt> </dl>

 

