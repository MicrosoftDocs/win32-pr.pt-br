---
description: Enviado a todas as janelas após o logon ou logoff do usuário. Quando o usuário faz logon ou logoff, o sistema atualiza as configurações específicas do usuário. O sistema envia essa mensagem imediatamente após a atualização das configurações.
title: Mensagem de WM_USERCHANGED (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowmessages\wm_userchanged.htm
api_name:
- WM_USERCHANGED
api_type:
- HeaderDef
api_location:
- Winuser.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2bb466e80070fe1be5cd7af7889fc5727c81f8caad89ad60c48c7a105b688fb4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119705696"
---
# <a name="wm_userchanged-message"></a>Mensagem do WM \_ USERchanged

Enviado a todas as janelas após o logon ou logoff do usuário. Quando o usuário faz logon ou logoff, o sistema atualiza as configurações específicas do usuário. O sistema envia essa mensagem imediatamente após a atualização das configurações.

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .

> [!Note]  
> essa mensagem não tem suporte a partir do Windows Vista.

 


```C++
#define WM_USERCHANGED                  0x0054
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **LRESULT**

Um aplicativo deve retornar zero se ele processar essa mensagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                |
| Cabeçalho<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Windows Sobre](windows.md)
</dt> </dl>

 

 
