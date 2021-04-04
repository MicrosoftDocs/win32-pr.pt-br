---
title: Mensagem de WM_CHANGEUISTATE (WinUser. h)
description: Um aplicativo envia a mensagem do WM \_ CHANGEUISTATE para indicar que o estado da interface do usuário deve ser alterado.
ms.assetid: d8dfc2fe-c64f-4e7e-b021-127aa85d5dd6
keywords:
- WM_CHANGEUISTATE menus de mensagens e outros recursos
topic_type:
- apiref
api_name:
- WM_CHANGEUISTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cdfec2a26b3b3d160d3d207c338c8ebecd32bf2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645170"
---
# <a name="wm_changeuistate-message"></a>Mensagem do WM \_ CHANGEUISTATE

Um aplicativo envia a mensagem do **WM \_ CHANGEUISTATE** para indicar que o estado da interface do usuário deve ser alterado.


```C++
#define WM_CHANGEUISTATE                0x0127
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

A palavra de ordem inferior Especifica a ação a ser executada. Esse membro pode ser um dos valores a seguir.



| Valor                                                                                                                                                                                                                   | Significado                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UIS_CLEAR"></span><span id="uis_clear"></span><dl> <dt>**UIs \_ LIMPAR**</dt> <dt>2</dt> </dl>                | Os sinalizadores de estado da interface do usuário especificados pela palavra de ordem superior devem ser apagados.<br/>                                                                  |
| <span id="UIS_INITIALIZE"></span><span id="uis_initialize"></span><dl> <dt>**UIs \_ INICIALIZAR**</dt> <dt>3</dt> </dl> | Os sinalizadores de estado da interface do usuário especificados pela palavra de ordem superior devem ser alterados com base no último evento de entrada. Para obter mais informações, consulte Comentários.<br/> |
| <span id="UIS_SET"></span><span id="uis_set"></span><dl> <dt>**UIs \_ CONJUNTO**</dt> <dt>1</dt> </dl>                      | Os sinalizadores de estado da interface do usuário especificados pela palavra de ordem superior devem ser definidos.<br/>                                                                      |



 

A palavra de ordem superior especifica quais elementos de estado da interface do usuário são afetados ou o estilo do controle. Esse membro pode ser um ou mais dos valores a seguir.



| Valor                                                                                                                                                                                                                     | Significado                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="UISF_ACTIVE"></span><span id="uisf_active"></span><dl> <dt>**UISF \_ ATIVO**</dt> <dt>0x4</dt> </dl>          | Um controle deve ser desenhado no estilo usado para controles ativos.<br/> |
| <span id="UISF_HIDEACCEL"></span><span id="uisf_hideaccel"></span><dl> <dt>**UISF \_**</dt> <dt>0x2</dt> HIDEACCEL </dl> | Os aceleradores de teclado estão ocultos.<br/>                                |
| <span id="UISF_HIDEFOCUS"></span><span id="uisf_hidefocus"></span><dl> <dt>**UISF \_ HIDEFOCUS**</dt> <dt>0x1</dt> </dl> | Os indicadores de foco estão ocultos.<br/>                                     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Esse parâmetro não é usado e deve ser 0.

</dd> </dl>

## <a name="remarks"></a>Comentários

Uma janela deve enviar essa mensagem para ela mesma ou para seu pai quando ela deve alterar os elementos de estado da interface do usuário de todas as janelas na mesma hierarquia. O procedimento de janela deve permitir que [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) processe essa mensagem para que toda a árvore de janela tenha um estado de interface de usuário consistente. Quando a janela de nível superior recebe a mensagem do **WM \_ CHANGEUISTATE** , ela envia uma mensagem do [**WM \_ UPDATEUISTATE**](wm-updateuistate.md) com os mesmos parâmetros para todas as janelas filhas. Quando o sistema processa a mensagem do **WM \_ UPDATEUISTATE** , ele faz a alteração no estado da interface do usuário.

Se a palavra de ordem inferior de *wParam* for \_ inicializada por UIS, o sistema enviará a mensagem do [**WM \_ UPDATEUISTATE**](wm-updateuistate.md) com um estado de interface do usuário com base no último evento de entrada. Por exemplo, se a última entrada for proveniente do mouse, o sistema ocultará as indicações de teclado. E, se a última entrada for proveniente do teclado, o sistema mostrará as indicações de teclado. Se o estado que resulta do processamento do **WM \_ CHANGEUISTATE** for igual ao estado antigo, o [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) não enviará essa mensagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**QUERYUISTATE do WM \_**](wm-queryuistate.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Aceleradores de teclado](keyboard-accelerators.md)
</dt> </dl>

 

