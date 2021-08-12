---
title: WM_RENDERFORMAT mensagem (Winuser.h)
description: Enviado para o proprietário da área de transferência se ele tiver atrasado a renderização de um formato de área de transferência específico e se um aplicativo tiver solicitado dados nesse formato.
ms.assetid: 81638109-4c5e-4b4c-b2db-4208b6ee83cc
keywords:
- WM_RENDERFORMAT de dados de Exchange
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
# <a name="wm_renderformat-message"></a>Mensagem WM \_ RENDERFORMAT

Enviado para o proprietário da área de transferência se ele tiver atrasado a renderização de um formato de área de transferência específico e se um aplicativo tiver solicitado dados nesse formato. O proprietário da área de transferência deve renderizar dados no formato especificado e coloque-os na área de transferência chamando a [**função SetClipboardData.**](/windows/win32/api/winuser/nf-winuser-setclipboarddata)


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

Se um aplicativo processa essa mensagem, ele deve retornar zero.

## <a name="remarks"></a>Comentários

Ao responder a uma **mensagem WM \_ RENDERFORMAT,** o proprietário da área de transferência não deve abrir a área de transferência antes de [**chamar SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata). Abrir a área de transferência não é necessário antes de colocar dados em resposta ao **WM \_ RENDERFORMAT** e qualquer tentativa de abrir a área de transferência falhará porque a área de transferência está sendo mantida aberta no momento pelo aplicativo que solicitou que o formato fosse renderizado.

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

[**Setclipboarddata**](/windows/win32/api/winuser/nf-winuser-setclipboarddata)
</dt> <dt>

[**WM \_ RENDERALLFORMATS**](wm-renderallformats.md)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Área de transferência](clipboard.md)
</dt> </dl>

 

 





