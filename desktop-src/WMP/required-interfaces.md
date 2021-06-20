---
title: Interfaces necessárias (SDK do Windows Media Player)
description: Saiba mais sobre as interfaces necessárias que o Windows Media Player implementa no DirectShow ou Media Foundation.
ms.assetid: 202d5769-edff-46df-bc05-bbb630a8f3f4
keywords:
- Plug-ins do Windows Media Player, interfaces
- plug-ins, interfaces
- plug-ins de processamento de sinal digital, interfaces
- Plug-ins do DSP, interfaces
- interfaces, plug-ins do DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d27a0c0ed56db5f35c8cde8203fcf99a81a9260
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406089"
---
# <a name="required-interfaces-windows-media-player-sdk"></a>Interfaces necessárias (SDK do Windows Media Player)

O Windows Media Player renderiza áudio e vídeo usando um dos pipelines a seguir.

-   DirectShow
-   Media Foundation

No Microsoft Windows XP e versões anteriores, o Player usa o DirectShow. No Windows Vista, às vezes o Player usa o DirectShow e, às vezes, usa Media Foundation.

Um plug-in do DSP implementa algumas ou todas as seguintes interfaces:

-   **IMediaObject**
-   **IWMPPluginEnable**
-   **IMFTransform**
-   **IMFGetService**
-   **ISpecifyPropertyPages**

Um plug-in que implementa **IMediaObject** e **IWMPPluginEnable** pode ser executado no pipeline do DirectShow. Ele também pode ser executado no pipeline de Media Foundation dentro de um wrapper fornecido pelo Media Foundation. Um plug-in desse tipo é chamado de Microsoft DirectX Media Object (DMO). É comum considerar um DMO como sendo análogo a um objeto de filtro no DirectShow. A documentação do DMO está na seção do DirectShow do SDK do Windows.

Um plug-in que implementa **IMFTransform** e **IMFGetService** pode ser executado nativamente (nenhum wrapper é necessário) no pipeline de Media Foundation. Um plug-in desse tipo é chamado de Media Foundation transformação (MFT). A documentação do MFT está na seção Media Foundation do SDK do Windows.

Um plug-in que implementa **IMediaObject**, **IWMPPluginEnable**, **IMFTransform** e **IMFGetService** pode ser executado no pipeline do DirectShow e também pode ser executado nativamente no pipeline de Media Foundation. Esse tipo de plug-in, chamado de plug-in de *DSP de modo duplo*, pode desempenhar a função de um DMO ou MFT.

Quando o Windows Media Player usa um plug-in de DSP de modo duplo no pipeline de Media Foundation, ele primeiro consulta a interface **IMFTransform** . Se essa consulta falhar, o Windows Media Player consultará a interface **IMediaObject** . Se a consulta **IMediaObject** for bem-sucedida, o plug-in será encapsulado e adicionado ao pipeline de Media Foundation.

Independentemente do pipeline, qualquer plug-in de DSP que permita ao usuário definir propriedades deve implementar **ISpecifyPropertyPages**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Visão geral do desenvolvedor de plug-in do DSP**](dsp-plug-in-developer-overview.md)
</dt> <dt>

[**Interfaces de plug-in do DSP**](dsp-plug-in-interfaces.md)
</dt> <dt>

[**Empacotamento de plug-in do DSP**](dsp-plug-in-packaging.md)
</dt> </dl>

 

 




