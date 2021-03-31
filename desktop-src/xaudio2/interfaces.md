---
title: Interfaces XAudio2
description: Esta seção contém informações sobre as interfaces fornecidas pela API do Microsoft XAudio2.
ms.assetid: 96691e00-9ed0-b31c-fbe9-4daaba0daf98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2d9f2c777a7b98c5cbc78a130c0a1431be5971d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172047"
---
# <a name="xaudio2-interfaces"></a>Interfaces XAudio2

Esta seção contém informações sobre as interfaces fornecidas pela API do Microsoft XAudio2.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                               | Descrição                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2)<br/>                             | IXAudio2 é a interface do objeto [XAudio2](xaudio2-apis-portal.md) que gerencia todos os Estados do mecanismo de áudio, o thread de processamento de áudio, o grafo de voz e assim por diante. <br/>                                                                                                                                                |
| [**IXAudio2Voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voice)<br/>                   | [**IXAudio2Voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voice) representa a interface base da qual [**IXAudio2SourceVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice), [**IXAudio2SubmixVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice) e [**IXAudio2MasteringVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice) são derivados. Os métodos listados abaixo são comuns a todas as subclasses de voz.<br/> |
| [**IXAudio2SourceVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)<br/>       | Use uma voz de origem para enviar dados de áudio para o pipeline de processamento XAudio2.<br/>                                                                                                                                                                                                                                                   |
| [**IXAudio2SubmixVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice)<br/>       | Uma voz submix é usada principalmente para melhorias de desempenho e processamento de efeitos. <br/>                                                                                                                                                                                                                                        |
| [**IXAudio2MasteringVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice)<br/> | Uma voz de mestre é usada para representar o dispositivo de saída de áudio.<br/>                                                                                                                                                                                                                                                               |
| [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback)<br/> | A interface IXAudio2EngineCallback contém métodos que notificam o cliente quando determinados eventos acontecem no mecanismo [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) .<br/>                                                                                                                                                                           |
| [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback)<br/>   | A interface [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) contém métodos que notificam o cliente quando determinados eventos acontecem em um determinado [**IXAudio2SourceVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice). <br/>                                                                                                                       |
| [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo)<br/>                                   | A interface para um objeto de processamento de áudio que é usado em uma cadeia de efeito de XAudio2.<br/>                                                                                                                                                                                                                                        |
| [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters)<br/>               | Uma interface opcional que permite que um XAPO use parâmetros específicos de efeito.<br/>                                                                                                                                                                                                                                                  |
| [**IXAPOHrtfParameters**](/windows/win32/api/hrtfapoapi/nn-hrtfapoapi-ixapohrtfparameters)<br/>       | A interface usada para definir parâmetros que controlam como a função de transferência relacionada ao cabeçalho (HRTF) é aplicada a um som.<br/>                                                                                                                                                                                                            |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de programação](programming-reference.md)
</dt> <dt>

[Referência de programação](./programming-reference.md)
</dt> </dl>

 

 
