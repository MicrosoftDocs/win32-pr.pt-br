---
description: Um AppContainer é implementado adicionando novas informações ao token de processo, alterando SeAccessCheck() para que todos os objetos herdados, ACL (lista de controle de acesso não modificada) bloqueiem solicitações de acesso de processos appContainer por padrão e objetos de re-ACL que devem estar disponíveis para AppContainers.
ms.assetid: C70A2F8C-27CB-4298-AA31-8F5099616625
title: Implementando um AppContainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df4d50c0a5aa9f80755084886554a533fe1c82a6791840a9ff4ea4fdcf1476fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119670796"
---
# <a name="implementing-an-appcontainer"></a>Implementando um AppContainer

Um AppContainer é implementado adicionando novas informações ao token de processo, alterando [**SeAccessCheck()**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-seaccesscheck) para que todos os objetos herdados, ACL (lista de controle de acesso não modificada) bloqueiem solicitações de acesso de processos appContainer por padrão e objetos de re-ACL que devem estar disponíveis para AppContainers.

## <a name="the-process"></a>O processo

Comece adicionando novas informações para o token de processo. Em seguida, **altere SeAccessCheck()** para que todas as ACLs herdadas e não modificadas bloqueiem solicitações de acesso dos processos do AppContainer por padrão. Por fim, recursos de re-ACL que devem estar disponíveis para AppContainers

O SID do AppContainer é um identificador exclusivo persistente para o appcontainer. Os SIDs de funcionalidade concedem acesso a grupos de recursos a grupos de AppContainers. Um AppContainerNumber é um **DWORD transitório** usado para distinguir entre AppContainers. No entanto, ele não deve ser usado como uma identidade para o AppContainer.

Para permitir que um único AppContainer acesse um recurso, adicione seu AppContainerSID à ACL para esse recurso.

Para permitir que vários AppContainers específicos acessem um recurso, adicione todos os seus AppContainerSIDs à ACL para esse recurso.

Para gerenciar grupos de permissões, crie um SID de funcionalidade (um GUID) e coloque esse SID de Funcionalidade em todos os recursos a serem concedidos. Em seguida, adicione o SID de Funcionalidade ao token de processo.

Para permitir que todos os AppContainers acessem um recurso, adicione o SID TODOS OS **PACOTES DE** APLICATIVOs à ACL para esse recurso. Isso funciona como um curinga.

Tanto AppContainerSID quanto CapabilitySID são suporte a máscaras de acesso em ACE (Entradas de Controle de Acesso). De definido conforme apropriado.

 

 
