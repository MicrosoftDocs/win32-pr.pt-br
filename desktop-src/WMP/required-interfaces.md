---
title: Interfaces necessárias (Windows Media Player SDK)
description: saiba mais sobre as interfaces necessárias que Windows Media Player implementa em DirectShow ou Media Foundation.
ms.assetid: 202d5769-edff-46df-bc05-bbb630a8f3f4
keywords:
- plug-ins Windows Media Player, interfaces
- plug-ins, interfaces
- plug-ins de processamento de sinal digital, interfaces
- Plug-ins do DSP, interfaces
- interfaces, plug-ins do DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18a3552cbe741b3b527c899e5bb7d68fe4d7c4e0bdc61203f822c57111e94a46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119646826"
---
# <a name="required-interfaces-windows-media-player-sdk"></a>Interfaces necessárias (Windows Media Player SDK)

Windows Media Player processa áudio e vídeo usando um dos pipelines a seguir.

-   DirectShow
-   Media Foundation

no Microsoft Windows XP e versões anteriores, o Player usa DirectShow. no Windows Vista, às vezes o Player usa DirectShow e, às vezes, usa Media Foundation.

Um plug-in do DSP implementa algumas ou todas as seguintes interfaces:

-   **IMediaObject**
-   **IWMPPluginEnable**
-   **IMFTransform**
-   **IMFGetService**
-   **ISpecifyPropertyPages**

um plug-in que implementa **IMediaObject** e **IWMPPluginEnable** pode ser executado no pipeline DirectShow. Ele também pode ser executado no pipeline de Media Foundation dentro de um wrapper fornecido pelo Media Foundation. Um plug-in desse tipo é chamado de objeto de mídia DirectX da Microsoft (DMO). é comum considerar um DMO como sendo análogo a um objeto de filtro no DirectShow. a documentação DMO está na seção DirectShow do SDK do Windows.

Um plug-in que implementa **IMFTransform** e **IMFGetService** pode ser executado nativamente (nenhum wrapper é necessário) no pipeline de Media Foundation. Um plug-in desse tipo é chamado de Media Foundation transformação (MFT). a documentação do MFT está na seção Media Foundation do SDK do Windows.

um plug-in que implementa **IMediaObject**, **IWMPPluginEnable**, **IMFTransform** e **IMFGetService** pode ser executado no pipeline de DirectShow e também pode ser executado nativamente no pipeline de Media Foundation. esse tipo de plug-in, chamado de plug-in de *DSP de modo duplo*, pode desempenhar a função de um DMO ou de um MFT.

quando Windows Media Player usa um plug-in de DSP de modo duplo no pipeline de Media Foundation, ele primeiro consulta a interface **IMFTransform** . se essa consulta falhar, Windows Media Player consultas para a interface **IMediaObject** . Se a consulta **IMediaObject** for bem-sucedida, o plug-in será encapsulado e adicionado ao pipeline de Media Foundation.

Independentemente do pipeline, qualquer plug-in de DSP que permita ao usuário definir propriedades deve implementar **ISpecifyPropertyPages**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Visão geral do desenvolvedor de plug-in do DSP**](dsp-plug-in-developer-overview.md)
</dt> <dt>

[**Interfaces de plug-in do DSP**](dsp-plug-in-interfaces.md)
</dt> <dt>

[**Empacotamento de plug-in do DSP**](dsp-plug-in-packaging.md)
</dt> </dl>

 

 




