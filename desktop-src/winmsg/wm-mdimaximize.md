---
description: Um aplicativo envia a mensagem do WM \_ MDIMAXIMIZE para uma janela de cliente MDI (interface de vários documentos) para maximizar uma janela filho MDI.
ms.assetid: 7c5e4157-13f6-40d7-a64a-076bd14aca0d
title: Mensagem de WM_MDIMAXIMIZE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8372bcb25f35a52793292de4fd94a4a9dadafe6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105772713"
---
# <a name="wm_mdimaximize-message"></a>Mensagem do WM \_ MDIMAXIMIZE

Um aplicativo envia a mensagem do **WM \_ MDIMAXIMIZE** para uma janela de cliente MDI (interface de vários documentos) para maximizar uma janela filho MDI. O sistema redimensiona a janela filho para que sua área cliente preencha a janela do cliente. O sistema coloca o ícone do menu de janela da janela filho na posição mais à direita da barra de menus da janela do quadro e coloca o ícone de restauração da janela filho na posição mais à esquerda. O sistema também acrescenta o texto da barra de título da janela filho ao da janela do quadro.


```C++
#define WM_MDIMAXIMIZE                  0x0225
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um identificador para a janela filho MDI a ser maximizado.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **zero**

O valor de retorno é sempre zero.

## <a name="remarks"></a>Comentários

Se uma janela do cliente MDI receber qualquer mensagem que altere a ativação de suas janelas filhas enquanto a janela filho MDI ativa no momento for maximizada, o sistema restaurará a janela filho ativa e maximizará a janela filho ativada recentemente.

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

[**MDIRESTORE do WM \_**](wm-mdirestore.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Interface de vários documentos](multiple-document-interface.md)
</dt> </dl>

 

 




