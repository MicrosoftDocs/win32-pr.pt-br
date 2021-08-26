---
title: Windows Estruturas do SDK de formato de mídia
description: Windows Estruturas do SDK de formato de mídia
ms.assetid: 118ef278-ca4f-4c30-9633-a2d851f5c758
keywords:
- Windows SDK de Formato de Mídia, estruturas
- ASF (Advanced Systems Format), structures
- ASF (Formato de Sistemas Avançados), estruturas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 319be2d061132f59c1c75ebb295c8ceb8ae87ffbcce48e8259a1faedcf18d666
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006606"
---
# <a name="windows-media-format-sdk-structures"></a>Windows Estruturas do SDK de formato de mídia

O Windows SDK de Formato de Mídia implementa as estruturas a seguir.



| Estrutura                                                                                | Descrição                                                                                                                                                               |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DRM \_ COPY \_ OPL**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_copy_opl)                                                   | Contém informações de nível de proteção de saída que se aplica à ação de cópia em uma licença drm.                                                                               |
| [**DADOS DE ESTADO \_ DE \_ LICENÇA DRM \_**](drm-license-state-data.md)                              | Contém [*informações*](wmformat-glossary.md) de licença sobre um direito [*DRM*](wmformat-glossary.md) especificado. |
| [**NÍVEIS \_ MÍNIMOS DE \_ PROTEÇÃO \_ DE SAÍDA DRM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_minimum_output_protection_levels) | Contém os níveis mínimos de proteção de saída exigidos por uma licença drm para reproduzir conteúdo em vários formatos.                                                                      |
| [**\_IDS DE SAÍDA OPL \_ \_ DRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_opl_output_ids)                                      | Contém uma matriz de identificadores de tecnologia DRM. Essa estrutura é usada para definir grupos de tecnologias em outras estruturas DRM.                                            |
| [**DRM \_ PLAY \_ OPL**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_play_opl)                                                   | Contém informações de nível de proteção de saída que se aplica à ação de reprodução em uma licença drm.                                                                               |
| [**ID DO CONTEÚDO \_ DA PLAYLIST \_ DO DRM \_**](drm-playlist-content-id.md)                            | Contém informações sobre o conteúdo que deve ser copiado para CD como parte de uma gravação de playlist.                                                                                 |
| [**DRM \_ VAL16**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-drm_val16)                                                          | Armazena um valor de 128 bits usado como um identificador de dispositivo.                                                                                                                       |
| [**PROTEÇÃO DE SAÍDA \_ \_ DE VÍDEO DRM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_output_protection)                    | Contém o identificador de uma tecnologia de proteção de vídeo e os dados de configuração exigidos por essa tecnologia.                                                             |
| [**\_ \_ IDS DE PROTEÇÃO DE SAÍDA DE VÍDEO \_ \_ DRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_video_output_protection_ids)           | Contém uma matriz de estruturas **DE PROTEÇÃO DE SAÍDA DE VÍDEO \_ \_ \_ DRM.**                                                                                                          |
| [**Waveformatex**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85))                                                | Define o formato de dados waveform-audio.                                                                                                                                |
| [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85))                                | Define o formato de dados waveform-audio para formatos com mais de dois canais.                                                                                      |
| [**WM \_ ADDRESS \_ ACCESSENTRY**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_address_accessentry)                               | Especifica uma entrada em uma lista de acesso de endereço IP.                                                                                                                          |
| [**PROPRIEDADES \_ DO CLIENTE \_ WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_client_properties)                                   | Registra informações sobre o cliente.                                                                                                                                     |
| [**PROPRIEDADES DO CLIENTE WM \_ \_ \_ EX**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_client_properties_ex)                            | Registra informações estendidas sobre o cliente.                                                                                                                            |
| [**OBTER \_ DADOS DE \_ LICENÇA DO WM \_**](wm-get-license-data.md)                                    | Contém informações sobre uma licença drm.                                                                                                                                 |
| [**WM \_ INDIVIDUALIZE \_ STATUS**](wm-individualize-status.md)                             | Registra o status do processo [*de individualização.*](wmformat-glossary.md)                                                                |
| [**PAR \_ DE BUCKETS \_ DE VAZAMENTO DE \_ WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_leaky_bucket_pair)                                  | Descreve os requisitos de buffer para um arquivo VBR (taxa de bits variável).                                                                                                  |
| [**DADOS \_ DE ESTADO DE LICENÇA \_ \_ WM**](/previous-versions/windows/desktop/legacy/dd757942(v=vs.85))                                | Encapsula uma estrutura [**DE DADOS DE ESTADO DE LICENÇA \_ \_ \_ DRM**](drm-license-state-data.md) que descreve os dados de estado da licença drm.                                              |
| [**TIPO \_ DE MÍDIA \_ WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type)                                                 | Descreve um exemplo de mídia.                                                                                                                                                 |
| [**WMMPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmmpeg2videoinfo)                                             | Descreve um fluxo de vídeo MPEG-2.                                                                                                                                         |
| [**WM \_ PICTURE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture)                                                        | Contém os dados para o atributo [**de metadados complexos WM/Picture.**](wmpicture.md)                                                                                     |
| [**INTERVALO \_ DE NÚMERO DA PORTA \_ \_ WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_port_number_range)                                  | Descreve o intervalo de números de porta usados pela interface **IWMReaderNetworkConfig.**                                                                                     |
| [**WM \_ READER \_ CLIENTINFO**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_clientinfo)                                   | Descreve o leitor de cliente (player) que acessa o fluxo de mídia.                                                                                                          |
| [**ESTATÍSTICAS \_ DE LEITOR DE WM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_statistics)                                   | Descreve o desempenho de uma operação de leitura.                                                                                                                         |
| [**WMSCRIPTFORMAT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmscriptformat)                                                 | Define o formato de um fluxo de script.                                                                                                                                    |
| [**REGISTRO DE \_ \_ PRIORIDADE DE FLUXO \_ WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_priority_record)                        | Contém um número de fluxo e especifica se a entrega desse fluxo é obrigatória.                                                                                      |
| [**INFORMAÇÕES DE \_ TIPO \_ DE FLUXO \_ WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_type_info)                                    | Contém os dados para o [**atributo de metadados complexo WM/StreamTypeInfo.**](wm-streamtypeinfo.md)                                                                      |
| [**WM \_ SYNCHRONED \_ DESINCRONIZADO**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_synchronised_lyrics)                               | Contém os dados para o [**atributo de \_ metadados complexos sincronizados wm/synchronizado.**](wm-lyrics-synchronised.md)                                                           |
| [**TEXTO \_ DO USUÁRIO \_ WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_user_text)                                                   | Contém os dados para o atributo de metadados complexos [**WM/Text.**](wm-text.md)                                                                                          |
| [**\_URL DA WEB DO USUÁRIO \_ \_ DO WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_user_web_url)                                            | Contém os dados para o atributo de metadados complexo [**WM/UserWebURL.**](wm-userweburl.md)                                                                              |
| [**ESTATÍSTICAS \_ DO WM WRITER \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics)                                   | Descreve o desempenho de uma operação de escrita.                                                                                                                         |
| [**WM \_ WRITER \_ STATISTICS \_ EX**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics_ex)                            | Contém estatísticas estendidas do autor.                                                                                                                                      |
| [**CHAVE DE CONTEÚDO \_ DE \_ IMPORTAÇÃO DO WMDRM \_**](wmdrm-import-content-key.md)                          | Contém a chave de conteúdo usada na importação de conteúdo protegido.                                                                                                                |
| [**\_STRUCT DO WMDRM IMPORT \_ \_ INIT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct)                          | Contém a chave de sessão criptografada e a chave de conteúdo usadas na importação de conteúdo protegido.                                                                                      |
| [**CHAVE DE SESSÃO \_ DE \_ IMPORTAÇÃO DO WMDRM \_**](wmdrm-import-session-key.md)                          | Contém a chave de sessão para importar conteúdo protegido.                                                                                                                    |
| [**SEGMENTO DE BUFFER WMT \_ \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_buffer_segment)                                       | Contém as informações necessárias para especificar um segmento em um pacote.                                                                                                      |
| [**DADOS DE EXTENSÃO DO WMT \_ \_ \_ COLORSPACEINFO**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_colorspaceinfo_extension_data)        | Contém os dados para a extensão de unidade de \_ dados ColorSpaceInfo do WM SampleExtensionGUID. \_                                                                                    |
| [**UNIDADE DE DADOS \_ WMT FILESINK \_ \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_filesink_data_unit)                              | Contém informações sobre um pacote.                                                                                                                                      |
| [**FRAGMENTO DE CARGA DO WMT \_ \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_payload_fragment)                                   | Contém as informações necessárias para extrair um fragmento de conteúdo de um pacote.                                                                                           |
| [**DADOS DE \_ EXTENSÃO DO WMT TIMECODE \_ \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data)                    | Contém um único código de hora SMPTE e informações relacionadas.                                                                                                                |
| [**EXEMPLO DE \_ VÍDEOIMAGE DO WMT \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample)                                 | Contém informações sobre um exemplo de Imagem de Vídeo.                                                                                                                          |
| [**ENTRADA DE \_ MARCA D'ÁGUA \_ WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_watermark_entry)                                     | Contém informações sobre um sistema de marca-d'água.                                                                                                                         |
| [**FORMATO WMT \_ \_ WEBSTREAM**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_format)                                   | Contém informações sobre um fluxo da Web.                                                                                                                                  |
| [**HEADER DE EXEMPLO DO WMT \_ WEBSTREAM \_ \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_sample_header)                    | Contém informações de header para exemplos de fluxo da Web.                                                                                                                       |
| [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader)                                           | Descreve o bitmap e as informações de cor de uma imagem de vídeo.                                                                                                             |
| [**WMVIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader2)                                         | Descreve as informações de bitmap e cor de uma imagem de vídeo, incluindo [*entrelaçamento*](wmformat-glossary.md), proteção de cópia e taxa de proporção.       |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de programação**](programming-reference.md)
</dt> </dl>

 

 
