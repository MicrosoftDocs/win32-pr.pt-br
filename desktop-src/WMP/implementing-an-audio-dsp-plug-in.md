---
title: Implementando um plug-in do DSP de áudio
description: Implementando um plug-in do DSP de áudio
ms.assetid: 93ff0c45-f418-443d-8fba-c0a62f6e4e80
keywords:
- Plug-ins do Windows Media Player, DSP de áudio
- plug-ins, DSP de áudio
- plug-ins de processamento de sinal digital, implementando código
- Plug-ins do DSP, implementando código
- plug-ins de processamento de sinal digital, modificando código de exemplo
- Plug-ins do DSP, modificando código de exemplo
- plug-ins de processamento de sinal digital, implementação de áudio
- Plug-ins do DSP, implementação de áudio
- plug-ins do DSP de áudio, implementando código
- plug-ins do DSP de áudio, modificando código de exemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdde8e7f00fc9ea3ad9bb8b7adb2d0a8bfba6b32
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005835"
---
# <a name="implementing-an-audio-dsp-plug-in"></a>Implementando um plug-in do DSP de áudio

Para criar um plug-in de DSP do Windows Media Player que processa áudio, você precisará modificar o código de exemplo na função chamada **DoProcessOutput**. **DoProcessOutput** é chamado cada vez que o Windows Media Player chama com êxito **IMediaObject::P rocessoutput**. É a função que executa as tarefas de processamento de sinal digital que produzem o resultado audível que o plug-in do DSP pretende produzir.

O processamento de um fluxo de áudio é como lidar com um evento cronometrado. **DoProcessOutput** será chamado repetidamente e em intervalos específicos. Cada vez que seu código for executado, ele precisará processar um número específico de bytes de dados. **DoProcessOutput** contém os seguintes parâmetros:



| Parâmetro          | Descrição                                                                                                             |
|--------------------|-------------------------------------------------------------------------------------------------------------------------|
| *pbOutputData*     | Esse é um ponteiro de **byte** para o buffer em que sua implementação de **DoProcessOutput** deve copiar seus dados processados. |
| *pbInputData*      | Esse é um ponteiro de **byte** constante para o buffer que contém os dados a serem processados.                               |
| *cbBytesToProcess* | Esse é um valor **DWORD** que contém uma contagem do número de bytes no buffer de entrada a ser processado.             |



 

As seções a seguir fornecem detalhes sobre como modificar o código gerado pelo assistente de plug-in do Windows Media Player para criar seu próprio plug-in de DSP de áudio:

-   [Implementando DoProcessOutput](implementing-doprocessoutput.md)
-   [Adicionando propriedades ao plug-in do DSP de áudio de exemplo](adding-properties-to-the-sample-audio-dsp-plug-in.md)
-   [Implementando a página de propriedades para um plug-in do DSP](implementing-the-property-page-for-a-dsp-plug-in.md)
-   [Alterando a propriedade de plug-in do DSP de áudio de exemplo](changing-the-sample-audio-dsp-plug-in-property.md)
-   [Sobre a descontinuidade](about-discontinuity.md)
-   [Sobre a alocação de recursos de streaming](about-allocating-streaming-resources.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre plug-ins do DSP**](about-dsp-plug-ins.md)
</dt> </dl>

 

 




