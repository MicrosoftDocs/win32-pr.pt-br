---
description: Um aplicativo envia a mensagem do WM \_ MDICREATE para uma janela de cliente MDI (interface de vários documentos) para criar uma janela filho MDI.
ms.assetid: f2313ffd-867f-4870-a667-3e5f5402776f
title: Mensagem de WM_MDICREATE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c69a894ebd2e55bb74486e26cd118366b1e533a490cc50feb5f77aad64c6be3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056006"
---
# <a name="wm_mdicreate-message"></a>Mensagem do WM \_ MDICREATE

Um aplicativo envia a mensagem do **WM \_ MDICREATE** para uma janela de cliente MDI (interface de vários documentos) para criar uma janela filho MDI.


```C++
#define WM_MDICREATE                    0x0220
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) que contém informações que o sistema usa para criar a janela filho MDI.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Digite: **HWND**

Se a mensagem tiver sucesso, o valor de retorno será o identificador para a nova janela filho.

Se a mensagem falhar, o valor de retorno será **nulo**.

## <a name="remarks"></a>Comentários

A janela filho MDI é criada com os bits de [**estilo de janela**](window-styles.md) **WS \_ filho**, **WS \_ CLIPSIBLINGS**, **WS \_ CLIPCHILDREN**, **WS \_ SYSMENU**, **WS \_ Caption**, **WS \_ THICKFRAME**, **WS \_ MINIMIZEBOX** e **WS \_ MAXIMIZEBOX**, além de bits de estilo adicionais especificados na estrutura [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) . O sistema adiciona o título da nova janela filho ao menu janela da janela do quadro. Um aplicativo deve usar essa mensagem para criar todas as janelas filhas da janela do cliente.

Se uma janela do cliente MDI receber qualquer mensagem que altere a ativação de suas janelas filhas enquanto a janela filho ativa for maximizada, o sistema restaura a janela filho ativa e maximiza a janela filho ativada recentemente.

Quando uma janela filho MDI é criada, o sistema envia a mensagem de [**\_ criação do WM**](wm-create.md) para a janela. O parâmetro *lParam* da mensagem **de \_ criação do WM** contém um ponteiro para uma estrutura [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) . O membro *lpCreateParams* dessa estrutura contém um ponteiro para a estrutura [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) passada com a mensagem **\_ MDICREATE do WM** que criou a janela filho MDI.

Um aplicativo não deve enviar uma segunda mensagem do **WM \_ MDICREATE** enquanto uma mensagem do **WM \_ MDICREATE** ainda está sendo processada. Por exemplo, ele não deve enviar uma mensagem do **WM \_ MDICREATE** enquanto uma janela filho MDI processa sua mensagem do **WM \_ MDICREATE** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**CreateMDIWindow**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa)
</dt> <dt>

[**OS CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa)
</dt> <dt>

[**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa)
</dt> <dt>

[**criação do WM \_**](wm-create.md)
</dt> <dt>

[**MDIDESTROY do WM \_**](wm-mdidestroy.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Interface de vários documentos](multiple-document-interface.md)
</dt> </dl>

 

 
