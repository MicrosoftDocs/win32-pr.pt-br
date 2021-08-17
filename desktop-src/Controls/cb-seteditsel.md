---
title: CB_SETEDITSEL mensagem (Winuser.h)
description: Um aplicativo envia uma mensagem CB SETEDITSEL para selecionar caracteres \_ no controle de edição de uma caixa de combinação.
ms.assetid: 25a07341-a21c-42a9-a220-62650997757b
keywords:
- CB_SETEDITSEL controles Windows mensagem
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
ms.openlocfilehash: 0e8deb133559332ea8f727758086e19cb17483b4c343f8b3f8f1a3694911eedd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117832263"
---
# <a name="cb_seteditsel-message"></a>Mensagem CB \_ SETEDITSEL

Um aplicativo envia uma **mensagem CB \_ SETEDITSEL** para selecionar caracteres no controle de edição de uma caixa de combinação.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> <dt>

*lParam* \[ Em\]
</dt> <dd>

A [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) de *lParam* especifica a posição inicial. Se o **LOWORD** for -1, a seleção, se for, será removida.

A [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) de *lParam* especifica a posição final. Se **HIWORD for** -1, todo o texto da posição inicial para o último caractere no controle de edição será selecionado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a mensagem for bem-sucedida, o valor de retorno será **TRUE.** Se a mensagem for enviada para uma caixa de combinação com o estilo [**CBS \_ DROPDOWNLIST,**](combo-box-styles.md) ela será CB \_ ERR.

## <a name="remarks"></a>Comentários

As posições são baseadas em zero. O primeiro caractere do controle de edição está na posição zero. O primeiro caractere após o último caractere selecionado está na posição final. Por exemplo, para selecionar os quatro primeiros caracteres do controle de edição, use uma posição inicial de 0 e uma posição final de 4.

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

[**CB \_ GETEDITSEL**](cb-geteditsel.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**MAKELPARAM**](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> </dl>

 

