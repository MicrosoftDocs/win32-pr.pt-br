---
description: O Windows 7 e o Windows Server 2008 R2 incluem os seguintes elementos de programação novos e atualizados para serviços.
ms.assetid: 4be7e244-ad4c-440d-b04e-23afb4c7ddf2
title: Novidades em serviços para o Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51bd2e8bfa5426447e24485ed026f27e90fdcaa1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755945"
---
# <a name="whats-new-in-services-for-windows-7"></a>O que há de novo nos serviços do Windows 7

O Windows 7 e o Windows Server 2008 R2 incluem os seguintes elementos de programação novos e atualizados para serviços.

## <a name="new-capabilities"></a>Novos recursos

Um serviço pode se registrar para ser iniciado ou interrompido quando ocorrer um evento de gatilho. Isso elimina a necessidade de que os serviços sejam iniciados quando o sistema é iniciado, ou para que os serviços sejam sondados ou aguardam ativamente um evento; um serviço pode ser iniciado quando necessário, em vez de iniciar automaticamente se o trabalho deve ou não ser feito. Para obter mais informações, consulte [eventos de gatilho de serviço](service-trigger-events.md).

## <a name="updated-functions"></a>Funções atualizadas



| Função                                                        | Descrição                                                                                                                                                                                                                                                                                |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga)<br/>   | Altera os parâmetros de configuração de um serviço. Essa função dá suporte a contas de serviço gerenciadas e contas virtuais. Para obter mais informações, consulte Guia passo a [passo das contas de serviço](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd548356(v=ws.10)).<br/>                                      |
| [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a)<br/> | Altera os parâmetros de configuração opcionais de um serviço. Essa função dá suporte a novos níveis de informações de configuração para grupos de processador e eventos de gatilho de serviço.<br/>                                                                                                        |
| [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)<br/>               | Cria um objeto de serviço e o adiciona ao banco de dados do Gerenciador de controle de serviço especificado. Essa função dá suporte a contas de serviço gerenciadas e contas virtuais. Para obter mais informações, consulte Guia passo a [passo das contas de serviço](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd548356(v=ws.10)).<br/> |
| [**HandlerEx**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex)<br/>                       | Uma função de retorno de chamada definida pelo aplicativo usada com a função [**RegisterServiceCtrlHandlerEx**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlerexa) . Essa função de retorno de chamada dá suporte a novos códigos de controle estendidos para alterações de horário do sistema e eventos de gatilho de serviço<br/>                            |
| [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a)<br/>   | Recupera os parâmetros de configuração opcionais de um serviço. Essa função dá suporte a novos níveis de informações de configuração para grupos de processador e eventos de gatilho de serviço.<br/>                                                                                                      |
| [**Falha em SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus)<br/>         | Atualiza as informações de status do Gerenciador de controle de serviço para o serviço de chamada. Essa função dá suporte a novos códigos de controle estendidos para alterações de horário do sistema e eventos de gatilho de serviço.<br/>                                                                                         |



 

## <a name="new-structures"></a>Novas estruturas



| Estrutura                                                                                       | Descrição                                                            |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**\_informações de TIMEchange do serviço \_**](/windows/desktop/api/winsvc/ns-winsvc-service_timechange_info)<br/>                         | Contém configurações de alteração de horário do sistema. <br/>                      |
| [**gatilho de serviço \_**](/windows/desktop/api/winsvc/ns-winsvc-service_trigger)<br/>                                          | Representa um evento de gatilho de serviço.<br/>                         |
| [**\_informações do gatilho de serviço \_**](/windows/desktop/api/winsvc/ns-winsvc-service_trigger_info)<br/>                               | Contém informações de evento de gatilho para um serviço.<br/>           |
| [**\_item de \_ \_ dados específico do gatilho \_ de serviço**](/windows/desktop/api/winsvc/ns-winsvc-service_trigger_specific_data_item)<br/> | Contém dados específicos do gatilho para um evento de gatilho de serviço.<br/> |



 

 

