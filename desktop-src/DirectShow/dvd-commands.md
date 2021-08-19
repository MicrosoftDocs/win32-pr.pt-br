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

os comandos de navegação e reprodução de dvd são definidos em uma seção da especificação de dvd chamada anexo J, que é o motivo pelo qual a documentação de DirectShow geralmente se refere aos "comandos do anexo j". no entanto, os nomes fornecidos no anexo J nem sempre são muito intuitivos, portanto DirectShow usa nomes que podem ser mais fáceis de entender.

a tabela a seguir lista os comandos do anexo J e seus equivalentes DirectShow.



| Comando anexo J                                                                           | Descrição                                                                  | Método IDvdControl2                                                                           |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| Título de \_ jogo                                                                               | Reproduza um título.                                                                | [**PlayTitle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playtitle)                                                   |
| PTT \_ Play                                                                                 | Jogue um capítulo em um título.                                                   | [**PlayChapterInTitle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playchapterintitle)                                 |
| Tempo de \_ reprodução                                                                                | Reproduzir um título começando a partir de uma hora especificada.                                 | [**PlayAtTimeInTitle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playattimeintitle)                                   |
| Stop                                                                                      | Pare a reprodução.                                                               | [**Stop**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stop)                                                             |
| Grupo                                                                                      | Retornar de um submenu para o menu pai.                                    | [**ReturnFromSubmenu**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-returnfromsubmenu)                                   |
| Pesquisa de tempo \_                                                                              | Reproduzir em um horário especificado dentro do título atual.                           | [**PlayAtTime**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playattime)                                                 |
| Pesquisa do PTT \_                                                                               | Jogue um capítulo dentro do título atual.                                     | [**PlayChapter**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playchapter)                                               |
| Pesquisa do PrevPG \_                                                                            | Vá até o início do capítulo anterior e retome a reprodução.                 | [**PlayPrevChapter**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playprevchapter)                                       |
| Pesquisa do TopPG \_                                                                             | Vá para o início do capítulo atual e retome a reprodução.                  | [**ReplayChapter**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-replaychapter)                                           |
| Pesquisa do NextPG \_                                                                            | Vá para o início do próximo capítulo e retome a reprodução.                     | [**PlayNextChapter**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playnextchapter)                                       |
| Encaminhar \_ verificação                                                                             | Reproduzir em uma taxa de reprodução especificada. A taxa de reprodução padrão é 1,0. | [**PlayForwards**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playforwards)                                             |
| \_Verificação retroativa                                                                            | Reproduzir para trás com uma taxa de reprodução especificada.                                  | [**PlayBackwards**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playbackwards)                                           |
| Chamada de menu \_                                                                                | Mostrar um menu.                                                                 | [**Menu de tudo**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-showmenu)                                                     |
| Retomar                                                                                    | Retornar de um menu e retomar a reprodução.                                      | [**Retomar**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-resume)                                                         |
| \_ \_ Seleção do botão superior, \_ seleção do botão inferior, seleção \_ \_ do botão esquerdo \_ , \_ seleção do botão direito \_ | Selecione um botão cuja posição seja relativa ao botão atualmente selecionado. | [**SelectButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectbutton)                                             |
| Botão \_ Ativar                                                                          | Ativar o botão selecionado.                                                | [**ActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activatebutton)                                         |
| Botão \_ selecionar \_ e \_ Ativar                                                             | Selecione e ative um botão.                                                | [**SelectAndActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectandactivatebutton)                       |
| Ainda \_ desativado                                                                                | Retome a reprodução ao exibir uma imagem ainda.                               | [**StillOff**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff)                                                     |
| Pausar \_ em                                                                                 | Pausar reprodução.                                                              | [**Pausar**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-pause)                                                           |
| Pausar \_                                                                                | Retome a reprodução do estado em pausa.                                       | [**Pausar**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-pause)                                                           |
| \_Seleção de idioma do menu \_                                                                    | Selecione o idioma para os menus.                                               | [**SelectDefaultMenuLanguage**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectdefaultmenulanguage)                   |
| \_Alteração de fluxo de áudio \_                                                                     | Defina o fluxo de áudio.                                                        | [**SelectAudioStream**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectaudiostream)                                   |
| Alteração de fluxo de subimagem \_ \_                                                               | Definir o fluxo de subimagem; habilitar ou desabilitar a exibição da subimagem.             | [**SelectSubpictureStream**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectsubpicturestream)                         |
| Alteração de ângulo \_                                                                             | Defina o ângulo da câmera.                                                        | [**SelectAngle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectangle)                                               |
| Seleção de \_ nível \_ pai                                                                   | Defina o nível do pai.                                                      | [**SelectParentalLevel**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectparentallevel)                               |
| Seleção de \_ país \_ pai                                                                 | Defina o país/região para o gerenciamento de pais.                              | [**SelectParentalCountry**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectparentalcountry)                           |
| \_Alteração do \_ modo de apresentação de áudio do karaokê \_ \_                                                | Defina o modo de mixagem de áudio para o karaokê.                                       | [**SelectKaraokeAudioPresentationMode**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectkaraokeaudiopresentationmode) |
| \_Mudança no \_ modo de apresentação de vídeo \_                                                         | Defina o modo de taxa de proporção como widescreen, Letterbox ou digitalização de panorâmica.             | [**SelectVideoModePreference**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectvideomodepreference)                   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aplicativos de DVD](dvd-applications.md)
</dt> </dl>

 

 



