---
description: Lista as exportações de DLL que devem ser implementadas para criar um gerenciador de credenciais.
ms.assetid: 8b176dd6-0e0b-4330-8889-f87384977ceb
title: Implementando um Gerenciador de Credenciais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1a1787fcf72d88ad809f904f9f83179ac86631b83a23314f9d24ee31ce3dec9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119482656"
---
# <a name="implementing-a-credential-manager"></a>Implementando um Gerenciador de Credenciais

Para criar um gerenciador de credenciais, você deve criar uma DLL que exporte as seguintes funções:

-   [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify)
-   [**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify)

Para restaurar notificações para as funções [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify) e [**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify) para logon de cartão inteligente, crie uma entrada do Registro chamada **SmartCardLogonNotify** como uma **DWORD** e de definido como 1:

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

**Windows Server 2003 e Windows XP:** A **entrada do Registro SmartCardLogonNotify** não é necessária.

Além disso, os gerenciadores de credenciais também devem dar suporte à função [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) para WNNC START (o suporte a outros índices não é necessário \_ para gerenciadores de credenciais). Isso informa à MPR quando um gerenciador de credenciais será iniciar. Ao chamar **NPGetCaps com** o parâmetro *nIndex* definido como WNNC START, a MPR obtém o tempo de espera antes de chamar as funções de ponto de entrada de gerenciamento de \_ credenciais do provedor. E se a MPR tiver essas informações, ela poderá encaminhá-la para o gerenciador de credenciais, definindo o tempo final.

 

 



