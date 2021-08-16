---
title: Mensagem de WM_RENDERFORMAT (WinUser. h)
description: Enviado ao proprietário da área de transferência se ele tiver um processamento atrasado em um formato de área de transferência específico e se um aplicativo tiver solicitado dados nesse formato.
ms.assetid: 81638109-4c5e-4b4c-b2db-4208b6ee83cc
keywords:
- WM_RENDERFORMAT Exchange de dados da mensagem
topic_type:
- apiref
api_name:
- WM_RENDERFORMAT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2885e056577656d6cabb8ea78f48a02a19f3c3c40bb3c30b1e5ca25c72cdf39b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118545305"
---
# <a name="wm_renderformat-message"></a>Mensagem do WM \_ RENDERFORMAT

Enviado ao proprietário da área de transferência se ele tiver um processamento atrasado em um formato de área de transferência específico e se um aplicativo tiver solicitado dados nesse formato. O proprietário da área de transferência deve renderizar dados no formato especificado e colocá-los na área de transferência chamando a função [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) .


```C++
#define WM_RENDERFORMAT                 0x0305
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O [formato da área de transferência](standard-clipboard-formats.md) a ser renderizado.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se um aplicativo processar essa mensagem, ele deverá retornar zero.

## <a name="remarks"></a>Comentários

Ao responder a uma mensagem do **WM \_ RENDERFORMAT** , o proprietário da área de transferência não deve abrir a área de transferência antes de chamar [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata). Não é necessário abrir a área de transferência antes de colocar dados em resposta ao **WM \_ RENDERFORMAT**, e qualquer tentativa de abrir a área de transferência falhará porque a área de transferência está sendo mantida no momento aberta pelo aplicativo que solicitou o formato a ser renderizado.

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

[**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata)
</dt> <dt>

[**RENDERALLFORMATS do WM \_**](wm-renderallformats.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Área de transferência](clipboard.md)
</dt> </dl>

 

 





