---
description: 'Notifica o objeto de retorno de chamada que a barra de status está sendo atualizada. Usado por IShellFolderViewCB:: MessageSFVCB.'
title: Mensagem de SFVM_UPDATESTATUSBAR (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: f1bac364-1011-4308-8b9b-8ed1800dd30d
api_name:
- SFVM_UPDATESTATUSBAR
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 14045c797d7292099c1c7b2c67f5958609d8d6b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104989016"
---
# <a name="sfvm_updatestatusbar-message"></a>\_Mensagem SFVM UPDATESTATUSBAR

Notifica o objeto de retorno de chamada que a barra de status está sendo atualizada. Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_UPDATESTATUSBAR 

    wParam = (WPARAM)(BOOL) fInitialize;

            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*fInitialize* \[ no\]
</dt> <dd>

Um valor **bool** que será definido como **true** se a barra de status estiver sendo inicializada.

</dd> </dl>

## <a name="remarks"></a>Comentários

Quando você receber esta notificação:

-   Retorne \_ os S ok se você for manipular a atualização.
-   Retorne MAKE \_ HRESULT ( \_ êxito de severidade, 0, 1) para que o objeto de exibição da pasta do sistema defina o texto da barra de status.
-   Return E \_ falha ao fazer com que o objeto de exibição da pasta do sistema manipule a barra de status.

O texto da barra de status padrão é o seguinte.



| Status                      | Texto da barra de status                         |
|-----------------------------|-----------------------------------------|
| Nenhum item selecionado           | " \# \# Objects" (na pasta)          |
| Um item selecionado           | O InfoTip do item, se disponível. |
| Mais de um item selecionado | " \# \# objetos selecionados"                 |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
