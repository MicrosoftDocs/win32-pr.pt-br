---
description: Quando um aplicativo tem privilégio de proprietário para uma sessão de comunicações, o aplicativo pode optar por entregar a propriedade a outro aplicativo.
ms.assetid: d6d188c9-9cbd-45af-93f0-b78850374919
title: Entregas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 343815e35f1fc331c57c4aa2d9d311697cab7022
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759476"
---
# <a name="handoffs"></a>Entregas

Quando um aplicativo tem [privilégio](privilege-ovr.md) de proprietário para uma sessão de comunicações, o aplicativo pode optar por entregar a propriedade a outro aplicativo. A operação de entrega normalmente é usada para permitir que o tipo de mídia da chamada seja alterado. O aplicativo de prioridade mais alta para o novo tipo de mídia deve tomar e tratar a chamada. A alteração do tipo de mídia geralmente ocorre por um dos motivos a seguir.

**Comando do usuário:** Por meio de uma interface do usuário ou de mensagens de janela, o aplicativo aprende que o usuário local deseja alterar o tipo de mídia. Por exemplo, o usuário informou ao novo aplicativo de destino (que ainda não é um proprietário) para obter uma chamada de voz existente para transmitir dados. O aplicativo de destino agora deve assumir o controle da chamada. Nesse caso, o proprietário atual observa o número de proprietários aumenta e, em seguida, abandona seu controle da chamada. Como alternativa, o usuário poderia instruir o proprietário atual da chamada para entregá-la a um aplicativo que possa manipular o novo tipo de mídia.

**Alteração do tipo de mídia:** O provedor de serviços pode detectar uma alteração de tipo de mídia. Por exemplo, o aplicativo local está reproduzindo uma mensagem de voz gravada para o chamador. Durante essa mensagem, o chamador decide espontaneamente a transmissão de um tom de chamada de fax, e o aplicativo local pode responder de acordo alterando o tipo de mídia para fax e, se necessário, entregando a chamada para um aplicativo de fax. Outra maneira de trabalhar com um aplicativo de monitoramento para habilitar o monitoramento do tipo de mídia e, quando o tipo de mídia no qual ele está interessado é detectado em uma chamada, ele pode solicitar a propriedade da chamada. Esse mecanismo torna desnecessário para cada aplicativo monitorar cada chamada para cada tipo de mídia.

**Comando da parte remota:** A parte remota pode indicar interativamente uma alteração nos tipos de mídia durante uma chamada existente, como se o aplicativo local estiver monitorando a entrada DTMF pelo chamador remoto. Por meio desse monitoramento, o chamador indica, por exemplo, que um fax está prestes a ser enviado. Outras maneiras pelas quais o chamador pode controlar aplicativos locais são com comandos recebidos em outras conexões de dados e por meio de mensagens de informações de usuário do usuário ISDN.

Uma entrega de chamada terá um destes resultados:

-   A chamada é dada a outro aplicativo (êxito).
-   O aplicativo de entrega é o próprio destino (TARGETSELF).
-   A entrega falha (TARGETNOTFOUND).

Se o aplicativo que está recebendo a chamada de retirada já tiver um identificador de chamada para a chamada, esse identificador de chamada antigo será usado. Caso contrário, um novo identificador de chamada será criado. Em ambos os casos, o aplicativo termina com os privilégios de proprietário para a chamada. Sempre que o aplicativo de entrega não for o mesmo que o aplicativo de destino, o destino será informado sobre a entrega em uma mensagem de estado de sessão como se estivesse recebendo uma nova chamada.

Se o aplicativo proprietário atual for instruído a alterar os tipos de mídia, ele fará isso entregando a chamada para um aplicativo usado para o tipo de mídia de destino. Os dois tipos de entregas de chamada são descritos em [entregas direcionadas](#directed-handoffs) e [entregas de tipo de mídia](#media-type-handoffs).

Nem todos os provedores de serviço dão suporte ao uso desta operação.

**TAPI 2. x:** Consulte [**lineHandoff**](/windows/win32/api/tapi/nf-tapi-linehandoff), com *lpszFileName* definido como o nome do aplicativo para uma entrega direta ou *dwMediaMode* definido como um tipo de mídia para uma entrega indireta.

**TAPI 3. x:** Consulte [**ITBasicCallControl:: HandoffDirect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-handoffdirect), [**ITBasicCallControl:: HandoffIndirect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-handoffindirect).

## <a name="directed-handoffs"></a>Entregas direcionadas

Uma *entrega direcionada* ocorre quando o aplicativo de destino é conhecido pelo nome para o aplicativo original. Essa situação ocorreria, por exemplo, entre um conjunto de aplicativos gravados pelo mesmo fornecedor. O usuário geralmente pode configurar o controle de entregas direcionadas. Com tal entrega, a chamada será dada ao aplicativo especificado se ele tiver aberto a linha na qual a chamada existe. O tipo de mídia especificado no momento em que o aplicativo abriu a linha é ignorado. Um exemplo comum é uma chamada de voz seguida por uma transmissão de fax na mesma chamada. A entrega direcionada geralmente seria usada por aplicativos do mesmo desenvolvedor que estão vinculados de outras maneiras também.

A entrega direcionada também pode ser usada em versões futuras como parte do processo de arbitrar vários aplicativos aguardando chamadas de entrada do mesmo tipo de mídia, com a seleção do aplicativo para tratar a chamada com base na detecção de protocolo de dados ou de nível superior em vez de tipo de mídia. Um exemplo de uso seria uma linha de modem de dados de entrada com aplicativos como tomada remotos, BBS, acesso remoto à rede e acesso remoto a email, todos esperando por chamadas simultaneamente.

## <a name="media-type-handoffs"></a>Entregas de tipo de mídia

Um *tipo de mídia entrega* ocorre quando há um novo tipo de mídia direcionado, geralmente quando o aplicativo proprietário determina que o tipo de mídia necessário para a chamada não está presente ou está prestes a ser alterado.

O processo para uma entrega dependente de mídia pode ser um processo de investigação se o bit de tipo de mídia desconhecido estiver ativado. É responsabilidade do aplicativo proprietário percorrer os tipos de mídia para encontrar o aplicativo de prioridade mais alta. A TAPI faz esse ciclo apenas na chamada de entrada inicial para encontrar o primeiro proprietário. Ele não faz isso para uma operação de entrega. Caso contrário, uma entrega é praticamente a mesma para a atribuição inicial de uma chamada para um aplicativo. A diferença é o fato de que apenas um tipo de mídia pode ser definido para uma entrega indireta (tipo de mídia).

Como apenas um único bit de tipo de mídia pode ser especificado, a chamada é dada ao aplicativo de prioridade mais alta para esse tipo de mídia. No entanto, é possível que mais de um tipo de mídia seja considerado para a entrega. Nesse caso, o aplicativo de entrega deve especificar a prioridade mais alta dos tipos de mídia possíveis como um parâmetro.

Se um aplicativo especificar o bit desconhecido ao executar uma entrega de tipo de mídia e a entrega falhar, isso significa que um aplicativo desconhecido capaz de executar a determinação do tipo de mídia não está em execução no momento. O aplicativo que está sendo entregue deve, então, tentar entregar a chamada para o aplicativo de prioridade mais alta registrado para o próximo tipo de mídia mais alto.

O aplicativo receptor agora é responsável pela chamada. Agora, ele investiga o tipo de mídia real da chamada. Se o aplicativo puder lidar com o tipo de mídia da chamada, ele deverá garantir que seja o aplicativo de prioridade mais alta registrado para esse tipo de mídia. Nesse caso, ele mantém a chamada e os processa normalmente. Caso contrário, ele entrega a chamada para outro aplicativo registrado para esse tipo de mídia.

No entanto, se a investigação desse tipo de mídia falhar, o aplicativo investigará novamente, tentando as possibilidades de modo de mídia restante. Primeiro, ele deve desligar o bit do tipo de mídia atual e, em seguida, tentar outra entrega com um tipo diferente.

Esse processo de investigação e de entrega continua e os tipos de mídia restantes são eliminados um a um. Ao longo do caminho, um dos aplicativos pode ver que o tipo de mídia que ele manipula está na chamada e a entrega é bem-sucedida.

O aplicativo deve então definir o tipo de mídia correto e limpar todos os outros bits do tipo de mídia. Isso informa outros aplicativos interessados do tipo de mídia correto. Esses outros aplicativos recebem uma mensagem de notificação de eventos informando que o tipo de mídia da chamada foi alterado.

 

 
