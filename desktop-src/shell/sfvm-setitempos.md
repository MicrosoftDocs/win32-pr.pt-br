---
description: Define a posição de um item na exibição do Shell. Usado pela \_ mensagem SHShellFolderView.
title: Mensagem de SFVM_SETITEMPOS (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: b89f2d62-095b-4cad-a47e-2d41e122cb3e
api_name:
- SFVM_SETITEMPOS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 450aeabee6e5edeba466e4a5fe64725c13eea32b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171870"
---
# <a name="sfvm_setitempos-message"></a>\_Mensagem SFVM SETITEMPOS

Define a posição de um item na exibição do Shell. Usado pela [**\_ mensagem SHShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).


```C++

                SFVM_SETITEMPOS 

    lParam = (LPSFV_SETITEMPOS)&sip;

            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*SIP* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura [**SFV \_ SETITEMPOS**](/windows/desktop/api/Shlobj/ns-shlobj-sfv_setitempos) .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP com SP1\]<br/>                                |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 




