---
title: Mensagem de WM_CHANGECBCHAIN (WinUser. h)
description: Enviado para a primeira janela na cadeia do Visualizador da área de transferência quando uma janela está sendo removida da cadeia. Uma janela recebe essa mensagem por meio de sua função WindowProc.
ms.assetid: 7be87342-87fa-4cd2-b066-0b36b7ef52f5
keywords:
- Troca de dados de mensagem WM_CHANGECBCHAIN
topic_type:
- apiref
api_name:
- WM_CHANGECBCHAIN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ab91640320e3659d0e9fb130f5c773ccbb7c4e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085692"
---
# <a name="wm_changecbchain-message"></a>Mensagem do WM \_ CHANGECBCHAIN

Enviado para a primeira janela na cadeia do Visualizador da área de transferência quando uma janela está sendo removida da cadeia.

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_CHANGECBCHAIN                0x030D
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um identificador para a janela que está sendo removida da cadeia do Visualizador da área de transferência.

</dd> <dt>

*lParam* 
</dt> <dd>

Um identificador para a próxima janela na cadeia após a janela que está sendo removida. Esse parâmetro será **nulo** se a janela que está sendo removida for a última janela na cadeia.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se um aplicativo processar essa mensagem, ele deverá retornar zero.

## <a name="remarks"></a>Comentários

Cada janela do Visualizador da área de transferência salva o identificador na próxima janela da cadeia do Visualizador da área de transferência. Inicialmente, esse identificador é o valor de retorno da função [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) .

Quando uma janela do Visualizador da área de transferência recebe a mensagem **\_ CHANGECBCHAIN do WM** , ela deve chamar a função [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) para passar a mensagem para a próxima janela na cadeia, a menos que a janela seguinte esteja sendo removida. Nesse caso, o Visualizador da área de transferência deve salvar o identificador especificado pelo parâmetro *lParam* como a próxima janela na cadeia.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

**Referência**
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Área de transferência](clipboard.md)
</dt> </dl>

 

