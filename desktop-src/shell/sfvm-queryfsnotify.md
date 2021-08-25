---
description: SFVM \_ QUERYFSNOTIFY pode ser alterado ou não disponível.
ms.assetid: 5d777115-bae3-47c4-9edc-c99c40a4f926
title: SFVM_QUERYFSNOTIFY mensagem (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 932650257ddb039e3841a583c3856316a86eca469db74a0e8ab6ebf33e9411f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941986"
---
# <a name="sfvm_queryfsnotify-message"></a>Mensagem SFVM \_ QUERYFSNOTIFY

\[**SFVM \_ QUERYFSNOTIFY** está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.\]

Permite que o objeto de retorno de chamada registre uma pasta para que as alterações na exibição dessa pasta gerem notificações. Usado por [**IShellFolderViewCB::MessageSFVCB.**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)


```C++
SFVM_QUERYFSNOTIFY 
    lParam = (LPARAM)(SHChangeNotifyEntry*) shcne;
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*shcne* \[ in, out\]
</dt> <dd>

Uma estrutura para manter o PIDL do item para observar eventos e uma indicação se as subpastas desse item também devem ser observadas.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                |
| Fim do suporte ao cliente<br/>    | Windows XP com SP2<br/>                                                      |
| Fim do suporte ao servidor<br/>    | Windows Server 2003<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
