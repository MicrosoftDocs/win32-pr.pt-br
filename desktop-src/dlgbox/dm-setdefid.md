---
title: Mensagem de DM_SETDEFID (WinUser. h)
description: Altera o identificador do botão de ação padrão de uma caixa de diálogo.
ms.assetid: 30720fa1-48cb-42d4-8370-87bdbaa34600
keywords:
- Caixas de diálogo de DM_SETDEFID mensagem
topic_type:
- apiref
api_name:
- DM_SETDEFID
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92749cc7eca569b57d239a36bb6559e59a6a7ebc31c63787a93d0720b334d1ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119741746"
---
# <a name="dm_setdefid-message"></a>\_Mensagem DM SETDEFID

Altera o identificador do botão de ação padrão de uma caixa de diálogo.


```C++
#define WM_USER              0x0400
#define DM_SETDEFID         (WM_USER+1)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O identificador de um controle de botão de ação que se tornará o padrão.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é sempre **verdadeiro**.

## <a name="remarks"></a>Comentários

Essa mensagem é processada pela função [**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw) . Para definir o botão de ação padrão, a função pode enviar mensagens do [**WM \_ GETDLGCODE**](wm-getdlgcode.md) e do [**BM \_ SetStyle**](../controls/bm-setstyle.md) para o controle especificado e o botão de push padrão atual.

O uso da mensagem **DM \_ SETDEFID** pode fazer com que mais de um botão pareça ter o estado padrão do botão de ação. Quando o sistema abre uma caixa de diálogo, ele desenha o primeiro botão de ação no modelo de caixa de diálogo com a borda de estado padrão. O envio de uma mensagem **DM \_ SETDEFID** para alterar o botão padrão nem sempre removerá a borda do estado padrão do primeiro botão de ação. Nesses casos, o aplicativo deve enviar uma mensagem [**\_ SetStyle BM**](../controls/bm-setstyle.md) para alterar o primeiro estilo de borda do botão de ação.

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

[**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw)
</dt> <dt>

[**\_GETDEFID DM**](dm-getdefid.md)
</dt> <dt>

[**GETDLGCODE do WM \_**](wm-getdlgcode.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Caixas de diálogo](dialog-boxes.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**SetStyle BM \_**](../controls/bm-setstyle.md)
</dt> <dt>

[**em \_ SETLIMITTEXT**](../controls/em-setlimittext.md)
</dt> </dl>

 

