---
description: Um aplicativo envia a mensagem WM WININICHANGE para todas as janelas de nível superior depois de fazer uma alteração no \_ WIN.INI arquivo. A função SystemParametersInfo envia essa mensagem depois que um aplicativo usa a função para alterar uma configuração no WIN.INI.
ms.assetid: 402f8d71-ad52-486d-be26-8b41a3f22045
title: WM_WININICHANGE mensagem (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81cfdfeff65c1580f0bd8373fdc5ef1eec409233a9624934ea67ba835ddf805e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810456"
---
# <a name="wm_wininichange-message"></a>Mensagem WM \_ WININICHANGE

Um aplicativo envia a **mensagem WM \_ WININICHANGE** para todas as janelas de nível superior depois de fazer uma alteração no WIN.INI arquivo. A [**função SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) envia essa mensagem depois que um aplicativo usa a função para alterar uma configuração em WIN.INI.

> [!Note]  
> A **mensagem WM \_ WININICHANGE** é fornecida apenas para compatibilidade com versões anteriores do sistema. Os aplicativos devem usar [**a mensagem WM \_ SETTINGCHANGE.**](wm-settingchange.md)

 

Uma janela recebe essa mensagem por meio de [**sua função WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_WININICHANGE                 0x001A
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma cadeia de caracteres que contém o nome do parâmetro do sistema que foi alterado. Por exemplo, essa cadeia de caracteres pode ser o nome de uma chave do Registro ou o nome de uma seção no arquivo Win.ini dados. Esse parâmetro não é particularmente útil para determinar qual parâmetro do sistema foi alterado. Por exemplo, quando a cadeia de caracteres é um nome de registro, ela normalmente indica apenas o nó folha no Registro, não o caminho inteiro. Além disso, alguns aplicativos enviam essa mensagem com *lParam definido* como **NULL.** Em geral, ao receber essa mensagem, você deve verificar e recarregar as configurações de parâmetro do sistema usadas pelo aplicativo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **LRESULT**

Se você processar essa mensagem, retorne zero.

## <a name="remarks"></a>Comentários

Para enviar a **mensagem WM \_ WININICHANGE** para todas as janelas de nível superior, use a função [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) com o parâmetro *hWnd* definido como **HWND \_ BROADCAST.**

Chamadas para funções que alteram WIN.INI podem ser mapeadas para o Registro. Esse mapeamento ocorre quando WIN.INI e a seção que está sendo alterada são especificadas no Registro sob a seguinte chave:

**HKEY \_ LOCAL MACHINE Software Microsoft Windows NT \_ \\ \\ \\ \\ CurrentVersion \\ IniFileMapping**

A alteração no local de armazenamento não tem nenhum efeito sobre o comportamento dessa mensagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Systemparametersinfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> </dl>

 

 
