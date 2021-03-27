---
description: SFVM \_ DIDDRAGDROP pode ser alterado ou indisponível.
ms.assetid: 5d37cf61-d8a7-4afa-9159-fea13d2b1d59
title: Mensagem de SFVM_DIDDRAGDROP (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 025bcf6320b014ff31b0819f394dd8b76fa90e59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104989042"
---
# <a name="sfvm_diddragdrop-message"></a>\_Mensagem SFVM DIDDRAGDROP

\[**SFVM \_ O DIDDRAGDROP** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.\]

Notifica a função de retorno de chamada que uma operação de arrastar e soltar começou. Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_DIDDRAGDROP 
    wParam = (WPARAM)(DWORD) dwEffect;
    lParam = (LPARAM)(IDataObject*) pIdo;
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwEffect* \[ no\]
</dt> <dd>

Um especificador de efeito de soltar da enumeração [**DROPEFFECT**](../com/dropeffect-constants.md) . Isso é obtido chamando [**SHDoDragDrop**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shdodragdrop).

</dd> <dt>

*pIdo* \[ no\]
</dt> <dd>

Um ponteiro para a instância [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                |
| Fim do suporte do cliente<br/>    | Windows XP com SP2<br/>                                                      |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                                                      |
| parâmetro<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
