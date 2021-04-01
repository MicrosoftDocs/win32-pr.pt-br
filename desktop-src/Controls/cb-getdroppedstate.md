---
title: Mensagem de CB_GETDROPPEDSTATE (WinUser. h)
description: Determina se a caixa de listagem de uma caixa de combinação é descartada.
ms.assetid: a3f4e352-298d-45ea-a5a7-007f1fc1a387
keywords:
- Controles de CB_GETDROPPEDSTATE de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_GETDROPPEDSTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ae321bbaa3078a04ffc97d4a8083a674d03d651
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009782"
---
# <a name="cb_getdroppedstate-message"></a>Mensagem do CB \_ GETremovestate

Determina se a caixa de listagem de uma caixa de combinação é descartada.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a caixa de listagem estiver visível, o valor de retorno será **true**; caso contrário, será **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_menu suspenso de CB**](cb-showdropdown.md)
</dt> </dl>

 

 





