---
title: Mensagem de TB_SETCOLORSCHEME (commctrl. h)
description: Define as informações do esquema de cores para o controle ToolBar.
ms.assetid: 96cf6464-b760-46af-910f-984e41dbfca5
keywords:
- controles de Windows de mensagem de TB_SETCOLORSCHEME
topic_type:
- apiref
api_name:
- TB_SETCOLORSCHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58c6a07c186fd3f5a521719ba0f75f8e468c3868d8ebfaa0595679d48b45089f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167496"
---
# <a name="tb_setcolorscheme-message"></a>TB de \_ mensagem SETCOLORSCHEME

Define as informações do esquema de cores para o controle ToolBar.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**ColorScheme**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) que contém as informações do esquema de cores.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor retornado para esta mensagem não é usado.

## <a name="remarks"></a>Comentários

O controle Toolbar usa as informações do esquema de cores ao desenhar os elementos 3-D no controle.

Quando os estilos visuais são habilitados, essa mensagem não tem nenhum efeito.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TB de \_ GETCOLORSCHEME**](tb-getcolorscheme.md)
</dt> </dl>

 

 





