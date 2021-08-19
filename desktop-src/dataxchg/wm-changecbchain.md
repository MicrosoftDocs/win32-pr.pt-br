---
title: WM_CHANGECBCHAIN mensagem (Winuser.h)
description: Enviado para a primeira janela na cadeia do visualizador da área de transferência quando uma janela está sendo removida da cadeia. Uma janela recebe essa mensagem por meio de sua função WindowProc.
ms.assetid: 7be87342-87fa-4cd2-b066-0b36b7ef52f5
keywords:
- WM_CHANGECBCHAIN dados de mensagem Exchange
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
ms.openlocfilehash: 25dac74784a214f77f8b2912e2fd643624ae767027121e2262d81989d54d3831
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736310"
---
# <a name="wm_changecbchain-message"></a>Mensagem WM \_ CHANGECBCHAIN

Enviado para a primeira janela na cadeia do visualizador da área de transferência quando uma janela está sendo removida da cadeia.

Uma janela recebe essa mensagem por meio de [**sua função WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_CHANGECBCHAIN                0x030D
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um alça para a janela que está sendo removida da cadeia do visualizador da área de transferência.

</dd> <dt>

*lParam* 
</dt> <dd>

Um alça para a próxima janela na cadeia após a janela que está sendo removida. Esse parâmetro será **NULL** se a janela que está sendo removida for a última janela na cadeia.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se um aplicativo processa essa mensagem, ele deve retornar zero.

## <a name="remarks"></a>Comentários

Cada janela do visualizador da área de transferência salva o alça para a próxima janela na cadeia do visualizador da área de transferência. Inicialmente, esse handle é o valor de retorno da [**função SetClipboardViewer.**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer)

Quando uma janela do visualizador da área de transferência recebe a mensagem **WM \_ CHANGECBCHAIN,** ela deve chamar a função [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) para passar a mensagem para a próxima janela na cadeia, a menos que a próxima janela seja a janela sendo removida. Nesse caso, o visualizador da área de transferência deve salvar o alça especificado pelo parâmetro *lParam* como a próxima janela na cadeia.

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

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**Setclipboardviewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Área de transferência](clipboard.md)
</dt> </dl>

 

