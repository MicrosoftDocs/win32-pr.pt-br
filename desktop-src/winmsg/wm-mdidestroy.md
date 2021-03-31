---
description: Um aplicativo envia a mensagem do WM \_ MDIDESTROY para uma janela de cliente MDI (interface de vários documentos) para fechar uma janela filho MDI.
ms.assetid: b415393d-a5c2-4b70-af18-0dc7b3939a47
title: Mensagem de WM_MDIDESTROY (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edea8fe8dadc691ca912df4e9ee5d57421124bcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647077"
---
# <a name="wm_mdidestroy-message"></a>Mensagem do WM \_ MDIDESTROY

Um aplicativo envia a mensagem do **WM \_ MDIDESTROY** para uma janela de cliente MDI (interface de vários documentos) para fechar uma janela filho MDI.


```C++
#define WM_MDIDESTROY                   0x0221
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um identificador para a janela filho MDI a ser fechado.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **zero**

Essa mensagem sempre retorna zero.

## <a name="remarks"></a>Comentários

Essa mensagem remove o título da janela filho MDI da janela do quadro MDI e desativa a janela filho. Um aplicativo deve usar essa mensagem para fechar todas as janelas filhas MDI.

Se uma janela do cliente MDI receber uma mensagem que altera a ativação de suas janelas filhas e a janela filho MDI ativa for maximizada, o sistema restaura a janela filho ativa e maximiza a janela filho ativada recentemente.

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

[**MDICREATE do WM \_**](wm-mdicreate.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Interface de vários documentos](multiple-document-interface.md)
</dt> </dl>

 

 




