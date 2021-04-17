---
title: Estruturas do Windows Media Format SDK
description: Estruturas do Windows Media Format SDK
ms.assetid: 118ef278-ca4f-4c30-9633-a2d851f5c758
keywords:
- SDK do Windows Media Format, estruturas
- ASF (Advanced Systems Format), estruturas
- ASF (formato de sistemas avançados), estruturas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f730ba3cbc5bd8bbec2a9f01c72df1fe46f0b64
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105763240"
---
# <a name="windows-media-format-sdk-structures"></a>Estruturas do Windows Media Format SDK

O SDK do Windows Media Format implementa as seguintes estruturas.



| Estrutura                                                                                | Descrição                                                                                                                                                               |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_OPL de cópia DRM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_copy_opl)                                                   | Mantém as informações de nível de proteção de saída que se aplicam à ação de cópia em uma licença DRM.                                                                               |
| [**\_dados de \_ estado da licença DRM \_**](drm-license-state-data.md)                              | Contém informações de [*licença*](wmformat-glossary.md) sobre um direito de [*DRM*](wmformat-glossary.md) especificado. |
| [**\_níveis mínimos de \_ proteção de saída \_ \_ do DRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_minimum_output_protection_levels) | Mantém os níveis de proteção de saída mínimos exigidos por uma licença DRM para reproduzir conteúdo em vários formatos.                                                                      |
| [**\_IDs de \_ saída \_ OPL DRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_opl_output_ids)                                      | Mantém uma matriz de identificadores de tecnologia DRM. Essa estrutura é usada para definir grupos de tecnologias em outras estruturas DRM.                                            |
| [**\_OPL de reprodução DRM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_play_opl)                                                   | Mantém as informações de nível de proteção de saída que se aplicam à ação de reprodução em uma licença DRM.                                                                               |
| [**\_ID do \_ conteúdo da playlist do DRM \_**](drm-playlist-content-id.md)                            | Contém informações sobre o conteúdo que deve ser copiado para o CD como parte de uma gravação de playlist.                                                                                 |
| [**\_VAL16 DRM**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-drm_val16)                                                          | Armazena um valor de 128 bits usado como um identificador de dispositivo.                                                                                                                       |
| [**\_proteção de \_ saída de vídeo DRM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_output_protection)                    | Mantém o identificador de uma tecnologia de proteção de vídeo e os dados de configuração exigidos por essa tecnologia.                                                             |
| [**\_IDs de \_ proteção de saída de vídeo DRM \_ \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_video_output_protection_ids)           | Mantém uma matriz de estruturas de **\_ proteção de \_ saída \_ de vídeo DRM** .                                                                                                          |
| [**WAVEFORMATEX**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85))                                                | Define o formato dos dados de Wave-Audio.                                                                                                                                |
| [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85))                                | Define o formato dos dados de áudio de forma de onda para formatos com mais de dois canais.                                                                                      |
| [**\_ACCESSENTRY de endereço do WM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_address_accessentry)                               | Especifica uma entrada em uma lista de acesso de endereço IP.                                                                                                                          |
| [**\_Propriedades do cliente do WM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_client_properties)                                   | Registra informações sobre o cliente.                                                                                                                                     |
| [**Propriedades do cliente do WM \_ \_ \_ ex**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_client_properties_ex)                            | Registra informações estendidas sobre o cliente.                                                                                                                            |
| [**\_dados de \_ licença de obtenção do WM \_**](wm-get-license-data.md)                                    | Contém informações sobre uma licença DRM.                                                                                                                                 |
| [**o \_ status individual do WM \_**](wm-individualize-status.md)                             | Registra o status do processo de [*individualização*](wmformat-glossary.md) .                                                                |
| [**\_ \_ par de buckets de vazamento do WM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_leaky_bucket_pair)                                  | Descreve os requisitos de buffer para um arquivo de taxa de bits variável (VBR).                                                                                                  |
| [**\_dados de \_ estado da licença do WM \_**](/previous-versions/windows/desktop/legacy/dd757942(v=vs.85))                                | Encapsula uma estrutura [**de \_ \_ \_ dados de estado de licença DRM**](drm-license-state-data.md) que descreve os dados de estado da licença DRM.                                              |
| [**\_tipo de mídia do WM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type)                                                 | Descreve um exemplo de mídia.                                                                                                                                                 |
| [**WMMPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmmpeg2videoinfo)                                             | Descreve um fluxo de vídeo MPEG-2.                                                                                                                                         |
| [**imagem do WM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture)                                                        | Contém os dados para o atributo de metadados de conteúdo complexo do [**WM/Picture**](wmpicture.md) .                                                                                     |
| [**\_intervalo de \_ número da porta do WM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_port_number_range)                                  | Descreve o intervalo de números de porta usados pela interface **IWMReaderNetworkConfig** .                                                                                     |
| [**CLIENTINFO do WM \_ Reader \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_clientinfo)                                   | Descreve o leitor de cliente (Player) que acessa o fluxo de mídia.                                                                                                          |
| [**estatísticas do WM \_ Reader \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_statistics)                                   | Descreve o desempenho de uma operação de leitura.                                                                                                                         |
| [**WMSCRIPTFORMAT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmscriptformat)                                                 | Define o formato de um fluxo de script.                                                                                                                                    |
| [**\_registro de \_ prioridade de fluxo do WM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_priority_record)                        | Contém um número de fluxo e especifica se a entrega desse fluxo é obrigatória.                                                                                      |
| [**\_informações de \_ tipo de fluxo do WM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_type_info)                                    | Contém os dados para o atributo de metadados complexos do [**WM/StreamTypeInfo**](wm-streamtypeinfo.md) .                                                                      |
| [**\_letras de músicas sincronizadas do WM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_synchronised_lyrics)                               | Contém os dados para o atributo de metadados complexos [**\_ sincronizados do WM/música**](wm-lyrics-synchronised.md) .                                                           |
| [**\_texto de usuário do WM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_user_text)                                                   | Contém os dados para o atributo de metadados do [**WM/Text**](wm-text.md) Complex.                                                                                          |
| [**\_ \_ URL da Web do usuário do WM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_user_web_url)                                            | Contém os dados para o atributo de metadados complexos do [**WM/UserWebURL**](wm-userweburl.md) .                                                                              |
| [**\_estatísticas do gravador do WM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics)                                   | Descreve o desempenho de uma operação de gravação.                                                                                                                         |
| [**estatísticas do gravador do WM \_ \_ \_ ex**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics_ex)                            | Contém estatísticas estendidas do gravador.                                                                                                                                      |
| [**\_chave de \_ conteúdo de importação do WMDRM \_**](wmdrm-import-content-key.md)                          | Mantém a chave de conteúdo usada na importação de conteúdo protegido.                                                                                                                |
| [**estrutura de inicialização do WMDRM \_ Import \_ \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct)                          | Mantém a chave de sessão criptografada e a chave de conteúdo usada na importação de conteúdo protegido.                                                                                      |
| [**\_chave de \_ sessão de importação do WMDRM \_**](wmdrm-import-session-key.md)                          | Mantém a chave de sessão para importar conteúdo protegido.                                                                                                                    |
| [**\_segmento de buffer WMT \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_buffer_segment)                                       | Contém as informações necessárias para especificar um segmento em um pacote.                                                                                                      |
| [**\_dados de \_ extensão WMT COLORSPACEINFO \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_colorspaceinfo_extension_data)        | Contém os dados para a extensão de unidade de dados do WM \_ SampleExtensionGUID \_ ColorSpaceInfo.                                                                                    |
| [**unidade de dados do WMT \_ FILEsink \_ \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_filesink_data_unit)                              | Contém informações sobre um pacote.                                                                                                                                      |
| [**\_fragmento de carga de WMT \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_payload_fragment)                                   | Contém as informações necessárias para extrair um fragmento de carga de um pacote.                                                                                           |
| [**\_dados de \_ extensão do código de WMT \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data)                    | Contém um único código de tempo SMPTE e informações relacionadas.                                                                                                                |
| [**\_exemplo de VIDEOIMAGE de WMT \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample)                                 | Contém informações sobre um exemplo de imagem de vídeo.                                                                                                                          |
| [**\_entrada de marca d' água WMT \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_watermark_entry)                                     | Contém informações sobre um sistema de marca d' água.                                                                                                                         |
| [**\_formato WEBstream do WMT \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_format)                                   | Contém informações sobre um fluxo da Web.                                                                                                                                  |
| [**\_cabeçalho de exemplo do WEBstream do WMT \_ \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_sample_header)                    | Contém informações de cabeçalho para exemplos de fluxo da Web.                                                                                                                       |
| [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader)                                           | Descreve as informações de bitmap e cor de uma imagem de vídeo.                                                                                                             |
| [**WMVIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader2)                                         | Descreve as informações de bitmap e cor de uma imagem de vídeo, incluindo [*entrelaçamento*](wmformat-glossary.md), proteção de cópia e taxa de proporção.       |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de programação**](programming-reference.md)
</dt> </dl>

 

 
