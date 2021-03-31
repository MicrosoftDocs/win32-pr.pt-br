---
title: Funções modais do usuário
description: As funções modais do usuário de gerenciamento de rede obtêm e definem parâmetros de todo o sistema relacionados ao comportamento do sistema de segurança.
ms.assetid: e655b9f6-2808-4bd4-998c-c8a2e980920b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c65595f78a412196b9fd54030ec1ac1f1fb8ae59
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917611"
---
# <a name="user-modal-functions"></a>Funções modais do usuário

As funções modais do usuário de gerenciamento de rede obtêm e definem parâmetros de todo o sistema relacionados ao comportamento do sistema de segurança.

As funções modais do usuário são listadas a seguir.



| Função                                     | Descrição                                                                                                                                                                                             |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetUserModalsGet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsget) | Retorna informações globais para todos os usuários e grupos globais no banco de dados de segurança, que é o banco de dados SAM (Gerenciador de contas de segurança) ou, no caso de controladores de domínio, o Active Directory. |
| [**NetUserModalsSet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset) | Define informações globais para todos os usuários e grupos globais no banco de dados de segurança.                                                                                                                       |



 

As funções **NetUserModalsGet** e **NetUserModalsSet** examinam e modificam as configurações de janela restrita, que são parâmetros globais que afetam cada conta no banco de dados de segurança (por exemplo, o comprimento mínimo permitido da senha). Todas as configurações de janela restrita podem ser alteradas chamando **NetUserModalsSet**. A maioria das modalidades também pode ser alterada usando o comando **net accounts** . As funções modais do usuário de gerenciamento de rede não exigem que o servidor tenha segurança em nível de usuário.

As informações modais do usuário estão disponíveis nos seguintes níveis:

-   [**Informações de modal do usuário \_ \_ \_ 0**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_0)
-   [**Informações de modal do usuário \_ \_ \_ 1**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1)
-   [**Informações de modal do usuário \_ \_ \_ 2**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_2)
-   [**Informações de modal do usuário \_ \_ \_ 3**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_3)

Os níveis de informações a seguir são válidos somente para [**NetUserModalsSet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset) e substituem a maneira mais antiga de passar um *Parmnum* para definir um campo específico:

-   [**Informações de modal do usuário \_ \_ \_ 1001**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1001)
-   [**Informações de modal do usuário \_ \_ \_ 1002**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1002)
-   [**Informações de modal do usuário \_ \_ \_ 1003**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1003)
-   [**Informações de modal do usuário \_ \_ \_ 1004**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1004)
-   [**Informações de modal do usuário \_ \_ \_ 1005**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1005)
-   [**Informações de modal do usuário \_ \_ \_ 1006**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1006)
-   [**Informações de modal do usuário \_ \_ \_ 1007**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1007)

Se você estiver programando para Active Directory, poderá chamar determinados métodos de interface do Active Directory Service (ADSI) para obter a mesma funcionalidade que pode obter ao chamar as funções modais do usuário de gerenciamento de rede. Para obter mais informações, consulte [**IADsDomain**](/windows/desktop/api/iads/nn-iads-iadsdomain).

 

 