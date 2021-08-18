---
title: Implementando seu código do DSP
description: Implementando seu código do DSP
ms.assetid: e1feaaee-1127-4a3a-9a4c-a30584a7e8ff
keywords:
- plug-ins Windows Media Player, processamento de sinal digital (DSP)
- plug-ins, processamento de sinal digital (DSP)
- plug-ins de processamento de sinal digital, implementando código
- Plug-ins do DSP, implementando código
- plug-ins de processamento de sinal digital, modificando código de exemplo
- Plug-ins do DSP, modificando código de exemplo
- plug-ins do DSP de áudio, implementando código
- plug-ins de DSP de vídeo, implementando código
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8504a44b9f3e980be612569e9b7cbe06081d0bfe704a5932e44eef789127687f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135559"
---
# <a name="implementing-your-dsp-code"></a>Implementando seu código do DSP

depois de criar o plug-in de dsp de exemplo, você pode modificar o código de criação do seu próprio plug-in do dsp Windows Media Player. Quais métodos você altera e quais você pode deixar, pois eles dependem dos seguintes fatores:

-   O número de propriedades que você deseja permitir que o usuário altere. Você certamente vai querer alterar a implementação da página de propriedades padrão para atender às suas necessidades, e talvez seja necessário adicionar propriedades adicionais.
-   Se o seu plug-in do DSP precisa alocar recursos de streaming. Seu plug-in pode exigir buffers adicionais.
-   se o plug-in do DSP de áudio precisa continuar a gerar dados após Windows Media Player parou de fornecer dados no buffer de entrada.

as seções a seguir usam o código de exemplo de plug-in do DSP gerado pelo assistente de plug-in Windows Media Player para ilustrar conceitos importantes. talvez você ache útil abrir Microsoft Visual Studio e gerar o código de exemplo primeiro para que possa consultá-lo enquanto lê esta seção. para obter detalhes sobre como usar o assistente de plug-in Windows Media Player, consulte [criando um Plug-in do DSP](building-a-dsp-plug-in.md).



| Seção                                                                    | Descrição                                                                                                       |
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [Implementando um plug-in do DSP de áudio](implementing-an-audio-dsp-plug-in.md) | Discute o que você precisa saber para criar seu próprio plug-in de DSP de áudio com base no exemplo gerado pelo assistente. |
| [Implementando um plug-in de DSP de vídeo](implementing-a-video-dsp-plug-in.md)   | Discute o que você precisa saber para criar seu próprio plug-in de DSP de vídeo com base no exemplo gerado pelo assistente. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre plug-ins do DSP**](about-dsp-plug-ins.md)
</dt> </dl>

 

 




