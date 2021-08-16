---
description: Comandos de DVD
ms.assetid: 1204c73e-c3de-4488-8ee3-e76edbf72da0
title: Comandos de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d02f9c0b6a50b6d7eb67832286ee980b0faf69460621a46caf98089efc24b19c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117820580"
---
# <a name="dvd-commands"></a>Comandos de DVD

Os comandos de navegação e reprodução de DVD são definidos em uma seção da especificação de DVD chamada Anexo J, que é o motivo pelo qual a documentação do DirectShow geralmente se refere a "Comandos anexo J". No entanto, os nomes dados no Anexo J nem sempre são muito intuitivos, portanto, DirectShow usa nomes que podem ser mais fáceis de entender.

A tabela a seguir lista os comandos anexo J e seus DirectShow equivalentes.



| Comando Anexo J                                                                           | Descrição                                                                  | Método IDvdControl2                                                                           |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| Jogo de \_ título                                                                               | Reproduzir um título.                                                                | [**PlayTitle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playtitle)                                                   |
| PTT \_ Play                                                                                 | Reproduza um capítulo em um título.                                                   | [**PlayChapterInTitle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playchapterintitle)                                 |
| Reprodução \_ de tempo                                                                                | Reproduza um título começando em um horário especificado.                                 | [**PlayAtTimeInTitle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playattimeintitle)                                   |
| Stop                                                                                      | Pare a reprodução.                                                               | [**Stop**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stop)                                                             |
| GoUp                                                                                      | Retorne de um submenu para o menu pai.                                    | [**ReturnFromSubmenu**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-returnfromsubmenu)                                   |
| Pesquisa de \_ Tempo                                                                              | Reproduzir em um momento especificado dentro do título atual.                           | [**PlayAtTime**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playattime)                                                 |
| Pesquisa \_ de PTT                                                                               | Reproduza um capítulo dentro do título atual.                                     | [**PlayChapter**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playchapter)                                               |
| Pesquisa de \_ PrevPG                                                                            | Vá para o início do capítulo anterior e retome a reprodução.                 | [**PlayPrevChapter**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playprevchapter)                                       |
| Pesquisa \_ TopPG                                                                             | Vá para o início do capítulo atual e retome a reprodução.                  | [**ReplayChapter**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-replaychapter)                                           |
| Pesquisa \_ nextPG                                                                            | Vá para o início do próximo capítulo e retome a reprodução.                     | [**PlayNextChapter**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playnextchapter)                                       |
| Verificação \_ de encaminhamento                                                                             | Reproduzir em uma taxa de reprodução especificada. A taxa de reprodução padrão é 1,0. | [**PlayForwards**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playforwards)                                             |
| Verificação \_ regressiva                                                                            | Reproduzir para trás em uma taxa de reprodução especificada.                                  | [**PlayBackwards**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playbackwards)                                           |
| Chamada de \_ menu                                                                                | Mostrar um menu.                                                                 | [**ShowMenu**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-showmenu)                                                     |
| Retomar                                                                                    | Retorne de um menu e retome a reprodução.                                      | [**Retomar**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-resume)                                                         |
| Botão \_ Superior \_ Selecionar, Selecionar Botão \_ \_ Inferior, Selecionar Botão \_ \_ Esquerdo, Selecionar Botão Direito \_ \_ Selecione | Selecione um botão cuja posição é relativa ao botão selecionado no momento. | [**SelectButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectbutton)                                             |
| Ativar \_ botão                                                                          | Ative o botão selecionado.                                                | [**ActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activatebutton)                                         |
| Botão \_ Selecionar \_ e \_ Ativar                                                             | Selecione e ative um botão.                                                | [**SelectAndActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectandactivatebutton)                       |
| Ainda \_ desligado                                                                                | Retomar a reprodução ao exibir uma imagem ainda.                               | [**StillOff**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff)                                                     |
| Pausar \_ em                                                                                 | Pausar a reprodução.                                                              | [**Pausar**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-pause)                                                           |
| \_Pausar                                                                                | Retomar a reprodução do estado em pausa.                                       | [**Pausar**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-pause)                                                           |
| Selecionar \_ Idioma do \_ Menu                                                                    | Selecione o idioma dos menus.                                               | [**SelectDefaultMenuLanguage**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectdefaultmenulanguage)                   |
| Alteração \_ de fluxo de \_ áudio                                                                     | Definir o fluxo de áudio.                                                        | [**SelectAudioStream**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectaudiostream)                                   |
| Alteração de fluxo de \_ \_ sub-imagem                                                               | Definir o fluxo de subspícone; habilitar ou desabilitar a exibição de subtípico.             | [**SelectSubpictureStream**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectsubpicturestream)                         |
| Alteração de \_ ângulo                                                                             | Definir o ângulo da câmera.                                                        | [**SelectAngle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectangle)                                               |
| Seleção \_ de nível dos \_ pais                                                                   | Definir o nível dos pais.                                                      | [**SelectParentalLevel**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectparentallevel)                               |
| Seleção \_ de país dos \_ pais                                                                 | Definir o país/região para gerenciamento dos pais.                              | [**SelectParentalCountry**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectparentalcountry)                           |
| Alteração no \_ modo de apresentação de áudio Dem. \_ \_ \_                                                | De definir o modo de combinação de áudio para o set.                                       | [**SelectOxokeAudioPresentationMode**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectkaraokeaudiopresentationmode) |
| Alteração \_ no modo de apresentação de \_ \_ vídeo                                                         | De definir o modo de proporção como widescreen, letterbox ou pan scan.             | [**SelectVideoModePreference**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectvideomodepreference)                   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aplicativos de DVD](dvd-applications.md)
</dt> </dl>

 

 



