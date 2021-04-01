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
# <a name="media-streaming-terminal-mst"></a>Terminal de streaming de mídia (MST)

O terminal de streaming de mídia (MST) é um terminal dinâmico com base no uso de filtros do DirectShow. Um MSP escrito usando as [classes base TAPI 3 MSP](tapi-3-msp-base-classes.md) incorporará um MST, mas os autores do MSP poderão optar por implementá-lo sem usar as classes base.

Para invocar a criação de MST, um aplicativo faz uma chamada para [**ITTerminalSupport:: createterminal**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal) usando *PTERMINALCLASS* definido como CLSID \_ MediaStreamTerminal.

As interfaces [**ITAMMediaFormat**](/windows/win32/api/tapi3/nn-tapi3-itammediaformat) e [**ITAllocatorProperties**](/windows/win32/api/tapi3/nn-tapi3-itallocatorproperties) são então expostas no terminal, permitindo que um aplicativo ajuste o desempenho de streaming. Essas interfaces são declaradas em Tapi3. h.

A implementação e o uso de um MST exigem familiaridade com filtros do DirectShow e o gerenciamento de gráficos de filtro. Consulte o material do DirectShow no nó gráficos e serviços de multimídia do SDK (Software Development Kit) da plataforma. A referência de streaming de multimídia será particularmente útil para autores MSP.

 

 
