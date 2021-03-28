---
description: Enviado para a janela do proprietário de um controle ou item de menu quando o controle ou o menu é criado.
ms.assetid: 4584a3da-6c92-4ecd-8cf2-e4afc1b8321d
title: Mensagem de DFM_WM_MEASUREITEM (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61c4ad79acf221ecaabf9060940ad2514422bef1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370609"
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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                      |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
