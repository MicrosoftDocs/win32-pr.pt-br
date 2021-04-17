---
description: Para iniciar um serviço de serviço ou de driver, o programa de controle de serviço usa a função StartService.
ms.assetid: 7d2ee779-1554-436a-a65c-f0322745f46a
title: Inicialização do serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f5fcd9ee820357e75bf07649da8e6c5445d3f42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748386"
---
# <a name="service-startup"></a>Inicialização do serviço

Para iniciar um serviço de serviço ou de driver, o programa de controle de serviço usa a função [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) . A função **StartService** falhará se o banco de dados estiver bloqueado. Se isso ocorrer, o programa de controle de serviço deve aguardar alguns segundos e chamar **StartService** novamente. Ele pode verificar o status de bloqueio atual do banco de dados chamando a função [**QueryServiceLockStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa) .

Se o programa de controle de serviço estiver iniciando um serviço, ele poderá usar a função [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) para especificar uma matriz de argumentos a serem passados para a [**função**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) ServiceName do serviço. A função **StartService** retorna depois que um novo thread é criado para executar a função de **immain** . O programa de controle de serviço pode recuperar o status do serviço iniciado recentemente em uma estrutura de [**\_ status de serviço**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) chamando a função [**QueryServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatus) . Durante a inicialização, o membro **dwCurrentState** deve ser o início do serviço \_ \_ pendente. O membro **dwWaitHint** é um intervalo de tempo, em milissegundos, que indica por quanto tempo o programa de controle de serviço deve aguardar antes de chamar **QueryServiceStatus** novamente. Quando a inicialização for concluída, o serviço alterará **dwCurrentState** para o serviço \_ em execução.

O Gerenciador de controle de serviço não dá suporte à passagem de variáveis de ambiente personalizadas para um serviço na inicialização. Além disso, o Gerenciador de controle de serviço não detecta e passa alterações em variáveis de ambiente enquanto o serviço está em execução. Em vez de tornar um serviço dependente de uma variável de ambiente, use valores de registro ou argumentos de [**usermain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) .

Veja a seguir uma visão geral simplificada do que acontece quando um serviço típico é iniciado pelo Gerenciador de controle de serviço:

-   O SCM lê o caminho do serviço do registro e se prepara para iniciar o serviço. Isso inclui a aquisição do bloqueio do serviço. Qualquer tentativa de iniciar outro serviço enquanto o bloqueio de serviço é mantido será bloqueado até que o bloqueio do serviço seja liberado.
-   O SCM inicia o processo e aguarda até que o processo filho seja encerrado (indicando uma falha) ou relate o \_ status de execução do serviço.
-   O aplicativo executa sua inicialização muito simples e chama a função [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) .
-   [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) conecta-se ao Gerenciador de controle de serviço e inicia um segundo thread que chama a função de serviço de [**Gerenciamento de serviços**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) . O serviço de **relatório deve ser** executado assim que \_ possível.
-   Quando o Gerenciador de controle de serviço é notificado de que o serviço está em execução, ele libera o bloqueio de serviço.

Se o serviço não atualizar seu status dentro de 80 segundos, além da última dica de espera, o Gerenciador de controle de serviço determinará que o serviço parou de responder. O Gerenciador de controle de serviço registrará um evento e interromperá o serviço.

Se o programa estiver iniciando um serviço de driver, [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) retornará depois que o driver de dispositivo concluir sua inicialização.

Para obter mais informações, consulte [iniciando um serviço](starting-a-service.md).

 

 
