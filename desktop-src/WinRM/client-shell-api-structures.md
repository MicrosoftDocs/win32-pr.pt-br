---
title: Estruturas e definições de API do Shell do Cliente
description: A tabela a seguir fornece uma visão geral das estruturas e outras definições para a API do Shell de Cliente Windows WinRM (Gerenciamento Remoto).
ms.assetid: b7a3c92e-6796-482f-9d70-18a48cce4ad8
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c9c3d1f6f9f9d476e9b49ef309e5236e4421e0b5afa77fa1072b92f2060cfcd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119643256"
---
# <a name="client-shell-api-structures-and-definitions"></a>Estruturas e definições de API do Shell do Cliente

A tabela a seguir fornece uma visão geral das estruturas e outras definições para a API do Shell de Cliente Windows WinRM (Gerenciamento Remoto).



| Função                                                                      | Descrição                                                                                  |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**FUNÇÃO DE CONCLUSÃO \_ DO SHELL \_ DO WSMAN \_**](/windows/win32/api/wsman/nc-wsman-wsman_shell_completion_function) | A função de retorno de chamada que é chamada para operações de shell, que resultam em uma solicitação remota. |



 



| Estrutura                                                                      | Descrição                                                                                                                                 |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**CREDENCIAIS DE \_ AUTENTICAÇÃO DO WSMAN \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_authentication_credentials) | Define o método de autenticação e as credenciais usadas para autenticação de servidor ou proxy.                                              |
| [**DADOS DO \_ WSMAN**](/windows/desktop/api/Wsman/ns-wsman-wsman_data)                                              | Armazena dados de entrada e saída usados na API do WinRM.                                                                                     |
| [**BINÁRIO DE \_ DADOS DO WSMAN \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_data_binary)                               | Armazena dados binários para uso com várias funções de API do WinRM.                                                                                |
| [**TEXTO DE DADOS \_ DO WSMAN \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_data_text)                                   | Armazena dados baseados em texto para uso com várias funções de API do WinRM.                                                                            |
| [**VARIÁVEL DE \_ AMBIENTE \_ WSMAN**](/windows/desktop/api/Wsman/ns-wsman-wsman_environment_variable)             | Define uma variável de ambiente individual usando um par nome e valor.                                                                  |
| [**CONJUNTO DE \_ VARIÁVEIS DE \_ AMBIENTE DO WSMAN \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_environment_variable_set)    | Define uma matriz de variáveis de ambiente.                                                                                                  |
| [**ERRO do \_ WSMAN**](/windows/desktop/api/Wsman/ns-wsman-wsman_error)                                     | Contém informações de erro.                                                                                                                 |
| [**CHAVE \_ WSMAN**](/windows/desktop/api/Wsman/ns-wsman-wsman_key)                                                | Representa um par chave e valor dentro de um conjunto de seletores e é usado para identificar um recurso específico.                                       |
| [**OPÇÃO \_ WSMAN**](/windows/desktop/api/Wsman/ns-wsman-wsman_option)                                          | Representa um par de nome e valor de opção específico.                                                                                           |
| [**WSMAN \_ OPTION \_ SET**](/windows/desktop/api/Wsman/ns-wsman-wsman_option_set)                                 | Representa um conjunto de opções.                                                                                                                |
| [**INFORMAÇÕES DE PROXY DO WSMAN \_ \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_proxy_info)                                 | Define as informações de proxy para cada sessão.                                                                                                |
| [**RESULTADO DE \_ RECEBIMENTO DE DADOS \_ DO \_ WSMAN**](/windows/desktop/api/Wsman/ns-wsman-wsman_receive_data_result)              | Representa os dados de saída recebidos da API [**WSManReceiveShellOutput.**](/windows/desktop/api/Wsman/nf-wsman-wsmanreceiveshelloutput)                                |
| [**DADOS DE RESPOSTA \_ DO WSMAN \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_response_data)                           | Representa os dados de saída recebidos de uma [**operação WSMan.**](wsman.md)                                                                |
| [**CONJUNTO DE \_ SELETORES DO WSMAN \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_selector_set)                             | Define um conjunto de chaves que representam a identidade de um recurso.                                                                            |
| [**WSMAN \_ SHELL \_ ASYNC**](/windows/desktop/api/Wsman/ns-wsman-wsman_shell_async)                               | Define uma estrutura assíncrona que é passada para todas as operações de shell.                                                                   |
| [**INFORMAÇÕES DE DESCONEXÃO \_ DO SHELL \_ DO WSMAN \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_shell_disconnect_info)          | TBD                                                                                                                                         |
| [**INFORMAÇÕES DE \_ INICIALIZAÇÃO DO SHELL \_ DO WSMAN \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_shell_startup_info_v10)                | Armazena todos os dados específicos do shell necessários para criar um shell usando a chamada de plug-in [**WSManCreateShell.**](/windows/desktop/api/Wsman/nf-wsman-wsmancreateshell) |
| [**CONJUNTO DE \_ \_ IDS DE FLUXO DO WSMAN \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_stream_id_set)                          | Lista todos os fluxos usados para entrada ou saída para o shell e comandos.                                                  |
| [**CREDS DE SENHA DE \_ \_ NOME DE USUÁRIO \_ DO WSMAN**](/windows/desktop/api/Wsman/ns-wsman-wsman_username_password_creds)      | Define as credenciais usadas para autenticação.                                                                                            |



 

 

 