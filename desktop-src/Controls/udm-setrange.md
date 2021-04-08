---
title: Mensagem de UDM_SETRANGE (commctrl. h)
description: Define as posições mínima e máxima (intervalo) para um controle de cima para baixo.
ms.assetid: 81875528-86cc-419a-a07c-f4f98baf1462
keywords:
- Controles de UDM_SETRANGE de mensagens do Windows
topic_type:
- apiref
api_name:
- UDM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb32a72ca8ca5182e87e2c0346cbc44ab25300e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009547"
---
# <a name="udm_setrange-message"></a>Mensagem do UDM \_ SETRANGE

Define as posições mínima e máxima (intervalo) para um controle de cima para baixo.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) é um **curto** que especifica a posição máxima para o controle de cima para baixo e o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) é um **curto** que especifica a posição mínima. Nenhuma posição pode ser maior que o \_ valor de maxVal UD ou menor que o \_ valor de minVal UD. Além disso, a diferença entre as duas posições não pode exceder UD \_ maxVal.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

A posição máxima pode ser menor que a posição mínima. Clicar no botão de seta para cima move a posição atual para mais perto da posição máxima e, ao clicar no botão de seta para baixo, move-se para a posição mínima.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MAKELPARAM**](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> <dt>

[**SETRANGE de UDM \_**](udm-setrange.md)
</dt> </dl>

 

