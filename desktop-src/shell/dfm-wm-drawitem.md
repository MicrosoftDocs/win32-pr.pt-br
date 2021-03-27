---
description: Enviado para a janela pai de um controle ou menu desenhado pelo proprietário quando um aspecto visual do controle ou do menu é alterado.
ms.assetid: 2515bbab-025f-4f00-8564-a732d68edea3
title: Mensagem de DFM_WM_DRAWITEM (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67255fea5c39bebc995e5c53d90378536b12921b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967329"
---
# <a name="dfm_wm_drawitem-message"></a>Mensagem do DFM do \_ WM \_ DRAWITEM

Enviado para a janela pai de um controle ou menu desenhado pelo proprietário quando um aspecto visual do controle ou do menu é alterado.


```C++
DFM_WM_DRAWITEM 

    wParam = (WPARAM);

    lParam = (LPARAM)(LPDRAWITEMSTRUCT) lpDrawItem;

            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* \[ no\]
</dt> <dd>

O identificador do controle que enviou a mensagem **DFM do \_ WM \_ DRAWITEM** . Se a mensagem foi enviada por um menu, esse parâmetro será zero.

</dd> <dt>

*lpDrawItem* \[ fora\]
</dt> <dd>

Um ponteiro para uma estrutura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) que contém informações sobre o item a ser desenhado e o tipo de desenho necessário.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se um aplicativo processar essa mensagem, ele deverá retornar **true**.

## <a name="remarks"></a>Comentários

O membro de **ação** da estrutura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) especifica a operação de desenho que um aplicativo deve executar.

Antes de retornar do processamento dessa mensagem, um aplicativo deve garantir que o contexto do dispositivo identificado pelo membro **HDC** da estrutura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) esteja no estado padrão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                      |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
