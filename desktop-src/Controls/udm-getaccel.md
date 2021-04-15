---
title: Mensagem de UDM_GETACCEL (commctrl. h)
description: Recupera informações de aceleração para um controle de cima para baixo.
ms.assetid: 794538d6-ca01-4f05-82d1-ce7bc0f76f64
keywords:
- Controles de UDM_GETACCEL de mensagens do Windows
topic_type:
- apiref
api_name:
- UDM_GETACCEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b86a9740e59631b737453763a10ccb9820056d95
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454819"
---
# <a name="udm_getaccel-message"></a>\_Mensagem de GETACCEL UDM

Recupera informações de aceleração para um controle de cima para baixo.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Número de elementos na matriz especificada por *lParam*.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma matriz de estruturas [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) que recebem informações de aceleração.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é o número de aceleradores definidos atualmente para o controle.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_SETACCEL UDM**](udm-setaccel.md)
</dt> </dl>

 

 





