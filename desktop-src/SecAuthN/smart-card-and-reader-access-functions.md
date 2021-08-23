---
description: Conexão e se comunicar com um cartão inteligente específico.
ms.assetid: 37d92491-174b-471e-b36e-46d9285dd404
title: Funções de acesso de cartão inteligente e leitor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b571764ae2d31865082e823996e8cc1ecde9d9d3e2dd618f28e528fd465a567
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118917951"
---
# <a name="smart-card-and-reader-access-functions"></a>Funções de acesso de cartão inteligente e leitor

As funções a seguir se conectam e se comunicam com um [*cartão inteligente*](../secgloss/s-gly.md)específico. As operações de e/s para o cartão usam um buffer para enviar ou receber dados e uma estrutura que contém informações de controle de protocolo. A estrutura de informações de controle de protocolo sempre começa com uma estrutura de [**\_ \_ solicitação de e/s scartar**](scard-io-request.md) .



| Tópico                                                  | Descrição                                                                                                                                                                                                                                |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SCardConnect**](/windows/desktop/api/Winscard/nf-winscard-scardconnecta)                   | Conexão a um cartão.                                                                                                                                                                                                                         |
| [**SCardReconnect**](/windows/desktop/api/Winscard/nf-winscard-scardreconnect)               | Restabelecer uma conexão.                                                                                                                                                                                                                  |
| [**SCardDisconnect**](/windows/desktop/api/Winscard/nf-winscard-scarddisconnect)             | Encerrar uma conexão.                                                                                                                                                                                                                    |
| [**SCardBeginTransaction**](/windows/desktop/api/Winscard/nf-winscard-scardbegintransaction) | Inicie uma [*transação*](../secgloss/t-gly.md), impedindo que outros aplicativos acessem um cartão.                                                                                            |
| [**SCardEndTransaction**](/windows/desktop/api/Winscard/nf-winscard-scardendtransaction)     | Encerrar uma transação, permitindo que outros aplicativos acessem um cartão.                                                                                                                                                                           |
| [**SCardStatus**](/windows/desktop/api/Winscard/nf-winscard-scardstatusa)                     | Forneça o status atual do leitor.                                                                                                                                                                                                  |
| [**SCardTransmit**](/windows/desktop/api/Winscard/nf-winscard-scardtransmit)                 | Solicita o serviço e recebe dados de volta de um cartão usando [*T = 0*](../secgloss/t-gly.md), [*T = 1*](../secgloss/t-gly.md)e protocolos brutos. |



 

 

 
