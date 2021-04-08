---
description: A conta LocalSystem é uma conta local predefinida usada pelo Gerenciador de controle de serviço.
ms.assetid: 692bceb6-f5bd-4b83-ab3b-ef8099dc84e1
title: Conta LocalSystem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0132e70044aec7886ce6875239a6bedb502fec8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920799"
---
# <a name="localsystem-account"></a>Conta LocalSystem

A conta LocalSystem é uma conta local predefinida usada pelo Gerenciador de controle de serviço. Essa conta não é reconhecida pelo subsistema de segurança, portanto, você não pode especificar seu nome em uma chamada para a função [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) . Ele tem privilégios extensos no computador local e atua como o computador na rede. Seu token inclui o sistema de Autoridade NT \\ e \\ os SIDs de administradores internos; essas contas têm acesso à maioria dos objetos do sistema. O nome da conta em todas as localidades é. \\ LocalSystem. O nome, LocalSystem ou *ComputerName* \\ LocalSystem também pode ser usado. Esta conta não tem uma senha. Se você especificar a conta LocalSystem em uma chamada para a função [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) ou [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) , qualquer informação de senha que você fornecer será ignorada.

Um serviço executado no contexto da conta LocalSystem herda o contexto de segurança do SCM. O SID de usuário é criado com base no valor de **\_ \_ \_ RID do sistema local de segurança** . A conta não está associada a nenhuma conta de usuário conectada. Isso tem várias implicações:

-   A chave do registro **HKEY \_ Current \_ User** está associada ao usuário padrão, não ao usuário atual. Para acessar o perfil de outro usuário, represente o usuário e, em seguida, acesse o **HKEY \_ Current \_ User**.
-   O serviço pode abrir a chave do registro **HKEY \_ local \_ Machine \\ Security**.
-   O serviço apresenta as credenciais do computador para servidores remotos.
-   Se o serviço abrir uma janela de comando e executar um arquivo em lotes, o usuário poderá pressionar CTRL + C para encerrar o arquivo em lotes e obter acesso a uma janela de comando com permissões LocalSystem.

A conta LocalSystem tem os seguintes privilégios:

-   **Se \_ \_Nome do ASSIGNPRIMARYTOKEN** (desabilitado)
-   **Se \_ \_Nome da auditoria** (habilitado)
-   **Se \_ \_Nome do backup** (desabilitado)
-   **Se \_ ALTERAR \_ \_ nome da notificação** (habilitado)
-   **Se \_ CRIAR \_ \_ nome global** (habilitado)
-   **Se \_ CRIAR \_ \_ nome do arquivo de paginação** (habilitado)
-   **Se \_ CRIAR \_ \_ nome permanente** (habilitado)
-   **Se \_ CRIAR \_ \_ nome do token** (desabilitado)
-   **Se \_ \_Nome da depuração** (habilitado)
-   **Se \_ REPRESENTAR \_ nome** (habilitado)
-   **Se \_ \_Nome da \_ prioridade \_ base Inc** . (habilitado)
-   **Se \_ AUMENTAR \_ o \_ nome da cota** (desabilitado)
-   **Se \_ CARREGAR \_ \_ nome do driver** (desabilitado)
-   **Se \_ BLOQUEAR \_ o \_ nome da memória** (habilitado)
-   **Se \_ Gerenciar \_ \_ nome do volume** (desabilitado)
-   **Se \_ \_Nome do \_ processo \_ único de Prof** (habilitado)
-   **Se \_ \_Nome da restauração** (desabilitado)
-   **Se \_ \_Nome da segurança** (desabilitado)
-   **Se \_ \_Nome do DESligamento** (desabilitado)
-   **Se \_ \_ \_ Nome do ambiente do sistema** (desabilitado)
-   **Se \_ \_Nome do SYSTEMTIME** (desabilitado)
-   **Se \_ Apropriar-se do \_ \_ nome** (desabilitado)
-   **Se \_ \_Nome do TCB** (habilitado)
-   **Se \_ Desencaixar \_ nome** (desabilitado)

A maioria dos serviços não precisa de um nível de privilégio alto. Se o serviço não precisar desses privilégios e não for um serviço interativo, considere o uso da [conta LocalService](localservice-account.md) ou da [conta NetworkService](networkservice-account.md). Para obter mais informações, consulte [segurança de serviço e direitos de acesso](service-security-and-access-rights.md).

 

 
