---
description: 'As estruturas a seguir são usadas ao trabalhar com enclaves que são usadas para criar ambientes de execução confiáveis:'
ms.assetid: 61F99132-E947-4EA4-86A0-914CE316B53A
title: Estruturas de execução confiáveis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44d934ec26f9973697b987bf3a816e95d94ea591
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105775551"
---
# <a name="trusted-execution-structures"></a>Estruturas de execução confiáveis

As estruturas a seguir são usadas ao trabalhar com enclaves que são usadas para criar ambientes de execução confiáveis:

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                         | Descrição                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ENCLAVE \_ criar \_ SGX de informações \_**](/windows/desktop/api/winnt/ns-winnt-enclave_create_info_sgx)<br/>                      | Contém informações específicas da arquitetura a serem usadas para criar um enclave quando o tipo enclave for **enclave de \_ tipo \_ SGX**, que especifica um enclave para a extensão de arquitetura de SGX (extensões de software de proteção da Intel).<br/>     |
| [**ENCLAVE \_ criar \_ informações \_ vbs**](/windows/desktop/api/winnt/ns-winnt-enclave_create_info_vbs)<br/>                      | Contém informações específicas da arquitetura a serem usadas para criar um enclave quando o tipo enclave é **enclave \_ tipo \_ vbs**, que especifica uma enclave de segurança baseada em virtualização (vbs).<br/>                                       |
| [**\_identidade enclave**](/windows/desktop/api/ntenclv/ns-ntenclv-enclave_identity)<br/>                                      | Descreve a identidade do módulo primário de um enclave. <br/>                                                                                                                                                                 |
| [**informações de ENCLAVE \_**](/windows/desktop/api/ntenclv/ns-ntenclv-enclave_information)<br/>                                | Contém informações sobre o enclave em execução no momento.<br/>                                                                                                                                                                  |
| [**\_SGX de \_ informações de inicialização enclave \_**](/windows/desktop/api/winnt/ns-winnt-enclave_init_info_sgx)<br/>                          | Contém informações específicas da arquitetura a serem usadas para inicializar um enclave quando o tipo enclave for **enclave de \_ tipo \_ SGX**, que especifica um enclave para a extensão de arquitetura de SGX (extensões de software de proteção da Intel).<br/> |
| [**ENCLAVE \_ init \_ info \_ vbs**](/windows/desktop/api/winnt/ns-winnt-enclave_init_info_vbs)<br/>                          | Contém informações específicas da arquitetura a serem usadas para inicializar um enclave quando o tipo enclave é **enclave \_ tipo \_ vbs**, que especifica uma enclave de segurança baseada em virtualização (vbs).<br/>                                   |
| [**ENCLAVE de imagem \_ \_ CONFIG32**](/windows/desktop/api/winnt/ns-winnt-image_enclave_config32)<br/>                         | Define o formato da configuração enclave para sistemas que executam o Windows de 32 bits.<br/>                                                                                                                                          |
| [**ENCLAVE de imagem \_ \_ CONFIG64**](/previous-versions/windows/desktop/legacy/mt844244(v=vs.85))<br/>                         | Define o formato da configuração enclave para sistemas que executam o Windows de 64 bits.<br/>                                                                                                                                          |
| [**\_importação de enclave de imagem \_**](/windows/desktop/api/winnt/ns-winnt-image_enclave_import)<br/>                             | Define uma entrada na matriz de imagens que um enclave pode importar.<br/>                                                                                                                                                           |
| [**\_relatório enclave \_ vbs**](/windows/desktop/api/ntenclv/ns-ntenclv-vbs_enclave_report)<br/>                                 | Descreve o formato da instrução assinada contida em um relatório gerado chamando a função [**EnclaveGetAttestationReport**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavegetattestationreport) .<br/>                                                     |
| [**\_módulo de \_ relatório \_ enclave vbs**](/windows/desktop/api/ntenclv/ns-ntenclv-vbs_enclave_report_module)<br/>                  | Descreve um módulo carregado para o enclave.<br/>                                                                                                                                                                                   |
| [**\_cabeçalho de \_ pacote de relatórios enclave \_ vbs \_**](/windows/desktop/api/ntenclv/ns-ntenclv-vbs_enclave_report_pkg_header)<br/>         | Descreve o conteúdo de um relatório gerado chamando a função [**EnclaveGetAttestationReport**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavegetattestationreport) .<br/>                                                                                     |
| [**\_enclave \_ VARDATA de \_ relatório \_ vbs**](/windows/desktop/api/ntenclv/ns-ntenclv-vbs_enclave_report_vardata_header)<br/> | Descreve o formato de um bloco de dados de variável contido em um relatório gerado pela função [**EnclaveGetAttestationReport**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavegetattestationreport) .<br/>                                                          |



 

 

 
