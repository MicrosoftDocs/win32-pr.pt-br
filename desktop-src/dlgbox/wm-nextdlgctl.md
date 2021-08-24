---
title: Mensagem de WM_NEXTDLGCTL (WinUser. h)
description: Enviado a um procedimento de caixa de diálogo para definir o foco do teclado para um controle diferente na caixa de diálogo.
ms.assetid: 63d9fac2-3057-4bfa-9960-911fd18877d4
keywords:
- Caixas de diálogo de WM_NEXTDLGCTL mensagem
topic_type:
- apiref
api_name:
- WM_NEXTDLGCTL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a14de889e614aaba28757716326bcd1cf843aed64fe2dc58ca86430d65db628
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606216"
---
# <a name="wm_nextdlgctl-message"></a>Mensagem do WM \_ NEXTDLGCTL

Enviado a um procedimento de caixa de diálogo para definir o foco do teclado para um controle diferente na caixa de diálogo.


```C++
#define WM_NEXTDLGCTL                   0x0028
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Se *lParam* for **true**, esse parâmetro identificará o controle que recebe o foco. Se *lParam* for **false**, esse parâmetro indicará se o controle seguinte ou anterior com o estilo **WS \_ TabStop** receberá o foco. Se *wParam* for zero, o próximo controle receberá o foco; caso contrário, o controle anterior com o estilo **WS \_ TabStop** receberá o foco.

</dd> <dt>

*lParam* 
</dt> <dd>

A palavra de ordem inferior indica como o sistema usa *wParam*. Se a palavra de ordem inferior for **verdadeira**, *wParam* é um identificador associado ao controle que recebe o foco; caso contrário, *wParam* é um sinalizador que indica se o controle seguinte ou anterior com o estilo **WS \_ TabStop** recebe o foco.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Um aplicativo deve retornar zero se ele processar essa mensagem.

## <a name="remarks"></a>Comentários

Essa mensagem executa operações de gerenciamento de caixa de diálogo adicionais além daquelas executadas pela função [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) do **WM \_ NEXTDLGCTL** atualiza a borda de pressão padrão, define o identificador de controle padrão e seleciona automaticamente o texto de um controle de edição (se a janela de destino for um controle de edição).

Não use a função [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) para enviar uma mensagem do **WM \_ NEXTDLGCTL** se seu aplicativo processar simultaneamente outras mensagens que definirem o foco. Em vez disso, use a função [**CreateMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) .

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

[**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Caixas de diálogo](dialog-boxes.md)
</dt> </dl>

 

