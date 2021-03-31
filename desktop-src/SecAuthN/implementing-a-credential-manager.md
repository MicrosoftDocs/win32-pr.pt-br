---
description: Lista as exportações de DLL que devem ser implementadas para criar um Gerenciador de credenciais.
ms.assetid: 8b176dd6-0e0b-4330-8889-f87384977ceb
title: Implementando um Gerenciador de credenciais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0bbd42f4ade57b754c6f7a067519d7df2711cfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829761"
---
# <a name="implementing-a-credential-manager"></a>Implementando um Gerenciador de credenciais

Para criar um Gerenciador de credenciais, você deve criar uma DLL que exporta as seguintes funções:

-   [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify)
-   [**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify)

Para restaurar as notificações para as funções [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify) e [**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify) para logon de cartão inteligente, crie uma entrada de registro chamada **SmartCardLogonNotify** como uma **DWORD** e defina-a como 1:

```
HKEY_LOCAL_MACHINE
   Software
   Microsoft
   Windows NT
   CurrentVersion
      Winlogon
         Notify
            SmartCardLogonNotify = 1
```

**Windows Server 2003 e Windows XP:** A entrada do registro **SmartCardLogonNotify** não é necessária.

Além disso, os gerenciadores de credenciais também devem dar suporte à função [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) para o WNNC \_ Iniciar (o suporte a outros índices não é necessário para os gerenciadores de credenciais). Isso informa ao MPR quando um Gerenciador de credenciais será iniciado. Chamando **NPGetCaps** com o parâmetro *NINDEX* definido como WNNC \_ Start, o MPR Obtém o tempo de espera antes de chamar as funções do ponto de entrada de gerenciamento de credenciais do provedor. E se o MPR tiver essas informações, ela poderá encaminhá-la ao Gerenciador de credenciais, definindo o tempo limite.

 

 



