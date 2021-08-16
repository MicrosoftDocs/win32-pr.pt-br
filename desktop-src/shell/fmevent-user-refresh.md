---
description: Enviado a uma DLL de extensão quando o usuário escolhe o comando Atualizar no menu Exibir no Gerenciador de arquivos. A extensão pode usar essa notificação para atualizar seu menu.
title: Mensagem de FMEVENT_USER_REFRESH (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_USER_REFRESH
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: b8fb4ce8-d284-4558-82a4-488d4d833bcb
ms.openlocfilehash: 9e2f514494ae8040c7bdb97f556555bd7f32794e4259300da240956ff6fcfe98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094141"
---
# <a name="fmevent_user_refresh-message"></a>FMEVENT \_ mensagem de atualização do usuário \_

Enviado a uma DLL de extensão quando o usuário escolhe o comando **Atualizar** no menu **Exibir** no Gerenciador de arquivos. A extensão pode usar essa notificação para atualizar seu menu.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Uma DLL de extensão deve retornar zero se ela processar essa mensagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> </dl>

 

 




