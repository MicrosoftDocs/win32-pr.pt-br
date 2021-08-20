---
description: Notifica o objeto de retorno de chamada de que ocorreu um evento que afeta um de seus itens. Usado por IShellFolderViewCB::MessageSFVCB.
title: SFVM_FSNOTIFY mensagem (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: ff159c35-afdf-4147-8dd6-7febd9519b18
api_name:
- SFVM_FSNOTIFY
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 93aab69cd4d4a49cc9af4601c22196d498f16e281639b96feda2d1e857fdca72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118048658"
---
# <a name="sfvm_fsnotify-message"></a>Mensagem FSNOTIFY do SFVM \_

Notifica o objeto de retorno de chamada de que ocorreu um evento que afeta um de seus itens. Usado por [**IShellFolderViewCB::MessageSFVCB.**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)


```C++
SFVM_FSNOTIFY 

    wParam = (WPARAM)(LPCITEMIDLIST*) ppidl;

    lParam = (LPARAM)(DWORD) lEvent;

            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppidl* \[ Em\]
</dt> <dd>

O ponteiro de PIDL do item afetado.

</dd> <dt>

*lEvent* \[ Em\]
</dt> <dd>

Um valor SHCNE que indica qual evento ocorreu. Para ver uma lista de valores possíveis, [**consulte SHChangeNotify.**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify)

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
