---
title: Windows Defender Estruturas
description: Estruturas usadas por aplicativos ao chamar para solicitar verificações, atualizações de assinatura ou informações de Windows Defender.
ms.assetid: EF4116D3-DA50-4078-A024-2D624945D8C1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa735805fd5f9b7f85e61bff748ee2714d915ab1ddf7f94eabb9fff316aba710
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975376"
---
# <a name="windows-defender-structures"></a>Windows Defender Estruturas

Estruturas usadas por aplicativos ao chamar para solicitar verificações, atualizações de assinatura ou informações de Windows Defender.



| Estrutura                                                      | Descrição                                                                             |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**DADOS \_ MPCALLBACK**](mpcallback-data.md)                    | Dados passados para a função de retorno de chamada.<br/>                                        |
| [**DADOS \_ MPCLEAN**](mpclean-data.md)                          | Dados de notificação passados para a função de retorno de chamada limpa.<br/>                         |
| [**DADOS DE \_ PRÉ-VERIFICAÇÃO MPCLEAN \_**](mpclean-precheck-data.md)       | Dados de notificação passados para limpar a função de retorno de chamada de pré-verificação.<br/>                |
| [**STATUS DO MPCOMPONENT \_**](mpcomponent-status.md)              | Informações de status do componente.<br/>                                                |
| [**VERSÃO DO \_ MPCOMPONENT**](mpcomponent-version.md)            | Versão e tempo de atualização para um componente individual.<br/>                         |
| [**DADOS MPCONFIGURATION \_**](mpconfiguration-data.md)          | Contém dados sobre alterações de configuração, incluindo os valores antigo e novo.<br/> |
| [**DADOS MPENDOFLIFE \_**](mpendoflife-data.md)                  | Dados de notificação de "Fim da vida útil".<br/>                                             |
| [**DADOS DE \_ MPEXPIRATION**](mpexpiration-data.md)                | Notificação de status de expiração do produto.<br/>                                      |
| [**DADOS \_ MPFASTPATH**](mpfastpath-data.md)                    | Notificação de atualização do FastPath.<br/>                                                |
| [**DADOS DE \_ MPHEALTH**](mphealth-data.md)                        | Dados de notificação de saúde.<br/>                                                    |
| [**DADOS MPMALWARETOAST \_**](mpmalwaretoast-data.md)            | Dados de notificação do toast de malware.<br/>                                             |
| [**DADOS PRIVADOS DO MP \_ \_ LTDA**](mpnis-private-data.md)             | Notificações de NIS privadas.<br/>                                                   |
| [**DADOS \_ RESERVADOS DO MP**](mpreserved-data.md)                    | Dados de notificação reservados.<br/>                                                  |
| [**INFORMAÇÕES DO MPRESOURCE \_**](mpresource-info.md)                    | Estrutura de informações de recurso.<br/>                                              |
| [**ESTATÍSTICAS DO MPRESOURCE \_**](mpresource-stats.md)                  | Estatísticas relacionadas a recursos.<br/>                                                 |
| [**DADOS MPSAMPLE \_**](mpsample-data.md)                        | Dados de notificação passados para a função de retorno de chamada de envio de exemplo.<br/>         |
| [**DADOS \_ DO MPSCAN**](mpscan-data.md)                            | Verificar dados passados para o retorno de chamada.<br/>                                            |
| [**RECURSOS DO \_ MPSCAN**](mpscan-resources.md)                  | Informações de recurso passadas durante uma operação de verificação.<br/>                         |
| [**MPSCAN \_ RESULT**](mpscan-result.md)                        | Os resultados de uma verificação.<br/>                                                       |
| [**DADOS MPSIGUPDATE \_**](mpsigupdate-data.md)                  | Dados de notificação passados para a função de retorno de chamada de atualização de assinatura.<br/>          |
| [**DADOS \_ MPSTATUS**](mpstatus-data.md)                        | Contém dados sobre o status atual de um componente do produto.<br/>        |
| [**MPSTATUS \_ DATAEX \_ UNUSED**](mpstatus-dataex-unused.md)     | Estrutura fiada para não SRP.<br/>                                                 |
| [**INFORMAÇÕES DE \_ MPSTATUS**](mpstatus-info.md)                        | Informações de status do gerenciador de proteção contra malware.<br/>                       |
| [**DADOS \_ MPTHREAT**](mpthreat-data.md)                        | Dados de notificação passados devido à detecção ou modificação de ameaças.<br/>            |
| [**INFORMAÇÕES DE \_ MPTHREAT**](mpthreat-info.md)                        | Contém informações sobre uma ameaça.<br/>                                         |
| [**COMPORTAMENTO DO \_ INFOEX \_ MPTHREAT**](mpthreat-infoex-behavior.md) | Contém informações específicas de modificação de comportamento.<br/>                         |
| [**MPTHREAT \_ INFOEX \_ NIS**](mpthreat-infoex-nis.md)           | Contém informações específicas de NIS.<br/>                                           |
| [**MPTHREAT \_ INFOEX \_ UNUSED**](mpthreat-infoex-unused.md)     | Estrutura fiada para ameaças de tipo de modificação sem comportamento.<br/>                  |
| [**INFORMAÇÕES LOCALIZADAS DO \_ MPTHREAT \_**](mpthreat-localized-info.md)   | Informações localizadas para uma ameaça.<br/>                                          |
| [**ESTATÍSTICAS DE \_ MPTHREAT**](mpthreat-stats.md)                      | Estatísticas relacionadas a ameaças.<br/>                                                   |
| [**DADOS DE ESTATÍSTICAS \_ MPTHREAT \_**](mpthreat-stats-data.md)           | Dados adicionais de estatísticas de ameaças.<br/>                                           |
| [**INFORMAÇÕES \_ DO MPVERSION**](mpversion-info.md)                      | Informações de versão para os componentes do gerenciador de proteção contra malware.<br/>         |



 

 

 





