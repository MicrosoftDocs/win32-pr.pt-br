---
title: Pools de sensores
description: Descreve três possíveis pools de sensor, privado e não atribuído.
ms.assetid: d7fd3c39-d719-4cfd-9af0-a87837f3f328
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 263275af5c7decff37ef70ad3a5396ec562562f4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366250"
---
# <a name="sensor-pools"></a>Pools de sensores

Para dar suporte aos cenários de autenticação do Windows e à autenticação definida pelo fornecedor, o serviço de biometria do Windows organiza as unidades biométricas em três pools de sensores possíveis:

-   **Pool privado** uma coleção de unidades biométricas alocadas para uso exclusivo por um aplicativo cliente. Os pools privados podem dar suporte a cenários de autenticação que não são baseados no Windows e possibilitam que um aplicativo acesse o hardware de uma unidade biométrica de uma maneira definida pelo fornecedor. Pode haver tantos pools de sensores privados no sistema quanto há unidades biométricas.
-   **Pool do sensor do sistema** uma coleção de unidades biométricas compartilháveis que fornecem acesso aos serviços de autenticação do Windows. Esse pool é usado pelo Winlogon, pelo UAC e por qualquer outro cliente que associa um SID a um modelo biométrico específico. Cada provedor de serviços biométricos tem um pool de sensor do sistema.
-   O **pool não atribuído** contém uma coleção (possivelmente vazia) de unidades biométricas que não são atribuídas ao pool do sistema ou ao pool privado.

Os aplicativos podem usar o pool de sistema compartilhado ou podem criar um pool privado composto por unidades biométricas removidas do sistema ou de pools não atribuídos. Quando um aplicativo libera seu pool particular, as unidades biométricas são reconfiguradas e retornadas para seus pools originais. Para evitar ataques de negação de serviço, somente usuários privilegiados têm permissão para remover o último sensor do pool do sistema. Para obter mais informações, consulte os tópicos a seguir.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                       | Descrição                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Pool de sensores privado](private-sensor-pool.md)<br/>   | Uma coleção de unidades biométricas reservadas para uso exclusivo por um aplicativo cliente. Os pools privados dão suporte a métodos de autenticação proprietários e permitem que um aplicativo cliente acesse uma unidade biométrica usando comandos de controle especificados pelo fornecedor.<br/> |
| [Pool do sensor do sistema](system-sensor-pool.md)<br/>     | Uma coleção de unidades biométricas compartilhadas que fornecem acesso aos serviços de autenticação do Windows. Esse pool é usado pelo Winlogon, pelo UAC e por qualquer outro cliente que associa um SID a um modelo biométrico específico.<br/>                                 |
| [Comportamento do pool do sistema](system-pool-behavior.md)<br/> | Discussão sobre as ações executadas pelo pool do sistema quando avisos de evento são enviados e quando nenhuma operação biométrica está pendente.<br/>                                                                                                                     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre a API de Windows Biometric Framework](./biometric-service-api-portal.md)
</dt> </dl>

 

