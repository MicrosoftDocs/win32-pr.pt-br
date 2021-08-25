---
description: Os senders PGM são fornecidos com determinadas configurações padrão que afetam o desempenho da transmissão de dados e por quanto tempo os dados são armazenados em buffer para levar em conta a perda de pacotes e solicitações de retransmissão de cliente PGM associadas.
ms.assetid: 56b15eac-ea0d-4d18-b5f6-2f1a7b1bb25f
title: Opções do remetente PGM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04bce19e096f269207a22f8e3078643fefd9a7ced31482305c2caeb0ae8b7749
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857897"
---
# <a name="pgm-sender-options"></a>Opções do remetente PGM

Os senders PGM são fornecidos com determinadas configurações padrão que afetam o desempenho da transmissão de dados e por quanto tempo os dados são armazenados em buffer para levar em conta a perda de pacotes e solicitações de retransmissão de cliente PGM associadas. Os parágrafos a seguir descrevem essas configurações padrão.

## <a name="window-size-and-transmission-rate"></a>Tamanho da janela e taxa de transmissão

A capacidade de definir o tamanho da janela e a taxa de transmissão permite que os aplicativos controlem a quantidade de dados que os buffers de transporte para retransmissão e a taxa na qual o fluxo de byte é transmitido.

Os dados de retransmissão são armazenados em um arquivo, portanto, o tamanho máximo da janela é limitado pelo espaço em disco que pode ser usável pelo transporte. O tamanho da janela padrão é 10 MB. Embora seja possível que um tamanho de envio ou mensagem exceda a janela ou o tamanho do buffer, o fluxo de dados permanece ininterrupto; o envio é canetado até que todos os dados foram enviados.

> [!Note]  
> O espaço máximo do buffer é limitado pelo número máximo de pacotes que podem ser mantidos na janela a qualquer momento, que é igual a 2^31 – 1.

 

A taxa de transmissão é o fluxo de saída combinado de pacotes de dados originais (ODATA), RDATA (pacotes de dados retransmitidos) e SPMs (pacotes de contabilidade específicos do transporte), expressos por segundo. Se o limite de taxa for definido como 56 quilobits por segundo por padrão. O tamanho da janela padrão é de 10 megabytes, com uma taxa padrão de 56 quilobits por segundo. Devido à relação entre os três membros da estrutura [**RM \_ SEND \_ WINDOW,**](/windows/desktop/api/Wsrm/ns-wsrm-rm_send_window) o tamanho da janela padrão é, portanto, 1428 segundos. Consulte **RM SEND WINDOW \_ \_ para** obter mais informações.

## <a name="window-advance-rate"></a>Taxa de avanço da janela

A taxa de avanço da janela é definida pela opção de [ \_ soquete RM SENDER \_ WINDOW \_ ADV \_ RATE.](socket-options.md) Essa opção permite que os aplicativos especifiquem o incremento no qual a janela do remetente PGM é avançada, expressa como um valor percentual não zero do tamanho da janela. O valor padrão é 15% e a taxa máxima é de 50%. Se o remetente PGM tiver dados de reparo pendentes que se enquadram no espaço da janela de incremento, a janela será avançada parcialmente à medida que cada pacote de reparo na janela for enviado.

## <a name="forward-error-correction-fec"></a>Correção de erro de encaminhamento (FEC)

A correção de erro de encaminhamento é definida por meio do uso da \_ opção de soquete RM USE \_ FEC. Essa opção de soquete permite que o remetente PGM envie pacotes de reparo como pacotes de paridade em vez de pacotes de dados regulares. Isso minimiza o número de pacotes de reparo enviados para reparar sequências diferentes perdidas por vários receptores de dentro do mesmo grupo de dados. A habilitação do FEC só é definida no remetente PGM. Os receptores PGM seguem automaticamente a política definida pelo remetente. Para uma discussão detalhada sobre o FEC, consulte o PGM RFC localizado no site [do IETF.](https://www.ietf.org/)

 

 



