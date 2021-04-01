---
description: O terminal de streaming de mídia (MST) é um terminal dinâmico com base no uso de filtros do DirectShow. Um MSP escrito usando as classes base TAPI 3 MSP incorporará um MST, mas os autores do MSP poderão optar por implementá-lo sem usar as classes base.
ms.assetid: 21015c33-2ad1-4472-b346-167953d06a21
title: Terminal de streaming de mídia (MST)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2afb9bb4b97d0e741aec96454b187beefe2d21eb
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103930148"
---
# <a name="media-streaming-terminal-mst"></a><span data-ttu-id="e950a-104">Terminal de streaming de mídia (MST)</span><span class="sxs-lookup"><span data-stu-id="e950a-104">Media Streaming Terminal (MST)</span></span>

<span data-ttu-id="e950a-105">O terminal de streaming de mídia (MST) é um terminal dinâmico com base no uso de filtros do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="e950a-105">The Media Streaming Terminal (MST) is a dynamic terminal based on use of DirectShow filters.</span></span> <span data-ttu-id="e950a-106">Um MSP escrito usando as [classes base TAPI 3 MSP](tapi-3-msp-base-classes.md) incorporará um MST, mas os autores do MSP poderão optar por implementá-lo sem usar as classes base.</span><span class="sxs-lookup"><span data-stu-id="e950a-106">An MSP written using the [TAPI 3 MSP Base Classes](tapi-3-msp-base-classes.md) will incorporate an MST, but MSP authors may choose to implement it without using the base classes.</span></span>

<span data-ttu-id="e950a-107">Para invocar a criação de MST, um aplicativo faz uma chamada para [**ITTerminalSupport:: createterminal**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal) usando *PTERMINALCLASS* definido como CLSID \_ MediaStreamTerminal.</span><span class="sxs-lookup"><span data-stu-id="e950a-107">To invoke MST creation, an application makes a call to [**ITTerminalSupport::CreateTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal) using *pTerminalClass* set to CLSID\_MediaStreamTerminal.</span></span>

<span data-ttu-id="e950a-108">As interfaces [**ITAMMediaFormat**](/windows/win32/api/tapi3/nn-tapi3-itammediaformat) e [**ITAllocatorProperties**](/windows/win32/api/tapi3/nn-tapi3-itallocatorproperties) são então expostas no terminal, permitindo que um aplicativo ajuste o desempenho de streaming.</span><span class="sxs-lookup"><span data-stu-id="e950a-108">The [**ITAMMediaFormat**](/windows/win32/api/tapi3/nn-tapi3-itammediaformat) and [**ITAllocatorProperties**](/windows/win32/api/tapi3/nn-tapi3-itallocatorproperties) interfaces are then exposed on the terminal, allowing an application to tune streaming performance.</span></span> <span data-ttu-id="e950a-109">Essas interfaces são declaradas em Tapi3. h.</span><span class="sxs-lookup"><span data-stu-id="e950a-109">These interfaces are declared in Tapi3.h.</span></span>

<span data-ttu-id="e950a-110">A implementação e o uso de um MST exigem familiaridade com filtros do DirectShow e o gerenciamento de gráficos de filtro.</span><span class="sxs-lookup"><span data-stu-id="e950a-110">Implementation and use of an MST requires familiarity with DirectShow filters and filter graph management.</span></span> <span data-ttu-id="e950a-111">Consulte o material do DirectShow no nó gráficos e serviços de multimídia do SDK (Software Development Kit) da plataforma.</span><span class="sxs-lookup"><span data-stu-id="e950a-111">Please refer to the DirectShow material under the Graphic and Multimedia Services node of the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="e950a-112">A referência de streaming de multimídia será particularmente útil para autores MSP.</span><span class="sxs-lookup"><span data-stu-id="e950a-112">The Multimedia Streaming Reference will be particularly useful to MSP authors.</span></span>

 

 
