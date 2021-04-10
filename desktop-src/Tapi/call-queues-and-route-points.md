---
description: Uma fila de chamadas ou um ponto de rota é um endereço especial dentro do comutador onde as chamadas são mantidas temporariamente pendentes.
ms.assetid: 1c801401-be05-4b5f-bc4f-628dde0f3cf7
title: Filas de chamadas e pontos de rota
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66895101b72ca8e16810d3766edf897efcfedddd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169360"
---
# <a name="call-queues-and-route-points"></a>Filas de chamadas e pontos de rota

Uma fila de chamadas ou um ponto de rota é um endereço especial dentro do comutador onde as chamadas são mantidas temporariamente pendentes. Essa característica é representada pela fila bits LINEADDRCAPFLAGS \_ e LINEADDRCAPFLAGS \_ ROUTEPOINT no membro **dwAddrCapFlags** no [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps). Todas as chamadas que aparecem nesse endereço estão aguardando ação pelo aplicativo, e pode haver ações padrão que ocorrem (por exemplo, transferência para um agente ou tronco) se o aplicativo não executar nenhuma ação dentro de um período de tempo definido. O aplicativo deve ser configurado pelo administrador do sistema para que ele saiba quais ações ele deve executar em relação a chamadas que aparecem em cada fila ou endereço de ponto de rota e a quantidade de tempo disponível para decidir sobre a ação a ser tomada.

Os aplicativos podem determinar o número de chamadas pendentes em uma fila ou ponto de rota usando [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus). A função [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) pode ser usada para obter informações como ID de chamada, ID chamada, origem de entrada ou saída e assim por diante e usada pelo aplicativo para tomar decisões sobre o tratamento de chamadas; as chamadas podem ser redirecionadas, transferidas, descartadas, removidas e assim por diante, ou apenas permitidas para a passagem automática da fila para um destino. Uma chamada vai para LINECALLSTATE \_ desconectada se for abandonada. As chamadas ficam *ociosas* quando saem da fila; **lineGetCallInfo** pode ser usado para ler o identificador de redirecionamento para determinar onde eles foram transferidos.

Algumas opções permitem chamadas em uma fila ou em espera para receber um tratamento específico, como silêncio, toque de chamada, sinal ocupado, música ou escuta de um comunicado gravado. A função [**lineSetCallTreatment**](/windows/desktop/api/Tapi/nf-tapi-linesetcalltreatment) permite que o aplicativo controle o tratamento. A estrutura delimitada pelos membros **dwCallTreatmentListSize** e **dwCallTreatmentListOffset** no [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) permite que os aplicativos determinem os tratamentos com suporte. O membro **dwCallTreatment** em [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) indica o tratamento atual e uma mensagem [**\_ CALLINFO de linha**](line-callinfo.md) com tratamento LINECALLINFOSTATE \_ indica quando isso é alterado. O \_ bit SETTRATAMENTO LINECALLFEATURE no membro **DwCallFeatures** no [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) indica quando o aplicativo tem permissão para alterar o tratamento. O \_ conjunto de constantes LINECALLTREATMENT define um conjunto limitado de tratamentos de chamada predefinidos; provedores de serviço podem definir muitos outros.

 

 



