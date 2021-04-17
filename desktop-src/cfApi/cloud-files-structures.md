---
description: As estruturas a seguir são usadas na criação e manutenção de diretórios e arquivos de espaço reservado.
ms.assetid: 50CCA8F5-7118-48E8-ADBF-337798FAF549
title: Estruturas de filtro de nuvem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eebe6623ad3d9d348d624f8ab8da3427416d4742
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755457"
---
# <a name="cloud-filter-structures"></a>Estruturas de filtro de nuvem

As estruturas a seguir são usadas na criação e manutenção de diretórios e arquivos de espaço reservado.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                   | Descrição                                                                                                                               |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**informações de retorno de chamada do CF \_ \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_callback_info)<br/>                          | Contém informações de retorno de chamada comuns.<br/>                                                                                          |
| [**parâmetros de retorno de chamada do CF \_ \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_callback_parameters)<br/>              | Contém parâmetros específicos de retorno de chamada, como deslocamento de arquivo, comprimento, sinalizadores, etc.<br/>                                                 |
| [**registro de retorno de chamada do CF \_ \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_callback_registration)<br/>          | Os retornos de chamada a serem registrados pelo provedor de sincronização.<br/>                                                                           |
| [**\_intervalo de arquivos do CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_file_range)<br/>                                | Especifica um intervalo de dados em um arquivo de espaço reservado.<br/>                                                                               |
| [**\_buffer de \_ intervalo de arquivos do CF \_**](/previous-versions/windows/desktop/legacy/mt844616(v=vs.85))<br/>                | Uma estrutura para descrever o local e o intervalo de dados em um arquivo.<br/>                                                              |
| [**metadados do CF \_ FS \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_fs_metadata)<br/>                              | Arquivo de espaço reservado ou metadados de diretório.<br/>                                                                                        |
| [**\_política de hidratação do CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_hydration_policy)<br/>                    | Especifica a política hidratação primária e seu modificador.<br/>                                                                       |
| [**\_informações da operação do CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_operation_info)<br/>                        | Informações sobre uma operação em um arquivo ou pasta de espaço reservado.<br/>                                                                |
| [**\_parâmetros de operação do CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_operation_parameters)<br/>            | Parâmetros de uma operação em um arquivo ou pasta de espaço reservado.<br/>                                                                    |
| [**\_informações básicas do espaço reservado do CF \_ \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_placeholder_basic_info)<br/>       | Informações básicas do espaço reservado.<br/>                                                                                                 |
| [**\_informações de criação do espaço reservado do CF \_ \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_placeholder_create_info)<br/>     | Contém informações de espaço reservado para criar novos arquivos de espaço reservado ou diretórios. <br/>                                           |
| [**\_informações padrão do espaço reservado do CF \_ \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_placeholder_standard_info)<br/> | Informações de espaço reservado padrão.<br/>                                                                                              |
| [**\_informações da plataforma CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_platform_info)<br/>                          | Retorna informações para a plataforma de arquivos de nuvem. Isso se destina a provedores de sincronização em execução em várias versões do Windows.<br/> |
| [**\_política de população do CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_population_policy)<br/>                  | Especifica a política principal de população e seu modificador.<br/>                                                                      |
| [**\_informações do processo do CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_process_info)<br/>                            | Contém informações sobre um processo de usuário.<br/>                                                                                     |
| [**\_políticas de sincronização do CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_policies)<br/>                          | Define as políticas de sincronização usadas por uma raiz de sincronização.<br/>                                                                                 |
| [**\_registro de sincronização do CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_registration)<br/>                  | Os detalhes do provedor de sincronização e da raiz de sincronização a serem registrados.<br/>                                                               |
| [**\_ \_ informações básicas da raiz de sincronização do \_ CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_root_basic_info)<br/>          | Informações básicas de raiz de sincronização.<br/>                                                                                                   |
| [**\_informações do \_ \_ provedor raiz de sincronização \_ do CF**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_root_provider_info)<br/>    | Sincronizar informações do provedor raiz.<br/>                                                                                                |
| [**\_ \_ informações padrão da raiz de sincronização do \_ CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_root_standard_info)<br/>    | Informações de raiz de sincronização padrão.<br/>                                                                                                |
| [**\_status de sincronização do CF \_**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_status)<br/>                              | Usado em uma estrutura de [**\_ \_ informações de operação do CF**](/windows/desktop/api/cfapi/ns-cfapi-cf_operation_info) para descrever o status de uma raiz de sincronização especificada.<br/>     |



 

 

