---
description: Uma transação é uma série de modificações de um armazenamento de dados (como um banco de dado ou sistema de arquivos) garantida para que seja executada com êxito ou não seja executada.
ms.assetid: 1567d9d3-7839-42f0-9507-7bbf61d8eaf2
title: Enfileiramento de mensagens transacionais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3282a95d4f9a3ba451e78fe4d9f17acf007b0007abea4fdb4951de9c1540383
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636726"
---
# <a name="transactional-message-queuing"></a>Enfileiramento de mensagens transacionais

Uma *transação* é uma série de modificações de um armazenamento de dados (como um banco de dado ou sistema de arquivos) garantida para que seja executada com êxito ou não seja executada. Para implementar uma transação, um registro é mantido do estado do armazenamento de dados antes do início da transação e, se uma das modificações falhar, a transação retornará uma falha e o estado inicial será restaurado (ou revertido). As transações são usadas para manter a integridade dos dados e, consequentemente, desempenhar um papel importante na programação de software comercial.

Muitas vezes, os aplicativos podem ser desenvolvidos usando uma transação comercial ou um fluxo de trabalho dividido em várias transações ou atividades menores. Essas atividades são separadas no tempo e, em seguida, conectadas usando filas de mensagens confiáveis.

1.  A primeira transação envolve o banco de dados de entrada de pedidos. O [enfileiramento de mensagens](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) move a mensagem de uma fila para outra, exatamente uma vez, usando recursos de transação. Se o banco de dados for atualizado, haverá uma mensagem na fila. Se a mensagem não atingir a fila, ela será anulada e o banco de dados será revertido.
2.  Um pouco mais tarde, o serviço de enfileiramento de mensagens descobre que o servidor está disponível. Não há sondagem de aplicativo para a existência do servidor. Esta é a segunda transação.
3.  A terceira transação envolve uma consulta de banco de dados de remessa e a atualização do banco de dados de envio. Se o servidor falhar no meio dessa transação, a modificação será revertida e a mensagem será retornada para a fila de entrada. Isso garante que a integridade dos dados e dos bancos de dados seja mantida durante as transações.

 

 



