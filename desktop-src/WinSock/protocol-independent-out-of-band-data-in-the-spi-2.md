---
description: Os dados fora de banda (OOB) são um canal de transmissão logicamente independente associado a um par de soquetes de fluxo conectados.
ms.assetid: 30f667cd-5be9-45f2-9d55-bff04834078f
title: Dados de out-of-Band independentes de protocolo no SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a55e186e34e401e56017097271d5f036f2666bdc51f8bc27c6692be7e12874e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993606"
---
# <a name="protocol-independentout-of-band-data-in-the-spi"></a>Dados de out-of-Band independentes de protocolo no SPI

Os dados fora de banda (OOB) são um canal de transmissão logicamente independente associado a um par de soquetes de fluxo conectados. Os dados OOB podem ser entregues ao usuário independentemente dos dados normais. A abstração define que os recursos de dados OOB devem dar suporte à entrega confiável de pelo menos um bloco de dados OOB de cada vez. Esse bloco de dados pode conter pelo menos um byte de dados, e pelo menos um bloco de dados OOB pode estar com entrega pendente para o usuário a qualquer momento. Para protocolos de comunicação que dão suporte à sinalização em banda (ou seja, TCP, em que os dados urgentes são entregues em sequência com os dados normais), o sistema normalmente extrai os dados OOB do fluxo de dados normal e os armazena separadamente (deixando uma lacuna no fluxo de dados normal). Isso permite que os usuários escolham entre receber os dados OOB em ordem e recebê-los fora de sequência sem precisar armazenar em buffer todos os dados intermediários. É possível inspecionar dados OOB.

Um usuário pode determinar se há algum dado OOB aguardando para ser lido usando a função [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) (SIOCATMARK). para protocolos em que o conceito da posição do bloco de dados OOB dentro do fluxo de dados normal é significativo (ou seja, TCP), um provedor de serviços de Windows sockets manterá um marcador conceitual que indica a posição do último byte de dados OOB dentro do fluxo de dados normal. Isso não é necessário para a implementação da funcionalidade **WSPIoctl** (SIOCATMARK) — a presença ou a ausência de dados OOB é tudo o que é necessário.

Para protocolos em que o conceito da posição do bloco de dados OOB dentro do fluxo de dados normal é significativo, um aplicativo pode preferir processar dados fora de banda embutidos, como parte do fluxo de dados normal. Isso é feito definindo a opção socket de modo que \_ OOBINLINE (consulte a seção [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85))). Para outros protocolos em que os blocos de dados OOB são verdadeiramente independentes do fluxo de dados normal, a tentativa de definir \_ OOBINLINE resultará em um erro. Um aplicativo pode usar o comando SIOCATMARK WSPIoctl para determinar se há algum dado OOB Não lido antes da marca. Por exemplo, ele pode usar isso para ressincronizar com seu par, garantindo que todos os dados até a marca no fluxo de dados sejam descartados quando apropriado.

Com o \_ OOBINLINE desabilitado (por padrão):

-   O provedor de serviços Winsock notifica um cliente sobre um evento de OOB do FD \_ , se o cliente estiver registrado para notificação com [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)), exatamente da mesma forma que a leitura de FD \_ é usada para notificar a presença de dados normais. Ou seja, FD \_ OOB é Postado quando dados OOB chegam e não havia dados OOB anteriormente enfileirados, e também quando os dados são lidos usando o sinalizador de OOB de MSG \_ e alguns dados OOB continuam sendo lidos depois que a operação de leitura é retornada. \_As mensagens de leitura do FD não são postadas para dados OOB.
-   O provedor de serviço Winsock retornará de [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)) com o conjunto de soquetes *exceptfds* apropriado se os dados OOB estiverem na fila no soquete.
-   O cliente pode chamar [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) com MSG \_ OOB para ler o bloco de dados urgentes a qualquer momento. O bloco de dados OOB salta a fila.
-   O cliente pode chamar [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) sem \_ o OOB de MSG para ler o fluxo de dados normal. O bloco de dados OOB Não será exibido no fluxo de dados com dados normais. Se os dados OOB permanecerem após qualquer chamada para **WSPRecv**, o provedor de serviços notificará o cliente com FD \_ OOB ou por meio de *exceptfds* ao usar o [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)).
-   Para protocolos em que os dados OOB têm uma posição dentro do fluxo de dados normal, uma única operação [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) não abrange essa posição. Um **WSPRecv** retornará os dados normais antes da marca e um segundo **WSPRecv** será necessário para começar a ler os dados após a marca.

Com o \_ OOBINLINE habilitado:

-   \_As mensagens OOB do FD não são postadas para dados OOB – para fins das funções [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)) e [**WSPASYNCSELECT**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) , os dados OOB são tratados como dados normais e indicados pela configuração do soquete no *readfds* ou pelo envio de uma mensagem de leitura FD, \_ respectivamente.
-   O cliente pode não chamar [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) com o sinalizador de mensagem \_ OOB definido para ler o bloco de dados OOB — o código de erro WSAEINVAL será retornado.
-   O cliente pode chamar [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) sem o conjunto de sinalizadores de OOB de MSG \_ . Todos os dados OOB serão entregues em sua ordem correta dentro do fluxo de dados normal. Os dados OOB nunca serão misturados com dados normais – deve haver três solicitações de leitura para passar os dados OOB. O primeiro retorna os dados normais antes do bloco de dados OOB, o segundo retorna os dados OOB, o terceiro retorna os dados normais que seguem os dados OOB. Em outras palavras, os limites de bloco de dados OOB são preservados.

A rotina [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) é particularmente adequada para lidar com a notificação da presença de dados OOB quando \_ OOBINLINE é desativado.

 

 
