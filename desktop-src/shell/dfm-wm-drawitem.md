---
description: Enviado para a janela pai de um controle ou menu desenhado pelo proprietário quando um aspecto visual do controle ou menu foi alterado.
ms.assetid: 2515bbab-025f-4f00-8564-a732d68edea3
title: DFM_WM_DRAWITEM mensagem (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7190d445490b581967c8dda67e170eb5db5665dfa59302313d7af736b275944d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118969465"
---
# <a name="dfm_wm_drawitem-message"></a>Mensagem \_ DFM WM \_ DRAWITEM

Enviado para a janela pai de um controle ou menu desenhado pelo proprietário quando um aspecto visual do controle ou menu foi alterado.


```C++
DFM_WM_DRAWITEM 

    wParam = (WPARAM);

    lParam = (LPARAM)(LPDRAWITEMSTRUCT) lpDrawItem;

            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* \[ Em\]
</dt> <dd>

O identificador do controle que enviou a mensagem **\_ DFM WM \_ DRAWITEM.** Se a mensagem foi enviada por um menu, esse parâmetro é zero.

</dd> <dt>

*lpDrawItem* \[ out\]
</dt> <dd>

Um ponteiro para uma [**estrutura DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) que contém informações sobre o item a ser desenhado e o tipo de desenho necessário.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se um aplicativo processa essa mensagem, ele deve retornar **TRUE.**

## <a name="remarks"></a>Comentários

O **membro itemAction** da estrutura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) especifica a operação de desenho que um aplicativo deve executar.

Antes de retornar do processamento dessa mensagem, um aplicativo deve garantir que o contexto do dispositivo identificado pelo membro **hDC** da estrutura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) está no estado padrão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                      |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
