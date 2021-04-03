---
title: Pacotes de solicitação do BITS
description: Pacotes de solicitação do BITS
ms.assetid: 4d8fd5f3-7621-438f-926f-38ece7a52f52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6738f77477342f1329818ae7c2ffb5c010b074c3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916021"
---
# <a name="bits-request-packets"></a>Pacotes de solicitação do BITS

Pacotes de solicitação descrevem solicitações de cliente. Pode haver apenas uma solicitação pendente em um determinado momento; Você deve receber um [ACK](bits-response-packets.md) para a solicitação atual do servidor antes de enviar outra solicitação.

A tabela a seguir lista os pacotes de solicitação enviados ao servidor BITS para trabalhos de upload e de resposta de upload. A tabela lista os pacotes na sequência típica que eles são enviados para o servidor.



| Pacote de solicitação                       | Finalidade                                                                                                                                                        |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Executar](ping.md)                     | Estabelece uma conexão e negocia a segurança com o servidor.                                                                                              |
| [Criar sessão](create-session.md) | Solicita uma sessão de carregamento com o servidor BITS.                                                                                                               |
| [Fragmento](fragment.md)             | Envia um fragmento do arquivo para o servidor BITS. O número de solicitações de fragmento enviadas depende do tamanho do fragmento escolhido e do tamanho do arquivo de carregamento. |
| [Fechar sessão](close-session.md)   | Encerra a sessão de carregamento de arquivo com o servidor BITS.                                                                                                             |
| [Cancelar sessão](cancel-session.md) | Encerra a sessão de carregamento de arquivo com o servidor BITS. Normalmente, você envia o pacote Cancel-Session se o usuário cancelou o trabalho.                                 |



 

O pacote de ping é opcional. Em vez de enviar um pacote de ping, você pode usar o pacote Create-Session para estabelecer uma conexão e negociar a segurança. No entanto, é mais eficiente usar o pacote de ping para essa finalidade.

 

 




