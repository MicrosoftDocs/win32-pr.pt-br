---
title: Mensagem de WM_UPDATEUISTATE (WinUser. h)
description: Um aplicativo envia a mensagem do WM \_ UPDATEUISTATE para alterar o estado da interface do usuário para a janela especificada e todas as suas janelas filhas.
ms.assetid: cbdeeddd-59b2-4a73-bfe9-17647d32bcf3
keywords:
- WM_UPDATEUISTATE menus de mensagens e outros recursos
topic_type:
- apiref
api_name:
- WM_UPDATEUISTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 003d9ca45b357a7d0ebc172000b1e2c01505db8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086480"
---
# <a name="wm_updateuistate-message"></a>Mensagem do WM \_ UPDATEUISTATE

Um aplicativo envia a mensagem do **WM \_ UPDATEUISTATE** para alterar o estado da interface do usuário para a janela especificada e todas as suas janelas filhas.


```C++
#define WM_UPDATEUISTATE                0x0128
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

A palavra de ordem inferior Especifica a ação a ser executada. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                                                   | Significado                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UIS_CLEAR"></span><span id="uis_clear"></span><dl> <dt>**UIs \_ LIMPAR**</dt> <dt>2</dt> </dl>                | O elemento de estado da interface do usuário especificado pela palavra de ordem superior deve estar oculto.<br/>                                                                   |
| <span id="UIS_INITIALIZE"></span><span id="uis_initialize"></span><dl> <dt>**UIs \_ INICIALIZAR**</dt> <dt>3</dt> </dl> | O elemento de estado da interface do usuário especificado pela palavra de ordem superior deve ser alterado com base no último evento de entrada. Para obter mais informações, consulte Comentários.<br/> |
| <span id="UIS_SET"></span><span id="uis_set"></span><dl> <dt>**UIs \_ CONJUNTO**</dt> <dt>1</dt> </dl>                      | O elemento de estado da interface do usuário especificado pela palavra de ordem superior deve estar visível.<br/>                                                                  |



 

A palavra de ordem superior especifica quais elementos de estado da interface do usuário são afetados ou o estilo do controle. Esse parâmetro pode ser um ou mais dos valores a seguir.



| Valor                                                                                                                                                                                                                     | Significado                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="UISF_ACTIVE"></span><span id="uisf_active"></span><dl> <dt>**UISF \_ ATIVO**</dt> <dt>0x4</dt> </dl>          | Um controle deve ser desenhado no estilo usado para controles ativos.<br/> |
| <span id="UISF_HIDEACCEL"></span><span id="uisf_hideaccel"></span><dl> <dt>**UISF \_**</dt> <dt>0x2</dt> HIDEACCEL </dl> | Aceleradores de teclado.<br/>                                           |
| <span id="UISF_HIDEFOCUS"></span><span id="uisf_hidefocus"></span><dl> <dt>**UISF \_ HIDEFOCUS**</dt> <dt>0x1</dt> </dl> | Indicadores de foco.<br/>                                                |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Uma janela deve enviar essa mensagem para alterar o estado da interface do usuário de todas as janelas filhas. Ao contrário da mensagem do [**WM \_ CHANGEUISTATE**](wm-changeuistate.md) , que é uma notificação, quando o [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) processa a mensagem **\_ UPDATEUISTATE do WM** , ele altera o estado da interface do usuário e propaga as alterações para todas as janelas filhas.

A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) atualiza o estado da interface do usuário de acordo com o valor *wParam* . Se o estado da interface do usuário for modificado, a função enviará a mensagem a todas as janelas filho imediatas. O **DefWindowProc** também envia essa mensagem quando recebe uma mensagem do [**WM \_ CHANGEUISTATE**](wm-changeuistate.md) notificando o sistema de que uma janela filho pretende modificar o estado da interface do usuário.

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**CHANGEUISTATE do WM \_**](wm-changeuistate.md)
</dt> <dt>

[**QUERYUISTATE do WM \_**](wm-queryuistate.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Aceleradores de teclado](keyboard-accelerators.md)
</dt> </dl>

 

