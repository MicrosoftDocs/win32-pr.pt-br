---
description: Um aplicativo envia a mensagem WM MDIDESTROY para uma janela de cliente \_ MDI (interface MDI) para fechar uma janela filho MDI.
ms.assetid: b415393d-a5c2-4b70-af18-0dc7b3939a47
title: WM_MDIDESTROY mensagem (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 232514831defe3c65cdce66a5e1c7348ad4f80508eb01615572b7aa5b7d8e9c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119772056"
---
# <a name="wm_mdidestroy-message"></a>Mensagem \_ MDIDESTROY wm

Um aplicativo envia a **mensagem WM \_ MDIDESTROY** para uma janela de cliente MDI (interface MDI) para fechar uma janela filho MDI.


```C++
#define WM_MDIDESTROY                   0x0221
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um alça para a janela filho MDI a ser fechada.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **zero**

Essa mensagem sempre retorna zero.

## <a name="remarks"></a>Comentários

Essa mensagem remove o título da janela filho MDI da janela de quadro MDI e desativa a janela filho. Um aplicativo deve usar essa mensagem para fechar todas as janelas filho MDI.

Se uma janela de cliente MDI receber uma mensagem que altera a ativação de suas janelas filho e a janela filho MDI ativa estiver maximizada, o sistema restaurará a janela filho ativa e maximizará a janela filho recém-ativada.

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

[**WM \_ MDICREATE**](wm-mdicreate.md)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Interface de vários documentos](multiple-document-interface.md)
</dt> </dl>

 

 




