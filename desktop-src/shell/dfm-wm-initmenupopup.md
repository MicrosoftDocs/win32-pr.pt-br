---
description: DFM_WM_INITMENUPOPUP mensagem – enviada quando um menu suspenso ou submenu está prestes a se tornar ativo. Isso permite que um aplicativo modifique o menu antes de ser exibido, sem alterar o menu inteiro.
title: DFM_WM_INITMENUPOPUP mensagem (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 314e83f7-839d-4ca0-b5c1-842c5bf14923
api_name:
- DFM_WM_INITMENUPOPUP
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4cb68b8251fa383ae9386eae3e6753158330c4be7566f02a8758a72dfe05de03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943146"
---
# <a name="dfm_wm_initmenupopup-message"></a>Mensagem DFM \_ WM \_ INITMENUPOPUP

Enviado quando um menu suspenso ou submenu está prestes a se tornar ativo. Isso permite que um aplicativo modifique o menu antes de ser exibido, sem alterar o menu inteiro.


```C++
DFM_WM_INITMENUPOPUP 

    wParam = (WPARAM);

    lParam = (LPARAM);

            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* \[ Em\]
</dt> <dd>

Um alça para o menu suspenso ou submenu.

</dd> <dt>

*lParam* \[ Em\]
</dt> <dd>

A palavra de ordem baixa especifica a posição relativa baseada em zero do item de menu que abre o menu suspenso ou o submenu.

A palavra de ordem alta indica se o menu suspenso é o menu da janela. Se o menu for o menu da janela, esse parâmetro será **TRUE;** caso contrário, será **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se um aplicativo processa essa mensagem, ele deve retornar zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                      |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 




