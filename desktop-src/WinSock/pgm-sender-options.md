---
description: Os remetentes de PGM são fornecidos com determinadas configurações padrão que afetam o desempenho da transmissão de dados e por quanto tempo os dados são armazenados em buffer para considerar a perda de pacotes e as solicitações de retransmissão de cliente PGM associadas.
ms.assetid: 56b15eac-ea0d-4d18-b5f6-2f1a7b1bb25f
title: Opções do remetente PGM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1c2e83ec7b098b9a82f74d4a3e0b6aa3ab03b63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764128"
---
# <a name="pgm-sender-options"></a>Opções do remetente PGM

Os remetentes de PGM são fornecidos com determinadas configurações padrão que afetam o desempenho da transmissão de dados e por quanto tempo os dados são armazenados em buffer para considerar a perda de pacotes e as solicitações de retransmissão de cliente PGM associadas. Os parágrafos a seguir descrevem essas configurações padrão.

## <a name="window-size-and-transmission-rate"></a>Tamanho da janela e taxa de transmissão

A capacidade de definir o tamanho da janela e a taxa de transmissão permite que os aplicativos controlem a quantidade de dados que os buffers de transporte para retransmissão e a taxa em que o byte-Stream é transmitido.

A retransmissão de dados é armazenada em um arquivo, portanto, o tamanho máximo da janela é limitado pelo espaço em disco utilizável pelo transporte. O tamanho padrão da janela é 10 MB. Embora seja possível que um tamanho de envio ou de mensagem exceda o tamanho da janela ou do buffer, o fluxo de dados permanece sem interrupção; o envio fica pendente até que todos os dados tenham sido enviados.

> [!Note]  
> O espaço máximo do buffer é limitado pelo número máximo de pacotes que podem ser mantidos na janela em um determinado momento, o que é igual a 2 ^ 31 – 1.

 

A taxa de transmissão é a saída combinada dos pacotes de dados originais (ODATA), os pacotes de dados retransmitidos (RDATA) e os SPMs (pacotes de escrituração específicos de transporte), expressos por segundo. Se o limite de taxa for definido como 56 kilobits por segundo por padrão. O tamanho da janela padrão é 10 megabytes, com uma taxa padrão de 56 kilobits por segundo. Devido à relação entre os três membros da estrutura de [**\_ \_ janela de envio do RM**](/windows/desktop/api/Wsrm/ns-wsrm-rm_send_window) , o tamanho da janela padrão é, portanto, 1428 segundos. Consulte **\_ \_ janela de envio do RM** para obter mais informações.

## <a name="window-advance-rate"></a>Taxa de adiantamento da janela

A taxa de adiantamento da janela é definida pela opção de soquete de [taxa de avçd da janela do remetente do RM \_ \_ \_ \_ ](socket-options.md) . Essa opção permite que os aplicativos especifiquem o incremento no qual a janela do remetente PGM é avançada, expressa como um valor percentual diferente de zero do tamanho da janela. O valor padrão é 15%, e a taxa máxima é de 50%. Se o remetente PGM tiver dados de reparo pendentes que se enquadram no espaço da janela de incremento, a janela será avançada parcialmente, pois cada pacote de reparo na janela será enviado.

## <a name="forward-error-correction-fec"></a>FEC (correção de erros de encaminhamento)

A correção de erro de encaminhamento é definida por meio do uso da \_ opção RM use o \_ soquete FEC. Essa opção de soquete permite que o remetente do PGM envie pacotes de reparo como pacotes de paridade em vez de pacotes de dados regulares. Isso minimiza o número de pacotes de reparo enviados para reparar sequências diferentes perdidas por vários receptores de dentro do mesmo grupo de dados. Habilitar o FEC só é definido no remetente do PGM. Os receptores de PGM seguem automaticamente a política definida pelo remetente. Para obter uma discussão detalhada sobre o FEC, consulte a RFC do PGM localizada no site da [IETF](https://www.ietf.org/) .

 

 



