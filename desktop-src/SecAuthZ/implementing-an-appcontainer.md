---
description: Um AppContainer é implementado adicionando novas informações ao token de processo, alterando SeAccessCheck () para que todos os objetos de ACL (lista de controle de acesso) herdados não modificados bloqueiem solicitações de acesso de processos do AppContainer por padrão e objetos de Nova ACL que devem estar disponíveis para o AppContainers.
ms.assetid: C70A2F8C-27CB-4298-AA31-8F5099616625
title: Implementando um AppContainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a6fc4c8d807d6a45f27f4f7a79d69ceb97edeb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829735"
---
# <a name="implementing-an-appcontainer"></a>Implementando um AppContainer

Um AppContainer é implementado adicionando novas informações ao token de processo, alterando [**SeAccessCheck ()**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-seaccesscheck) para que todos os objetos de ACL (lista de controle de acesso) herdados não modificados bloqueiem solicitações de acesso de processos do AppContainer por padrão e objetos de Nova ACL que devem estar disponíveis para o AppContainers.

## <a name="the-process"></a>O processo

Comece adicionando novas informações para o token de processo. Em seguida, altere **SeAccessCheck ()** para que todas as ACLs herdadas e não modificadas bloqueiem solicitações de acesso de processos do AppContainer por padrão. Por fim, recursos de Nova ACL que devem estar disponíveis para AppContainers

O SID do AppContainer é um identificador exclusivo persistente para o AppContainer. Os SIDs de capacidade concedem acesso a grupos de recursos a grupos de AppContainers. Um AppContainerNumber é um **DWORD** transitório usado para distinguir entre AppContainers. No entanto, ele não deve ser usado como uma identidade para o AppContainer.

Para permitir que um único AppContainer acesse um recurso, adicione seu AppContainerSID à ACL para esse recurso.

Para permitir que vários AppContainers específicos acessem um recurso, adicione todos os seus AppContainerSIDs à ACL para esse recurso.

Para gerenciar grupos de permissões, crie um SID de recurso (um GUID) e coloque o SID de recurso em todos os recursos a serem concedidos. Em seguida, adicione o SID de recurso ao seu token de processo.

Para permitir que todos os AppContainers acessem um recurso, adicione o SID **todos os pacotes de aplicativos** à ACL para esse recurso. Isso funciona como um curinga.

O AppContainerSID e o CapabilitySID dão suporte a máscaras de acesso em entradas de controle de acesso (ACE). Defina conforme apropriado.

 

 
