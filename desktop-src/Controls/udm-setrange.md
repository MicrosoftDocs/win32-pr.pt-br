---
title: Mensagem de UDM_SETRANGE (commctrl. h)
description: Define as posições mínima e máxima (intervalo) para um controle de cima para baixo.
ms.assetid: 81875528-86cc-419a-a07c-f4f98baf1462
keywords:
- controles de Windows de mensagem de UDM_SETRANGE
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
ms.openlocfilehash: 60499c960b7f2e496dc4317229865a8838013fc5d78c194072bee27e761ba4d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118408051"
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

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

A posição máxima pode ser menor que a posição mínima. Clicar no botão de seta para cima move a posição atual para mais perto da posição máxima e, ao clicar no botão de seta para baixo, move-se para a posição mínima.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MAKELPARAM**](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> <dt>

[**SETRANGE de UDM \_**](udm-setrange.md)
</dt> </dl>

 

