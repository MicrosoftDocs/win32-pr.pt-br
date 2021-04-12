---
title: Modelos de conformidade do dispositivo de áudio
description: Modelos de conformidade do dispositivo de áudio
ms.assetid: dad3dd2c-595e-45ce-bd84-2a20bc656cfb
keywords:
- SDK do Windows Media Format, modelos de conformidade do dispositivo
- ASF (Advanced Systems Format), modelos de conformidade do dispositivo
- ASF (formato de sistemas avançados), modelos de conformidade do dispositivo
- SDK do Windows Media Format, modelos de conformidade do dispositivo de áudio
- ASF (Advanced Systems Format), modelos de conformidade de dispositivo de áudio
- ASF (formato de sistemas avançados), modelos de conformidade de dispositivo de áudio
- Codec do Windows Media Audio 9, modelos de conformidade do dispositivo de áudio
- codecs, codec do Windows Media Audio 9
- modelos de conformidade do dispositivo, vídeo
- modelos de conformidade do dispositivo de áudio
- modelos, modelos de conformidade do dispositivo de áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39e1065395e64fdd2d8e60585900307a4dd3f39b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292163"
---
# <a name="audio-device-conformance-templates"></a>Modelos de conformidade do dispositivo de áudio

A tabela a seguir lista os modelos de conformidade do dispositivo e os parâmetros associados para o codec do Windows Media Audio 9 ou posterior.



| Cadeia de caracteres do modelo | Intervalo de taxa de bits     | Observações                                                                                                                                                                                                                                |
|-----------------|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| L1            | 64 Kbps 160 kbps | Este modelo destina-se a dispositivos com somente áudio restrito.                                                                                                                                                                        |
| Cache            | <= 160 kbps     | Este modelo corresponde à classe 4 no kit de portabilidade de áudio do Windows Media, que dá suporte a toda a implementação do decodificador de áudio do Windows Media.                                                                                   |
| MB            | <= 384 kbps     | Este modelo corresponde à classe 4 no kit de portabilidade de áudio do Windows Media, que dá suporte a toda a implementação do decodificador de áudio do Windows Media. O intervalo de taxa de bits é a única diferença entre este modelo e o L2.<br/> |
| Debug             | Todas as taxas de bits      | Este modelo é para uso apenas com computadores pessoais e é geralmente usado para demonstrar os recursos completos do codec.                                                                                                           |



 

A tabela a seguir lista os modelos de conformidade do dispositivo e os parâmetros associados para o codec de voz do Windows Media Audio 9.



| Cadeia de caracteres do modelo | Intervalo de taxa de bits | Observações                                                                                                                      |
|-----------------|----------------|----------------------------------------------------------------------------------------------------------------------------|
| S1            | <= 20 kbps  | Este modelo destina-se apenas a dispositivos de baixa complexidade. Este modelo é somente fala.<br/>                    |
| S2            | <= 20 kbps  | Esse é o modelo recomendado para a maioria dos aplicativos. Este modelo dá suporte a combinações de fala e música.<br/> |



 

A tabela a seguir lista os modelos de conformidade do dispositivo e os parâmetros associados para o codec do Windows Media Audio 9 Professional ou posterior.



| Cadeia de caracteres do modelo | Propriedades                                                                                   | Observações                                                                                                                                                                                                                                           |
|-----------------|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| M1            | Taxa de bits <= 384 taxa de KbpsSampling <= 48 kHz<br/> Canais <= 5,1<br/>   | Esse modelo é recomendado para filmes padrão com Surround Sound.                                                                                                                                                                           |
| M2            | Taxa de bits <= 768 taxa de KbpsSampling <= 96 kHz<br/> Canais <= 5,1<br/>   | Esse modelo é recomendado para filmes de alta definição com som surround.                                                                                                                                                                    |
| M3            | Taxa de bits <= 1.500 taxa de KbpsSampling <= 96 kHz<br/> Canais <= 7,1<br/> | Este modelo é recomendado para filmes de alta definição com som surround de 8 canais, como conteúdo codificado para apresentação em teatros.                                                                                                    |
| “M”             | Todas as taxas de amostragem de ratesAll de bits<br/> Todos os canais<br/>                           | Este modelo é para uso apenas com computadores pessoais e é geralmente usado para demonstrar os recursos completos do codec. Essa também é a designação de modelo para todos os áudios codificados com o codec Windows Media Audio 9 Lossless.<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Parâmetros do modelo de conformidade do dispositivo**](device-conformance-template-parameters.md)
</dt> <dt>

[**Combinações de modelo de conformidade do dispositivo recomendado**](recommended-device-conformance-template-combinations.md)
</dt> <dt>

[**Modelos de conformidade de dispositivo de vídeo**](video-device-conformance-templates.md)
</dt> </dl>

 

 





