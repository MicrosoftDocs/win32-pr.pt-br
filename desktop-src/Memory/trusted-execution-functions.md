---
description: 'As funções a seguir são usadas ao trabalhar com enclaves que são usadas para criar ambientes de execução confiáveis:'
ms.assetid: DF6CDEE1-CAAA-429C-9939-DDC844302027
title: Funções de execução confiável
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4b1bd2411d0448346f0a8afcca870c26b4a61ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758423"
---
# <a name="trusted-execution-functions"></a>Funções de execução confiável

As funções a seguir são usadas ao trabalhar com enclaves que são usadas para criar ambientes de execução confiáveis:

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                               | Descrição                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CallEnclave**](/windows/desktop/api/Enclaveapi/nf-enclaveapi-callenclave)<br/>                                       | Chama uma função em um enclave. <br/>                                                                                                                                                                                |
| [**CreateEnclave**](/windows/desktop/api/enclaveapi/nf-enclaveapi-createenclave)<br/>                                   | Cria um novo enclave não inicializado. Um enclave é uma região isolada de código e dados dentro do espaço de endereço de um aplicativo. Somente o código que é executado no enclave pode acessar dados dentro do mesmo enclave.<br/> |
| [**DeleteEnclave**](/windows/desktop/api/Enclaveapi/nf-enclaveapi-deleteenclave)<br/>                                   | Exclui o enclave especificado.<br/>                                                                                                                                                                                      |
| [**EnclaveGetAttestationReport**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavegetattestationreport)<br/>       | Obtém um relatório de atestado de enclave que descreve o enclave atual e é assinado pela autoridade responsável pelo tipo de enclave. <br/>                                                              |
| [**EnclaveGetEnclaveInformation**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavegetenclaveinformation)<br/>     | Obtém informações sobre o enclave em execução no momento.<br/>                                                                                                                                                             |
| [**EnclaveSealData**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavesealdata)<br/>                               | Gera um objeto binário grande criptografado (BLOB) de dados unencypted.<br/>                                                                                                                                             |
| [**EnclaveUnsealData**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclaveunsealdata)<br/>                           | Descriptografa um objeto binário grande criptografado (BLOB).<br/>                                                                                                                                                                   |
| [**EnclaveVerifyAttestationReport**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclaveverifyattestationreport)<br/> | Verifica um relatório de atestado que foi gerado no sistema atual. <br/>                                                                                                                                           |
| [**InitializeEnclave**](/windows/desktop/api/enclaveapi/nf-enclaveapi-initializeenclave)<br/>                           | Inicializa um enclave que você criou e carregou com dados.<br/>                                                                                                                                                       |
| [**IsEnclaveTypeSupported**](/windows/desktop/api/enclaveapi/nf-enclaveapi-isenclavetypesupported)<br/>                 | Recupera se há suporte para o tipo especificado de enclave.<br/>                                                                                                                                                       |
| [**LoadEnclaveData**](/windows/desktop/api/enclaveapi/nf-enclaveapi-loadenclavedata)<br/>                               | Carrega dados em um enclave não inicializado que você criou chamando [**CreateEnclave**](/windows/desktop/api/enclaveapi/nf-enclaveapi-createenclave).<br/>                                                                                                        |
| [**LoadEnclaveImage**](/windows/desktop/api/Enclaveapi/nf-enclaveapi-loadenclaveimagew)<br/>                             | Carrega uma imagem e todas as suas importações em um enclave.<br/>                                                                                                                                                              |
| [**TerminateEnclave**](/windows/desktop/api/Enclaveapi/nf-enclaveapi-terminateenclave)<br/>                             | Encerra a execução dos threads que estão sendo executados em um enclave.<br/>                                                                                                                                               |



 

 

 




