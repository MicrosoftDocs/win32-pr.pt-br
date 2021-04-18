---
description: Um aplicativo envia a mensagem do WM \_ MDIRESTORE para uma janela de cliente MDI (interface de vários documentos) para restaurar uma janela filho MDI do tamanho maximizado ou minimizado.
ms.assetid: bb99fda1-9eb5-4307-9326-9a417a046c22
title: Mensagem de WM_MDIRESTORE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc2cf36a0b428e1e9003682a5e766f613fd7ba81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105796258"
---
# <a name="wm_mdirestore-message"></a>Mensagem do WM \_ MDIRESTORE

Um aplicativo envia a mensagem do **WM \_ MDIRESTORE** para uma janela de cliente MDI (interface de vários documentos) para restaurar uma janela filho MDI do tamanho maximizado ou minimizado.


```C++
#define WM_MDIRESTORE                   0x0223
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um identificador para a janela filho MDI a ser restaurado.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **zero**

O valor de retorno é sempre zero.

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

[**MDIMAXIMIZE do WM \_**](wm-mdimaximize.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Interface de vários documentos](multiple-document-interface.md)
</dt> </dl>

 

 




