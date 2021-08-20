---
title: TB_SETBUTTONSIZE mensagem (Commctrl.h)
description: Define o tamanho dos botões em uma barra de ferramentas.
ms.assetid: ef6beed7-a3d6-4379-b9c1-c64a5e33ce78
keywords:
- TB_SETBUTTONSIZE controles Windows mensagem
topic_type:
- apiref
api_name:
- TB_SETBUTTONSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58b0b957ad6328515da7aee2f978870662801aa6aba81133e9e4bc22ee7d9c92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167725"
---
# <a name="tb_setbuttonsize-message"></a>Mensagem TB \_ SETBUTTONSIZE

Define o tamanho dos botões em uma barra de ferramentas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

A [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica a largura, em pixels, dos botões. O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica a altura, em pixels, dos botões.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **TRUE se** for bem-sucedido ou FALSE **caso** contrário.

## <a name="remarks"></a>Comentários

**TB \_ SETBUTTONSIZE** geralmente deve ser chamado depois de adicionar botões.

Use [**TB \_ SETBUTTONWIDTH**](tb-setbuttonwidth.md) para definir as larguras máximas e mínimas permitidas para os botões antes que eles sejam adicionados. Use **TB \_ SETBUTTONSIZE** para definir o tamanho real dos botões.

## <a name="examples"></a>Exemplos

O código de exemplo a seguir define a largura dos botões como 80 pixels e a altura como 30 pixels.


```C++
// hWndToolbar is a handle to the toolbar window.
SendMessage(hWndToolbar, TB_SETBUTTONSIZE, 0, MAKELPARAM(80, 30);
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

