---
title: Mensagem de TB_SETPADDING (commctrl. h)
description: Define o preenchimento de um controle ToolBar.
ms.assetid: a18c4efb-1140-4149-8dce-dfc1f03bb61a
keywords:
- controles de Windows de mensagem de TB_SETPADDING
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
ms.openlocfilehash: da488c7aab3a6856fd1bd8db6911336eb52881da396e287937678600158d9655
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078160"
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

## <a name="return-value"></a>Valor retornado

Retorna um valor **DWORD** que contém o preenchimento horizontal anterior no [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) e o preenchimento vertical anterior no [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)), em pixels.

## <a name="remarks"></a>Comentários

Os valores de preenchimento são usados para criar uma área em branco entre a borda do botão e a imagem e/ou o texto do botão. Onde e quanto preenchimento é realmente aplicado depende do tipo do botão e se ele tem uma imagem. O preenchimento horizontal é aplicado à direita e à esquerda do botão e o preenchimento vertical é aplicado tanto na parte superior e inferior do botão. O preenchimento só é aplicado a botões que têm o estilo [**\_ AUTOSIZE de TBSTYLE**](toolbar-control-and-button-styles.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**autopadding TB \_**](tb-getpadding.md)
</dt> </dl>

 

