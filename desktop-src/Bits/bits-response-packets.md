---
title: Pacotes de resposta do BITS
description: Pacotes de resposta do BITS
ms.assetid: 30755476-daa9-42ea-8fb3-5b505fc9dd75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 755e28b749d201a2c90640ea9e456f012f790453
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822302"
---
# <a name="bits-response-packets"></a>Pacotes de resposta do BITS

A tabela a seguir lista os pacotes de resposta enviados para o cliente BITS para trabalhos de upload e upload-reply. A tabela lista os pacotes na sequência típica que eles são enviados para o cliente.



| Pacote de resposta                                      | Finalidade                                                                                                                                                                                     |
|------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ACK para ping](ack-for-ping.md)                     | Reconhece a solicitação de [ping](ping.md) .                                                                                                                                                  |
| [ACK para Create-Session](ack-for-create-session.md) | Reconhece a solicitação de [criação de sessão](create-session.md) e retorna um identificador de sessão que o cliente bits usa em todas as solicitações subsequentes para identificar essa sessão de transferência de arquivos. |
| [Confirmação para fragmento](ack-for-fragment.md)             | Reconhece a solicitação de [fragmento](fragment.md) e grava o fragmento no arquivo de carregamento no servidor.                                                                                 |
| [ACK para fechamento de sessão](ack-for-close-session.md)   | Reconhece a solicitação de [fechamento de sessão](close-session.md) e libera todos os recursos associados à sessão.                                                                         |
| [ACK para cancelamento de sessão](ack-for-cancel-session.md) | Reconhece a solicitação de [cancelamento de sessão](cancel-session.md) e libera todos os recursos associados à sessão.                                                                       |



 

 

 




