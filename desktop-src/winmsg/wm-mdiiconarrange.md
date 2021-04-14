---
description: Um aplicativo envia a mensagem do WM \_ MDIICONARRANGE para uma janela de cliente de interface de vários documentos (MDI) para organizar todas as janelas filho MDI minimizadas. Ele não afeta as janelas filhas que não são minimizadas.
ms.assetid: 935b9e29-224d-449e-b89f-b6062bed7702
title: Mensagem de WM_MDIICONARRANGE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc2d50d4bccebe3e9758752cc7d0d259e973875c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461068"
---
# <a name="wm_mdiiconarrange-message"></a>Mensagem do WM \_ MDIICONARRANGE

Um aplicativo envia a mensagem do **WM \_ MDIICONARRANGE** para uma janela de cliente de interface de vários documentos (MDI) para organizar todas as janelas filho MDI minimizadas. Ele não afeta as janelas filhas que não são minimizadas.


```C++
#define WM_MDIICONARRANGE               0x0228
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Esse parâmetro não é usado; Ele deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Esse parâmetro não é usado; Ele deve ser zero.

</dd> </dl>

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

[**MDICASCADE do WM \_**](wm-mdicascade.md)
</dt> <dt>

[**MDITILE do WM \_**](wm-mditile.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Interface de vários documentos](multiple-document-interface.md)
</dt> </dl>

 

 




