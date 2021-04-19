---
description: Um serviço pode se registrar para ser iniciado ou interrompido quando ocorrer um evento de gatilho.
ms.assetid: ca02a3ae-b16a-4427-b6db-b935c9cf23b3
title: Eventos de gatilho de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdefd94b7896936f7ab4fc014647b08470611573
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754112"
---
# <a name="service-trigger-events"></a>Eventos de gatilho de serviço

Um serviço pode se registrar para ser iniciado ou interrompido quando ocorrer um evento de gatilho. Isso elimina a necessidade de que os serviços sejam iniciados quando o sistema é iniciado, ou para que os serviços sejam sondados ou aguardam ativamente um evento; um serviço pode ser iniciado quando necessário, em vez de iniciar automaticamente se o trabalho deve ou não ser feito. Exemplos de eventos de gatilho predefinidos incluem a chegada de um dispositivo de uma classe de interface de dispositivo especificada ou a disponibilidade de uma porta de firewall específica. Um serviço também pode se registrar para um evento de gatilho personalizado gerado por um provedor de ETW ( [rastreamento de eventos para Windows](../etw/event-tracing-portal.md) ).

**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Não há suporte para eventos de gatilho de serviço até o Windows Server 2008 R2 e o Windows 7.

Um gatilho consiste em um tipo de evento de gatilho, um subtipo de evento de gatilho, a ação a ser executada em resposta ao evento de gatilho e (para determinados tipos de evento de gatilho) um ou mais itens de dados específicos do gatilho. O subtipo e os itens de dados específicos do gatilho juntos especificam as condições para notificar o serviço do evento. O formato de um item de dados depende do tipo de evento Trigger; um item de dados pode ser dados binários, uma cadeia de caracteres ou uma cadeia de caracteres. Cadeias de caracteres devem ser Unicode; Não há suporte para cadeias de caracteres ANSI.

Para se registrar para eventos de gatilho, o serviço chama [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) com **informações de gatilho de configuração de serviço \_ \_ \_** e fornece uma estrutura de [**\_ \_ informações de gatilho de serviço**](/windows/desktop/api/winsvc/ns-winsvc-service_trigger_info) . A estrutura de **\_ \_ informações do gatilho de serviço** aponta para uma matriz de estruturas de [**\_ gatilho de serviço**](/windows/desktop/api/winsvc/ns-winsvc-service_trigger) , cada uma especificando um gatilho.

A ação de gatilho especificada será executada se a condição do gatilho for verdadeira quando o sistema for iniciado, ou se a condição do gatilho se tornar verdadeira enquanto o sistema estiver em execução. Por exemplo, se um serviço se registrar para ser iniciado quando um dispositivo específico estiver disponível, o serviço será iniciado quando o sistema for iniciado se o dispositivo já estiver conectado ao computador; o serviço é iniciado quando o dispositivo chega se o usuário se conecta ao dispositivo enquanto o sistema está em execução.

Se um gatilho tiver itens de dados específicos do gatilho, a ação do gatilho será executada somente se o item de dados que acompanha o evento de gatilho corresponder a um dos itens de dados que o serviço especificou com o gatilho. A correspondência de dados binários é feita pela comparação de bits. Correspondência de cadeia de caracteres não diferencia maiúsculas de minúsculas. Se o item de dados for uma cadeia de caracteres multistring, todas as cadeias de caracteres em multistring deverão corresponder.

Quando um serviço é iniciado em resposta a um evento de gatilho, o serviço recebe o **argumento do gatilho de serviço \_ \_ \_ iniciado** como *argv* \[ 1 \] em sua função de retorno de chamada de [*immain*](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) . *Argv* \[ 0 \] é sempre o nome curto do serviço.

Um serviço que se registra para ser iniciado em resposta a um evento de gatilho pode ser interrompido após um tempo limite ocioso quando o serviço não tem nenhum trabalho a fazer. Um serviço que se interrompe deve ser preparado para manipular solicitações de controle de **\_ \_ TRIGGEREVENT de controle de serviço** que chegam enquanto o serviço está se interrompendo. O SCM envia uma solicitação de controle **\_ \_ TRIGGEREVENT de controle de serviço** sempre que um novo evento de gatilho ocorre enquanto o serviço está em estado de execução. Para evitar a perda de eventos de gatilho, o serviço deve retornar o **\_ desligamento \_ de erro em \_ andamento** para qualquer solicitação de controle **TRIGGEREVENT de \_ controle \_ de serviço** que chega enquanto o serviço está em transição de em execução para parado. Isso instrui o SCM a enfileirar eventos de gatilho e aguardar o serviço entrar no estado parado. Em seguida, o SCM executa a ação associada ao evento de gatilho enfileirado, como iniciar o serviço.

Quando o serviço estiver pronto para lidar com eventos de gatilho novamente, ele definirá o **serviço de \_ aceitação de \_ TRIGGEREVENT** em sua máscara de controles aceita em uma chamada para [**falha em SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus). Isso geralmente é feito quando o serviço chama **falha em SetServiceStatus** com o **serviço \_ em execução**. Em seguida, o SCM emite uma solicitação de **\_ \_ TRIGGEREVENT de controle de serviço** para cada evento de gatilho Enfileirado até que a fila esteja vazia.

Um serviço que tem serviços dependentes em execução não pode ser interrompido em resposta a um evento de gatilho.

As solicitações Trigger-Start e Trigger-Stop não são garantidas em condições de memória insuficiente.

Use a função [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) para recuperar a configuração de evento de gatilho de um serviço.

A ferramenta SC (sc.exe) pode ser usada para configurar ou consultar os eventos de gatilho de um serviço no prompt de comando. Use a opção **triggerinfo** para configurar um serviço para iniciar ou parar em resposta a um evento de gatilho. Use a opção **qtriggerinfo** para consultar a configuração do gatilho de um serviço.

O exemplo a seguir consulta a configuração do gatilho do serviço W32time, que é configurado para iniciar quando o computador é ingressado em um domínio e parar quando o computador sair do domínio.

``` syntax
C:\>sc qtriggerinfo w32time
[SC] QueryServiceConfig2 SUCCESS

SERVICE_NAME: w32time

        START SERVICE
          DOMAIN JOINED STATUS         : 1ce20aba-9851-4421-9430-1ddeb766e809 [DOMAIN JOINED]
        STOP SERVICE
          DOMAIN JOINED STATUS         : ddaf516e-58c2-4866-9574-c3b615d42ea1 [NOT DOMAIN JOINED]
```

O exemplo a seguir consulta a configuração do gatilho do serviço de entrada do Tablet, que é configurado para iniciar quando um dispositivo HID com o **GUID** {4d1e55b2-f16f-11CF-88cb-001111000030} e qualquer uma das IDs de dispositivo HID especificadas chegar.

``` syntax
C:\>sc qtriggerinfo tabletinputservice
[SC] QueryServiceConfig2 SUCCESS

SERVICE_NAME: tabletinputservice

        START SERVICE
          DEVICE INTERFACE ARRIVAL     : 4d1e55b2-f16f-11cf-88cb-001111000030 [INTERFACE CLASS GUID]
            DATA                       : HID_DEVICE_UP:000D_U:0001
            DATA                       : HID_DEVICE_UP:000D_U:0002
            DATA                       : HID_DEVICE_UP:000D_U:0003
            DATA                       : HID_DEVICE_UP:000D_U:0004
```

 

 
