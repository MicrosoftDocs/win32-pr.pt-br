---
title: Elemento EQUALIZERSETTINGS
description: Elemento EQUALIZERSETTINGS
ms.assetid: 521f1c95-7904-4085-a8bc-5399d667dfb1
keywords:
- Capas do Windows Media Player, elemento EQUALIZERSETTINGS
- Skins, elemento EQUALIZERSETTINGS
- Elemento EQUALIZERSETTINGS
- referência para capas, elemento EQUALIZERSETTINGS
- elementos, EQUALIZERSETTINGS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae20500dfba656450c3102ee80b4a06e089fe8ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498708"
---
# <a name="equalizersettings-element"></a>Elemento EQUALIZERSETTINGS

O elemento **EQUALIZERSETTINGS** fornece uma maneira de manipular o equalizador gráfico e outras configurações de áudio do Windows Media Player usando os atributos e o método listados aqui.

O elemento **EQUALIZERSETTINGS** dá suporte aos seguintes atributos.



| Atributo                                                          | Descrição                                                                                             |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [bandas](equalizersettings-bands.md)                               | Recupera o número de faixas de frequência com suporte.                                                      |
| [pular](equalizersettings-bypass.md)                             | Especifica ou recupera um valor que indica se o filtro de equalizador é ignorado no gráfico de filtro. |
| [Fading cruzado](equalizersettings-crossfade.md)                       | Especifica ou recupera um valor que indica se o esmaecimento cruzado está habilitado.                                |
| [crossFadeWindow](equalizersettings-crossfadewindow.md)           | Especifica ou recupera a quantidade de sobreposição de esmaecimento cruzado em milissegundos.                                |
| [currentPreset](equalizersettings-currentpreset.md)               | Especifica ou recupera o índice da predefinição atual.                                                 |
| [currentPresetTitle](equalizersettings-currentpresettitle.md)     | Recupera o título da predefinição atual.                                                              |
| [currentSpeakerName](equalizersettings-currentspeakername.md)     | Recupera o nome da configuração do alto-falante atual.                                                      |
| [enableSplineTension](equalizersettings-enablesplinetension.md)   | Especifica ou recupera um valor que indica se a tensão de spline está habilitada ou desabilitada.                |
| [enhancedAudio](equalizersettings-enhancedaudio.md)               | Especifica ou recupera um valor que indica se o áudio avançado está ativado.                          |
| [gainLevels](equalizersettings-gainlevels.md)                     | Especifica ou recupera o nível de lucro da faixa correspondente ao índice fornecido.                  |
| [gainLevel1](equalizersettings-gainlevel1.md)                     | Especifica ou recupera o nível de lucro da faixa 1.                                                        |
| [gainLevel2](equalizersettings-gainlevel2.md)                     | Especifica ou recupera o nível de lucro da faixa 2.                                                        |
| [gainLevel3](equalizersettings-gainlevel3.md)                     | Especifica ou recupera o nível de lucro da faixa 3.                                                        |
| [gainLevel4](equalizersettings-gainlevel4.md)                     | Especifica ou recupera o nível de lucro da faixa 4.                                                        |
| [gainLevel5](equalizersettings-gainlevel5.md)                     | Especifica ou recupera o nível de lucro da banda 5.                                                        |
| [gainLevel6](equalizersettings-gainlevel6.md)                     | Especifica ou recupera o nível de lucro da faixa 6.                                                        |
| [gainLevel7](equalizersettings-gainlevel7.md)                     | Especifica ou recupera o nível de lucro da banda 7.                                                        |
| [gainLevel8](equalizersettings-gainlevel8.md)                     | Especifica ou recupera o nível de lucro da banda 8.                                                        |
| [gainLevel9](equalizersettings-gainlevel9.md)                     | Especifica ou recupera o nível de lucro da banda 9.                                                        |
| [gainLevel10](equalizersettings-gainlevel10.md)                   | Especifica ou recupera o nível de lucro da faixa 10.                                                       |
| [normalização](equalizersettings-normalization.md)               | Especifica ou recupera um valor que indica se a normalização está habilitada.                             |
| [normalizationAverage](equalizersettings-normalizationaverage.md) | Recupera o valor de normalização média.                                                              |
| [normalizationPeak](equalizersettings-normalizationpeak.md)       | Recupera o valor de normalização de pico.                                                                 |
| [presetCount](equalizersettings-presetcount.md)                   | Recupera o número de predefinições disponíveis.                                                              |
| [Alto-falante](equalizersettings-speakersize.md)                   | Especifica ou recupera o índice do tamanho atual do alto-falante.                                           |
| [splineTension](equalizersettings-splinetension.md)               | Especifica ou recupera a tensão de spline para o controle equalizador.                                    |
| [truBassLevel](equalizersettings-trubasslevel.md)                 | Especifica ou recupera o nível de TruBass do SRS.                                                           |
| [wowLevel](equalizersettings-wowlevel.md)                         | Especifica ou recupera o nível de efeito de WOW do SRS.                                                        |



 

O elemento **EQUALIZERSETTINGS** dá suporte aos métodos a seguir.



| Método                                                 | Descrição                                                          |
|--------------------------------------------------------|----------------------------------------------------------------------|
| [nextPreset](equalizersettings-nextpreset.md)         | Aplica a próxima predefinição de equalizador.                                   |
| [presetTitle](equalizersettings-presettitle.md)       | Recupera o nome da predefinição do equalizador com o índice especificado. |
| [previousPreset](equalizersettings-previouspreset.md) | Aplica a predefinição anterior do equalizador.                               |
| [reset](equalizersettings-reset.md)                   | Redefine os níveis de lucro de todas as faixas para zero decibéis.                |



 

O elemento **EQUALIZERSETTINGS** pode implementar o [atributo \_ onChange](attribute-onchange.md) manipuladores de eventos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de programação de capa**](skin-programming-reference.md)
</dt> </dl>

 

 




