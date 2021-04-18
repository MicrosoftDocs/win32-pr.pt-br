---
title: Mensagem de WM_QUERYUISTATE (WinUser. h)
description: Um aplicativo envia a mensagem do WM \_ QUERYUISTATE para recuperar o estado da interface do usuário para uma janela.
ms.assetid: 3a9e3477-b5d7-4c55-b6d4-8a479451fee8
keywords:
- WM_QUERYUISTATE menus de mensagens e outros recursos
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
ms.openlocfilehash: f1574fe0dab2a0885c8012bf19eed50facfd6cce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105763871"
---
# <a name="wm_queryuistate-message"></a>Mensagem do WM \_ QUERYUISTATE

Um aplicativo envia a mensagem do **WM \_ QUERYUISTATE** para recuperar o estado da interface do usuário para uma janela.


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

## <a name="return-value"></a>Retornar valor

O valor de retorno será **nulo** se os indicadores de foco e os aceleradores de teclado estiverem visíveis. Caso contrário, o valor de retorno poderá ser um ou mais dos valores a seguir.



| Código/valor de retorno                                                                                                                                       | Descrição                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**UISF \_ ATIVO**</dt> <dt>0x4</dt> </dl>    | Um controle deve ser desenhado no estilo usado para controles ativos.<br/> |
| <dl> <dt>**UISF \_**</dt> <dt>0x2</dt> HIDEACCEL </dl> | Os aceleradores de teclado estão ocultos.<br/>                                |
| <dl> <dt>**UISF \_ HIDEFOCUS**</dt> <dt>0x1</dt> </dl> | Os indicadores de foco estão ocultos.<br/>                                     |



 

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

[**CHANGEUISTATE do WM \_**](wm-changeuistate.md)
</dt> <dt>

[**UPDATEUISTATE do WM \_**](wm-updateuistate.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Aceleradores de teclado](keyboard-accelerators.md)
</dt> </dl>

 

 





