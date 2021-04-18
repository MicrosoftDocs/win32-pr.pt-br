---
description: O computador dos usuários pode ter acesso a vários dispositivos que são selecionáveis pelo usuário e usados para conduzir conversas de voz interativas.
ms.assetid: cc7ad70a-157e-4db4-b5e4-00d25686a9dd
title: Configurando um terminal para conversas por telefone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75b12e772d8f941cb7c68e25136a843ec5f9a1f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810454"
---
# <a name="setting-a-terminal-for-phone-conversations"></a>Configurando um terminal para conversas por telefone

O computador do usuário pode ter acesso a vários dispositivos que são selecionáveis pelo usuário e usados para conduzir conversas de voz interativas. Primeiro, há o próprio dispositivo de telefone, completo com lâmpadas, botões, vídeo, anel e dispositivo de e/s de voz (monofone, viva-voz, headset). O computador do usuário também pode ter um dispositivo de e/s de voz separado (como um headset ou uma combinação de microfone/palestrante anexada a uma placa de som) para uso com conversas telefônicas.

O TSPI permite que o usuário selecione onde rotear as informações que o comutador envia sobre a linha, o endereço ou a chamada. A opção normalmente espera que esse seja um de seus conjuntos de telefone e envia solicitações de anel, eventos de lâmpada (para telefones de estímulo), dados de exibição e dados de voz, conforme apropriado. O telefone, por sua vez, envia eventos Hookswitch, eventos de pressionamento de botão (para telefones de estímulo) e dados de voz de volta para o comutador.

A parte de *linha* de TSPI faz eventos de lâmpada, eventos de exibição e eventos de anel disponíveis, como códigos de retorno funcionais para as várias operações de linha em TSPI ou como mensagens de status de chamada funcional não solicitadas que são enviadas para o retorno de chamada do aplicativo. A implementação do provedor de serviços é responsável pelo mapeamento entre o nível de TSPI funcional e as mensagens de estímulo ou funcionais subjacentes usadas pela rede de telefonia. Em ambientes de telefonia funcional, as funções TSPI são mapeadas para o protocolo funcional.

Usando a função [**TSPI \_ lineSetTerminal**](/windows/win32/api/tspi/nf-tspi-tspi_linesetterminal) , a TAPI pode controlar o roteamento de diferentes eventos de nível inferior trocados entre a opção e a estação; ele também pode optar por não rotear alguns desses eventos de baixo nível para um dispositivo. O roteamento das diferentes classes de eventos pode ser controlado individualmente. Por exemplo, o fluxo de mídia de uma chamada (como voz) pode ser enviado para qualquer dispositivo transdutor se o provedor de serviços e o hardware forem capazes de fazer isso. Eventos de anel da mudança para o telefone podem ser mapeados para um alerta visual na tela do computador ou podem ser roteados para um dispositivo de telefone. Eventos de lâmpada e eventos de exibição podem ser ignorados ou roteados para um dispositivo de telefone (que parece se comportar como um conjunto de telefone normal). Por fim, os pressionamentos de botão em um dispositivo de telefone podem ou não ser passados para a linha. Em qualquer caso, esse roteamento de sinais de baixo nível da linha não afeta a operação da parte da linha do TSPI, que sempre mapeia os eventos de nível baixo para seu equivalente funcional. Os aplicativos podem consultar os recursos do dispositivo de uma linha para determinar os terminais que ele tem disponíveis.

Em outras palavras, a função [**TSPI \_ lineSetTerminal**](/windows/win32/api/tspi/nf-tspi-tspi_linesetterminal) especifica o dispositivo de terminal para o qual a linha especificada, os eventos de endereço ou os eventos de fluxo de mídia de chamada são roteados. Os terminais separados podem ser especificados para cada classe de evento. As classes de evento incluem lâmpadas, botões, display, anéis, Hookswitch e fluxo de mídia.

 

 
