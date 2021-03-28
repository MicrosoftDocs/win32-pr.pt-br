---
description: 'Notifica o objeto de retorno de chamada do site de contêiner. Isso é usado somente quando IObjectWithSite:: SetSite não tem suporte e SHCreateShellFolderViewEx é usado. Usado por IShellFolderViewCB:: MessageSFVCB.'
ms.assetid: a4aa40f8-1d98-4686-86e2-87280e470aac
title: Mensagem de SFVM_SETISFV (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83021f1d6d52286f08e8ec7bd51bbaa806c17c7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968232"
---
# <a name="sfvm_setisfv-message"></a>\_Mensagem SFVM SETISFV

\[Essa notificação é suportada por meio do Windows XP Service Pack 2 (SP2) e do Windows Server 2003. Ele pode não ter suporte em versões subsequentes do Windows.\]

Notifica o objeto de retorno de chamada do site de contêiner. Isso é usado somente quando [**IObjectWithSite:: SetSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768221(v=vs.85)) não tem suporte e [**SHCreateShellFolderViewEx**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderviewex) é usado. Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_SETISFV
    lParam = (LPARAM)(IUnknown*) site;
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*site* \[ do no\]
</dt> <dd>

Um ponteiro para a interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) do site do contêiner.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
