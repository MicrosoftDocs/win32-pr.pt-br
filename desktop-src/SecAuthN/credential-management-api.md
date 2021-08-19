---
description: API de gerenciamento de credenciais
ms.assetid: e393041b-f10c-4053-bc6c-65a89f40e74f
title: API de gerenciamento de credenciais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a290cf9d7e5a2d527368c2fd7350fa1bb9549af862c7da7c3845ceae9efc8aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008834"
---
# <a name="credential-management-api"></a>API de gerenciamento de credenciais

As funções de gerenciamento de credenciais constituem o conjunto de funções que um Gerenciador de credenciais deve implementar. Eles são:

-   [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify), uma função de manipulador de eventos que o MPR chama quando um usuário faz logon.
-   [**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify), uma função de manipulador de eventos que o MPR chama quando uma senha de conta é alterada.

As funções de gerenciamento de credenciais são sempre chamadas no contexto do sistema (LocalSystem) em vez do contexto do usuário.

Para obter mais informações sobre como criar e registrar um aplicativo Gerenciador de credenciais, consulte [implementando um Gerenciador de credenciais](implementing-a-credential-manager.md) e [registrando provedores de rede e gerenciadores de credenciais](registering-network-providers-and-credential-managers.md).

 

 



