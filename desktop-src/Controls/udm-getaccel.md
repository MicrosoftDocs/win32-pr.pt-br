---
title: UDM_GETACCEL mensagem (Commctrl.h)
description: Recupera informações de aceleração para um controle up-down.
ms.assetid: 794538d6-ca01-4f05-82d1-ce7bc0f76f64
keywords:
- UDM_GETACCEL controles de Windows mensagem
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
ms.openlocfilehash: 3603f364a6caa4f4726460e4b5b71e0d79564fbe9178414576fbed2ce5f5777d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120132186"
---
# <a name="udm_getaccel-message"></a>Mensagem GETACCEL do UDM \_

Recupera informações de aceleração para um controle up-down.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Número de elementos na matriz especificada por *lParam*.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma matriz de [**estruturas UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) que recebem informações de aceleração.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é o número de aceleradores atualmente definidos para o controle.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**UDM \_ SETACCEL**](udm-setaccel.md)
</dt> </dl>

 

 





