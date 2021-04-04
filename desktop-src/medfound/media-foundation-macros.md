---
description: Media Foundation macros
ms.assetid: c460b1cd-13d7-4b65-a755-23b2ea87864d
title: Media Foundation macros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bed83710f41957edc1b945fecd5d68b5550b4ed
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103930100"
---
# <a name="media-foundation-macros"></a>Media Foundation macros

## <a name="in-this-section"></a>Nesta seção



| Atributo                                                                                              | Descrição                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DEFINIR \_ o \_ GUID de MediaType**](/windows/desktop/api/mfapi/nf-mfapi-define_mediatype_guid)<br/>                              | Define um GUID de subtipo de mídia de um código FOURCC, um valor **D3DFORMAT** ou um tipo de formato de áudio.<br/>                                                                       |
| [**MFP \_ obter \_ \_ evento de \_ credencial do usuário \_ de obtenção**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_acquire_user_credential_event)<br/> | Converte um ponteiro [**de \_ \_ cabeçalho de evento de MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) em um ponteiro de [**\_ \_ \_ \_ evento de credencial de usuário de aquisição de MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_acquire_user_credential_event) .<br/> |
| [**\_evento de obtenção de \_ erro do MFP \_**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_error_event)<br/>                                       | Converte um ponteiro [**de \_ \_ cabeçalho de evento de MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) em um ponteiro de [**\_ \_ evento de erro da MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_error_event) .<br/>                                       |
| [**MFP \_ obter \_ o \_ evento de etapa de quadro \_**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_frame_step_event)<br/>                            | Converte um ponteiro [**de \_ \_ cabeçalho de evento de MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) em um ponteiro de [**\_ \_ \_ evento de etapa de quadro de MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_frame_step_event) .<br/>                            |
| [**MFP \_ obter \_ \_ evento MEDIAITEM limpo \_**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_mediaitem_cleared_event)<br/>              | Converte um ponteiro [**de \_ \_ cabeçalho de evento de MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) em um ponteiro de [**\_ \_ evento MEDIAITEM limpo**](/windows/desktop/api/mfplay/ns-mfplay-mfp_mediaitem_cleared_event) .<br/>                   |
| [**MFP \_ obter \_ \_ evento MEDIAITEM criado \_**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_mediaitem_created_event)<br/>              | Converte um ponteiro [**de \_ \_ cabeçalho de evento de MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) em um ponteiro de [**\_ \_ \_ evento de MEDIAITEM de MFP criado**](/windows/desktop/api/mfplay/ns-mfplay-mfp_mediaitem_created_event) .<br/>              |
| [**MFP \_ Get \_ MEDIAITEM \_ definir \_ evento**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_mediaitem_set_event)<br/>                      | Converte um ponteiro [**de \_ \_ cabeçalho de evento de MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) em um ponteiro de [**\_ \_ \_ evento MEDIAITEM de MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_mediaitem_set_event) .<br/>                      |
| [**\_evento de obtenção de \_ MF do MFP \_**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_mf_event)<br/>                                             | Converte um ponteiro [**de \_ \_ cabeçalho de evento de MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) em um ponteiro de [**\_ \_ evento da MFP MF**](/windows/win32/api/mfplay/ns-mfplay-mfp_mf_event) .<br/>                                              |
| [**\_evento de obtenção de \_ pausa do MFP \_**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_pause_event)<br/>                                       | Converte um ponteiro [**de \_ \_ cabeçalho de evento de MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) em um ponteiro de [**\_ \_ evento de pausa de MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_pause_event) .<br/>                                       |
| [**\_evento de get \_ Play \_ da MFP**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_play_event)<br/>                                         | Converte um ponteiro [**de \_ \_ cabeçalho de evento de MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) em um ponteiro de [**\_ \_ evento de reprodução de MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_play_event) .<br/>                                         |
| [**evento de obtenção de reprodução de MFP \_ \_ \_ finalizado \_**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_playback_ended_event)<br/>                    | Converte um ponteiro [**de \_ \_ cabeçalho de evento de MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) em um ponteiro de [**evento de reprodução de MFP \_ \_ encerrado \_**](/windows/desktop/api/mfplay/ns-mfplay-mfp_playback_ended_event) .<br/>                    |
| [**\_evento de obtenção de \_ posição do \_ MFP \_**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_position_set_event)<br/>                        | Converte um ponteiro [**de \_ \_ cabeçalho de evento de MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) em um ponteiro de [**\_ \_ \_ evento de definição de posição de MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_position_set_event) .<br/>                        |
| [**\_evento de \_ conjunto de taxa de obtenção de MFP \_ \_**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_rate_set_event)<br/>                                | Converte um ponteiro [**de \_ \_ cabeçalho de evento de MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) em um ponteiro de [**\_ \_ \_ evento de conjunto de taxa de MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_rate_set_event) .<br/>                                |
| [**\_evento de get \_ Stop \_ da MFP**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_stop_event)<br/>                                         | Converte um ponteiro [**de \_ \_ cabeçalho de evento de MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) em um ponteiro de [**\_ \_ evento de parada de MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_stop_event) .<br/>                                         |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de programação do Media Foundation](media-foundation-programming-reference.md)
</dt> </dl>

 

 
