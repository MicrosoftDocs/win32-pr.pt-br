---
description: Um serviço pode se registrar para ser iniciado ou interrompido quando ocorre um evento de gatilho.
ms.assetid: ca02a3ae-b16a-4427-b6db-b935c9cf23b3
title: Eventos de gatilho de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67b6c219f91668af3372cf6c50b005d544a2544232d83e2e215d50a194db95b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117967259"
---
# <a name="service-trigger-events"></a>Eventos de gatilho de serviço

Um serviço pode se registrar para ser iniciado ou interrompido quando ocorre um evento de gatilho. Isso elimina a necessidade de os serviços iniciarem quando o sistema é iniciado ou que os serviços façam sondagem ou aguardem ativamente por um evento; um serviço pode iniciar quando for necessário, em vez de iniciar automaticamente, independentemente de haver trabalho a ser feito ou não. Exemplos de eventos de gatilho predefinidos incluem a chegada de um dispositivo de uma classe de interface do dispositivo especificada ou a disponibilidade de uma porta de firewall específica. Um serviço também pode se registrar para um evento de gatilho personalizado gerado por um provedor ETW (Rastreamento de Eventos [para Windows).](../etw/event-tracing-portal.md)

**Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Não há suporte para eventos de gatilho de serviço Windows Server 2008 R2 e Windows 7.

Um gatilho consiste em um tipo de evento de gatilho, um subtipo de evento de gatilho, a ação a ser tomada em resposta ao evento de gatilho e (para determinados tipos de evento de gatilho) um ou mais itens de dados específicos do gatilho. O subtipo e os itens de dados específicos do gatilho juntos especificam as condições para notificar o serviço do evento. O formato de um item de dados depende do tipo de evento de gatilho; um item de dados pode ser dados binários, uma cadeia de caracteres ou uma multistring. As cadeias de caracteres devem ser Unicode; Não há suporte para cadeias de caracteres ANSI.

Para se registrar para eventos de gatilho, o serviço [**chama ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) com INFORMAÇÕES DE GATILHO **DE \_ CONFIGURAÇÃO \_ \_** DE SERVIÇO e fornece uma estrutura [**DE INFORMAÇÕES DO GATILHO \_ \_ DE**](/windows/desktop/api/winsvc/ns-winsvc-service_trigger_info) SERVIÇO. A **estrutura SERVICE TRIGGER \_ \_ INFO** aponta para uma matriz de estruturas [**SERVICE \_ TRIGGER,**](/windows/desktop/api/winsvc/ns-winsvc-service_trigger) cada uma especificando um gatilho.

A ação de gatilho especificada será tomada se a condição do gatilho for verdadeira quando o sistema for iniciado ou se a condição do gatilho se tornar verdadeira enquanto o sistema estiver em execução. Por exemplo, se um serviço for registrado para ser iniciado quando um dispositivo específico estiver disponível, o serviço será iniciado quando o sistema for iniciado se o dispositivo já estiver conectado ao computador; o serviço será iniciado quando o dispositivo chegar se o usuário conectar o dispositivo enquanto o sistema estiver em execução.

Se um gatilho tiver itens de dados específicos do gatilho, a ação de gatilho será tomada somente se o item de dados que acompanha o evento de gatilho corresponde a um dos itens de dados especificados pelo serviço com o gatilho. A correspondência de dados binários é feita por comparação bit a bit. A correspondência de cadeia de caracteres não faz maiúsculas de minúsculas. Se o item de dados for uma multistring, todas as cadeias de caracteres na multistring deverão corresponder.

Quando um serviço é iniciado em resposta a um evento de gatilho, o serviço recebe **SERVICE \_ TRIGGER STARTED \_ \_ ARGUMENT** como *argv* 1 em sua função de retorno de chamada \[ \] [*ServiceMain.*](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) *Argv* \[ 0 \] é sempre o nome curto do serviço.

Um serviço que se registra para ser iniciado em resposta a um evento de gatilho pode parar a si mesmo após um tempo de tempo de ociosidade quando o serviço não tem trabalho a ser feito. Um serviço que se interrompe deve estar preparado para lidar com solicitações de controle **\_ SERVICE CONTROL \_ TRIGGEREVENT** que chegam enquanto o serviço está parando a si mesmo. O SCM envia uma solicitação de controle **\_ SERVICE CONTROL \_ TRIGGEREVENT** sempre que um novo evento de gatilho ocorre enquanto o serviço está no estado de execução. Para evitar a perda de eventos de gatilho, o serviço deve retornar **ERROR SHUTDOWN IN PROGRESS \_ \_ \_ para** qualquer solicitação de controle **SERVICE CONTROL \_ \_ TRIGGEREVENT** que chega enquanto o serviço está fazendo a transição da execução para interrompida. Isso instrui o SCM a enfilar eventos de gatilho e aguardar até que o serviço entre no estado parado. Em seguida, o SCM toma a ação associada ao evento de gatilho na fila, como iniciar o serviço.

Quando o serviço está pronto para lidar com eventos de gatilho novamente, ele define **SERVICE \_ ACCEPT \_ TRIGGEREVENT** em sua máscara aceita por controles em uma chamada para [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus). Isso geralmente é feito quando o serviço chama **SetServiceStatus** com **SERVICE \_ RUNNING**. Em seguida, o SCM emite uma solicitação **\_ SERVICE CONTROL \_ TRIGGEREVENT** para cada evento de gatilho na fila até que a fila seja vazia.

Um serviço que tem serviços dependentes em execução não pode ser interrompido em resposta a um evento de gatilho.

As solicitações de gatilho e de parada de gatilho não são garantidas em condições de memória baixa.

Use a [**função QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) para recuperar a configuração de evento de gatilho de um serviço.

A ferramenta sc (sc.exe) pode ser usada para configurar ou consultar eventos de gatilho de um serviço no prompt de comando. Use a **opção triggerinfo** para configurar um serviço para iniciar ou parar em resposta a um evento de gatilho. Use a **opção qtriggerinfo** para consultar a configuração de gatilho de um serviço.

O exemplo a seguir consulta a configuração de gatilho do serviço W32time, que é configurado para iniciar quando o computador é ingressado em um domínio e parar quando o computador sai do domínio.

``` syntax
C:\>sc qtriggerinfo w32time
[SC] QueryServiceConfig2 SUCCESS

SERVICE_NAME: w32time

        START SERVICE
          DOMAIN JOINED STATUS         : 1ce20aba-9851-4421-9430-1ddeb766e809 [DOMAIN JOINED]
        STOP SERVICE
          DOMAIN JOINED STATUS         : ddaf516e-58c2-4866-9574-c3b615d42ea1 [NOT DOMAIN JOINED]
```

O exemplo a seguir consulta a configuração de gatilho do serviço de entrada do tablet, que é configurado para iniciar quando um dispositivo HID com **o GUID** {4d1e55b2-f16f-11cf-88cb-0011111000030} e qualquer uma das IDs de dispositivo HID especificadas chega.

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

 

 
