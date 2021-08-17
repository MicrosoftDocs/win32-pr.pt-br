---
description: As estruturas a seguir são usadas na criação e manutenção de arquivos e diretórios de espaço reservado.
ms.assetid: 50CCA8F5-7118-48E8-ADBF-337798FAF549
title: Estruturas de filtro de nuvem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6da8cf5e512c6e65e88d17c5904fca264c28829dd0a0e842227da4b069aa82d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130218"
---
# <a name="cloud-filter-structures"></a>Estruturas de filtro de nuvem

As estruturas a seguir são usadas na criação e manutenção de arquivos e diretórios de espaço reservado.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                   | Descrição                                                                                                                               |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**INFORMAÇÕES \_ DE RETORNO DE CHAMADA DO \_ CF**](/windows/desktop/api/cfapi/ns-cfapi-cf_callback_info)<br/>                          | Contém informações comuns de retorno de chamada.<br/>                                                                                          |
| [**PARÂMETROS \_ DE RETORNO DE CHAMADA DO CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_callback_parameters)<br/>              | Contém parâmetros específicos de retorno de chamada, como deslocamento de arquivo, comprimento, sinalizadores etc.<br/>                                                 |
| [**REGISTRO \_ DE RETORNO DE CHAMADA DO CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_callback_registration)<br/>          | Os retornos de chamada a serem registrados pelo provedor de sincronização.<br/>                                                                           |
| [**INTERVALO \_ DE ARQUIVOS \_ CF**](/windows/desktop/api/cfapi/ns-cfapi-cf_file_range)<br/>                                | Especifica um intervalo de dados em um arquivo de espaço reservado.<br/>                                                                               |
| [**BUFFER DE \_ INTERVALO \_ DE ARQUIVOS \_ CF**](/previous-versions/windows/desktop/legacy/mt844616(v=vs.85))<br/>                | Uma estrutura para descrever o local e o intervalo de dados em um arquivo.<br/>                                                              |
| [**METADADOS do CF \_ FS \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_fs_metadata)<br/>                              | Metadados de diretório ou arquivo de espaço reservado.<br/>                                                                                        |
| [**POLÍTICA \_ DE HYDRATION \_ DO CF**](/windows/desktop/api/cfapi/ns-cfapi-cf_hydration_policy)<br/>                    | Especifica a política de hidratação primária e seu modificador.<br/>                                                                       |
| [**INFORMAÇÕES \_ DE OPERAÇÃO DO \_ CF**](/windows/desktop/api/cfapi/ns-cfapi-cf_operation_info)<br/>                        | Informações sobre uma operação em um arquivo ou pasta de espaço reservado.<br/>                                                                |
| [**PARÂMETROS \_ DE OPERAÇÃO DO CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_operation_parameters)<br/>            | Parâmetros de uma operação em um arquivo ou pasta de espaço reservado.<br/>                                                                    |
| [**INFORMAÇÕES \_ BÁSICAS DO ESPAÇO RESERVADO \_ \_ DO CF**](/windows/desktop/api/cfapi/ns-cfapi-cf_placeholder_basic_info)<br/>       | Informações básicas de espaço reservado.<br/>                                                                                                 |
| [**INFORMAÇÕES \_ DE CRIAÇÃO DE ESPAÇO RESERVADO \_ \_ DO CF**](/windows/desktop/api/cfapi/ns-cfapi-cf_placeholder_create_info)<br/>     | Contém informações de espaço reservado para criar novos arquivos ou diretórios de espaço reservado. <br/>                                           |
| [**INFORMAÇÕES \_ PADRÃO DO ESPAÇO RESERVADO \_ \_ CF**](/windows/desktop/api/cfapi/ns-cfapi-cf_placeholder_standard_info)<br/> | Informações de espaço reservado padrão.<br/>                                                                                              |
| [**INFORMAÇÕES \_ DA PLATAFORMA \_ CF**](/windows/desktop/api/cfapi/ns-cfapi-cf_platform_info)<br/>                          | Retorna informações para a plataforma de arquivos de nuvem. Isso destina-se a provedores de sincronização em execução em várias versões do Windows.<br/> |
| [**POLÍTICA \_ DE POPULAÇÃO DO \_ CF**](/windows/desktop/api/cfapi/ns-cfapi-cf_population_policy)<br/>                  | Especifica a política de população primária e seu modificador.<br/>                                                                      |
| [**INFORMAÇÕES \_ DO PROCESSO DO \_ CF**](/windows/desktop/api/cfapi/ns-cfapi-cf_process_info)<br/>                            | Contém informações sobre um processo de usuário.<br/>                                                                                     |
| [**POLÍTICAS DE \_ SINCRONIZAÇÃO DO CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_policies)<br/>                          | Define as políticas de sincronização usadas por uma raiz de sincronização.<br/>                                                                                 |
| [**REGISTRO DE \_ SINCRONIZAÇÃO DO CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_registration)<br/>                  | Os detalhes do provedor de sincronização e a raiz de sincronização a serem registrados.<br/>                                                               |
| [**INFORMAÇÕES \_ \_ BÁSICAS BÁSICAS \_ DA SINCRONIZAÇÃO DO \_ CF**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_root_basic_info)<br/>          | Informações básicas da raiz de sincronização.<br/>                                                                                                   |
| [**INFORMAÇÕES \_ DO PROVEDOR RAIZ DE \_ \_ SINCRONIZAÇÃO \_ DO CF**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_root_provider_info)<br/>    | Sincronizar informações do provedor raiz.<br/>                                                                                                |
| [**INFORMAÇÕES \_ PADRÃO \_ DA SINCRONIZAÇÃO \_ DE \_ CF**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_root_standard_info)<br/>    | Informações de raiz de sincronização padrão.<br/>                                                                                                |
| [**STATUS \_ DA SINCRONIZAÇÃO DO \_ CF**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_status)<br/>                              | Usado em uma estrutura [**\_ CF OPERATION \_ INFO**](/windows/desktop/api/cfapi/ns-cfapi-cf_operation_info) para descrever o status de uma raiz de sincronização especificada.<br/>     |



 

 

