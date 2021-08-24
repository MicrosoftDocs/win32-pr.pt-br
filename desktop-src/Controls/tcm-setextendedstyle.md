---
title: TCM_SETEXTENDEDSTYLE mensagem (Commctrl.h)
description: Define os estilos estendidos que o controle de tabulação usará. Você pode enviar essa mensagem explicitamente ou usando a macro TabCtrl \_ SetExtendedStyle.
ms.assetid: 96ccebe1-2836-4198-8cd7-858401562c21
keywords:
- TCM_SETEXTENDEDSTYLE controles Windows mensagem
topic_type:
- apiref
api_name:
- TCM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a4a28bcf4cffe9aa2559f96a990d23511ece9fbbfc65468f84a4a874dce678a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876446"
---
# <a name="tcm_setextendedstyle-message"></a>Mensagem TCM \_ SETEXTENDEDSTYLE

Define os estilos estendidos que o controle de tabulação usará. Você pode enviar essa mensagem explicitamente ou usando a [**macro TabCtrl \_ SetExtendedStyle.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setextendedstyle)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um **valor DWORD** que indica quais estilos em *lParam* devem ser afetados. Somente os estilos estendidos *no wParam* serão alterados. Todos os outros estilos serão mantidos como estão. Se esse parâmetro for zero, todos os estilos em *lParam* serão afetados.

</dd> <dt>

*lParam* 
</dt> <dd>

Valor que especifica os estilos de controle de tabulação estendidos. Esse valor é uma combinação de estilos estendidos de controle [de tabulação](tab-control-extended-styles.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor DWORD** que contém os estilos estendidos do controle de tabulação anterior.

## <a name="remarks"></a>Comentários

O *parâmetro wParam* permite modificar um ou mais estilos estendidos sem precisar recuperar os estilos existentes primeiro. Por exemplo, se você passar [**TCS \_ EX \_ FLATSEPARATORS**](tab-control-extended-styles.md) para *wParam* e 0 para *lParam*, o estilo **TCS \_ EX \_ FLATSEPARATORS** será limpo, mas todos os outros estilos permanecerão os mesmos.

Por motivos de compatibilidade com variáveis, a macro [**\_ TabCtrl SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setextendedstyle) não foi atualizada para usar *dwExMask.*

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TCM \_ GETEXTENDEDSTYLE**](tcm-getextendedstyle.md)
</dt> </dl>

 

 





