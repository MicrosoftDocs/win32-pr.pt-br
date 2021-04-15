---
title: Serialização de buffer dinâmico
description: Ao usar o estilo de buffer dinâmico de serialização, o buffer de Marshalling é alocado pelo stub e os dados são codificados nesse buffer e passados de volta para você. Ao desempacotamento, você fornece o buffer que contém os dados.
ms.assetid: d2c3805b-47bf-4bca-b904-9414e26dde68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10c1b97124c502e48c4d3ba18e424770bc936496
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453600"
---
# <a name="dynamic-buffer-serialization"></a>Serialização de buffer dinâmico

Ao usar o estilo de buffer dinâmico de serialização, o buffer de Marshalling é alocado pelo stub e os dados são codificados nesse buffer e passados de volta para você. Ao desempacotamento, você fornece o buffer que contém os dados.

O estilo do buffer dinâmico da serialização usa as seguintes rotinas:

-   [**MesEncodeDynBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodedynbufferhandlecreate)
-   [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate)
-   [**MesBufferHandleReset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset)
-   [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree)

A função [**MesEncodeDynBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodedynbufferhandlecreate) aloca a memória necessária para o identificador de codificação e, em seguida, inicializa-a. O aplicativo pode chamar [**MesBufferHandleReset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset) para reinicializar o identificador. Ele chama [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) para liberar a memória do identificador. Para criar um identificador de decodificação correspondente ao identificador de codificação de buffer dinâmico, use [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate).

 

 




