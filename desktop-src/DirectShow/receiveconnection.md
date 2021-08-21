---
description: Receiveconnection
ms.assetid: 90a6a09a-95e1-4adf-8e0b-269f971aaa67
title: Receiveconnection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55a8a91cbf9870d6c53592ff823f710eb5875fa939592309425df0a0bca6f0e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072760"
---
# <a name="receiveconnection"></a>Receiveconnection

Esse mecanismo permite que um pino de saída propor uma alteração de formato para seu par downstream, quando o novo formato exigir um buffer maior. O pino de saída faz o seguinte:

1.  Chama [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) no pino de entrada downstream.
2.  Se `ReceiveConnection` for bem-sucedido, [**chamará IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) no pino de entrada.

Além disso, o pino de saída pode precisar chamar [**IMemAllocator::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) e, em seguida, descommitir e recomendar o alocador para alterar os tamanhos do buffer. Certifique-se de entregar todos os exemplos pendentes no formato antigo antes de alterar o tamanho do buffer.

Alguns decodificadores MPEG-2 usam esse mecanismo para alternar entre a saída MPEG-1 e MPEG-2 ou se o tamanho do vídeo mudar.

 

 



