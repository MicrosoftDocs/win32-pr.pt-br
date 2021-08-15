---
description: As funções a seguir são usadas ou implementadas por serviços.
ms.assetid: 63666848-cbac-4853-8b91-89303f9854c0
title: Funções de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55553e29b2ae9fb8e60db2f421fd8aa68cee1c6b79542c7d3d61ef5bcef490f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118888958"
---
# <a name="service-functions"></a>Funções de serviço

As funções a seguir são usadas ou implementadas por serviços.



| Função                                                             | Descrição                                                                                                                           |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**Manipulador**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function)                                           | Uma função de retorno de chamada definida pelo aplicativo usada com [**a função RegisterServiceCtrlHandler.**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlera)     |
| [**HandlerEx**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex)                                       | Uma função de retorno de chamada definida pelo aplicativo usada com [**a função RegisterServiceCtrlHandlerEx.**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlerexa) |
| [**RegisterServiceCtrlHandler**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlera)     | Registra uma função para lidar com solicitações de controle de serviço.                                                                              |
| [**RegisterServiceCtrlHandlerEx**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlerexa) | Registra uma função para lidar com solicitações de controle de serviço estendidas.                                                                     |
| [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona)                                   | Uma função definida pelo aplicativo que serve como o ponto de partida para um serviço.                                                      |
| [**SetServiceBits**](/windows/desktop/api/Lmserver/nf-lmserver-setservicebits)                             | Registra um tipo de serviço com o gerenciador de controle de serviço e o serviço servidor.                                                     |
| [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus)                         | Atualiza as informações de status do gerenciador de controle de serviço para o serviço de chamada.                                                     |
| [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera)     | Conecta o thread principal de um processo de serviço ao gerenciador de controle de serviço.                                                         |



 

As funções a seguir são usadas por programas que controlam, configuram ou interagem com serviços.



| Função                                                                 | Descrição                                                                                                                                 |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga)                       | Altera os parâmetros de configuração de um serviço.                                                                                          |
| [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a)                     | Altera os parâmetros de configuração opcionais de um serviço.                                                                                 |
| [**CloseServiceHandle**](/windows/desktop/api/Winsvc/nf-winsvc-closeservicehandle)                         | Fecha o identificador especificado para um objeto do gerenciador de controle de serviço ou um objeto de serviço.                                                        |
| [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice)                                 | Envia um código de controle para um serviço.                                                                                                          |
| [**ControlServiceEx**](/windows/desktop/api/Winsvc/nf-winsvc-controlserviceexa)                             | Envia um código de controle para um serviço.                                                                                                          |
| [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)                                   | Cria um objeto de serviço e o adiciona ao banco de dados do gerenciador de controle de serviço especificado.                                                     |
| [**DeleteService**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice)                                   | Marca o serviço especificado para exclusão do banco de dados do gerenciador de controle de serviço.                                                         |
| [**EnumDependentServices**](/windows/desktop/api/Winsvc/nf-winsvc-enumdependentservicesa)                   | Recupera o nome e o status de cada serviço que depende do serviço especificado.                                                        |
| [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa)                     | Enumera serviços no banco de dados do gerenciador de controle de serviço especificado com base no nível de informações especificado.                             |
| [**GetServiceDisplayName**](/windows/desktop/api/Winsvc/nf-winsvc-getservicedisplaynamea)                   | Recupera o nome de exibição do serviço especificado.                                                                                        |
| [**GetServiceKeyName**](/windows/desktop/api/Winsvc/nf-winsvc-getservicekeynamea)                           | Recupera o nome do serviço do serviço especificado.                                                                                        |
| [**NotifyBootConfigStatus**](/windows/desktop/api/Winsvc/nf-winsvc-notifybootconfigstatus)                 | Relata o status de inicialização para o gerenciador de controle de serviço.                                                                                     |
| [**NotifyServiceStatusChange**](/windows/desktop/api/Winsvc/nf-winsvc-notifyservicestatuschangea)           | Permite que um aplicativo receba notificação quando o serviço especificado é criado ou excluído ou quando seu status muda.                 |
| [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera)                                   | Estabelece uma conexão com o gerenciador de controle de serviço no computador especificado e abre o banco de dados do gerenciador de controle de serviço especificado. |
| [**Openservice**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea)                                       | Abre um serviço existente.                                                                                                                  |
| [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga)                         | Recupera os parâmetros de configuração do serviço especificado.                                                                            |
| [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a)                       | Recupera os parâmetros de configuração opcionais do serviço especificado.                                                                   |
| [**QueryServiceDynamicInformation**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicedynamicinformation) | Recupera informações dinâmicas relacionadas ao início do serviço atual.                                                                         |
| [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity)    | Recupera uma cópia do descritor de segurança associado a um objeto de serviço.                                                               |
| [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex)                     | Recupera o status atual do serviço especificado com base no nível de informações especificado.                                             |
| [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity)        | Define o descritor de segurança de um objeto de serviço.                                                                                           |
| [**Startservice**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea)                                     | Inicia um serviço.                                                                                                                           |



 

## <a name="obsolete-functions"></a>Funções obsoletas

As funções a seguir estão obsoletas.<dl>

[**EnumServicesStatus**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusa)  
[**LockServiceDatabase**](/windows/desktop/api/Winsvc/nf-winsvc-lockservicedatabase)  
[**QueryServiceLockStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa)  
[**QueryServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatus)  
[**UnlockServiceDatabase**](/windows/desktop/api/Winsvc/nf-winsvc-unlockservicedatabase)  
</dl>

 

 
