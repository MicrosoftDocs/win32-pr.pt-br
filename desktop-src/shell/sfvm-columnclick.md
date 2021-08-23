---
description: Notifica o objeto de retorno de chamada de que o usuário clicou em um header de coluna para classificar a lista de objetos na exibição de pasta. Usado por IShellFolderViewCB::MessageSFVCB.
title: SFVM_COLUMNCLICK mensagem (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 351be842-6ea5-4223-8162-0e6c4e6a5afb
api_name:
- SFVM_COLUMNCLICK
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d5ebd98ebc887d26bcee4799ffa3412df803fd0dfa099ac41bc69e1c25d83f06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592696"
---
# <a name="sfvm_columnclick-message"></a>Mensagem SFVM \_ COLUMNCLICK

Notifica o objeto de retorno de chamada de que o usuário clicou em um header de coluna para classificar a lista de objetos na exibição de pasta. Usado por [**IShellFolderViewCB::MessageSFVCB.**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)


```C++
SFVM_COLUMNCLICK 

    wParam = (WPARAM)(UINT)iColumn;

            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*iColumn* \[ Em\]
</dt> <dd>

O índice da coluna que foi clicada.

</dd> </dl>

## <a name="remarks"></a>Comentários

Em resposta a essa notificação, você deve retornar S \_ OK para reorganizar a lista por conta própria. Para que o objeto de exibição de pasta do sistema reorganize a lista, retorne S \_ FALSE.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
