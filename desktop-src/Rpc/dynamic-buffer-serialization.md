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
# <a name="dynamic-buffer-serialization"></a><span data-ttu-id="d60a8-104">Serialização de buffer dinâmico</span><span class="sxs-lookup"><span data-stu-id="d60a8-104">Dynamic Buffer Serialization</span></span>

<span data-ttu-id="d60a8-105">Ao usar o estilo de buffer dinâmico de serialização, o buffer de Marshalling é alocado pelo stub e os dados são codificados nesse buffer e passados de volta para você.</span><span class="sxs-lookup"><span data-stu-id="d60a8-105">When using the dynamic buffer style of serialization, the marshalling buffer is allocated by the stub, and the data is encoded into this buffer and passed back to you.</span></span> <span data-ttu-id="d60a8-106">Ao desempacotamento, você fornece o buffer que contém os dados.</span><span class="sxs-lookup"><span data-stu-id="d60a8-106">When unmarshaling, you supply the buffer that contains the data.</span></span>

<span data-ttu-id="d60a8-107">O estilo do buffer dinâmico da serialização usa as seguintes rotinas:</span><span class="sxs-lookup"><span data-stu-id="d60a8-107">The dynamic buffer style of serialization uses the following routines:</span></span>

-   [<span data-ttu-id="d60a8-108">**MesEncodeDynBufferHandleCreate**</span><span class="sxs-lookup"><span data-stu-id="d60a8-108">**MesEncodeDynBufferHandleCreate**</span></span>](/windows/desktop/api/Midles/nf-midles-mesencodedynbufferhandlecreate)
-   [<span data-ttu-id="d60a8-109">**MesDecodeBufferHandleCreate**</span><span class="sxs-lookup"><span data-stu-id="d60a8-109">**MesDecodeBufferHandleCreate**</span></span>](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate)
-   [<span data-ttu-id="d60a8-110">**MesBufferHandleReset**</span><span class="sxs-lookup"><span data-stu-id="d60a8-110">**MesBufferHandleReset**</span></span>](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset)
-   [<span data-ttu-id="d60a8-111">**MesHandleFree**</span><span class="sxs-lookup"><span data-stu-id="d60a8-111">**MesHandleFree**</span></span>](/windows/desktop/api/Midles/nf-midles-meshandlefree)

<span data-ttu-id="d60a8-112">A função [**MesEncodeDynBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodedynbufferhandlecreate) aloca a memória necessária para o identificador de codificação e, em seguida, inicializa-a.</span><span class="sxs-lookup"><span data-stu-id="d60a8-112">The [**MesEncodeDynBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodedynbufferhandlecreate) function allocates the memory needed for the encoding handle and then initializes it.</span></span> <span data-ttu-id="d60a8-113">O aplicativo pode chamar [**MesBufferHandleReset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset) para reinicializar o identificador.</span><span class="sxs-lookup"><span data-stu-id="d60a8-113">The application can call [**MesBufferHandleReset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset) to reinitialize the handle.</span></span> <span data-ttu-id="d60a8-114">Ele chama [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) para liberar a memória do identificador.</span><span class="sxs-lookup"><span data-stu-id="d60a8-114">It calls [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) to free the handle's memory.</span></span> <span data-ttu-id="d60a8-115">Para criar um identificador de decodificação correspondente ao identificador de codificação de buffer dinâmico, use [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate).</span><span class="sxs-lookup"><span data-stu-id="d60a8-115">To create a decoding handle corresponding to the dynamic buffer encoding handle, use [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate).</span></span>

 

 




