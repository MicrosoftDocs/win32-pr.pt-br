---
description: Quando um programa de controle de serviço solicita que um novo serviço seja executado, o SCM (Gerenciador de controle de serviço) inicia o serviço e envia uma solicitação de início para o Dispatcher de controle.
ms.assetid: e55e056f-7628-4e3d-9aea-b55c371b4287
title: Função Service-Main
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed50f0f378f348415e56827a09fcf17eea7fc330
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922612"
---
# <a name="service-servicemain-function"></a>Função Service-Main

Quando um programa de controle de serviço solicita que um novo serviço seja executado, o SCM (Gerenciador de controle de serviço) inicia o serviço e envia uma solicitação de início para o Dispatcher de controle. O Dispatcher de controle cria um novo thread para executar a função de serviço de [**immain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) . Para obter um exemplo, consulte [escrevendo uma função de immain](writing-a-servicemain-function.md).

A função de [**immain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) deve executar as seguintes tarefas:

1.  Inicializar todas as variáveis globais.
2.  Chame a função [**RegisterServiceCtrlHandler**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlera) imediatamente para registrar uma função de [**manipulador**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) para manipular solicitações de controle para o serviço. O valor de retorno de **RegisterServiceCtrlHandler** é um *identificador de status de serviço* que será usado em chamadas para notificar o SCM do status do serviço.
3.  Execute a inicialização. Se espera-se que o tempo de execução do código de inicialização seja muito curto (menos de um segundo), a inicialização pode ser executada diretamente no [**usermain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona).

    Se espera-se que o tempo de inicialização seja maior que um segundo, o serviço deve usar uma das seguintes técnicas de inicialização:

    -   Chame a função [**falha em SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) para relatar o serviço \_ , mas não aceite controles até que a inicialização seja concluída. O serviço faz isso chamando **falha em SetServiceStatus** com **DWCURRENTSTATE** definido como serviço \_ em execução e **dwControlsAccepted** definido como 0 na estrutura de [**\_ status do serviço**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) . Isso garante que o SCM não enviará nenhuma solicitação de controle ao serviço antes de estar pronto e liberará o SCM para gerenciar outros serviços. Essa abordagem de inicialização é recomendada para o desempenho, especialmente para serviços de inicialização automática.
    -   Início do \_ serviço \_ de relatório pendente, não aceite controles e especifique uma dica de espera. Se o código de inicialização do serviço executar tarefas que devem levar mais tempo do que o valor da dica de espera inicial, seu código deverá chamar a função [**falha em SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) periodicamente (possivelmente com uma dica de espera revisada) para indicar que o progresso está sendo feito. Certifique-se de chamar **falha em SetServiceStatus** somente se a inicialização estiver progredindo. Caso contrário, o SCM pode aguardar o serviço entrar no \_ estado de execução do serviço, supondo que o serviço esteja progredindo e impeça a inicialização de outros serviços. Não chame **falha em SetServiceStatus** de um thread separado, a menos que você tenha certeza de que o thread que está executando a inicialização está realmente progredindo.

        Um serviço que usa essa abordagem também pode especificar um valor de ponto de verificação e incrementar o valor periodicamente durante uma inicialização demorada. O programa que iniciou o serviço pode chamar [**QueryServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatus) ou [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) para obter o valor de ponto de verificação mais recente do SCM e usar o valor para relatar o progresso incremental ao usuário.

4.  Quando a inicialização for concluída, chame [**falha em SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) para definir o estado do serviço como serviço \_ em execução e especifique os controles que o serviço está preparado para aceitar. Para obter uma lista de controles, consulte a estrutura de [**\_ status do serviço**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) .
5.  Execute as tarefas de serviço ou, se não houver nenhuma tarefa pendente, retorne o controle ao chamador. Qualquer alteração no estado do serviço garante uma chamada para [**falha em SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) para relatar novas informações de status.
6.  Se ocorrer um erro enquanto o serviço estiver inicializando ou em execução, o serviço deverá chamar [**falha em SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) para definir o estado do serviço como serviço de \_ parada \_ pendente se a limpeza for longa. Após a conclusão da limpeza, chame **falha em SetServiceStatus** para definir o estado do serviço como serviço \_ parado do último thread a ser encerrado. Certifique-se de definir os membros **dwServiceSpecificExitCode** e **dwWin32ExitCode** da estrutura de [**\_ status do serviço**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) para identificar o erro.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Escrevendo uma função de immain](writing-a-servicemain-function.md)
</dt> </dl>

 

 
