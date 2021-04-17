---
title: Mensagem de TB_SETBUTTONSIZE (commctrl. h)
description: Define o tamanho dos botões em uma barra de ferramentas.
ms.assetid: ef6beed7-a3d6-4379-b9c1-c64a5e33ce78
keywords:
- Controles de TB_SETBUTTONSIZE de mensagens do Windows
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
ms.openlocfilehash: 5db17b943c8a7cc8e71735d08718ece02a8c2582
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105754804"
---
# <a name="tb_setbuttonsize-message"></a>TB \_ SETbuttonse mensagem

Define o tamanho dos botões em uma barra de ferramentas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica a largura, em pixels, dos botões. O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica a altura, em pixels, dos botões.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

**TB \_ Setbuttonse** deve ser geralmente chamado após a adição de botões.

Use [**TB \_ SETBUTTONWIDTH**](tb-setbuttonwidth.md) para definir as larguras máximas e mínimas permitidas para botões antes de serem adicionadas. Use **TB \_ SetButtons** para definir o tamanho real dos botões.

## <a name="examples"></a>Exemplos

O código de exemplo a seguir define a largura dos botões como 80 pixels e a altura como 30 pixels.


```C++
// hWndToolbar is a handle to the toolbar window.
SendMessage(hWndToolbar, TB_SETBUTTONSIZE, 0, MAKELPARAM(80, 30);
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

