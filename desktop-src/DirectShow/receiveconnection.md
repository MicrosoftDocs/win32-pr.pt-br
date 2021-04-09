---
description: ReceiveConnection
ms.assetid: 90a6a09a-95e1-4adf-8e0b-269f971aaa67
title: ReceiveConnection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80fd9fe31f87a34dc3bfdfc4ecfb532255138b9c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087656"
---
# <a name="receiveconnection"></a>ReceiveConnection

Esse mecanismo permite que um pino de saída proponha uma alteração de formato ao seu par downstream, quando o novo formato requer um buffer maior. O pino de saída faz o seguinte:

1.  Chama [**IPin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) no pino de entrada downstream.
2.  Se `ReceiveConnection` tiver sucesso, chama [**IMemInputPin:: NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) no pino de entrada.

Além disso, o pino de saída pode precisar chamar [**IMemAllocator:: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) e, em seguida, desconfirmar e reconfirmar o alocador para alterar os tamanhos do buffer. Certifique-se de entregar todas as amostras pendentes no formato antigo antes de alterar o tamanho do buffer.

Alguns decodificadores MPEG-2 usam esse mecanismo para alternar entre MPEG-1 e MPEG-2 output ou se o tamanho do vídeo for alterado.

 

 



