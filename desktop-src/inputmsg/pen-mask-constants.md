---
title: Máscara de caneta
description: Valores que podem aparecer no campo penMask da estrutura POINTER_PEN_INFO dados.
ms.assetid: 6A44B701-55E1-41D4-9C4A-807E57441DA4
topic_type:
- apiref
api_name:
- PEN_MASK_NONE
- PEN_MASK_PRESSURE
- PEN_MASK_ROTATION
- PEN_MASK_TILT_X
- PEN_MASK_TILT_Y
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: f8b44787dd1039bd3ffd3fa9afef76a527e2143cfe52bdcfa7676c15efa51342
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119666107"
---
# <a name="pen-mask"></a>Máscara de caneta

Valores que podem aparecer no campo **penMask** da [**estrutura POINTER_PEN_INFO.**](/previous-versions/windows/desktop/api)

<dl> <dt>

<span id="PEN_MASK_NONE"></span><span id="pen_mask_none"></span>**PEN_MASK_NONE**
</dt> <dd> <dl> <dt>

0x00000000
</dt> <dt>



Padrão. Nenhum dos campos opcionais é válido.


</dt> </dl> </dd> <dt>

<span id="PEN_MASK_PRESSURE"></span><span id="pen_mask_pressure"></span>**PEN_MASK_PRESSURE**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



**A** pressão da [**estrutura POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) é válida.


</dt> </dl> </dd> <dt>

<span id="PEN_MASK_ROTATION"></span><span id="pen_mask_rotation"></span>**PEN_MASK_ROTATION**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



**rotação** da [**estrutura POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) é válida.


</dt> </dl> </dd> <dt>

<span id="PEN_MASK_TILT_X____"></span><span id="pen_mask_tilt_x____"></span>**PEN_MASK_TILT_X** 
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



**OtexX** da [**estrutura POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) é válida.


</dt> </dl> </dd> <dt>

<span id="PEN_MASK_TILT_Y"></span><span id="pen_mask_tilt_y"></span>**PEN_MASK_TILT_Y**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



**O meio-dia** da [**estrutura POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) é válida.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes](constants.md)
</dt> <dt>

[**POINTER_INFO**](/previous-versions/windows/desktop/api)
</dt> </dl>

 

 





