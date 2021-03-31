---
description: Lista as enumerações usadas pelas funções de gerenciamento de política LSA.
ms.assetid: f4fd2a61-61bc-44d2-b01f-3ca07699bcb8
title: Enumerações de gerenciamento de segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39bec2cdd731e2a3befe75e543f692d93bc5d9ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169681"
---
# <a name="security-management-enumerations"></a>Enumerações de gerenciamento de segurança

As enumerações de gerenciamento de segurança incluem o seguinte:

-   [Enumerações de política LSA](#lsa-policy-enumerations)
-   [Enumerações mais seguras](#safer-enumerations)

## <a name="lsa-policy-enumerations"></a>Enumerações de política LSA

Os tipos de enumeração a seguir são usados pelas funções de gerenciamento de política LSA.



| Enumeração                                                                               | Descrição                                                                                                                           |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**\_tipo de \_ evento de auditoria de política \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_audit_event_type)                             | Define os tipos de eventos que o sistema pode auditar.                                                                                     |
| [**\_classe de informações de política \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_information_class)                            | Define os tipos de informações que podem ser definidas ou consultadas para um objeto de [**política**](policy-object.md) .                             |
| [**\_função de \_ servidor \_ LSA de política**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_lsa_server_role)                               | Indique a função de um servidor LSA.                                                                                                   |
| [**\_classe de \_ informações de notificação de política \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_notification_information_class) | Define os tipos de informações de política e informações de domínio de política para os quais seu aplicativo pode solicitar a notificação de alterações. |
| [**\_estado de \_ habilitação do servidor de políticas \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_server_enable_state)                       | Representa o estado do servidor LSA, ou seja, se ele está habilitado ou desabilitado.                                                   |
| [**\_classe de informações confiáveis \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-trusted_information_class)                          | Define os tipos de informações que podem ser definidas ou consultadas para um domínio confiável.                                                     |



 

## <a name="safer-enumerations"></a>Enumerações mais seguras

O [mais seguro](safer.md) usa os seguintes tipos enumerados.



| Name                                                               | Descrição                                                                                                                                                                                      |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**tipos de \_ identificação mais seguros \_**](/windows/desktop/api/WinSafer/ne-winsafer-safer_identification_types) | Tipo de enumeração que define os possíveis tipos de estruturas de regra de identificação que podem ser identificadas pela estrutura de [**\_ \_ cabeçalho de identificação mais segura**](/windows/desktop/api/WinSafer/ns-winsafer-safer_identification_header) . |
| [**classe de \_ informações de objeto mais seguro \_ \_**](/windows/desktop/api/WinSafer/ne-winsafer-safer_object_info_class)      | Tipo de enumeração que define o tipo de informações solicitadas sobre um objeto mais seguro.                                                                                                            |
| [**classe de \_ informações de política mais segura \_ \_**](/windows/desktop/api/WinSafer/ne-winsafer-safer_policy_info_class)      | Tipo de enumeração que define as maneiras em que uma política pode ser consultada.                                                                                                                         |



 

 

 



