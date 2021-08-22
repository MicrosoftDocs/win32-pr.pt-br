---
description: A conta LocalSystem é uma conta local predefinida usada pelo gerenciador de controle de serviço.
ms.assetid: 692bceb6-f5bd-4b83-ab3b-ef8099dc84e1
title: Conta localSystem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d4dca5655402b3b4f400d3c1941ccf3978a7d385363567fac01a1d3024f1dff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118889437"
---
# <a name="localsystem-account"></a>Conta localSystem

A conta LocalSystem é uma conta local predefinida usada pelo gerenciador de controle de serviço. Essa conta não é reconhecida pelo subsistema de segurança, portanto, você não pode especificar seu nome em uma chamada para a [**função LookupAccountName.**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) Ele tem privilégios extensos no computador local e atua como o computador na rede. Seu token inclui os SIDs NT AUTHORITY SYSTEM e BUILTIN Administrators; essas contas têm \\ acesso à maioria dos objetos do \\ sistema. O nome da conta em todas as localidades é . \\ Localsystem. O nome LocalSystem ou *ComputerName* \\ LocalSystem também pode ser usado. Essa conta não tem uma senha. Se você especificar a conta LocalSystem em uma chamada para a função [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) ou [**ChangeServiceConfig,**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) todas as informações de senha fornecidas por você são ignoradas.

Um serviço executado no contexto da conta LocalSystem herda o contexto de segurança do SCM. O SID do usuário é criado com o **valor SECURITY LOCAL SYSTEM \_ \_ \_ RID.** A conta não está associada a nenhuma conta de usuário conectado. Isso tem várias implicações:

-   A chave do Registro **HKEY \_ CURRENT \_ USER** está associada ao usuário padrão, não ao usuário atual. Para acessar o perfil de outro usuário, represente o usuário e, em seguida, **acesse HKEY \_ CURRENT \_ USER**.
-   O serviço pode abrir a chave do Registro **HKEY \_ LOCAL MACHINE \_ \\ SECURITY.**
-   O serviço apresenta as credenciais do computador para servidores remotos.
-   Se o serviço abrir uma janela de comando e executa um arquivo em lotes, o usuário poderá atingir CTRL+C para encerrar o arquivo em lotes e obter acesso a uma janela de comando com permissões LocalSystem.

A conta LocalSystem tem os seguintes privilégios:

-   **ES \_ ASSIGNPRIMARYTOKEN \_ NAME** (desabilitado)
-   **ES \_ AUDIT \_ NAME** (habilitado)
-   **ES \_ NOME \_ DO BACKUP** (desabilitado)
-   **ES \_ ALTERAR \_ O NOME DA \_ NOTIFICAÇÃO** (habilitado)
-   **ES \_ CREATE \_ GLOBAL \_ NAME** (habilitado)
-   **ES \_ CREATE \_ PAGEFILE \_ NAME** (habilitado)
-   **ES \_ CREATE \_ PERMANENT \_ NAME** (habilitado)
-   **ES \_ CREATE \_ TOKEN \_ NAME** (desabilitado)
-   **ES \_ NOME DE \_ DEPURAÇÃO** (habilitado)
-   **ES \_ IMPERSONATE \_ NAME** (habilitado)
-   **ES \_ INC \_ BASE \_ PRIORITY \_ NAME** (habilitado)
-   **ES \_ AUMENTAR \_ O NOME DA \_ COTA** (desabilitado)
-   **ES \_ LOAD \_ DRIVER \_ NAME** (desabilitado)
-   **ES \_ LOCK \_ MEMORY \_ NAME** (habilitado)
-   **ES \_ GERENCIAR \_ NOME \_ DO VOLUME** (desabilitado)
-   **ES \_ NOME \_ DO PROCESSO ÚNICO \_ \_ DO PROF** (habilitado)
-   **ES \_ RESTORE \_ NAME** (desabilitado)
-   **ES \_ NOME \_ DE SEGURANÇA** (desabilitado)
-   **ES \_ NOME \_ DO DESLIGAMENTO** (desabilitado)
-   **ES \_ NOME \_ DO AMBIENTE DO \_ SISTEMA** (desabilitado)
-   **ES \_ SYSTEMTIME \_ NAME** (desabilitado)
-   **ES \_ TAKE \_ OWNERSHIP \_ NAME** (desabilitado)
-   **ES \_ TCB \_ NAME** (habilitado)
-   **ES \_ NOME \_ UNDOCK** (desabilitado)

A maioria dos serviços não precisa de um nível de privilégio tão alto. Se o serviço não precisar desses privilégios e não for um serviço interativo, considere usar a conta [LocalService](localservice-account.md) ou a [conta NetworkService](networkservice-account.md). Para obter mais informações, consulte [Segurança do serviço e direitos de acesso](service-security-and-access-rights.md).

 

 
