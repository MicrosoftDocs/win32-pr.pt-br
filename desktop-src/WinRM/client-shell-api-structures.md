---
title: Definições e estruturas da API do shell do cliente
description: A tabela a seguir fornece uma visão geral das estruturas e outras definições para a API do Shell de cliente Gerenciamento Remoto do Windows (WinRM).
ms.assetid: b7a3c92e-6796-482f-9d70-18a48cce4ad8
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c00a908856a6df8233e377d917ff28029dc8468e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366169"
---
# <a name="client-shell-api-structures-and-definitions"></a>Definições e estruturas da API do shell do cliente

A tabela a seguir fornece uma visão geral das estruturas e outras definições para a API do Shell de cliente Gerenciamento Remoto do Windows (WinRM).



| Função                                                                      | Descrição                                                                                  |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**\_função de \_ conclusão do Shell WSMan \_**](/windows/win32/api/wsman/nc-wsman-wsman_shell_completion_function) | A função de retorno de chamada que é chamada para operações de Shell, que resultam em uma solicitação remota. |



 



| Estrutura                                                                      | Descrição                                                                                                                                 |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_credenciais de autenticação do WSMan \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_authentication_credentials) | Define o método de autenticação e as credenciais usadas para autenticação de servidor ou proxy.                                              |
| [**\_dados WSMan**](/windows/desktop/api/Wsman/ns-wsman-wsman_data)                                              | Armazena dados de entrada e de saída usados na API do WinRM.                                                                                     |
| [**\_binário de dados WSMan \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_data_binary)                               | Armazena dados binários para uso com várias funções de API do WinRM.                                                                                |
| [**\_texto de dados do WSMan \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_data_text)                                   | Armazena dados baseados em texto para uso com várias funções de API do WinRM.                                                                            |
| [**\_variável de ambiente WSMan \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_environment_variable)             | Define uma variável de ambiente individual usando um par de nome e valor.                                                                  |
| [**\_conjunto de \_ variáveis de ambiente WSMan \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_environment_variable_set)    | Define uma matriz de variáveis de ambiente.                                                                                                  |
| [**erro de WSMAN \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_error)                                     | Contém informações de erro.                                                                                                                 |
| [**\_chave WSMan**](/windows/desktop/api/Wsman/ns-wsman-wsman_key)                                                | Representa um par de chave e valor dentro de um conjunto de seletor e é usado para identificar um recurso específico.                                       |
| [**\_opção WSMan**](/windows/desktop/api/Wsman/ns-wsman-wsman_option)                                          | Representa um par de nome de opção e valor específico.                                                                                           |
| [**\_conjunto de opções WSMan \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_option_set)                                 | Representa um conjunto de opções.                                                                                                                |
| [**\_informações de proxy do WSMan \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_proxy_info)                                 | Define as informações de proxy para cada sessão.                                                                                                |
| [**\_resultado de \_ dados de recebimento do WSMan \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_receive_data_result)              | Representa os dados de saída recebidos da API [**WSManReceiveShellOutput**](/windows/desktop/api/Wsman/nf-wsman-wsmanreceiveshelloutput) .                                |
| [**\_dados de resposta do WSMan \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_response_data)                           | Representa os dados de saída recebidos de uma operação [**WSMan**](wsman.md) .                                                                |
| [**\_conjunto de seletores WSMan \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_selector_set)                             | Define um conjunto de chaves que representam a identidade de um recurso.                                                                            |
| [**Shell do WSMAN \_ \_ Async**](/windows/desktop/api/Wsman/ns-wsman-wsman_shell_async)                               | Define uma estrutura assíncrona que é passada para todas as operações de Shell.                                                                   |
| [**\_informações de \_ desconexão do shell do WSMan \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_shell_disconnect_info)          | TBD                                                                                                                                         |
| [**\_informações de \_ inicialização do Shell WSMan \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_shell_startup_info_v10)                | Armazena todos os dados específicos do Shell necessários para criar um shell usando a chamada de plug-in [**WSManCreateShell**](/windows/desktop/api/Wsman/nf-wsman-wsmancreateshell) . |
| [**\_conjunto de \_ IDs de fluxo WSMan \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_stream_id_set)                          | Lista todos os fluxos que são usados para entrada ou saída para o Shell e os comandos.                                                  |
| [**credenciais de senha de nome de \_ usuário WSMan \_ \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_username_password_creds)      | Define as credenciais usadas para autenticação.                                                                                            |



 

 

 