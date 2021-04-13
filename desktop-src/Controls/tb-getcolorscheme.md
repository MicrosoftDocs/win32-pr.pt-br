---
title: Mensagem de TB_GETCOLORSCHEME (commctrl. h)
description: Recupera as informações do esquema de cores do controle ToolBar.
ms.assetid: af172631-309e-4181-a690-05946cd6e143
keywords:
- Controles de TB_GETCOLORSCHEME de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_GETCOLORSCHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61344439ae8bc2b3a9ecd47472174577d652aa96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455276"
---
# <a name="tb_getcolorscheme-message"></a>TB de \_ mensagem GETCOLORSCHEME

Recupera as informações do esquema de cores do controle ToolBar.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**ColorScheme**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) que receberá as informações do esquema de cores. Você deve definir o membro **cbSize** dessa estrutura como **sizeof**(ColorScheme) antes de enviar esta mensagem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará zero se for bem-sucedido ou nenhum outro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TB de \_ SETCOLORSCHEME**](tb-setcolorscheme.md)
</dt> </dl>

 

 





