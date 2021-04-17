---
title: Mensagem de TB_SETANCHORHIGHLIGHT (commctrl. h)
description: Define a configuração de realce de âncora para uma barra de ferramentas.
ms.assetid: d31652d5-e9cf-4bf3-8f90-818eb078fa87
keywords:
- Controles de TB_SETANCHORHIGHLIGHT de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_SETANCHORHIGHLIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 809f71e446f7768d637258152db1dd2d56346dfd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755648"
---
# <a name="tb_setanchorhighlight-message"></a>TB de \_ mensagem SETANCHORHIGHLIGHT

Define a configuração de realce de âncora para uma barra de ferramentas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor **bool** que especifica se o realce de âncora está habilitado ou desabilitado. Se esse valor for diferente de zero, o realce de âncora será habilitado. Se esse valor for zero, o realce de âncora será desabilitado.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna a configuração de realce da âncora anterior. Se esse valor for diferente de zero, o realce de âncora foi habilitado. Se esse valor for zero, o realce de âncora foi desabilitado.

## <a name="remarks"></a>Comentários

Realce de âncora em uma barra de ferramentas significa que o último item realçado permanecerá realçado até que outro item seja realçado. Isso ocorre mesmo que o cursor saia do controle ToolBar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





