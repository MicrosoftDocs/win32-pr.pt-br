---
title: Requisitos para funções de gerenciamento de rede em servidores e estações de trabalho
description: Se você chamar uma das funções de gerenciamento de rede listadas neste tópico em um servidor ou estação de trabalho, os requisitos de acesso diferentes se aplicarão a consultas de informações e atualizações de informações.
ms.assetid: 05ff1771-8058-4c86-8f45-735bf41dc128
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b06e516aa06465c67966cc076a0ca524d4ae4003
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823941"
---
# <a name="requirements-for-network-management-functions-on-servers-and-workstations"></a>Requisitos para funções de gerenciamento de rede em servidores e estações de trabalho

Se você chamar uma das funções de gerenciamento de rede listadas neste tópico em um servidor ou estação de trabalho, os requisitos de acesso diferentes se aplicarão a consultas de informações e atualizações de informações.

## <a name="queries"></a>Consultas

Se você chamar uma das seguintes funções para executar uma consulta em um servidor ou estação de trabalho, por padrão, todos os usuários autenticados poderão ler e enumerar as informações.

-   [**NetGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum), [**NetGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetinfo), [**NetGroupGetUsers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetusers)
-   [**NetLocalGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupenum), [**NetLocalGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetinfo), [**NetLocalGroupGetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetmembers)
-   [**NetQueryDisplayInformation**](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation)
-   [**NetSessionGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsessiongetinfo) (somente níveis 1 e 2)
-   [**NetShareEnum**](/windows/desktop/api/lmshare/nf-lmshare-netshareenum) (somente níveis 2 e 502)
-   [**NetUserEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum), [**NetUserGetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetgroups), [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo), [**NetUserGetLocalGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups), [**NetUserModalsGet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsget)
-   [**NetWkstaGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo), [ **NetWkstaUserEnum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum)

Veja a seguir informações adicionais sobre o acesso anônimo ao ler e enumerar informações.

**Windows Server 2003 e Windows XP:** O acesso anônimo a informações é possível se a configuração de política EveryoneIncludesAnonymous permitir acesso anônimo.

**Windows 2000:** O acesso anônimo a objetos protegíveis é possível se a configuração de política RestrictAnonymous permitir acesso anônimo. Você pode restringir o acesso anônimo definindo a seguinte chave no registro para o valor 1.

**HKEY \_ \_Sistema de máquina local \\ \\ CurrentControlSet \\ controle \\ LSA** \\ **RestrictAnonymous** = 1

Para obter mais informações, consulte o seguinte artigo na base de dados de conhecimento Microsoft:

ID do artigo: [Q246261](https://support.microsoft.com/kb/246261)

Título: como usar o valor do Registro RestrictAnonymous.

## <a name="updates"></a>Atualizações

Por padrão, somente administradores e usuários avançados podem gravar informações.

Para obter mais informações sobre como controlar o acesso a objetos protegíveis, consulte [controle de acesso](/windows/desktop/SecAuthZ/access-control), [privilégios](/windows/desktop/SecAuthZ/privileges)e [objetos protegíveis](/windows/desktop/SecAuthZ/securable-objects). Para obter mais informações sobre como chamar funções que exigem privilégios de administrador, consulte [executando com privilégios especiais](/windows/desktop/SecBP/running-with-special-privileges).

 

 