---
description: Muitos aplicativos dependem da relação de tempo entre os eventos de mídia (por exemplo, dígitos DTMF recebidos) para determinar a natureza de uma operação solicitada.
ms.assetid: 8d25a31f-de40-4c74-b8e7-a81fbfd47db2
title: Temporizadores de eventos de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a584518c9c33e8991bd2388f01cb863bab1c7a3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105813054"
---
# <a name="media-event-timers"></a>Temporizadores de eventos de mídia

Muitos aplicativos dependem da relação de tempo entre os eventos de mídia (por exemplo, dígitos DTMF recebidos) para determinar a natureza de uma operação solicitada. Por exemplo, em um aplicativo de correio de voz, dois dígitos de "1" de DTMF consecutivos podem significar "fazer backup de dois segmentos" ou "repetir desde o início da mensagem", dependendo de quanto tempo decorrido entre os dois dígitos. Em um ambiente de cliente/servidor, se a detecção de DTMF estiver sendo executada em um processador separado daquele em que o aplicativo está sendo executado, a latência na rede local tornará muito provável que a relação de tempo entre os eventos de mídia seja distorcida, com o resultado de que essas diferenças com base no tempo poderiam ser perdidas ou se tornarem não confiáveis.

Para resolver esse problema, várias mensagens TAPI podem ser marcadas com carimbo de data/hora. Como é o tempo relativo entre esses eventos que é importante, a "hora do relógio" do evento não é importante e o tempo de subsegundo está envolvido, esses carimbos de data/hora usam a resolução de milissegundos "tempo desde o início do Windows" retornados pela função [**ObterContagemMarcaEscala**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-gettickcount) . Os aplicativos devem estar cientes de que essa é a contagem em escala no servidor (ou computador onde o provedor de serviços Gerenciando diretamente o hardware está em execução) e não é necessariamente o mesmo computador no qual o aplicativo está sendo executado; assim, os carimbos de data/hora dessas mensagens TAPI só podem ser comparados entre si e não ao valor retornado por **ObterContagemMarcaEscala** no processador no qual o aplicativo está sendo executado.

As mensagens TAPI que podem ser marcadas com carimbo de data/hora são: [**linha \_ GATHERDIGITS**](line-gatherdigits.md), [**\_ geração de linha**](line-generate.md), [**linha \_ MONITORDIGITS**](line-monitordigits.md), [**linha \_ MONITORMEDIA**](line-monitormedia.md)e [**linha \_ MONITORTONE**](line-monitortone.md). A contagem em escala é inserida em *dwParam3* dessas mensagens. Se o carimbo de data/hora não for suportado pelo provedor de serviços (que é indicado pela configuração do provedor de serviços *dwParam3* nessas mensagens como 0), a TAPI em si irá inserir a contagem de tiques em *dwParam3* de todas essas mensagens (ela pode ser distorcido um pouco, mas menor que se o aplicativo tiver feito o mesmo depois que as mensagens tiverem atravessado um esquema de comunicação entre

 

 
