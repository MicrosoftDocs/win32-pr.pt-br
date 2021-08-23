---
title: Métodos ID2D1SvgElement SetAttributeValue (D2d1svg.h)
description: Define um atributo desse elemento.
ms.assetid: 33403a07-28d1-4138-ea7f-04f3ac42a8f7
keywords:
- Métodos SetAttributeValue Direct2D
topic_type:
- apiref
api_location:
- d2d1svg.h
api_type:
- HeaderDef
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 95ac3021abdf641b268e2278e92dfd86227244cde1d1d51f992953e68584fa69
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119527136"
---
# <a name="id2d1svgelementsetattributevalue-methods"></a>Métodos ID2D1SvgElement::SetAttributeValue

Define um atributo desse elemento.

### <a name="overload-list"></a>Lista de sobrecargas



| Método                                                                                                                      | Descrição                                                                                                                                                 |
|:----------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SetAttributeValue(PCWSTR, FLOAT)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_float))                                             | Define um atributo desse elemento usando um float.<br/>                                                                                                 |
| [**SetAttributeValue(PCWSTR, D2D1 \_ COLOR \_ F &)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_constd2d1_color_f_))                                  | Define um atributo desse elemento como uma cor.<br/>                                                                                                    |
| [**SetAttributeValue(PCWSTR, D2D1 \_ FILL \_ MODE)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_fill_mode))                                  | Define um atributo desse elemento como um modo de preenchimento. Esse método pode ser usado para definir o valor das propriedades 'fill-rule' ou 'clip-rule'.<br/>         |
| [**SetAttributeValue(PCWSTR, D2D1 \_ SVG \_ DISPLAY)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_svg_display))                                | Obtém um atributo desse elemento como um valor de exibição. Esse método pode ser usado para obter o valor da propriedade de exibição.<br/>                          |
| [**SetAttributeValue(PCWSTR, D2D1 \_ EXTEND \_ MODE)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_extend_mode))                               | Define um atributo desse elemento como um valor de modo de extensão. Esse método pode ser usado para definir o valor de um atributo spreadMethod.<br/>                 |
| [**SetAttributeValue(PCWSTR, D2D1 \_ SVG \_ OVERFLOW)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_svg_overflow))                               | Define um atributo desse elemento como um valor de estouro. Esse método pode ser usado para definir o valor da propriedade overflow.<br/>                       |
| [**SetAttributeValue(PCWSTR, D2D1 \_ SVG \_ LINE \_ CAP)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_svg_line_cap))                             | Define um atributo desse elemento como um valor de limite de linha. Esse método pode ser usado para definir o valor da propriedade stroke-linecap.<br/>                  |
| [**SetAttributeValue(PCWSTR, D2D1 \_ SVG \_ LENGTH &)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_constd2d1_svg_length_))                              | Define um atributo desse elemento como um valor de comprimento.<br/>                                                                                             |
| [**SetAttributeValue(PCWSTR, D2D1 \_ SVG \_ LINE \_ JOIN)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_svg_line_join))                             | Define um atributo desse elemento como um valor de junção de linha. Esse método pode ser usado para definir o valor da propriedade stroke-linejoin.<br/>                |
| [**SetAttributeValue(PCWSTR, D2D1 \_ SVG \_ UNIT \_ TYPE)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_svg_unit_type))                            | Define um atributo desse elemento como um valor de tipo de unidade. Esse método pode ser usado para definir o valor de um atributo gradientUnits ou clipPathUnits.<br/>  |
| [**SetAttributeValue(PCWSTR, ID2D1SvgAttribute \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_id2d1svgattribute))                              | Define um atributo desse elemento usando uma interface .<br/>                                                                                            |
| [**SetAttributeValue(PCWSTR, D2D1 \_ SVG \_ VISIBILITY)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_svg_visibility))                            | Define um atributo desse elemento como um valor de visibilidade. Esse método pode ser usado para definir o valor da propriedade de visibilidade.<br/>                    |
| [**SetAttributeValue(PCWSTR, D2D1 \_ MATRIX \_ 3X2 \_ F &)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_constd2d1_matrix_3x2_f_))                           | Define um atributo desse elemento como um valor de matriz. Esse método pode ser usado para definir o valor de um atributo transform ou gradientTransform.<br/>     |
| [**SetAttributeValue(PCWSTR, D2D1 \_ SVG \_ PRESERVE ASPECT RATIO \_ \_ &)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_constd2d1_svg_preserve_aspect_ratio_))             | Define um atributo desse elemento como um valor de proporção de preservação. Esse método pode ser usado para definir o valor de um atributo preserveAspectRatio.<br/> |
| [**SetAttributeValue(PCWSTR, D2D1 \_ SVG \_ ATTRIBUTE \_ STRING \_ TYPE, PCWSTR)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_svg_attribute_string_type_pcwstr))          | Define um atributo desse elemento usando uma cadeia de caracteres. <br/>                                                                                               |
| [**SetAttributeValue(PCWSTR, D2D1 \_ SVG \_ ATTRIBUTE \_ POD \_ TYPE , void \* , UINT32)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_svg_attribute_pod_type_constvoid_uint32)) | Define um atributo desse elemento usando um tipo POD.<br/>                                                                                              |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|--------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D2d1svg.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ID2D1SvgElement**](/windows/win32/api/d2d1svg/nn-d2d1svg-id2d1svgelement)
</dt> </dl>

�

�
