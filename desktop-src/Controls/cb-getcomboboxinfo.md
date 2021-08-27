---
title: CB_GETCOMBOBOXINFO mensagem (Winuser.h)
description: Obtém informações sobre a caixa de combinação especificada.
ms.assetid: 3239dfa8-7301-48e3-ba8e-29c5d5f43b39
keywords:
- CB_GETCOMBOBOXINFO controles Windows mensagem
topic_type:
- apiref
api_name:
- CB_GETCOMBOBOXINFO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ce6227df0031c01b15892daa14eea9cc8d25bd2c7eede68af275063d7201505
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089286"
---
# <a name="cb_getcomboboxinfo-message"></a>Mensagem \_ CB GETCOMBOBOXINFO

Obtém informações sobre a caixa de combinação especificada.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> <dt>

*lParam* \[ out\]
</dt> <dd>

Um ponteiro para uma [**estrutura COMBOBOXINFO**](/windows/win32/api/winuser/ns-winuser-comboboxinfo) que recebe as informações.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor retornado será diferente de zero.

Se a função falhar, o valor retornado será zero. Para obter informações de erro estendidas, chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentários

Essa mensagem é equivalente a [**GetComboBoxInfo.**](/windows/desktop/api/Winuser/nf-winuser-getcomboboxinfo)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**COMBOBOXINFO**](/windows/win32/api/winuser/ns-winuser-comboboxinfo)
</dt> <dt>

[**GetComboBoxInfo**](/windows/desktop/api/Winuser/nf-winuser-getcomboboxinfo)
</dt> </dl>

 

