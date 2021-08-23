---
description: O MST (Terminal de Streaming de Mídia) é um terminal dinâmico baseado no uso de filtros DirectShow mídia. Um MSP escrito usando as Classes Base do TAPI 3 MSP incorporará um MST, mas os autores do MSP podem optar por implementá-lo sem usar as classes base.
ms.assetid: 21015c33-2ad1-4472-b346-167953d06a21
title: MST (Terminal de Streaming de Mídia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8eeb9ad231c114ca18b4dea0926b861360ab5a359cd9ee8c48fd1c388a941a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002904"
---
# <a name="media-streaming-terminal-mst"></a>MST (Terminal de Streaming de Mídia)

O MST (Terminal de Streaming de Mídia) é um terminal dinâmico baseado no uso de filtros DirectShow mídia. Um MSP escrito usando as Classes Base do [TAPI 3 MSP](tapi-3-msp-base-classes.md) incorporará um MST, mas os autores do MSP podem optar por implementá-lo sem usar as classes base.

Para invocar a criação do MST, um aplicativo faz uma chamada para [**ITTerminalSupport::CreateTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal) usando *pTerminalClass* definido como CLSID \_ MediaStreamTerminal.

As interfaces [**ITAMMediaFormat**](/windows/win32/api/tapi3/nn-tapi3-itammediaformat) e [**ITAllocatorProperties**](/windows/win32/api/tapi3/nn-tapi3-itallocatorproperties) são expostas no terminal, permitindo que um aplicativo ajuste o desempenho de streaming. Essas interfaces são declaradas em Tapi3.h.

A implementação e o uso de um MST exigem familiaridade com DirectShow filtros e gerenciamento de grafo de filtro. Consulte o material DirectShow no nó Serviços Gráficos e Multimídia do SDK (Kit de Desenvolvimento de Software de Plataforma). A Referência de Streaming multimídia será particularmente útil para autores do MSP.

 

 
