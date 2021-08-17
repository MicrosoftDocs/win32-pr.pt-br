---
title: Estruturas de API de plug-in do WinRM
description: Estruturas de API de plug-in do WinRM
ms.assetid: 745619bc-c7b3-48fa-8212-cb1b5b9ed4db
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4a57cbc31ae19bd858a191cec827760d055a87fc7ca19b134f61b17f8fd065e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742764"
---
# <a name="winrm-plug-in-api-structures"></a>Estruturas de API de plug-in do WinRM

a tabela a seguir fornece uma visão geral das estruturas na API (interface de programação de aplicativo) do plug-in do Gerenciamento Remoto do Windows (WinRM).



| Estrutura                                                        | Descrição                                                                              |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [**cota do WSMAN \_ AUTHZ \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_authz_quota)                 | Define informações de cotas para cada usuário.                                           |
| [**\_detalhes do certificado WSMan \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_certificate_details) | Representa os campos dentro do certificado do cliente.                                     |
| [**\_conjunto de \_ ARG de comando WSMan \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_command_arg_set)        | Representa o conjunto de argumentos que são passados para a linha de comando.                  |
| [**\_filtro WSMan**](/windows/desktop/api/Wsman/ns-wsman-wsman_filter)                            | Define a filtragem usada para uma operação.                                             |
| [**fragmento do WSMAN \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_fragment)                        | Define as informações de fragmento para uma operação.                                       |
| [**\_informações da operação do WSMan \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_operation_info)           | Representa um ponto de extremidade de recurso específico para o qual o plug-in deve executar a solicitação. |
| [**\_solicitação de plug-in do WSMan \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_plugin_request)           | Contém informações sobre a solicitação e é passado para cada operação de plug-in.       |
| [**\_detalhes do remetente WSMan \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_sender_details)           | Especifica os detalhes do cliente para cada solicitação de entrada.                                      |



 

 

 




