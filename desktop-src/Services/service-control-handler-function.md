---
description: Cada serviço tem um manipulador de controle, a função de manipulador, que é invocado pelo Dispatcher de controle quando o processo de serviço recebe uma solicitação de controle de um programa de controle de serviço.
ms.assetid: 437334ed-05fa-4ab6-aab3-dc2739113e19
title: Função do manipulador do controle de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1303bff45421ee7206d02be9ee30066324648823
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754113"
---
# <a name="service-control-handler-function"></a>Função do manipulador do controle de serviço

Cada serviço tem um manipulador de controle, a função de [**manipulador**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) , que é invocado pelo Dispatcher de controle quando o processo de serviço recebe uma solicitação de controle de um programa de controle de serviço. Portanto, essa função é executada no contexto do Dispatcher de controle. Para obter um exemplo, consulte [escrevendo uma função de manipulador de controle](writing-a-control-handler-function.md).

Um serviço chama a função [**RegisterServiceCtrlHandler**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlera) ou [**RegisterServiceCtrlHandlerEx**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlerexa) para registrar sua função de manipulador de controle de serviço.

Quando o manipulador de controle de serviço é invocado, o serviço deve chamar a função [**falha em SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) para relatar seu status para o SCM somente se manipular o código de controle faz com que o status do serviço seja alterado. Se a manipulação do código de controle não fizer com que o status do serviço seja alterado, não será necessário chamar **falha em SetServiceStatus**.

Um programa de controle de serviço pode enviar solicitações de controle usando a função [**chamada ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) . Todos os serviços devem aceitar e processar o código de controle **\_ \_ Interrogate de controle de serviço** . Você pode habilitar ou desabilitar a aceitação dos outros códigos de controle chamando [**falha em SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus). Para receber o código de controle **\_ \_ DEVICEEVENT de controle de serviço** , você deve chamar a função [**RegisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa) . Os serviços também podem manipular códigos de controle adicionais definidos pelo usuário.

Se um serviço aceitar o código de controle de **\_ \_ parada de controle de serviço** , ele deverá parar após o recebimento, indo para o estado de interrupção de **serviço \_ \_ pendente** ou **serviço \_ parado** . Depois que o SCM enviar esse código de controle, ele não enviará outros códigos de controle.

**Windows XP:** Se o serviço **não retornar nenhum \_ erro** e continuar a ser executado, ele continuará a receber códigos de controle. Esse comportamento mudou a partir do Windows Server 2003 e do Windows XP com Service Pack 2 (SP2).

O manipulador de controle deve retornar dentro de 30 segundos ou o SCM retorna um erro. Se um serviço precisar fazer processamento longo quando o serviço estiver executando o manipulador de controle, ele deverá criar um thread secundário para executar o processamento longo e, em seguida, retornar do manipulador de controle. Isso impede que o serviço se vinculasse ao dispatcher de controle. Por exemplo, ao tratar a solicitação de parada de um serviço que leva muito tempo, crie outro thread para manipular o processo de parada. O manipulador de controle deve simplesmente chamar [**falha em SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) com a mensagem de interrupção de serviço e retorno **\_ \_ pendentes** .

Quando o usuário desliga o sistema, todos os manipuladores de controle que chamaram [**falha em SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) com o código de controle de **\_ \_ desligamento de aceitação do serviço** recebem o código de controle de **\_ \_ pré-desligamento do controle de serviço** . O Gerenciador de controle de serviço aguarda até que o serviço seja interrompido ou o valor de tempo limite de pré-desligamento especificado expire (esse valor pode ser definido com a função [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) ). Esse código de controle deve ser usado apenas em circunstâncias especiais, porque um serviço que manipula essa notificação bloqueia o desligamento do sistema até que o serviço seja interrompido ou o intervalo de tempo limite de pré-desligamento expire.

Após a conclusão das notificações de pré-desligamento, todos os manipuladores de controle que chamaram [**falha em SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) com o código de controle de desligamento de **\_ aceitação \_ do serviço** receberão o código de controle de **\_ \_ desligamento do controle de serviço** . Eles são notificados na ordem em que aparecem no banco de dados dos serviços instalados. Por padrão, um serviço tem aproximadamente 20 segundos para executar tarefas de limpeza antes de o sistema ser desligado. Depois que esse tempo expirar, o desligamento do sistema continuará independentemente de o desligamento do serviço ser concluído. Observe que, se o sistema for deixado no estado de desligamento (não reiniciado ou desligado), o serviço continuará a ser executado.

Se o serviço exigir mais tempo para a limpeza, ele enviará mensagens de status de **parada \_ pendentes** , juntamente com uma dica de espera, para que o controlador de serviço saiba por quanto tempo esperar antes de relatar ao sistema que o desligamento do serviço foi concluído. No entanto, para impedir que um serviço pare o desligamento, há um limite de quanto tempo o controlador de serviço espera. Se o serviço estiver sendo desligado por meio do snap-in serviços, o limite será de 125 segundos ou 125.000 milissegundos. Se o sistema operacional estiver sendo reinicializado, o limite de tempo será especificado no valor de **WaitToKillServiceTimeout** (em milissegundos) da seguinte chave do registro:

**HKEY \_ \_ computador local \\ sistema \\ CurrentControlSet \\ Control**

> [!IMPORTANT]
> Um serviço não deve tentar aumentar o limite de tempo modificando esse valor. Se você precisar definir **WaitToKillServiceTimeout** manualmente, o valor deverá ser em milissegundos.

Os clientes precisam de um desligamento rápido do sistema operacional. Por exemplo, se um computador que executa o no-break não puder concluir o desligamento antes de o UPS ficar sem energia, os dados poderão ser perdidos. Portanto, os serviços devem concluir suas tarefas de limpeza o mais rápido possível. É uma boa prática minimizar dados não salvos salvando dados regularmente, controlando os dados que são salvos em disco e salvando apenas os dados não salvos no desligamento. Como o computador está sendo desligado, não perca tempo liberando memória alocada ou outros recursos do sistema. Se você precisar notificar um servidor que está sendo encerrado, minimize o tempo gasto aguardando uma resposta, pois problemas de rede podem atrasar o desligamento do serviço.

Observe que durante o desligamento do serviço, por padrão, o SCM não leva em consideração as dependências. O SCM enumera a lista de serviços em execução e envia o comando de **\_ \_ desligamento do controle de serviço** . Portanto, um serviço pode falhar porque outro serviço do qual ele depende já parou.

Para definir a ordem de desligamento dos serviços manualmente, crie um valor de registro multistring que contenha os nomes de serviço na ordem em que eles devem ser desligados e atribua-os ao valor **PreshutdownOrder** da chave de controle, da seguinte maneira:

**HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Control \\ PreshutdownOrder = "desligar ordem"**

Para definir a ordem de desligamento dos serviços dependentes do seu aplicativo, use a função [**SetProcessShutdownParameters**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters) . O SCM usa essa função para dar seu manipulador 0x1E0 prioridade. O SCM envia notificações de **\_ \_ desligamento de controle de serviço** quando seu manipulador de controle é chamado e aguarda a saída dos serviços antes de retornar de seu manipulador de controle.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Escrevendo uma função de manipulador de controle](writing-a-control-handler-function.md)
</dt> </dl>

 

 
