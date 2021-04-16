---
title: Negociação de formato
description: Negociação de formato
ms.assetid: 7847d4e3-1250-4c35-88e1-52d61bf1553f
keywords:
- Plug-ins do Windows Media Player, negociação de formato
- plug-ins, negociação de formato
- plug-ins de processamento de sinal digital, negociação de formato
- Plug-ins do DSP, negociação de formato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbc805b18d3e2be081e4f85bcc5ed42aded06853
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105794470"
---
# <a name="format-negotiation"></a>Negociação de formato

Para o Windows Media Player e um plug-in do DSP para compartilhar dados, ambos os programas devem concordar com o formato dos dados que estão processando. O plug-in do DSP implementa métodos que o Player chama para determinar os formatos aos quais o plug-in dá suporte. O plug-in também implementa métodos que o Player chama para definir o formato atual.

Se o plug-in estiver agindo como um DMO (DirextX Media Object), o Windows Media Player descobre e define os formatos de mídia chamando métodos da interface **IMediaObject** . Por exemplo, o Player chama repetidamente o plug-in **IMediaObject:: GetInputType** para obter uma lista de todos os formatos de entrada com suporte pelo plug-in. Plug-ins do DMO usam a estrutura do **\_ \_ tipo de mídia DMO** para organizar as informações que especificam um formato de mídia. Para obter mais informações sobre como plug-ins de DMO e o formato de negociação do Player, consulte [about IMediaObject](about-imediaobject.md).

Se o plug-in estiver agindo como uma Media Foundation transformação (MFT), o Windows Media Player descobre e define os formatos de mídia chamando métodos da interface **IMFTransform** . Por exemplo, o Player chama a **IMFTransform:: GetInputAvailableType** repetidamente do plug-in para obter uma lista de todos os formatos de entrada com suporte no plug-in. Plug-ins de MFT e o Player usam a interface **IMFMediaType** para organizar e trocar informações de formato.

O Windows Media Player usará um plug-in de DSP de áudio somente se o plug-in der suporte à mesma profundidade do áudio digital que está sendo reproduzido. Por exemplo, se o áudio digital for de 20 bits, o plug-in deverá ser escrito para processar áudio de 20 bits. Para áudio de CD, plug-ins DSP devem dar suporte ao processamento de 20 bits.

Durante a negociação de formato de conteúdo de vários canais em um computador configurado para uso com alto-falantes estéreo, o Windows Media Player primeiro tenta se conectar a um plug-in de DSP de áudio usando o formato de entrada e saída existente chamando **IMediaObject:: SetInputType** e **IMediaObject:: SetOutputType**. Depois que essa negociação inicial ocorre, o Player enumera os formatos aos quais o plug-in dá suporte e tenta negociar a melhor combinação de formato para o Player e o plug-in. Se o plug-in aceitar áudio estéreo (definido por uma estrutura **WAVEFORMATEX** ) como o formato de entrada durante a negociação inicial e depois aceitar somente o áudio de vários canais (definido por uma estrutura **WAVEFORMATEXTENSIBLE** ), o Player fornecerá áudio multicanal como o formato de entrada para o plug-in. Esse comportamento durante a negociação de formato está disponível para uso no sistema operacional Microsoft Windows XP. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Visão geral do desenvolvedor de plug-in do DSP**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




