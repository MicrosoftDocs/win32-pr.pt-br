---
UID: ''
title: Função de retorno de chamada ShellProc
description: A função recebe notificações de eventos do shell do sistema.
old-location: ''
ms.assetid: na
ms.date: 04/05/2019
ms.keywords: ''
ms.topic: reference
req.header: ''
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location: ''
api_name: ''
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 3776748994b44b3a870fd4689fa9f4019bff99ae8d6f7dd7b13edbf2c98054d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119449096"
---
# <a name="shellproc-function"></a>Função ShellProc

## <a name="description"></a>Descrição

Uma função de retorno de chamada definida por aplicativo ou definida pela biblioteca usada com a função [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .
A função recebe notificações de eventos do shell do sistema.

O tipo **HOOKPROC** define um ponteiro para essa função de retorno de chamada.
**ShellProc** é um espaço reservado para o nome da função definida pelo aplicativo ou definido pela biblioteca.

```cpp
LRESULT CALLBACK ShellProc(
  _In_ int    nCode,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a>Parâmetros

### <a name="ncode-in"></a>nCode [in]

Tipo: **int**

O código do gancho.
Se *nCode* for menor que zero, o procedimento de gancho deverá passar a mensagem para a função [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) sem processamento adicional e deverá retornar o valor retornado por **CallNextHookEx**.
Esse parâmetro pode usar um dos valores a seguir.

| Valor | Significado |
|-------|---------|
| **HSHELL_ACCESSIBILITYSTATE** 11 | O estado de acessibilidade foi alterado. |
| **HSHELL_ACTIVATESHELLWINDOW** 3 | O Shell deve ativar sua janela principal. |
| **HSHELL_APPCOMMAND** 12 | O usuário concluiu um evento de entrada (por exemplo, pressionou um botão de comando do aplicativo no mouse ou uma tecla de comando do aplicativo no teclado) e o aplicativo não manipula a mensagem de [WM_APPCOMMAND](/windows/desktop/inputdev/wm-appcommand) gerada por essa entrada. Se o procedimento do Shell manipular a mensagem de [WM_COMMAND](/windows/desktop/menurc/wm-command) , ele não deve chamar **CallNextHookEx**. Consulte a seção valor de retorno para obter mais informações. |
| **HSHELL_GETMINRECT** 5 | Uma janela está sendo minimizada ou maximizada. O sistema precisa das coordenadas do retângulo minimizado para a janela. |
| **HSHELL_LANGUAGE** 8 | O idioma do teclado foi alterado ou um novo layout de teclado foi carregado. |
| **HSHELL_REDRAW** 6 | O título de uma janela na barra de tarefas foi redesenhado. |
| **HSHELL_TASKMAN** 7 | O usuário selecionou a lista de tarefas. um aplicativo de shell que fornece uma lista de tarefas deve retornar **TRUE** para impedir Windows de iniciar sua lista de tarefas. |
| **HSHELL_WINDOWACTIVATED** 4 | A ativação foi alterada para uma janela diferente de nível superior e sem proprietário. |
| **HSHELL_WINDOWCREATED** 1 | Uma janela de nível superior e sem proprietário foi criada. A janela existe quando o sistema chama esse gancho. |
| **HSHELL_WINDOWDESTROYED** 2 | Uma janela sem proprietário de nível superior está prestes a ser destruída. A janela ainda existe quando o sistema chama esse gancho. |
| **HSHELL_WINDOWREPLACED** 13 | Uma janela de nível superior está sendo substituída. A janela existe quando o sistema chama esse gancho. |

### <a name="wparam-in"></a>wParam [in]

Tipo: **wParam**

Esse parâmetro depende do valor do parâmetro *nCode* , conforme mostrado na tabela a seguir.

| nCode | wParam |
|-------|---------|
| **HSHELL_ACCESSIBILITYSTATE** | Indica qual recurso de acessibilidade alterou o estado. Esse valor é um dos seguintes: **ACCESS_FILTERKEYS**, **ACCESS_MOUSEKEYS** ou **ACCESS_STICKYKEYS**. |
| **HSHELL_APPCOMMAND** | Indica onde a mensagem de **WM_APPCOMMAND** foi enviada originalmente; por exemplo, o identificador para uma janela. Para obter mais informações, consulte parâmetro cmd em **WM_APPCOMMAND**. |
| **HSHELL_GETMINRECT** | Um identificador para a janela minimizada ou maximizada. |
| **HSHELL_LANGUAGE** | Um identificador para a janela. |
| **HSHELL_REDRAW** | Um identificador para a janela redesenhar. |
| **HSHELL_WINDOWACTIVATED** | Um identificador para a janela ativada. |
| **HSHELL_WINDOWCREATED** | Um identificador para a janela criada. |
| **HSHELL_WINDOWDESTROYED** | Um identificador para a janela destruída. |
| **HSHELL_WINDOWREPLACED** | Um identificador para a janela que está sendo substituída. Windows 2000: sem suporte. |

### <a name="lparam-in"></a>lParam [in]

Tipo: **lParam**

Esse parâmetro depende do valor do parâmetro *nCode* , conforme mostrado na tabela a seguir.

| nCode | lParam |
|-------|---------|
| **HSHELL_APPCOMMAND** | `GET_APPCOMMAND_LPARAM(lParam)` é o comando de aplicativo correspondente ao evento de entrada. `GET_DEVICE_LPARAM(lParam)` indica o que gerou o evento de entrada; por exemplo, o mouse ou o teclado. Para obter mais informações, consulte a descrição do parâmetro *udevice* em **WM_APPCOMMAND**. `GET_FLAGS_LPARAM(lParam)` depende do valor do *cmd* no **WM_APPCOMMAND**. Por exemplo, isso pode indicar quais chaves virtuais foram mantidas quando a **WM_APPCOMMAND** mensagem foi enviada originalmente. Para obter mais informações, consulte o parâmetro de descrição *dwCmdFlags* em **WM_APPCOMMAND**. |
| **HSHELL_GETMINRECT** | Um ponteiro para uma estrutura [Rect](/previous-versions/dd162897(v=vs.85)) . |
| **HSHELL_LANGUAGE** | Um identificador para um layout de teclado. |
| **HSHELL_MONITORCHANGED** | Um identificador para a janela que foi movida para um monitor diferente. |
| **HSHELL_REDRAW** | O valor será **true** se a janela estiver piscando, caso contrário, retornará **false** . |
| **HSHELL_WINDOWACTIVATED** | O valor será TRUE se a janela estiver no modo de tela inteira ou **false** caso contrário. |
| **HSHELL_WINDOWREPLACED** | Um identificador para a nova janela. Windows 2000: sem suporte. |

## <a name="returns"></a>Retornos

Tipo: **LRESULT**

O valor de retorno deve ser zero, a menos que o valor de nCode seja **HSHELL_APPCOMMAND** e o procedimento de shell manipule a mensagem de **WM_COMMAND** .
Nesse caso, o retorno deve ser diferente de zero.

## <a name="remarks"></a>Comentários

Instale esse procedimento de conexão especificando o tipo de gancho [WH_SHELL](about-hooks.md) e um ponteiro para o procedimento de gancho em uma chamada para a função **SetWindowsHookEx** .

## <a name="see-also"></a>Confira também

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[WM_APPCOMMAND](/windows/desktop/inputdev/wm-appcommand)

[WM_COMMAND](/windows/desktop/menurc/wm-command)

[Ganchos](hooks.md)
