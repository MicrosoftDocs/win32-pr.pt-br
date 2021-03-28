---
description: SFVM \_ QUERYFSNOTIFY pode ser alterado ou indisponível.
ms.assetid: 5d777115-bae3-47c4-9edc-c99c40a4f926
title: Mensagem de SFVM_QUERYFSNOTIFY (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a4416bda249e3ec0f2a0c0f2d45ac353961e180
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172074"
---
# <a name="sfvm_queryfsnotify-message"></a>\_Mensagem SFVM QUERYFSNOTIFY

\[**SFVM \_ O QUERYFSNOTIFY** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.\]

Permite que o objeto de retorno de chamada registre uma pasta para que as alterações na exibição dessa pasta gerem notificações. Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_QUERYFSNOTIFY 
    lParam = (LPARAM)(SHChangeNotifyEntry*) shcne;
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*shcne* \[ entrada, saída\]
</dt> <dd>

Uma estrutura para manter o PIDL do item para observar eventos e uma indicação se as subpastas desse item também devem ser observadas.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                |
| Fim do suporte do cliente<br/>    | Windows XP com SP2<br/>                                                      |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                                                      |
| parâmetro<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
