---
description: 'As seguintes estruturas são usadas ao trabalhar com enclaves usados para criar ambientes de execução confiáveis:'
ms.assetid: 61F99132-E947-4EA4-86A0-914CE316B53A
title: Estruturas de execução confiável
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9349c8c4e4c04ecc664ccab668abe55cdca1e1720b6fa17fd35bb7139f53f19c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118386247"
---
# <a name="trusted-execution-structures"></a>Estruturas de execução confiável

As seguintes estruturas são usadas ao trabalhar com enclaves usados para criar ambientes de execução confiáveis:

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                         | Descrição                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ENCLAVE \_ CREATE \_ INFO \_ SGX**](/windows/desktop/api/winnt/ns-winnt-enclave_create_info_sgx)<br/>                      | Contém informações específicas da arquitetura a ser usadas para criar um enclave quando o tipo de enclave é **ENCLAVE \_ TYPE \_ SGX**, que especifica um enclave para a extensão de arquitetura intel Software Guard Extensions (SGX).<br/>     |
| [**VBS DE INFORMAÇÕES \_ \_ DE CRIAÇÃO DE \_ ENCLAVE**](/windows/desktop/api/winnt/ns-winnt-enclave_create_info_vbs)<br/>                      | Contém informações específicas da arquitetura a ser usadas para criar um enclave quando o tipo de enclave é **ENCLAVE \_ TYPE \_ VBS**, que especifica um enclave VBS (segurança baseada em virtualização).<br/>                                       |
| [**IDENTIDADE DO \_ ENCLAVE**](/windows/desktop/api/ntenclv/ns-ntenclv-enclave_identity)<br/>                                      | Descreve a identidade do módulo primário de um enclave. <br/>                                                                                                                                                                 |
| [**INFORMAÇÕES SOBRE \_ ENCLAVE**](/windows/desktop/api/ntenclv/ns-ntenclv-enclave_information)<br/>                                | Contém informações sobre o enclave em execução no momento.<br/>                                                                                                                                                                  |
| [**SGX DE \_ INFORMAÇÕES DE \_ \_ INIT DO ENCLAVE**](/windows/desktop/api/winnt/ns-winnt-enclave_init_info_sgx)<br/>                          | Contém informações específicas da arquitetura a ser usadas para inicializar um enclave quando o tipo de enclave é **ENCLAVE \_ TYPE \_ SGX,** que especifica um enclave para a extensão de arquitetura intel Software Guard Extensions (SGX).<br/> |
| [**VBS DE \_ INFORMAÇÕES DE INIT \_ DO ENCLAVE \_**](/windows/desktop/api/winnt/ns-winnt-enclave_init_info_vbs)<br/>                          | Contém informações específicas da arquitetura a ser usadas para inicializar um enclave quando o tipo de enclave é **ENCLAVE \_ TYPE \_ VBS**, que especifica um enclave VBS (segurança baseada em virtualização).<br/>                                   |
| [**IMAGE \_ ENCLAVE \_ CONFIG32**](/windows/desktop/api/winnt/ns-winnt-image_enclave_config32)<br/>                         | Define o formato da configuração de enclave para sistemas que executam sistemas de 32 bits Windows.<br/>                                                                                                                                          |
| [**IMAGE \_ ENCLAVE \_ CONFIG64**](/previous-versions/windows/desktop/legacy/mt844244(v=vs.85))<br/>                         | Define o formato da configuração de enclave para sistemas que executam sistemas de 64 bits Windows.<br/>                                                                                                                                          |
| [**IMPORTAÇÃO \_ DE ENCLAVE DE \_ IMAGEM**](/windows/desktop/api/winnt/ns-winnt-image_enclave_import)<br/>                             | Define uma entrada na matriz de imagens que um enclave pode importar.<br/>                                                                                                                                                           |
| [**RELATÓRIO DE \_ ENCLAVE do \_ VBS**](/windows/desktop/api/ntenclv/ns-ntenclv-vbs_enclave_report)<br/>                                 | Descreve o formato da instrução assinada contida em um relatório gerado chamando a [**função EnclaveGetAttestationReport.**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavegetattestationreport)<br/>                                                     |
| [**MÓDULO DE \_ RELATÓRIO DO ENCLAVE do VBS \_ \_**](/windows/desktop/api/ntenclv/ns-ntenclv-vbs_enclave_report_module)<br/>                  | Descreve um módulo carregado para o enclave.<br/>                                                                                                                                                                                   |
| [**VBS \_ ENCLAVE \_ REPORT \_ PKG \_ HEADER**](/windows/desktop/api/ntenclv/ns-ntenclv-vbs_enclave_report_pkg_header)<br/>         | Descreve o conteúdo de um relatório gerado chamando a [**função EnclaveGetAttestationReport.**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavegetattestationreport)<br/>                                                                                     |
| [**VBS \_ ENCLAVE \_ REPORT \_ VARDATA \_ HEADER**](/windows/desktop/api/ntenclv/ns-ntenclv-vbs_enclave_report_vardata_header)<br/> | Descreve o formato de um bloco de dados variável contido em um relatório que a [**função EnclaveGetAttestationReport**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavegetattestationreport) gera.<br/>                                                          |



 

 

 
