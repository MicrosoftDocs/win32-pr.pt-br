---
description: Lista as enumerações usadas pelas funções de gerenciamento de política LSA.
ms.assetid: f4fd2a61-61bc-44d2-b01f-3ca07699bcb8
title: Enumerações de gerenciamento de segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf87e6c41cb3e687a8927c294fe3bc1433a294aaf48991310b1c230f4741f299
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118894452"
---
# <a name="security-management-enumerations"></a>Enumerações de gerenciamento de segurança

As enumerações de gerenciamento de segurança incluem o seguinte:

-   [Enumerações de política LSA](#lsa-policy-enumerations)
-   [Enumerações mais seguras](#safer-enumerations)

## <a name="lsa-policy-enumerations"></a>Enumerações de política LSA

Os seguintes tipos de enumeração são usados pelas funções de gerenciamento de política LSA.



| Enumeração                                                                               | Descrição                                                                                                                           |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**TIPO \_ DE EVENTO DE AUDITORIA DE \_ \_ POLÍTICA**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_audit_event_type)                             | Define os tipos de eventos que o sistema pode auditar.                                                                                     |
| [**CLASSE \_ DE INFORMAÇÕES DE \_ POLÍTICA**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_information_class)                            | Define os tipos de informações que podem ser definidas ou consultadas para um [**objeto Policy.**](policy-object.md)                             |
| [**FUNÇÃO \_ DE SERVIDOR POLICY LSA \_ \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_lsa_server_role)                               | Indique a função de um servidor LSA.                                                                                                   |
| [**CLASSE DE \_ INFORMAÇÕES \_ DE NOTIFICAÇÃO DE \_ POLÍTICA**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_notification_information_class) | Define os tipos de informações de política e informações de domínio de política para os quais seu aplicativo pode solicitar notificação de alterações. |
| [**ESTADO \_ DE \_ HABILITAR SERVIDOR \_ DE POLÍTICA**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_server_enable_state)                       | Representa o estado do servidor LSA, ou seja, se ele está habilitado ou desabilitado.                                                   |
| [**CLASSE \_ DE INFORMAÇÕES \_ CONFIÁVEIS**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-trusted_information_class)                          | Define os tipos de informações que podem ser definidas ou consultadas para um domínio confiável.                                                     |



 

## <a name="safer-enumerations"></a>Enumerações mais seguras

[Mais](safer.md) seguro usa os seguintes tipos enumerados.



| Nome                                                               | Descrição                                                                                                                                                                                      |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TIPOS DE \_ IDENTIFICAÇÃO MAIS \_ SEGUROS**](/windows/desktop/api/WinSafer/ne-winsafer-safer_identification_types) | Tipo de enumeração que define os possíveis tipos de estruturas de regra de identificação que podem ser identificados pela estrutura [**DE \_ \_ HEADER DE IDENTIFICAÇÃO MAIS**](/windows/desktop/api/WinSafer/ns-winsafer-safer_identification_header) SEGURA. |
| [**CLASSE DE INFORMAÇÕES DE OBJETO MAIS \_ \_ \_ SEGURO**](/windows/desktop/api/WinSafer/ne-winsafer-safer_object_info_class)      | Tipo de enumeração que define o tipo de informação solicitada sobre um objeto Mais Seguro.                                                                                                            |
| [**CLASSE DE \_ INFORMAÇÕES DE POLÍTICA MAIS \_ \_ SEGURA**](/windows/desktop/api/WinSafer/ne-winsafer-safer_policy_info_class)      | Tipo de enumeração que define as maneiras pelas quais uma política pode ser consultada.                                                                                                                         |



 

 

 



