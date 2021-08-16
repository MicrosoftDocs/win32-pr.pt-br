---
title: Empacotamento de plug-in do DSP
description: Empacotamento de plug-in do DSP
ms.assetid: 5d40a39b-0fe8-4f77-9465-8e31d1f2708e
keywords:
- Windows Media Player plug-ins,Media Foundation pipeline
- plug-ins, Media Foundation pipeline
- plug-ins de processamento de sinal digital, Media Foundation pipeline
- Plug-ins do DSP, Media Foundation pipeline
- Media Foundation pipeline
- Windows Media Player plug-ins,DirectShow pipeline
- plug-ins, DirectShow pipeline
- plug-ins de processamento de sinal digital, DirectShow pipeline
- Plug-ins do DSP, DirectShow pipeline
- DirectShow pipeline
- plug-ins de processamento de sinal digital, básico
- Plug-ins do DSP, básico
- Windows Media Player plug-ins, DSP básico
- plug-ins, DSP básico
- plug-ins DSP básicos
- Windows Media Player plug-ins, DSP de modo duplo
- plug-ins, DSP de modo duplo
- plug-ins de processamento de sinal digital, modo duplo
- Plug-ins DSP, modo duplo
- plug-ins DSP de modo duplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2bd87e1729b4d8759f3b9f1d7d4d7993660512d49c34ea9bf9aa34802b69cd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117749501"
---
# <a name="dsp-plug-in-packaging"></a>Empacotamento de plug-in do DSP

Windows Media Player renderiza áudio e vídeo usando um dos pipelines a seguir.

-   DirectShow
-   Media Foundation

No Microsoft Windows XP e anterior, o Player usa DirectShow. No Windows Vista, o Player às vezes usa DirectShow e, às vezes, usa Media Foundation.

Um plug-in DSP projetado para ser executado no pipeline DirectShow é chamado de *plug-in DSP básico.* Um plug-ins DSP básico atua como um objeto de mídia directX (DMO). Um plug-in básico do DSP pode ser executado na nações DirectShow pipeline do DirectShow e também pode ser executado no pipeline do Media Foundation dentro de um wrapper fornecido pelo Media Foundation.

Um plug-in DSP que foi projetado para ser executado na nativa (nenhum wrapper necessário) nos pipelines DirectShow e Media Foundation é chamado de *plug-in DSP* de modo duplo. Um plug-in DSP de modo duplo pode atuar como um DMO ou como uma transformação Media Foundation (MFT).

Um plug-in DSP é um objeto COM que é empacotado como um arquivo de registro .dll auto-registro. As interfaces que o plug-in implementa dependem se o plug-in foi projetado como um plug-in DSP básico ou como um plug-in DSP de modo duplo. Para obter informações detalhadas sobre as interfaces que os plug-ins DSP devem implementar, consulte [Interfaces necessárias.](required-interfaces.md)

Um plug-in DSP que é executado no pipeline Media Foundation (nações ou empacotado) deve registrar seu modelo de threading como "Ambos". Para obter informações detalhadas sobre sub-chaves e entradas do Registro associadas a plug-ins DSP, consulte [Registrando plug-ins DSP](registering-dsp-plug-ins.md).

Um plug-in DSP que implementa interfaces personalizadas e é executado no pipeline do Media Foundation (nações ou empacotados) deve ser emparelhado com um arquivo proxy-stub .dll que pode realizar marshal das interfaces personalizadas entre os limites do processo. Para obter informações sobre o componente proxy-stub, consulte Atualizando [plug-ins](updating-existing-dsp-plug-ins.md) e atualizações do DSP existentes para o Assistente de [Plug-in DSP para Windows Media Player 11](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md).

Objetos de plug-in DSP não devem ser criados como singletons. Windows Media Player ser capaz de criar várias instâncias separadas de um plug-in DSP específico.

Os plug-ins DSP executados no Windows PMP (Caminho de Mídia Protegida) do Vista devem ser assinados. Para obter mais informações, consulte [Assinatura de código para componentes de mídia protegidos no Windows Vista](/windows-hardware/test/hlk/).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Visão geral do desenvolvedor do plug-in DSP**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 