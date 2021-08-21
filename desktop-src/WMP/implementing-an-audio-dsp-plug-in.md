---
title: Implementando um plug-in DSP de áudio
description: Implementando um plug-in DSP de áudio
ms.assetid: 93ff0c45-f418-443d-8fba-c0a62f6e4e80
keywords:
- Windows Media Player plug-ins, DSP de áudio
- plug-ins, DSP de áudio
- plug-ins de processamento de sinal digital, implementando código
- Plug-ins DSP, implementando código
- plug-ins de processamento de sinal digital, modificando o código de exemplo
- Plug-ins DSP, modificando o código de exemplo
- plug-ins de processamento de sinal digital, implementação de áudio
- Plug-ins DSP, implementação de áudio
- plug-ins DSP de áudio, implementando código
- plug-ins DSP de áudio, modificando o código de exemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f18ca0aada7072ca7cd1c0796c3cd6770a9b45340a4d9f67a342944f4c22887
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118338637"
---
# <a name="implementing-an-audio-dsp-plug-in"></a>Implementando um plug-in DSP de áudio

Para criar um Windows Media Player plug-in DSP que processa o áudio, você precisará modificar o código de exemplo na função chamada **DoProcessOutput**. **DoProcessOutput** é chamado sempre que Windows Media Player chama **IMediaObject::P rocessOutput com êxito.** É a função que executa as tarefas de processamento de sinal digital que produzem o resultado audível que o plug-in DSP se destina a produzir.

O processamento de um fluxo de áudio é como lidar com um evento de tempo. **DoProcessOutput será** chamado repetidamente e em intervalos específicos. Sempre que o código é executado, ele precisará processar um número específico de bytes de dados. **DoProcessOutput** contém os seguintes parâmetros:



| Parâmetro          | Descrição                                                                                                             |
|--------------------|-------------------------------------------------------------------------------------------------------------------------|
| *pbOutputData*     | Este é um **ponteiro BYTE** para o buffer em que sua implementação **de DoProcessOutput** deve copiar seus dados processados. |
| *pbInputData*      | Esse é um ponteiro **BYTE** constante para o buffer que contém os dados a serem processados.                               |
| *cbBytesToProcess* | Esse é um **valor DWORD** que contém uma contagem do número de bytes no buffer de entrada a ser processado.             |



 

As seções a seguir fornecem detalhes sobre como modificar o código gerado pelo Assistente de Plug-in Windows Media Player para criar seu próprio plug-in DSP de áudio:

-   [Implementando DoProcessOutput](implementing-doprocessoutput.md)
-   [Adicionando propriedades ao plug-in DSP de áudio de exemplo](adding-properties-to-the-sample-audio-dsp-plug-in.md)
-   [Implementando a página de propriedades para um plug-in DSP](implementing-the-property-page-for-a-dsp-plug-in.md)
-   [Alterando a propriedade de plug-in DSP de áudio de exemplo](changing-the-sample-audio-dsp-plug-in-property.md)
-   [Sobre descontinuidade](about-discontinuity.md)
-   [Sobre como alocar recursos de streaming](about-allocating-streaming-resources.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre plug-ins DSP**](about-dsp-plug-ins.md)
</dt> </dl>

 

 




