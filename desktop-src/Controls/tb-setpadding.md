---
title: Mensagem de TB_SETPADDING (commctrl. h)
description: Define o preenchimento de um controle ToolBar.
ms.assetid: a18c4efb-1140-4149-8dce-dfc1f03bb61a
keywords:
- Controles de TB_SETPADDING de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_SETPADDING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65fae53f7e7702528915af7631bd675f11188b71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086246"
---
# <a name="tb_setpadding-message"></a>\_Mensagem SETpadding de TB

Define o preenchimento de um controle ToolBar.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica o preenchimento horizontal, em pixels. O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o preenchimento vertical, em pixels.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **DWORD** que contém o preenchimento horizontal anterior no [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) e o preenchimento vertical anterior no [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)), em pixels.

## <a name="remarks"></a>Comentários

Os valores de preenchimento são usados para criar uma área em branco entre a borda do botão e a imagem e/ou o texto do botão. Onde e quanto preenchimento é realmente aplicado depende do tipo do botão e se ele tem uma imagem. O preenchimento horizontal é aplicado à direita e à esquerda do botão e o preenchimento vertical é aplicado tanto na parte superior e inferior do botão. O preenchimento só é aplicado a botões que têm o estilo [**\_ AUTOSIZE de TBSTYLE**](toolbar-control-and-button-styles.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**autopadding TB \_**](tb-getpadding.md)
</dt> </dl>

 

