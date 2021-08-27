---
title: Serialização de buffer dinâmico
description: Ao usar o estilo de buffer dinâmico de serialização, o buffer de marshaling é alocado pelo stub e os dados são codificados nesse buffer e passados de volta para você. Ao desmarcar, você fornece o buffer que contém os dados.
ms.assetid: d2c3805b-47bf-4bca-b904-9414e26dde68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 906ea47a87a9d2e566dcfb033b0c9e9403ae72081afe0a1554337dbacfef9c84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021676"
---
# <a name="dynamic-buffer-serialization"></a>Serialização de buffer dinâmico

Ao usar o estilo de buffer dinâmico de serialização, o buffer de marshaling é alocado pelo stub e os dados são codificados nesse buffer e passados de volta para você. Ao desmarcar, você fornece o buffer que contém os dados.

O estilo de buffer dinâmico da serialização usa as seguintes rotinas:

-   [**MesEncodeDynBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodedynbufferhandlecreate)
-   [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate)
-   [**MesBufferHandleReset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset)
-   [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree)

A [**função MesEncodeDynBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodedynbufferhandlecreate) aloca a memória necessária para o alça de codificação e, em seguida, a inicializa. O aplicativo pode chamar [**MesBufferHandleReset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset) para reinicializar o handle. Ele chama [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) para liberar a memória do handle. Para criar um alça de decodificação correspondente ao alça de codificação de buffer dinâmico, use [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate).

 

 




