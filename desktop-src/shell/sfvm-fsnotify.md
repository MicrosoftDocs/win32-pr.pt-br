---
description: 'Notifica o objeto de retorno de chamada que um evento executou que afeta um de seus itens. Usado por IShellFolderViewCB:: MessageSFVCB.'
title: Mensagem de SFVM_FSNOTIFY (shlobj. h)
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
ms.openlocfilehash: 74c17f9d4b8c8c1979fa7da2d6f0ff63dff74a9b
ms.sourcegitcommit: cd9672511263d04c0e4bc41758dd1d9e89ea92b4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2021
ms.locfileid: "104989118"
---
# <a name="sfvm_fsnotify-message"></a>\_Mensagem SFVM FSNOTIFY

Notifica o objeto de retorno de chamada que um evento executou que afeta um de seus itens. Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_FSNOTIFY 

    wParam = (WPARAM)(LPCITEMIDLIST*) ppidl;

    lParam = (LPARAM)(DWORD) lEvent;

            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppidl* \[ no\]
</dt> <dd>

O ponteiro de PIDL do item afetado.

</dd> <dt>

*Levent* \[ no\]
</dt> <dd>

Um valor SHCNE que indica qual evento ocorreu. Para obter uma lista de valores possíveis, consulte [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
