---
description: Enviado para a janela do proprietário de um controle ou item de menu quando o controle ou o menu é criado.
ms.assetid: 4584a3da-6c92-4ecd-8cf2-e4afc1b8321d
title: Mensagem de DFM_WM_MEASUREITEM (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e7ad0d39a56f598a8ef4773c70f4f438388e91a2154b3083fdf85a1ebebec22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117860894"
---
# <a name="dfm_wm_measureitem-message"></a>Mensagem do DFM do \_ WM \_ MEASUREITEM

Enviado para a janela do proprietário de um controle ou item de menu quando o controle ou o menu é criado.


```C++
DFM_WM_MEASUREITEM 

    wParam = (WPARAM);

    lParam = (LPARAM)(LPMEASUREITEMSTRUCT) lpMeasureItem;

            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* \[ no\]
</dt> <dd>

O valor do membro **CtlID** da estrutura [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) apontada pelo parâmetro *lpMeasureItem* . Esse valor identifica o controle que enviou a mensagem **DFM do \_ WM \_ MEASUREITEM** .

</dd> <dt>

*lpMeasureItem* \[ fora\]
</dt> <dd>

Um ponteiro para uma estrutura [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) que contém as dimensões do controle ou item de menu desenhado pelo proprietário.

</dd> </dl>

## <a name="remarks"></a>Comentários

Quando a janela do proprietário recebe a mensagem **DFM do \_ WM \_ MEASUREITEM** , o proprietário preenche a estrutura [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) apontada pelo parâmetro *lpMeasureItem* da mensagem e retorna; isso informa o sistema das dimensões do controle.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                      |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
