---
title: Mensagem de CB_SETEDITSEL (WinUser. h)
description: Um aplicativo envia uma \_ mensagem de SETEDITSEL CB para selecionar caracteres no controle de edição de uma caixa de combinação.
ms.assetid: 25a07341-a21c-42a9-a220-62650997757b
keywords:
- Controles de CB_SETEDITSEL de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_SETEDITSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a54e09697e266b4e0c4260104e90f454a5e3edfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455118"
---
# <a name="cb_seteditsel-message"></a>\_Mensagem de SETEDITSEL CB

Um aplicativo envia uma mensagem de **\_ SETEDITSEL CB** para selecionar caracteres no controle de edição de uma caixa de combinação.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> <dt>

*lParam* \[ no\]
</dt> <dd>

O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) de *lParam* especifica a posição inicial. Se **LOWORD** for-1, a seleção, se houver, será removida.

O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) de *lParam* especifica a posição final. Se **HIWORD** for-1, todo o texto da posição inicial para o último caractere no controle de edição será selecionado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a mensagem tiver sucesso, o valor de retorno será **true**. Se a mensagem for enviada para uma caixa de combinação com o estilo do [**CBS \_ DROPDOWNLIST**](combo-box-styles.md) , será CB \_ Err.

## <a name="remarks"></a>Comentários

As posições são baseadas em zero. O primeiro caractere do controle de edição está na posição zero. O primeiro caractere após o último caractere selecionado está na posição final. Por exemplo, para selecionar os quatro primeiros caracteres do controle de edição, use uma posição inicial de 0 e uma posição final de 4.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**\_GETEDITSEL CB**](cb-geteditsel.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**MAKELPARAM**](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> </dl>

 

