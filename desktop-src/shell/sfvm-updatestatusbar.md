---
description: Notifica o objeto de retorno de chamada de que a barra de status está sendo atualizada. Usado por IShellFolderViewCB::MessageSFVCB.
title: SFVM_UPDATESTATUSBAR mensagem (Shlobj.h)
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
ms.openlocfilehash: 106782383b90af85dca82e445dfc21f77e0f3def73174da9147aadc988f2694e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883896"
---
# <a name="sfvm_updatestatusbar-message"></a>Mensagem SFVM \_ UPDATESTATUSBAR

Notifica o objeto de retorno de chamada de que a barra de status está sendo atualizada. Usado por [**IShellFolderViewCB::MessageSFVCB.**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)


```C++
SFVM_UPDATESTATUSBAR 

    wParam = (WPARAM)(BOOL) fInitialize;

            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*fInitialize* \[ Em\]
</dt> <dd>

Um **valor BOOL** definido como **TRUE se** a barra de status estiver sendo inicializada.

</dd> </dl>

## <a name="remarks"></a>Comentários

Quando você receber essa notificação:

-   Retorne S \_ OK se você manipular a atualização.
-   Retorne MAKE \_ HRESULT(SEVERITY SUCCESS,0,1) para que o objeto de exibição de pasta do sistema \_ defina o texto da barra de status.
-   Retornar E \_ FAIL para que o objeto de exibição de pasta do sistema manipular a barra de status.

O texto da barra de status padrão é o seguinte.



| Status                      | Texto da barra de status                         |
|-----------------------------|-----------------------------------------|
| Nenhum item selecionado           | \# \# "objects" (na pasta)          |
| Um item selecionado           | A infotip para o item, se disponível. |
| Mais de um item selecionado | "objetos \# \# selecionados"                 |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
