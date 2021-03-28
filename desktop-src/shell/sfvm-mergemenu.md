---
description: 'Permite que o objeto de retorno de chamada mescle itens de menu nos menus do Windows Explorer. Usado por IShellFolderViewCB:: MessageSFVCB.'
title: Mensagem de SFVM_MERGEMENU (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 59bb99a3-9a5a-4ea5-9830-b04d7d886b3f
api_name:
- SFVM_MERGEMENU
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5cf95a7576c15ab1c3e64ebe55e244feffa6d86d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968220"
---
# <a name="sfvm_mergemenu-message"></a>\_Mensagem SFVM MERGEMENU

Permite que o objeto de retorno de chamada mescle itens de menu nos menus do Windows Explorer. Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_MERGEMENU 

    lParam = (LPARAM)(LPQCMINFO) pInfo;

            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pInfo* \[ fora\]
</dt> <dd>

Uma estrutura [**QCMINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo) que contém as informações necessárias para mesclar os itens no menu.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa mensagem serve essencialmente a mesma finalidade que [**IShellBrowser:: InsertMenusSB**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-insertmenussb) e [**IShellBrowser:: SetMenuSB**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-setmenusb) em uma exibição de pasta personalizada. Consulte a seção *usando o IShellBrowser para se comunicar com o Windows Explorer* de [implementando uma exibição de pasta](../lwef/nse-folderview.md) para uma discussão adicional.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
