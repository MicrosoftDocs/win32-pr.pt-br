---
title: Windows Tipos de enumeração do SDK de formato de mídia
description: Saiba mais sobre os tipos de enumeração que o SDK Windows Media Format implementa, como DRM_HTTP_STATUS e DRM_LICENSE_STATE_CATEGORY.
ms.assetid: cd28f608-25ba-44a7-868b-b1cd4dfcfa45
keywords:
- Windows SDK de Formato de Mídia, tipos de enumeração
- ASF (Advanced Systems Format), tipos de enumeração
- ASF (Formato de Sistemas Avançados), tipos de enumeração
- tipos de enumeração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16b3a53688e21e58b0d9509cc901a72399f26b9d758cac89511e66a76d740db1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117848155"
---
# <a name="windows-media-format-sdk-enumeration-types"></a>Windows Tipos de enumeração do SDK de formato de mídia

O Windows SDK de Formato de Mídia implementa os seguintes tipos de enumeração.



| Tipo de enumeração                                                               | Descrição                                                                                                                      |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**STATUS \_ HTTP DO DRM \_**](drm-http-status.md)                                   | Define um intervalo de estados para uma solicitação DRM.                                                                                     |
| [**CATEGORIA DE ESTADO \_ DA \_ LICENÇA DRM \_**](drm-license-state-category.md)            | Define as categorias para cadeias de caracteres de licença DRM.                                                                                  |
| [**STATUS DE INDIVIDUALIZAÇÃO DO DRM \_ \_**](drm-individualization-status.md)         | Define os estados válidos para individualização de DRM.                                                                              |
| [**CONFIGURAÇÕES \_ DE URL DO NETSOURCECREDPOLICY \_**](/previous-versions/windows/desktop/api/wmsinternaladminnetsource/ne-wmsinternaladminnetsource-netsource_urlcredpolicy_settings) | Define as possíveis configurações de política de segurança que podem existir em um computador cliente.                                                   |
| [**WM \_ AETYPE**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wm_aetype)                                                | Especifica as permissões para uma entrada em uma lista de acesso de endereço IP.                                                             |
| [**WMT \_ ATTR \_ DATATYPE**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_attr_datatype)                               | Define uma variedade de tipos de dados básicos. Esses valores são usados para identificar o tipo de dados retornado por vários métodos neste SDK. |
| [**WMT \_ ATTR \_ IMAGETYPE**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_attr_imagetype)                             | Define um intervalo de tipos de imagem que podem ser armazenados em um header de arquivo ASF.                                                         |
| [**TIPO DE \_ INFORMAÇÕES DO WMT CODEC \_ \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_codec_info_type)                          | Define um intervalo de tamanhos de dados usados por um codec.                                                                                   |
| [**SINALIZADORES \_ DE CREDENCIAL \_ WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_credential_flags)                         | Define os sinalizadores que podem ser usados ao adquirir credenciais.                                                                   |
| [**WMT \_ DRMLA \_ TRUST**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_drmla_trust)                                   | Define o estado de confiança de uma URL de aquisição de licença DRM.                                                                        |
| [**MODO WMT \_ FILESINK \_**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_filesink_mode)                               | Define os tipos de entrada aceitos pelo sink de arquivo.                                                                            |
| [**TIPO DE IMAGEM WMT \_ \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_image_type)                                     | Define os tipos de imagem possíveis usados para anúncios de faixa.                                                                            |
| [**TIPO DE ÍNDICE WMT \_ \_**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_index_type)                                     | Define o objeto ao qual um índice baseado em tempo pode ser associado.                                                              |
| [**TIPO DE \_ INDEXADOR \_ WMT**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_indexer_type)                                 | Define os tipos de indexação com suporte pelo indexador.                                                                          |
| [**PROTOCOLO WMT \_ NET \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_net_protocol)                                 | Define os tipos de protocolos aos quais o sink de rede dá suporte.                                                                   |
| [**MODO DE CLASSE WMT \_ MUSICSPEECH \_ \_**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_musicspeech_class_mode)            | Define os modos de compactação disponíveis para o codec Windows Media Audio 9 Voice.                                                |
| [**FORMATO DE \_ DESLOCAMENTO WMT \_**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_offset_format)                               | Define os tipos de deslocamentos usados neste SDK.                                                                                   |
| [**MODO DE REPRODUÇÃO DO WMT \_ \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_play_mode)                                       | Define as opções de reprodução do leitor.                                                                                      |
| [**CONFIGURAÇÕES \_ DE PROXY \_ WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_proxy_settings)                             | Define as configurações de proxy de rede para uso com um objeto de leitor.                                                                 |
| [**DIREITOS DO \_ WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_rights)                                              | Define os direitos que podem ser especificados em uma licença drm.                                                                       |
| [**STATUS DO WMT \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status)                                              | Define um intervalo de sinalizadores de status.                                                                                                 |
| [**FORMATO DE \_ ARMAZENAMENTO WMT \_**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_storage_format)                             | Define os tipos de arquivo que podem ser manipulados com esse SDK.                                                                    |
| [**SELEÇÃO DE \_ FLUXO WMT \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_stream_selection)                         | Define o status de um fluxo.                                                                                                  |
| [**TIPO DE \_ TRANSPORTE WMT \_**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_transport_type)                             | Define os tipos de transporte com suporte neste SDK.                                                                               |
| [**VERSÃO \_ DO WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_version)                                            | Define os números de versão do SDK Windows Formato de Mídia.                                                                     |
| [**TIPO DE \_ ENTRADA DE MARCA \_ D'ÁGUA WMT \_**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_watermark_entry_type)                | Define os tipos de marcas-d'água com suporte.                                                                                       |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de programação**](programming-reference.md)
</dt> </dl>

 

 




