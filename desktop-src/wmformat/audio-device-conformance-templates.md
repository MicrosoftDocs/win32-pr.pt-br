---
title: Modelos de conformidade do dispositivo de áudio
description: Modelos de conformidade do dispositivo de áudio
ms.assetid: dad3dd2c-595e-45ce-bd84-2a20bc656cfb
keywords:
- Windows SDK de Formato de Mídia, modelos de conformidade do dispositivo
- ASF (Advanced Systems Format), modelos de conformidade do dispositivo
- ASF (Formato de Sistemas Avançados), modelos de conformidade do dispositivo
- Windows SDK de Formato de Mídia, modelos de conformidade do dispositivo de áudio
- ASF (Advanced Systems Format), modelos de conformidade do dispositivo de áudio
- ASF (Formato de Sistemas Avançados), modelos de conformidade do dispositivo de áudio
- Windows Codec de Áudio de Mídia 9, modelos de conformidade do dispositivo de áudio
- codecs,Windows Media Audio 9 codec
- modelos de conformidade do dispositivo, vídeo
- modelos de conformidade do dispositivo de áudio
- modelos, modelos de conformidade do dispositivo de áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b66c3c414ef2132120cb0824e1e48847310396cf8002d95be13d7f841a0ff6db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119840246"
---
# <a name="audio-device-conformance-templates"></a>Modelos de conformidade do dispositivo de áudio

A tabela a seguir lista os modelos de conformidade do dispositivo e os parâmetros associados para o codec Windows Media Audio 9 ou posterior.



| Cadeia de caracteres de modelo | Intervalo de taxa de bits     | Observações                                                                                                                                                                                                                                |
|-----------------|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "L1"            | 64 Kbps 160 Kbps | Esse modelo destina-se a dispositivos restritos somente áudio.                                                                                                                                                                        |
| "L2"            | <= 160 Kbps     | Esse modelo corresponde à Classe 4 no kit Windows Decodificador de Áudio de Mídia, que dá suporte a toda Windows decodificador de áudio de mídia.                                                                                   |
| "L3"            | <= 384 Kbps     | Esse modelo corresponde à Classe 4 no kit Windows de portação de áudio de mídia, que dá suporte a toda a implementação Windows decodificador de áudio de mídia. O intervalo de taxa de bits é a única diferença entre esse modelo e l2.<br/> |
| "L"             | Todas as taxas de bits      | Esse modelo é para uso somente com computadores pessoais e geralmente é usado para demonstrar os recursos completos do codec.                                                                                                           |



 

A tabela a seguir lista os modelos de conformidade do dispositivo e os parâmetros associados para o codec Windows Media Audio 9 Voice.



| Cadeia de caracteres de modelo | Intervalo de taxa de bits | Observações                                                                                                                      |
|-----------------|----------------|----------------------------------------------------------------------------------------------------------------------------|
| "S1"            | <= 20 Kbps  | Esse modelo destina-se apenas a dispositivos de baixa complexidade. Esse modelo é somente fala.<br/>                    |
| "S2"            | <= 20 Kbps  | Esse é o modelo recomendado para a maioria dos aplicativos. Esse modelo dá suporte a combinações de fala e música.<br/> |



 

A tabela a seguir lista os modelos de conformidade do dispositivo e os parâmetros associados para o Windows Media Audio 9 Professional codec ou posterior.



| Cadeia de caracteres de modelo | Propriedades                                                                                   | Observações                                                                                                                                                                                                                                           |
|-----------------|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "M1"            | Taxa de bits <= 384 KbpsSampling rate <= 48 kHz<br/> Canais <= 5,1<br/>   | Esse modelo é recomendado para filmes padrão com som surround.                                                                                                                                                                           |
| "M2"            | Taxa de bits <= 768 KbpsSampling rate <= 96 kHz<br/> Canais <= 5,1<br/>   | Esse modelo é recomendado para filmes de alta definição com som surround.                                                                                                                                                                    |
| "M3"            | Taxa de bits <= 1.500 KbpsSampling rate <= 96 kHz<br/> Canais <= 7.1<br/> | Esse modelo é recomendado para filmes de alta definição com som surround de 8 canais, como conteúdo codificado para apresentação em canais.                                                                                                    |
| “M”             | Todas as taxas de bitsTodas as taxas de amostragem<br/> Todos os canais<br/>                           | Esse modelo é para uso somente com computadores pessoais e geralmente é usado para demonstrar os recursos completos do codec. Essa também é a designação de modelo para todos os áudios codificados com o codec Windows Media Audio 9 Lossless.<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Parâmetros do modelo de conformidade do dispositivo**](device-conformance-template-parameters.md)
</dt> <dt>

[**Combinações de modelo de conformidade de dispositivo recomendadas**](recommended-device-conformance-template-combinations.md)
</dt> <dt>

[**Modelos de conformidade do dispositivo de vídeo**](video-device-conformance-templates.md)
</dt> </dl>

 

 





