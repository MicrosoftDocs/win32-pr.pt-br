---
title: Objeto Controls
description: O objeto Controls fornece uma maneira de manipular a reprodução de mídia usando as propriedades e os métodos a seguir.
ms.assetid: bcc1e768-4fa6-4c82-a12f-52c9bfb4c10c
keywords:
- Objeto de controles Windows Media Player
topic_type:
- apiref
api_name:
- Controls Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7bac91c522c95c1b45565ca013a000022c73bcc4
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2019
ms.locfileid: "103638718"
---
# <a name="controls-object"></a>Objeto Controls

O objeto **Controls** fornece uma maneira de manipular a reprodução de mídia usando as propriedades e os métodos a seguir.

O objeto **Controls** dá suporte às propriedades a seguir.



| Propriedade                                                            | Descrição                                                                                                                                       |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [audioLanguageCount](controls-audiolanguagecount.md)               | Recupera o número de idiomas de áudio com suporte.                                                                                                |
| [currentAudioLanguage](controls-currentaudiolanguage.md)           | Especifica ou recupera o LCID (identificador de localidade) do idioma de áudio para reprodução                                                            |
| [currentAudioLanguageIndex](controls-currentaudiolanguageindex.md) | Especifica ou recupera o índice com base em um que corresponde ao idioma de áudio para reprodução.                                                   |
| [currentItem](controls-currentitem.md)                             | Especifica ou recupera o item de mídia atual.                                                                                                    |
| [currentMarker](controls-currentmarker.md)                         | Especifica ou recupera o número do marcador atual.                                                                                                 |
| [currentPosition](controls-currentposition.md)                     | Especifica ou recupera a posição atual no item de mídia em segundos desde o início.                                                      |
| [currentPositionString](controls-currentpositionstring.md)         | Recupera a posição atual no item de mídia como uma **cadeia de caracteres**.                                                                                 |
| [currentPositionTimecode](controls-currentpositiontimecode.md)     | Especifica ou recupera a posição atual no item de mídia atual usando um formato de código de tempo. Essa propriedade atualmente dá suporte ao código de tempo SMPTE. |
| [isAvailable](controls-isavailable.md)                             | Recupera se um tipo especificado de informação está disponível ou se uma determinada ação pode ser executada.                                                |



 

O objeto **Controls** dá suporte aos métodos a seguir.



| Método                                                                  | Descrição                                                                                      |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [fastForward](controls-fastforward.md)                                 | Inicia a reprodução rápida do item de mídia na direção de encaminhamento.                                     |
| [fastReverse](controls-fastreverse.md)                                 | Inicia a reprodução rápida do item de mídia na direção inversa.                                     |
| [getAudioLanguageDescription](controls-getaudiolanguagedescription.md) | Recupera a descrição do idioma de áudio correspondente ao índice baseado em um especificado. |
| [getAudioLanguageID](controls-getaudiolanguageid.md)                   | Recupera o LCID para um índice de idioma de áudio especificado.                                         |
| [getLanguageName](controls-getlanguagename.md)                         | Recupera o nome do idioma de áudio com o LCID especificado.                                |
| [avançar](controls-next.md)                                               | Define o item atual para o próximo item na lista de reprodução.                                          |
| [pause](controls-pause.md)                                             | Pausa a reprodução do item de mídia.                                                            |
| [reproduzir](controls-play.md)                                               | Faz com que o item de mídia inicie a reprodução.                                                          |
| [playItem](controls-playitem.md)                                       | Faz com que o item de mídia atual inicie a reprodução ou retome a reprodução de um item pausado.                |
| [Anterior](controls-previous.md)                                       | Define o item atual para o item anterior na lista de reprodução.                                      |
| [etapa](controls-step.md)                                               | Faz com que o item de mídia de vídeo atual congele a reprodução no próximo quadro.                        |
| [stop](controls-stop.md)                                               | Interrompe a reprodução do item de mídia.                                                             |



 

O objeto **Controls** é acessado por meio da propriedade a seguir.



| Objeto                      | Propriedade                        |
|-----------------------------|---------------------------------|
| [Jogador](player-object.md) | [controles](player-controls.md) |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de modelo de objeto para scripts**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




