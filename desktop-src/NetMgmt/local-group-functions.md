---
title: Funções de grupo local
description: Um grupo local pode conter contas de usuário ou contas de grupo globais de um ou mais domínios. (Grupos globais podem conter usuários de apenas um domínio.) Um grupo local compartilha privilégios comuns e direitos somente dentro de seu próprio domínio.
ms.assetid: ed4c59d6-6532-4190-9807-95678053fc72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd13a23b322a860d6896a213b27fb6263586412
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641228"
---
# <a name="local-group-functions"></a>Funções de grupo local

Um *grupo local* pode conter contas de usuário ou contas de grupo globais de um ou mais domínios. (Grupos globais podem conter usuários de apenas um domínio.) Um grupo local compartilha privilégios comuns e direitos somente dentro de seu próprio domínio.

As funções de grupo local de gerenciamento de rede controlam os membros de grupos locais de forma que as funções só possam ser chamadas localmente no sistema no qual o grupo local é definido. Em uma estação de trabalho ou em um servidor que não seja um controlador de domínio, você pode usar apenas um grupo local definido nesse sistema.

No Active Directory, os domínios que estão no modo nativo, os grupos locais são chamados de *grupos locais de domínio*. Grupos locais de domínio estão disponíveis em todos os controladores de domínio, servidores membros e estações de trabalho ingressados no domínio. Active Directory domínios de modo misto são definidos no controlador de domínio primário e replicados para todos os outros controladores de domínio no domínio. Portanto, um grupo local está disponível em todos os controladores de domínio no domínio em que foi criado..

As funções de grupo local criam ou excluem grupos locais e revisam ou ajustam as associações de grupos locais. Essas funções são listadas a seguir.



| Função                                                   | Descrição                                                             |
|------------------------------------------------------------|-------------------------------------------------------------------------|
| [**NetLocalGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupadd)               | Cria um grupo local.                                                  |
| [**NetLocalGroupAddMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupaddmembers) | Adiciona um ou mais usuários ou grupos globais a um grupo local existente.     |
| [**NetLocalGroupDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupdel)               | Exclui um grupo local, removendo todos os membros existentes do grupo.    |
| [**NetLocalGroupDelMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupdelmembers) | Remove um ou mais membros de um grupo local existente.               |
| [**NetLocalGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupenum)             | Retorna informações sobre cada conta de grupo local em um servidor.         |
| [**NetLocalGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetinfo)       | Retorna informações sobre uma conta de grupo local específica em um servidor. |
| [**NetLocalGroupGetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetmembers) | Lista todos os membros de um grupo local especificado.                           |
| [**NetLocalGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetinfo)       | Define informações gerais sobre um grupo local.                           |
| [**NetLocalGroupSetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetmembers) | Atribui membros a um grupo local.                                       |



 

Você pode adicionar um membro a um grupo local especificando o SID (identificador de segurança) do membro. Para converter um nome de conta de membro em um SID, chame a função [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) .

Ao criar um grupo local chamando a função [**NetLocalGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupadd) , você deve fornecer um nome de grupo local. Inicialmente, o grupo local não tem membros.

As informações de conta do grupo local estão disponíveis nos seguintes níveis:

-   [**Informações do \_ localgroup \_ 0**](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_info_0)
-   [**Informações do \_ localgroup \_ 1**](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_info_1)
-   [**Informações do \_ localgroup \_ 1002**](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_info_1002)

As informações de associação de grupo local estão disponíveis nos seguintes níveis de informações:

-   [**Informações de \_ membros do localgroup \_ \_ 0**](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_members_info_0)
-   [**Informações de \_ membros do localgroup \_ \_ 1**](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_members_info_1)
-   [**Informações de \_ membros do localgroup \_ \_ 2**](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_members_info_2)
-   [**Informações de \_ membros do localgroup \_ \_ 3**](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_members_info_3)

Você pode recuperar os nomes dos grupos locais aos quais um usuário pertence chamando a função [**NetUserGetLocalGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups) , especificando o seguinte nível de informação:

[**Informações de \_ usuários do localgroup \_ \_ 0**](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_users_info_0)

Para obter mais informações, consulte as [funções do grupo](group-functions.md)de gerenciamento de rede.

Se você estiver programando para Active Directory, poderá chamar determinados métodos da interface de serviço Active Directory (ADSI) para obter a mesma funcionalidade que pode obter ao chamar as funções de grupo local de gerenciamento de rede. Para obter mais informações, consulte [**IADs**](/windows/desktop/api/iads/nn-iads-iadsgroup).

 

 