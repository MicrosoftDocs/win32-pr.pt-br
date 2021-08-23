---
description: SFVM \_ THISIDLIST pode ser alterado ou indisponível.
ms.assetid: 488f696d-aa71-4727-bbd2-c99e7d245d85
title: Mensagem de SFVM_THISIDLIST (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd00f1cfc2b6661dac2414f0327cab03d4c0586eb62b992b5e33f81e64565246
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968625"
---
# <a name="sfvm_thisidlist-message"></a>\_Mensagem SFVM THISIDLIST

\[**SFVM \_ O THISIDLIST** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.\]

Permite que o objeto de retorno de chamada especifique o ponteiro da exibição para uma lista de identificadores de item (PIDL). Isso é usado somente quando [**IPersistIDList:: SetIDList**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistidlist-setidlist) e [**IPersistFolder2:: GetCurFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder2-getcurfolder) falharam. Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_THISIDLIST
    lParam = (LPARAM)(LPITEMIDLIST*) pidl;
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PIDL* \[ fora\]
</dt> <dd>

O endereço do PIDL da exibição.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                |
| Fim do suporte do cliente<br/>    | Windows XP com SP2<br/>                                                      |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
