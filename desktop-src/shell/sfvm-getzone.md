---
description: 'Permite que o objeto de retorno de chamada forneça informações de zona da Internet. Usado por IShellFolderViewCB:: MessageSFVCB.'
ms.assetid: 6fae7925-b1be-4270-9318-7fa517563dad
title: Mensagem de SFVM_GETZONE (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5586188aeab6a054e22e4b242039beaae1ce390d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506237"
---
# <a name="sfvm_getzone-message"></a>SFVM \_ mensagem GETzone

\[Essa notificação é suportada por meio do Windows XP Service Pack 2 (SP2) e do Windows Server 2003. Ele pode não ter suporte em versões subsequentes do Windows.\]

Permite que o objeto de retorno de chamada forneça informações de zona da Internet. Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_GETZONE
    lParam = (LPARAM)(DWORD*) zone;
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*zona* \[ do fora\]
</dt> <dd>

Um dos valores a seguir indicando a zona da Internet. Esses valores constituem a enumeração [**UrlZone**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537175(v=vs.85)) , definida em Urlmon. h.

<dt>

<span id="URLZONE_LOCAL_MACHINE"></span><span id="urlzone_local_machine"></span>

<span id="URLZONE_LOCAL_MACHINE"></span><span id="urlzone_local_machine"></span>**\_computador local \_ UrlZone**


</dt> <dd>

Zona usada para conteúdo que já está no computador local do usuário. Essa zona não é exposta pela interface do usuário.

</dd> <dt>

<span id="URLZONE_INTRANET"></span><span id="urlzone_intranet"></span>

<span id="URLZONE_INTRANET"></span><span id="urlzone_intranet"></span>**INTRANET do URLZONE \_**


</dt> <dd>

Zona usada para conteúdo encontrado em uma intranet.

</dd> <dt>

<span id="URLZONE_TRUSTED"></span><span id="urlzone_trusted"></span>

<span id="URLZONE_TRUSTED"></span><span id="urlzone_trusted"></span>**URLZONE \_ confiável**


</dt> <dd>

Zona usada para sites confiáveis na Internet.

</dd> <dt>

<span id="URLZONE_INTERNET"></span><span id="urlzone_internet"></span>

<span id="URLZONE_INTERNET"></span><span id="urlzone_internet"></span>**\_Internet UrlZone**


</dt> <dd>

Zona usada para a maior parte do conteúdo na Internet.

</dd> <dt>

<span id="URLZONE_UNTRUSTED"></span><span id="urlzone_untrusted"></span>

<span id="URLZONE_UNTRUSTED"></span><span id="urlzone_untrusted"></span>**URLZONE \_ não confiável**


</dt> <dd>

Zona usada para sites que não são confiáveis.

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
