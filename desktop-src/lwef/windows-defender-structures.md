---
title: Estruturas do Windows Defender
description: Estruturas usadas por aplicativos ao chamar para solicitar verificações, atualizações de assinatura ou informações do Windows Defender.
ms.assetid: EF4116D3-DA50-4078-A024-2D624945D8C1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81d690de552137ce267b9d1d7a9cec711b161528
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635387"
---
# <a name="windows-defender-structures"></a>Estruturas do Windows Defender

Estruturas usadas por aplicativos ao chamar para solicitar verificações, atualizações de assinatura ou informações do Windows Defender.



| Estrutura                                                      | Descrição                                                                             |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**dados do MPCALLBACK \_**](mpcallback-data.md)                    | Dados passados para a função de retorno de chamada.<br/>                                        |
| [**dados do MPCLEAN \_**](mpclean-data.md)                          | Dados de notificação passados para a função de retorno de chamada limpa.<br/>                         |
| [**MPCLEAN \_ dados de verificação \_**](mpclean-precheck-data.md)       | Dados de notificação passados para a função de retorno de chamada de verificação limpa.<br/>                |
| [**STATUS do MPCOMPONENT \_**](mpcomponent-status.md)              | Informações de status do componente.<br/>                                                |
| [**versão do MPCOMPONENT \_**](mpcomponent-version.md)            | Versão e tempo de atualização para um componente individual.<br/>                         |
| [**dados do MPCONFIGURATION \_**](mpconfiguration-data.md)          | Contém dados sobre alterações de configuração, incluindo os valores novos e antigos.<br/> |
| [**dados do MPENDOFLIFE \_**](mpendoflife-data.md)                  | Dados de notificação "fim da vida útil".<br/>                                             |
| [**dados do MPEXPIRATION \_**](mpexpiration-data.md)                | Notificação de status de expiração do produto.<br/>                                      |
| [**dados do MPFASTPATH \_**](mpfastpath-data.md)                    | Notificação de atualização do FastPath.<br/>                                                |
| [**dados do MPHEALTH \_**](mphealth-data.md)                        | Dados de notificação de integridade.<br/>                                                    |
| [**dados do MPMALWARETOAST \_**](mpmalwaretoast-data.md)            | Dados de notificação do sistema de malware.<br/>                                             |
| [**MPNIS \_ \_ dados privados**](mpnis-private-data.md)             | Notificações NIS privadas.<br/>                                                   |
| [**dados do MPRESERVED \_**](mpreserved-data.md)                    | Dados de notificação reservados.<br/>                                                  |
| [**informações de MPRESOURCE \_**](mpresource-info.md)                    | Estrutura de informações do recurso.<br/>                                              |
| [**Estatísticas de MPRESOURCE \_**](mpresource-stats.md)                  | Estatísticas relacionadas a recursos.<br/>                                                 |
| [**dados do MPSAMPLE \_**](mpsample-data.md)                        | Dados de notificação passados para a função de retorno de chamada de envio de exemplo.<br/>         |
| [**dados do MPSCAN \_**](mpscan-data.md)                            | Verifique os dados passados para o retorno de chamada.<br/>                                            |
| [**recursos do MPSCAN \_**](mpscan-resources.md)                  | Informações de recurso passadas durante uma operação de verificação.<br/>                         |
| [**resultado do MPSCAN \_**](mpscan-result.md)                        | Os resultados de uma verificação.<br/>                                                       |
| [**dados do MPSIGUPDATE \_**](mpsigupdate-data.md)                  | Dados de notificação passados para a função de retorno de chamada de atualização de assinatura.<br/>          |
| [**dados do MPSTATUS \_**](mpstatus-data.md)                        | Contém dados sobre o status atual de um componente do produto.<br/>        |
| [**MPSTATUS \_ DATAEX \_ não usado**](mpstatus-dataex-unused.md)     | Estrutura fictícia para não SRP.<br/>                                                 |
| [**informações de MPSTATUS \_**](mpstatus-info.md)                        | Informações de status do Malware Protection Manager.<br/>                       |
| [**dados do MPTHREAT \_**](mpthreat-data.md)                        | Dados de notificação passados devido a uma detecção de ameaças ou modificação.<br/>            |
| [**informações de MPTHREAT \_**](mpthreat-info.md)                        | Contém informações sobre uma ameaça.<br/>                                         |
| [**\_comportamento MPTHREAT INFOEX \_**](mpthreat-infoex-behavior.md) | Contém informações específicas de modificação de comportamento.<br/>                         |
| [**MPTHREAT \_ INFOEX \_ NIS**](mpthreat-infoex-nis.md)           | Contém informações específicas do NIS.<br/>                                           |
| [**MPTHREAT \_ INFOEX \_ não usado**](mpthreat-infoex-unused.md)     | Estrutura fictícia para ameaças de tipo de modificação sem comportamento.<br/>                  |
| [**\_informações localizadas do MPTHREAT \_**](mpthreat-localized-info.md)   | Informações localizadas para uma ameaça.<br/>                                          |
| [**Estatísticas de MPTHREAT \_**](mpthreat-stats.md)                      | Estatísticas relacionadas a ameaças.<br/>                                                   |
| [**\_dados de estatísticas do MPTHREAT \_**](mpthreat-stats-data.md)           | Dados de estatísticas de ameaças adicionais.<br/>                                           |
| [**informações de MPVERSION \_**](mpversion-info.md)                      | Informações de versão dos componentes do Malware Protection Manager.<br/>         |



 

 

 





