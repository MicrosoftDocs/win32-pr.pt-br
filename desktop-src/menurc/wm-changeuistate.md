---
title: WM_CHANGEUISTATE mensagem (Winuser.h)
description: Um aplicativo envia a mensagem WM \_ CHANGEUISTATE para indicar que o estado da interface do usuário deve ser alterado.
ms.assetid: d8dfc2fe-c64f-4e7e-b021-127aa85d5dd6
keywords:
- WM_CHANGEUISTATE menus de mensagem e outros recursos
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
ms.openlocfilehash: 3849f9a5d2ccd0cec1bcaba4280e125ea01a669c8535c2dc520ebb98c3a3fcdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117869706"
---
# <a name="wm_changeuistate-message"></a>Mensagem WM \_ CHANGEUISTATE

Um aplicativo envia a **mensagem WM \_ CHANGEUISTATE** para indicar que o estado da interface do usuário deve ser alterado.


```C++
#define WM_CHANGEUISTATE                0x0127
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

A palavra de ordem baixa especifica a ação a ser tomada. Esse membro pode ser um dos valores a seguir.



| Valor                                                                                                                                                                                                                   | Significado                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UIS_CLEAR"></span><span id="uis_clear"></span><dl> <dt>**UIS \_ CLEAR**</dt> <dt>2</dt> </dl>                | Os sinalizadores de estado da interface do usuário especificados pela palavra de ordem alta devem ser limpos.<br/>                                                                  |
| <span id="UIS_INITIALIZE"></span><span id="uis_initialize"></span><dl> <dt>**UIS \_ INITIALIZE**</dt> <dt>3</dt> </dl> | Os sinalizadores de estado da interface do usuário especificados pela palavra de ordem alta devem ser alterados com base no último evento de entrada. Para obter mais informações, consulte Comentários.<br/> |
| <span id="UIS_SET"></span><span id="uis_set"></span><dl> <dt>**UIS \_ SET**</dt> <dt>1</dt> </dl>                      | Os sinalizadores de estado da interface do usuário especificados pela palavra de ordem alta devem ser definidos.<br/>                                                                      |



 

A palavra de ordem alta especifica quais elementos de estado da interface do usuário são afetados ou o estilo do controle. Esse membro pode ser um ou mais dos valores a seguir.



| Valor                                                                                                                                                                                                                     | Significado                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="UISF_ACTIVE"></span><span id="uisf_active"></span><dl> <dt>**UISF \_ Active**</dt> <dt>0x4</dt> </dl>          | Um controle deve ser desenhado no estilo usado para controles ativos.<br/> |
| <span id="UISF_HIDEACCEL"></span><span id="uisf_hideaccel"></span><dl> <dt>**UISF \_ HIDEACCEL**</dt> <dt>0x2</dt> </dl> | Os aceleradores de teclado estão ocultos.<br/>                                |
| <span id="UISF_HIDEFOCUS"></span><span id="uisf_hidefocus"></span><dl> <dt>**UISF \_ HIDEFOCUS**</dt> <dt>0x1</dt> </dl> | Os indicadores de foco estão ocultos.<br/>                                     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Esse parâmetro não é usado e deve ser 0.

</dd> </dl>

## <a name="remarks"></a>Comentários

Uma janela deve enviar essa mensagem para si mesmo ou seu pai quando ela precisa alterar os elementos de estado da interface do usuário de todas as janelas na mesma hierarquia. O procedimento de janela deve permitir [**que DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) processe essa mensagem para que toda a árvore de janelas tenha um estado de interface do usuário consistente. Quando a janela de nível superior recebe a mensagem **WM \_ CHANGEUISTATE,** ela envia uma mensagem [**WM \_ UPDATEUISTATE**](wm-updateuistate.md) com os mesmos parâmetros para todas as janelas filho. Quando o sistema processa **a mensagem WM \_ UPDATEUISTATE,** ele faz a alteração no estado da interface do usuário.

Se a palavra de ordem baixa de *wParam* for UIS INITIALIZE, o sistema enviará a mensagem \_ [**WM \_ UPDATEUISTATE**](wm-updateuistate.md) com um estado de interface do usuário com base no último evento de entrada. Por exemplo, se a última entrada veio do mouse, o sistema ocultará as responsabilidades do teclado. E, se a última entrada tiver vindo do teclado, o sistema mostrará as dicas de teclado. Se o estado que resulta do processamento **de WM \_ CHANGEUISTATE** for o mesmo que o estado antigo, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) não enviará essa mensagem.

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

[**Hiword**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**Loword**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM \_ QUERYUISTATE**](wm-queryuistate.md)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Aceleradores de teclado](keyboard-accelerators.md)
</dt> </dl>

 

