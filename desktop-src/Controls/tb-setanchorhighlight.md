---
title: TB_SETANCHORHIGHLIGHT mensagem (Commctrl.h)
description: Define a configuração de realçada de âncora para uma barra de ferramentas.
ms.assetid: d31652d5-e9cf-4bf3-8f90-818eb078fa87
keywords:
- TB_SETANCHORHIGHLIGHT controles Windows mensagem
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
ms.openlocfilehash: 77a66193aebee80a2ffde97b7e802b5bab750f0a9e2f1773b32d872211d52150
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167979"
---
# <a name="tb_setanchorhighlight-message"></a>Mensagem TB \_ SETANCHORHIGHLIGHT

Define a configuração de realçada de âncora para uma barra de ferramentas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

**Valor BOOL** que especifica se o realçamento de âncora está habilitado ou desabilitado. Se esse valor for não zero, o realçamento de âncora será habilitado. Se esse valor for zero, o realçamento de âncora será desabilitado.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna a configuração de realçada de âncora anterior. Se esse valor for não zero, o realçamento de âncora será habilitado. Se esse valor for zero, o realçamento de âncora será desabilitado.

## <a name="remarks"></a>Comentários

Realçamento de âncora em uma barra de ferramentas significa que o último item realçado permanecerá realçado até que outro item seja realçado. Isso ocorre mesmo se o cursor sair do controle da barra de ferramentas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





