---
title: WM_QUERYUISTATE mensagem (Winuser.h)
description: Um aplicativo envia a mensagem WM \_ QUERYUISTATE para recuperar o estado da interface do usuário de uma janela.
ms.assetid: 3a9e3477-b5d7-4c55-b6d4-8a479451fee8
keywords:
- WM_QUERYUISTATE menus de mensagem e outros recursos
topic_type:
- apiref
api_name:
- WM_QUERYUISTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e62fc33fb79594f3e07c0d44d4b25fd16e980ef3a4a89b3079c69ef6eb5d1b89
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119267906"
---
# <a name="wm_queryuistate-message"></a>Mensagem WM \_ QUERYUISTATE

Um aplicativo envia a **mensagem WM \_ QUERYUISTATE** para recuperar o estado da interface do usuário de uma janela.


```C++
#define WM_QUERYUISTATE                 0x0129
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Esse parâmetro não é usado e deve ser 0.

</dd> <dt>

*lParam* 
</dt> <dd>

Esse parâmetro não é usado e deve ser 0.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno será **NULL se** os indicadores de foco e os aceleradores de teclado estão visíveis. Caso contrário, o valor de retorno pode ser um ou mais dos valores a seguir.



| Valor/código de retorno                                                                                                                                       | Descrição                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**UISF \_ ACTIVE**</dt> <dt>0x4</dt> </dl>    | Um controle deve ser desenhado no estilo usado para controles ativos.<br/> |
| <dl> <dt>**UISF \_ HIDEACCEL**</dt> <dt>0x2</dt> </dl> | Os aceleradores de teclado estão ocultos.<br/>                                |
| <dl> <dt>**UISF \_ HIDEFOCUS**</dt> <dt>0x1</dt> </dl> | Os indicadores de foco estão ocultos.<br/>                                     |



 

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

[**WM \_ CHANGEUISTATE**](wm-changeuistate.md)
</dt> <dt>

[**WM \_ UPDATEUISTATE**](wm-updateuistate.md)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Aceleradores de teclado](keyboard-accelerators.md)
</dt> </dl>

 

 





