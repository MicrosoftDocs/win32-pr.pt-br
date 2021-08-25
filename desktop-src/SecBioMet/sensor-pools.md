---
title: Sensor Pools
description: Descreve três sistemas de pools de sensor possíveis, privados e não atribuídos.
ms.assetid: d7fd3c39-d719-4cfd-9af0-a87837f3f328
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d28bd03d84e2558f0fb1ba090440aa2bda62292c51773d54d5094466ba9e494
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035256"
---
# <a name="sensor-pools"></a>Sensor Pools

Para dar suporte a cenários Windows autenticação e autenticação definida pelo fornecedor, o serviço biométrico Windows organiza unidades biométricas em três pools de sensor possíveis:

-   **Pool privado** uma coleção de unidades biométricas alocadas para uso exclusivo por um aplicativo cliente. Os pools privados podem dar suporte a cenários de autenticação que não são baseados em Windows e possibilitam que um aplicativo acesse o hardware de uma unidade biométrica de maneira definida pelo fornecedor. Pode haver tantos pools de sensor privados no sistema quanto unidades biométricas.
-   **O pool de sensor do** sistema é uma coleção de unidades biométricas compartilháveis que fornecem acesso aos Windows de autenticação. Esse pool é usado pelo Winlogon, pelo UAC e por qualquer outro cliente que associe um SID a um modelo biométrico específico. Cada provedor de serviços biométricos tem um pool de sensor do sistema.
-   **O pool não atribuído** contém uma coleção (possivelmente vazia) de unidades biométricas que não são atribuídas ao pool do sistema ou ao pool privado.

Os aplicativos podem usar o pool de sistema compartilhado ou podem criar um pool privado com unidades biométricas removidas do sistema ou pools não atribuídos. Quando um aplicativo libera seu pool privado, as unidades biométricas são reconfiguradas e retornadas para seus pools originais. Para evitar ataques de negação de serviço, somente usuários privilegiados têm permissão para remover o último sensor do pool do sistema. Para obter mais informações, consulte estes tópicos.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                       | Descrição                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Pool de Sensor Privado](private-sensor-pool.md)<br/>   | Uma coleção de unidades biométricas reservadas para uso exclusivo por um aplicativo cliente. Os pools privados suportam métodos de autenticação proprietários e permitem que um aplicativo cliente acesse uma unidade biométrica usando comandos de controle especificados pelo fornecedor.<br/> |
| [Pool de Sensor do Sistema](system-sensor-pool.md)<br/>     | Uma coleção de unidades biométricas compartilháveis que fornecem acesso aos Windows de autenticação. Esse pool é usado pelo Winlogon, pelo UAC e por qualquer outro cliente que associe um SID a um modelo biométrico específico.<br/>                                 |
| [Comportamento do pool do sistema](system-pool-behavior.md)<br/> | Discussão sobre as ações tomadas pelo pool do sistema quando os avisos de evento são enviados e quando nenhuma operação biométrica está pendente.<br/>                                                                                                                     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre a API Windows Biometric Framework](./biometric-service-api-portal.md)
</dt> </dl>

 

