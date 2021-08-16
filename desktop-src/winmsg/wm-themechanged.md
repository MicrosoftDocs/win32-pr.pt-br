---
description: Transmitir para cada janela após um evento de alteração de tema. Exemplos de eventos de alteração de tema são a ativação de um tema, a desativação de um tema ou uma transição de um tema para outro.
ms.assetid: 1a4051ac-cc6e-4520-ab66-d0a41a8a4c73
title: WM_THEMECHANGED mensagem (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b070cb492fa5db94acb97cd07f3de87455189d542aaaad2a51a3e0ecc6b4268d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118199905"
---
# <a name="wm_themechanged-message"></a>Mensagem WM \_ THEMECHANGED

Transmitir para cada janela após um evento de alteração de tema. Exemplos de eventos de alteração de tema são a ativação de um tema, a desativação de um tema ou uma transição de um tema para outro.


```C++
#define WM_THEMECHANGED                 0x031A
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Esse parâmetro é reservado.

</dd> <dt>

*lParam* 
</dt> <dd>

Esse parâmetro é reservado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **LRESULT**

Se um aplicativo processa essa mensagem, ele deve retornar zero.

## <a name="remarks"></a>Comentários

Uma janela recebe essa mensagem por meio de [**sua função WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))

> [!Note]  
> Essa mensagem é postada pelo sistema operacional. Normalmente, os aplicativos não enviam essa mensagem.

 

Os temas são especificações para a aparência dos controles, de modo que o elemento visual de um controle seja tratado separadamente de sua funcionalidade.

Para liberar um alça de tema existente, [**chame CloseThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-closethemedata). Para adquirir um novo alça de tema, use [**OpenThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata).

Após a **difusão WM \_ THEMECHANGED,** todos os alças de tema existentes são inválidos. Uma janela com conhecimento de tema deve liberar e reabrir qualquer um de seus alças de tema pré-existentes quando receber a mensagem **WM \_ THEMECHANGED.** Se a [**função OpenThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata) retornar **NULL,** a janela deverá pintar sem-teda.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Outros recursos**
</dt> <dt>

[**CloseThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-closethemedata)
</dt> <dt>

[**IsThemeActive**](/windows/win32/api/uxtheme/nf-uxtheme-isthemeactive)
</dt> <dt>

[**OpenThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata)
</dt> </dl>

 

 
