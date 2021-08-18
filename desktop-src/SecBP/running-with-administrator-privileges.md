---
description: Para ajudar a evitar ataques mal-intencionados, determine se seu aplicativo requer privilégios de administrador. para funções que exigem permissões de administrador, crie um aplicativo separado e use o comando de linha de comando Windows RunAs.
ms.assetid: afa520fc-c206-49de-8d73-8f6566ec4fb6
title: Executando com privilégios de administrador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87533e71fbce613ff01ec2cf4670f1632d46786eb2a5b77900f950357a9eaa8a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622716"
---
# <a name="running-with-administrator-privileges"></a>Executando com privilégios de administrador

A primeira etapa para estabelecer o tipo de conta em que seu aplicativo precisa ser executado é examinar quais recursos o aplicativo usará e quais APIs com privilégios ele chamará. Você pode achar que o aplicativo, ou partes grandes, não exigem privilégios de administrador. *Escrever código seguro*, de Michael Howard e David LeBlanc, oferece uma descrição excelente de como realizar essa avaliação e é altamente recomendável. (Esse recurso pode não estar disponível em alguns idiomas e países.)

Você pode fornecer os privilégios de que seu aplicativo precisa com menos exposição a um ataque mal-intencionado usando uma das seguintes abordagens:

-   Execute sob uma conta com menos privilégios. Uma maneira de fazer isso é usar [**PrivilegeCheck**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-privilegecheck) para determinar quais privilégios estão habilitados em um token. Se os privilégios disponíveis não forem adequados para a operação atual, você poderá desabilitar esse código e solicitar que o usuário faça logon em uma conta com privilégios de administrador.
-   Quebra em uma função de aplicativo separada que exige permissões de administrador. Você pode fornecer ao usuário um atalho que execute o comando RunAs. Para obter instruções detalhadas sobre como configurar o atalho, pesquise "runas" na ajuda. Programaticamente, você pode configurar o comando [runas](/windows/desktop/com/runas) na chave do registro da [chave AppID](/windows/desktop/com/appid-key) para seu aplicativo.
-   Autentique o usuário chamando [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) (GUI) ou [**CredUICmdLinePromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduicmdlinepromptforcredentialsa) (linha de comando) para obter o nome de usuário e a senha. Para obter um exemplo, consulte [solicitando credenciais ao usuário](asking-the-user-for-credentials.md).
-   Representar o usuário. Um processo que inicia sob uma conta altamente privilegiada, como o sistema, pode representar uma conta de usuário chamando [**ImpersonateLoggedOnUser**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) ou funções de representação semelhantes, reduzindo assim o nível de privilégio. No entanto, se uma chamada para [**RevertToSelf**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-reverttoself) for injetada no thread, o processo retornará aos privilégios do sistema original.

Se você determinou que seu aplicativo deve ser executado em uma conta com privilégios de administrador e que uma senha de administrador deve ser armazenada no sistema de software, consulte [tratamento de senhas](handling-passwords.md) para métodos de fazer isso com segurança.

 

 
