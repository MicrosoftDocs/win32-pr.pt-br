---
title: Métodos setattributevalue do ID2D1SvgElement (D2d1svg. h)
description: Define um atributo deste elemento.
ms.assetid: 33403a07-28d1-4138-ea7f-04f3ac42a8f7
keywords:
- Métodos setattributevalue Direct2D
topic_type:
- apiref
api_location:
- d2d1svg.h
api_type:
- HeaderDef
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: c49f224d364523653e13fb7b6cc141e8e8c6eca7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761780"
---
# <a name="id2d1svgelementsetattributevalue-methods"></a>Métodos ID2D1SvgElement:: setattributevalue

Define um atributo deste elemento.

### <a name="overload-list"></a>Lista de sobrecargas



| Método                                                                                                                      | Descrição                                                                                                                                                 |
|:----------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Setattributevalue (PCWSTR, FLOAT)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_float))                                             | Define um atributo desse elemento usando um float.<br/>                                                                                                 |
| [**Setattributevalue (PCWSTR, D2D1 \_ Color \_ F &)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_constd2d1_color_f_))                                  | Define um atributo desse elemento como uma cor.<br/>                                                                                                    |
| [**Setattributevalue (PCWSTR, modo de preenchimento de D2D1 \_ \_ )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_fill_mode))                                  | Define um atributo desse elemento como um modo de preenchimento. Esse método pode ser usado para definir o valor das propriedades ' Fill-Rule ' ou ' clip-Rule '.<br/>         |
| [**Setattributevalue (PCWSTR, D2D1 \_ SVG \_ Display)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_svg_display))                                | Obtém um atributo desse elemento como um valor de exibição. Esse método pode ser usado para obter o valor da propriedade Display.<br/>                          |
| [**Setattributevalue (PCWSTR, \_ modo de extensão d2d1 \_ )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_extend_mode))                               | Define um atributo desse elemento como um valor de modo de extensão. Esse método pode ser usado para definir o valor de um atributo spreadMethod.<br/>                 |
| [**Setattributevalue (PCWSTR, \_ estouro SVG de d2d1 \_ )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_svg_overflow))                               | Define um atributo desse elemento como um valor de estouro. Esse método pode ser usado para definir o valor da propriedade overflow.<br/>                       |
| [**Setattributevalue (PCWSTR, Cap D2D1 de \_ \_ linha SVG \_ )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_svg_line_cap))                             | Define um atributo desse elemento como um valor de limite de linha. Esse método pode ser usado para definir o valor da Propriedade Stroke-LineCap.<br/>                  |
| [**Setattributevalue (PCWSTR, \_ comprimento d2d1 SVG \_ &)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_constd2d1_svg_length_))                              | Define um atributo desse elemento como um valor de comprimento.<br/>                                                                                             |
| [**Setattributevalue (PCWSTR, \_ junção de \_ linha SVG d2d1 \_ )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_svg_line_join))                             | Define um atributo desse elemento como um valor de junção de linha. Esse método pode ser usado para definir o valor da Propriedade Stroke-LineJoin.<br/>                |
| [**Setattributevalue (PCWSTR, \_ tipo de \_ unidade SVG d2d1 \_ )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_svg_unit_type))                            | Define um atributo desse elemento como um valor de tipo de unidade. Esse método pode ser usado para definir o valor de um atributo gradientUnits ou clipPathUnits.<br/>  |
| [**Setattributevalue (PCWSTR, ID2D1SvgAttribute \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_id2d1svgattribute))                              | Define um atributo desse elemento usando uma interface.<br/>                                                                                            |
| [**Setattributevalue (PCWSTR, visibilidade de D2D1 \_ SVG \_ )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_svg_visibility))                            | Define um atributo desse elemento como um valor de visibilidade. Esse método pode ser usado para definir o valor da propriedade Visibility.<br/>                    |
| [**Setattributevalue (PCWSTR, \_ matriz d2d1 \_ 3X2 \_ F &)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_constd2d1_matrix_3x2_f_))                           | Define um atributo desse elemento como um valor de matriz. Esse método pode ser usado para definir o valor de um atributo Transform ou gradientTransform.<br/>     |
| [**Setattributevalue (PCWSTR, D2D1 \_ SVG \_ preservar \_ taxa de proporção \_ &)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_constd2d1_svg_preserve_aspect_ratio_))             | Define um atributo desse elemento como um valor de taxa de proporção de preservação. Esse método pode ser usado para definir o valor de um atributo preserveAspectRatio.<br/> |
| [**Setattributevalue (PCWSTR, \_ tipo de cadeia de caracteres de atributo SVG d2d1 \_ \_ \_ , PCWSTR)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_svg_attribute_string_type_pcwstr))          | Define um atributo desse elemento usando uma cadeia de caracteres. <br/>                                                                                               |
| [**Setattributevalue (PCWSTR, \_ tipo de pod de atributo SVG d2d1 \_ \_ \_ , void \* , UINT32)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_svg_attribute_pod_type_constvoid_uint32)) | Define um atributo desse elemento usando um tipo de POD.<br/>                                                                                              |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|--------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D2d1svg. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ID2D1SvgElement**](/windows/win32/api/d2d1svg/nn-d2d1svg-id2d1svgelement)
</dt> </dl>

�

�
