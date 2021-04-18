---
title: Empacotamento de plug-in do DSP
description: Empacotamento de plug-in do DSP
ms.assetid: 5d40a39b-0fe8-4f77-9465-8e31d1f2708e
keywords:
- Plug-ins do Windows Media Player, Media Foundation pipeline
- plug-ins, pipeline de Media Foundation
- plug-ins de processamento de sinal digital, Media Foundation pipeline
- Plug-ins do DSP, pipeline de Media Foundation
- Pipeline de Media Foundation
- Plug-ins do Windows Media Player, pipeline do DirectShow
- plug-ins, pipeline do DirectShow
- plug-ins de processamento de sinal digital, pipeline do DirectShow
- Plug-ins do DSP, pipeline do DirectShow
- Pipeline do DirectShow
- plug-ins de processamento de sinal digital, básico
- Plug-ins do DSP, básico
- Plug-ins do Windows Media Player, DSP básico
- plug-ins, DSP básico
- plug-ins básicos do DSP
- Plug-ins do Windows Media Player, DSP de modo duplo
- plug-ins, DSP de modo duplo
- plug-ins de processamento de sinal digital, modo duplo
- Plug-ins do DSP, modo duplo
- plug-ins DSP de modo duplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62535abe0d82975bf07fef178ac43cf066c6afbd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105811337"
---
# <a name="dsp-plug-in-packaging"></a>Empacotamento de plug-in do DSP

O Windows Media Player renderiza áudio e vídeo usando um dos pipelines a seguir.

-   DirectShow
-   Media Foundation

No Microsoft Windows XP e versões anteriores, o Player usa o DirectShow. No Windows Vista, às vezes o Player usa o DirectShow e, às vezes, usa Media Foundation.

Um plug-in do DSP projetado para ser executado no pipeline do DirectShow é chamado de *plug-in básico do DSP*. Os plug-ins básicos do DSP atuam como um DMO (objeto de mídia do DirectX). Um plug-in de DSP básico pode ser executado nativamente no pipeline do DirectShow e também pode ser executado no pipeline de Media Foundation dentro de um wrapper fornecido pelo Media Foundation.

Um plug-in do DSP projetado para ser executado nativamente (nenhum wrapper necessário) nos pipelines do DirectShow e do Media Foundation é chamado de *plug-in de DSP de modo duplo*. Um plug-in DSP de modo duplo pode atuar como um DMO ou como uma Media Foundation transformação (MFT).

Um plug-in do DSP é um objeto COM que é empacotado como um arquivo. dll de registro automático. As interfaces que o plug-in implementa dependem se o plug-in foi projetado como um plug-in de DSP básico ou como um plug-in de DSP de modo duplo. Para obter informações detalhadas sobre as interfaces que os plug-ins do DSP devem implementar, consulte [interfaces necessárias](required-interfaces.md).

Um plug-in DSP executado no pipeline de Media Foundation (nativamente ou encapsulado) deve registrar seu modelo de Threading como "ambos". Para obter informações detalhadas sobre as subchaves do registro e as entradas associadas aos plug-ins do DSP, consulte [registrando plug-ins do DSP](registering-dsp-plug-ins.md).

Um plug-in de DSP que implementa interfaces personalizadas e execuções no pipeline de Media Foundation (nativamente ou encapsulado) deve ser emparelhado com um arquivo de stub de proxy. dll que pode realizar marshaling das interfaces personalizadas entre limites de processo. Para obter informações sobre o componente de stub de proxy, consulte [atualizando plug-ins de DSP existentes](updating-existing-dsp-plug-ins.md) e [atualizações para o assistente de plug-in do DSP para Windows Media Player 11](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md).

Os objetos de plug-in do DSP não devem ser criados como singletons. O Windows Media Player deve ser capaz de criar várias instâncias separadas de um plug-in de DSP específico.

Plug-ins DSP executados no caminho de mídia protegida do Windows Vista (PMP) devem ser assinados. Para obter mais informações, consulte [assinatura de código para componentes de mídia protegidos no Windows Vista](/windows-hardware/test/hlk/).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Visão geral do desenvolvedor de plug-in do DSP**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 