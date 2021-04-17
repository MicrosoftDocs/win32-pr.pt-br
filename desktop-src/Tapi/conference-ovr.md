---
description: A conferência avançada usando redes baseadas em IP é descrita na conferência de telefonia IP da 3S de reunião da TAPI. O material a seguir está relacionado à conferência básica.
ms.assetid: f685097b-1b54-412b-999f-d9bdb3120ab9
title: Conferência
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ace4cb45bf74335298a3d4d262d064eb85c547f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768579"
---
# <a name="conference"></a>Conferência

A conferência avançada usando redes baseadas em IP é descrita na conferência de [telefonia IP da reunião](rendezvous-ip-telephony-conferencing.md)do TAPI 3. O material a seguir está relacionado à conferência básica.

As sessões de conferência são sessões que incluem mais de duas partes simultaneamente. Eles podem ser configurados usando uma ponte baseada no servidor externo ou uma ponte de conferência baseada em comutador.

Em sessões de conferência baseadas em servidor, todas as partes participantes se conectam ao servidor, que combina os fluxos de mídia juntos e envia a cada participante a combinação. Pode não haver nenhuma noção de partes individuais na chamada à conferência, somente a partir de uma única chamada entre o aplicativo e o servidor de ponte. Para a TAPI, esse tipo de chamada de conferência parece ser uma conexão um-para-um normal.

A conferência baseada em switches continua em estágios, algumas das quais podem ser combinadas se o provedor de serviços oferecer suporte a ela:

1.  Inicie uma sessão de comunicações comum.
2.  Crie uma sessão de conferência com seu primeiro membro da parte que iniciou a conferência.
3.  Crie uma sessão de consultoria de conferência com a parte na outra extremidade da conexão atual.
4.  Adicione a sessão de consulta à conferência.

Depois que uma sessão se torna membro de uma conferência, o estado do membro é revertido para a conferência. O estado da sessão de conferência normalmente se torna *conectado*. Os identificadores de sessão para a conferência e todas as partes adicionadas permanecem válidas. Eventos de estado podem ser recebidos sobre todas as chamadas. Por exemplo, se um dos membros se desconectar ao desligar, uma mensagem de estado apropriada poderá informar o aplicativo desse fato.

**TAPI 2. x:** Os aplicativos podem usar o recurso "sem reter a conferência" dos PBXs usando a \_ opção LINECALLPARAMFLAGS NOHOLDCONFERENCE; esse recurso permite que outro dispositivo, como um supervisor ou um dispositivo de gravação, seja conectado silenciosamente à linha.

Ao cancelar a sessão de consulta para a terceira parte de uma conferência ou ao remover a terceira parte de uma conferência estabelecida anteriormente, o provedor de serviços pode liberar a conferência e reverter a sessão para uma conexão normal de duas partes. Se esse for o caso, a sessão de conferência fará a transição para o estado *ocioso* e a única sessão participante restante passará da conferência para o estado *conectado* .

Nem todos os provedores de serviço dão suporte à conferência.

**TAPI 2. x:** A função [**lineSetupConference**](/windows/win32/api/tapi/nf-tapi-linesetupconference) usa a chamada original de duas partes como entrada, aloca uma chamada de conferência, conecta a chamada original à conferência e aloca uma chamada de consulta cujo identificador é retornado para o aplicativo.

Se o aplicativo for adicionar outro membro à conferência, uma operação de discagem poderá ser executada na chamada de consulta. O identificador de chamada de conferência e a conexão de chamada de consulta são usados na função [**lineAddToConference**](/windows/win32/api/tapi/nf-tapi-lineaddtoconference) . Os membros da conferência também podem ser adicionados usando a função [**linePrepareAddToConference**](/windows/win32/api/tapi/nf-tapi-lineprepareaddtoconference) , se houver suporte do provedor de serviços.

Os membros da conferência são removidos usando a função [**lineRemoveFromConference**](/windows/win32/api/tapi/nf-tapi-lineremovefromconference) , se o provedor de serviços oferecer suporte a ele.

Como alternativa, uma conferência pode ser criada usando a função [**lineSetupTransfer**](/windows/win32/api/tapi/nf-tapi-linesetuptransfer) , que retorna um identificador de chamada de consulta e a função [**lineCompleteTransfer**](/windows/win32/api/tapi/nf-tapi-linecompletetransfer) com a opção de conferência (em vez da opção de [transferência](transfer-ovr.md) ).

**TAPI 3. x:** O método [**ITBasicCallControl:: Conference**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-conference) usa a sessão existente como entrada e cria um [objeto CallHub](callhub-object.md) , caso ainda não exista uma. O método [**ITBasicCallControl:: Finish**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-finish) adiciona a chamada de consulta ao CallHub. Outras sessões de consulta podem ser criadas usando [**ITAddress:: createcall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall)e adicionadas usando os métodos **Conference** e **Finish** .

> [!Note]  
> Os recursos do dispositivo de linha endereçada podem limitar o número de partes em conferência em uma única chamada e se uma conferência começa ou não com uma chamada de dois participantes normal.

 

 

 
