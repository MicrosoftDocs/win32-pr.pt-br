---
title: Assistente de plug-in do DSP
description: Assistente de plug-in do DSP
ms.assetid: 3d1ae5ef-12c4-4db3-815a-2adc73353f20
keywords:
- Plug-ins do Windows Media Player, assistente de plug-in
- plug-ins, assistente de plug-in
- plug-ins de processamento de sinal digital, assistente de plug-in
- Plug-ins do DSP, assistente de plug-in
- Assistente de plug-in
- Visual Studio, assistente de plug-in do DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e9a7228056d821d2c2bca258f5c236fe1dce11d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498679"
---
# <a name="dsp-plug-in-wizard"></a>Assistente de plug-in do DSP

O SDK do Windows Media Player fornece um assistente de plug-in que você pode adicionar ao Visual Studio. O assistente pode gerar um código de exemplo para uma variedade de plug-ins, incluindo os seguintes tipos de plug-ins do DSP:

-   Plug-in do DSP de áudio
-   Plug-in do DSP de áudio (modo duplo)
-   Plug-in de DSP de vídeo
-   Plug-in de DSP de vídeo (modo dual)

Cada um dos dois plug-ins básicos de exemplo, DSP de áudio e DSP de vídeo, funciona como um DMO (objeto de mídia do DirectX). Ou seja, cada plug-in de exemplo implementa a interface **IMediaObject** . Cada um dos dois plug-ins de exemplo de modo duplo pode funcionar como um DMO ou como uma Media Foundation transformação (MFT). Ou seja, cada plug-in de exemplo de modo duplo implementa a interface **IMediaObject** e a interface **IMFTransform** .

Você pode compilar, vincular, registrar e testar o código de plug-in de exemplo. Em seguida, você pode modificar o código de exemplo gerado para criar seu próprio plug-in de DSP.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando um plug-in do DSP**](building-a-dsp-plug-in.md)
</dt> <dt>

[**Visão geral do desenvolvedor de plug-in do DSP**](dsp-plug-in-developer-overview.md)
</dt> <dt>

[**Atualizações para o assistente de plug-in do DSP para Windows Media Player 11**](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md)
</dt> </dl>

 

 




