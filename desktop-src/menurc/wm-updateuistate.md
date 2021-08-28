---
title: WM_UPDATEUISTATE mensagem (Winuser.h)
description: Um aplicativo envia a mensagem WM UPDATEUISTATE para alterar o estado da interface do usuário para a janela \_ especificada e todas as janelas filho.
ms.assetid: cbdeeddd-59b2-4a73-bfe9-17647d32bcf3
keywords:
- WM_UPDATEUISTATE menus de mensagem e outros recursos
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
ms.openlocfilehash: 351770019f18c52c4ff1588a09c803d07f0f58ce032b35af53501ff4e47b6aed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112856"
---
# <a name="wm_updateuistate-message"></a>Mensagem WM \_ UPDATEUISTATE

Um aplicativo envia a **mensagem WM \_ UPDATEUISTATE** para alterar o estado da interface do usuário para a janela especificada e todas as janelas filho.


```C++
#define WM_UPDATEUISTATE                0x0128
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

A palavra de ordem baixa especifica a ação a ser executada. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                                                   | Significado                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UIS_CLEAR"></span><span id="uis_clear"></span><dl> <dt>**UIS \_ CLEAR**</dt> <dt>2</dt> </dl>                | O elemento de estado da interface do usuário especificado pela palavra de ordem alta deve estar oculto.<br/>                                                                   |
| <span id="UIS_INITIALIZE"></span><span id="uis_initialize"></span><dl> <dt>**UIS \_ INITIALIZE**</dt> <dt>3</dt> </dl> | O elemento de estado da interface do usuário especificado pela palavra de ordem alta deve ser alterado com base no último evento de entrada. Para obter mais informações, consulte Comentários.<br/> |
| <span id="UIS_SET"></span><span id="uis_set"></span><dl> <dt>**UIS \_ SET**</dt> <dt>1</dt> </dl>                      | O elemento de estado da interface do usuário especificado pela palavra de ordem alta deve estar visível.<br/>                                                                  |



 

A palavra de ordem alta especifica quais elementos de estado da interface do usuário são afetados ou o estilo do controle. Esse parâmetro pode ser um ou mais dos valores a seguir.



| Valor                                                                                                                                                                                                                     | Significado                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="UISF_ACTIVE"></span><span id="uisf_active"></span><dl> <dt>**UISF \_ ACTIVE**</dt> <dt>0x4</dt> </dl>          | Um controle deve ser desenhado no estilo usado para controles ativos.<br/> |
| <span id="UISF_HIDEACCEL"></span><span id="uisf_hideaccel"></span><dl> <dt>**UISF \_ HIDEACCEL**</dt> <dt>0x2</dt> </dl> | Aceleradores de teclado.<br/>                                           |
| <span id="UISF_HIDEFOCUS"></span><span id="uisf_hidefocus"></span><dl> <dt>**UISF \_ HIDEFOCUS**</dt> <dt>0x1</dt> </dl> | Indicadores de foco.<br/>                                                |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Uma janela deve enviar essa mensagem para alterar o estado da interface do usuário de todas as janelas filho. Ao contrário da mensagem [**WM \_ CHANGEUISTATE,**](wm-changeuistate.md) que é uma notificação, quando [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) processa a mensagem **WM \_ UPDATEUISTATE,** ela altera o estado da interface do usuário e propaga as alterações para todas as janelas filho.

A [**função DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) atualiza o estado da interface do usuário de acordo com o *valor wParam.* Se o estado da interface do usuário for modificado, a função enviará a mensagem para todas as janelas filho imediatas. **DefWindowProc** também envia essa mensagem quando recebe uma mensagem [**WM \_ CHANGEUISTATE**](wm-changeuistate.md) notificando o sistema de que uma janela filho pretende modificar o estado da interface do usuário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**Defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**WM \_ CHANGEUISTATE**](wm-changeuistate.md)
</dt> <dt>

[**WM \_ QUERYUISTATE**](wm-queryuistate.md)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Aceleradores de teclado](keyboard-accelerators.md)
</dt> </dl>

 

