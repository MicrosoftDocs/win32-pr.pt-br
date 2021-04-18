---
description: Com a função lineSetTerminal, o aplicativo pode controlar ou suprimir o roteamento de eventos de baixo nível especificados (trocados entre a opção e a estação) em um dispositivo.
ms.assetid: 36658d83-0ea4-4f62-b2e5-c0f6d6569d0d
title: Roteamento de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df6749969faf89ac0212c19049fe02c9dad57a96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761362"
---
# <a name="event-routing"></a>Roteamento de eventos

Com a função [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) , o aplicativo pode controlar ou suprimir o roteamento de eventos de baixo nível especificados (trocados entre a opção e a estação) em um dispositivo. Com o **lineSetTerminal**, o aplicativo especifica o dispositivo de terminal para o qual esses eventos (como linha, endereço ou chamada de eventos de fluxo de mídia) são roteados.

O roteamento das diferentes classes de eventos pode ser controlado individualmente, permitindo que terminais separados sejam especificados para cada classe de evento. As classes de evento incluem lâmpadas, botões, display, anéis, Hookswitch e fluxo de mídia.

Por exemplo, o fluxo de mídia de uma chamada (voz, por exemplo) pode ser enviado para qualquer dispositivo transdutor se o provedor de serviços e o hardware forem capazes de fazer isso. Em geral, um *transdutor* significa o mesmo que o que é conhecido como um dispositivo *Hookswitch* na TAPI, algo que tem um microfone e um palestrante. Eventos de anel da mudança para o telefone podem ser mapeados para um alerta visual na tela do computador ou podem ser roteados para um dispositivo de telefone. Eventos de lâmpada e eventos de exibição podem ser ignorados ou roteados para um dispositivo de telefone (que parece se comportar como um conjunto de telefone normal). Por fim, os pressionamentos de botão em um dispositivo de telefone podem ou não ser passados para a linha. De qualquer forma, esse roteamento de sinais de baixo nível da linha não afeta a operação da parte da linha da TAPI, que sempre mapeia eventos de nível baixo para seus equivalentes funcionais. Para determinar os terminais que um dispositivo de linha tem disponível (e seus recursos), consulte os recursos do dispositivo de linha com [**lineGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps).

Suponha inicialmente que o aplicativo tenha suprimido o roteamento de todos os eventos (com [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal)) e o usuário selecione um headset como o dispositivo de e/s atual. Uma chamada de entrada envia uma mensagem [**\_ callstate de linha**](line-callstate.md) e uma mensagem de [**\_ LINEDEVSTATE de linha**](line-linedevstate.md) com a indicação de *toque* . Como o roteamento de todos os eventos é suprimido, os eventos de anel não são roteados para o telefone, portanto, o toque é suprimido. Em vez disso, o aplicativo notifica o usuário com uma caixa de diálogo pop-up e um aviso do sistema no headset.

O usuário decide responder à chamada. Como o dispositivo de e/s atual do usuário é o headset, o aplicativo de telefonia invoca [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) na chamada de entrada para rotear a mídia da chamada para o headset e responder à chamada. O aplicativo também pode invocar **lineSetTerminal** para rotear a lâmpada e exibir eventos de informações para o conjunto de telefone para que ele se comporte como de costume.

Como um segundo exemplo, suponha que uma chamada de entrada esteja alertando no computador do usuário. Em vez de selecionar a opção de resposta com o mouse, o usuário decide simplesmente pegar o monofone do telefone para responder à chamada. O status offhook no telefone envia uma mensagem para o aplicativo. O aplicativo pode interpretar esse status como uma solicitação pelo usuário para selecionar o aparelho de telefone para realizar a conversa. Em seguida, o aplicativo invoca [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) para rotear os dados de voz na chamada para o conjunto de telefone.

 

 



