---
title: Funções de grupo
description: Um grupo global contém contas de usuário de um domínio que são agrupados em um nome de conta de grupo.
ms.assetid: 2199258d-bde9-4fdb-b9c1-147616420fbe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17f57a36f0fbe3835df3661bfe56138f56a9a3d69bf3a2d5716ee298fab9ef4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117797332"
---
# <a name="group-functions"></a>Funções de grupo

Um *grupo global* contém contas de usuário de um domínio que são agrupados em um nome de conta de grupo. Um grupo global pode conter somente Membros (usuários) do domínio em que o grupo global é criado; Ele não pode conter grupos locais. Um grupo global está disponível em seu próprio domínio e em qualquer domínio confiante.

As funções do grupo de gerenciamento de rede controlam grupos globais. As funções de grupo são listadas a seguir.



| Função                                     | Descrição                                                                       |
|----------------------------------------------|-----------------------------------------------------------------------------------|
| [**NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd)           | Cria um grupo global.                                                           |
| [**NetGroupAddUser**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadduser)   | Adiciona um usuário a um grupo global existente.                                        |
| [**NetGroupDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdel)           | Remove um grupo global, independentemente de o grupo ter ou não membros.                  |
| [**NetGroupDelUser**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdeluser)   | Remove um nome de usuário de um grupo global.                                        |
| [**NetGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum)         | Lista todos os grupos globais em um servidor.                                              |
| [**NetGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetinfo)   | Retorna informações sobre um determinado grupo global.                              |
| [**NetGroupGetUsers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetusers) | Lista todos os membros de um determinado grupo global.                                   |
| [**NetGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo)   | Define informações gerais sobre um grupo global.                                    |
| [**NetGroupSetUsers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetusers) | Atribui membros a um novo grupo global; substitui os membros de um grupo existente. |



 

Ao chamar a função [**NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd) para criar um grupo global, você deve fornecer um nome de grupo. Inicialmente, um novo grupo não tem nenhum membro.

As contas de usuário pertencem automaticamente aos usuários do domínio do grupo global especial. A associação a esse grupo é controlada indiretamente pelas funções [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd), [**NetUserDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel)e [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .

As informações de conta de grupo global estão disponíveis nos seguintes níveis:

-   [**Informações do grupo \_ \_ 0**](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_0)
-   [**Informações do grupo \_ \_ 1**](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_1)
-   [**Informações do grupo \_ \_ 2**](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_2)
-   [**Informações do grupo \_ \_ 3**](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_3)
-   [**Informações do grupo \_ \_ 1002**](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_1002)
-   [**Informações do grupo \_ \_ 1005**](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_1005)

Os níveis 1002 e 1005 são válidos somente para a função [**NetGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo) .

As informações do membro do grupo global estão disponíveis no seguinte nível de informação:

-   [**Informações de usuários do grupo \_ \_ \_ 0**](/windows/desktop/api/Lmaccess/ns-lmaccess-group_users_info_0)

Para obter mais informações, consulte funções de [grupo local](local-group-functions.md)de gerenciamento de rede.

Se estiver programando para Active Directory, você poderá chamar determinados métodos ADSI (interface do serviço de Active Directory) para obter a mesma funcionalidade que pode obter ao chamar as funções do grupo de gerenciamento de rede. Para obter mais informações, consulte [**IADs**](/windows/desktop/api/iads/nn-iads-iadsgroup).

 

 