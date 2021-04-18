---
description: Conecte-se e comunique-se com um cartão inteligente específico.
ms.assetid: 37d92491-174b-471e-b36e-46d9285dd404
title: Funções de acesso de cartão inteligente e leitor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7202b2d6165b49bfe80e55f15c4d69cb4a6909a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755322"
---
# <a name="smart-card-and-reader-access-functions"></a>Funções de acesso de cartão inteligente e leitor

As funções a seguir se conectam e se comunicam com um [*cartão inteligente*](../secgloss/s-gly.md)específico. As operações de e/s para o cartão usam um buffer para enviar ou receber dados e uma estrutura que contém informações de controle de protocolo. A estrutura de informações de controle de protocolo sempre começa com uma estrutura de [**\_ \_ solicitação de e/s scartar**](scard-io-request.md) .



| Tópico                                                  | Descrição                                                                                                                                                                                                                                |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SCardConnect**](/windows/desktop/api/Winscard/nf-winscard-scardconnecta)                   | Conecte-se a um cartão.                                                                                                                                                                                                                         |
| [**SCardReconnect**](/windows/desktop/api/Winscard/nf-winscard-scardreconnect)               | Restabelecer uma conexão.                                                                                                                                                                                                                  |
| [**SCardDisconnect**](/windows/desktop/api/Winscard/nf-winscard-scarddisconnect)             | Encerrar uma conexão.                                                                                                                                                                                                                    |
| [**SCardBeginTransaction**](/windows/desktop/api/Winscard/nf-winscard-scardbegintransaction) | Inicie uma [*transação*](../secgloss/t-gly.md), impedindo que outros aplicativos acessem um cartão.                                                                                            |
| [**SCardEndTransaction**](/windows/desktop/api/Winscard/nf-winscard-scardendtransaction)     | Encerrar uma transação, permitindo que outros aplicativos acessem um cartão.                                                                                                                                                                           |
| [**SCardStatus**](/windows/desktop/api/Winscard/nf-winscard-scardstatusa)                     | Forneça o status atual do leitor.                                                                                                                                                                                                  |
| [**SCardTransmit**](/windows/desktop/api/Winscard/nf-winscard-scardtransmit)                 | Solicita o serviço e recebe dados de volta de um cartão usando [*T = 0*](../secgloss/t-gly.md), [*T = 1*](../secgloss/t-gly.md)e protocolos brutos. |



 

 

 
