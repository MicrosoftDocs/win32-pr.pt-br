---
description: Atributos de transformação
ms.assetid: 9beb1306-1378-499c-b9e1-c768a7b4c8bc
title: Atributos de transformação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e68240f5341319db2b06ad6160cf8153f107eca9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461214"
---
# <a name="transform-attributes"></a>Atributos de transformação

Os atributos a seguir se aplicam a [transformações de Media Foundation](media-foundation-transforms.md) (MFTs) ou a [objetos de ativação](activation-objects.md) para MFTs, ou ambos.



| Atributo                                                                                                     | Descrição                                                                                                                                                                                   | Aplica-se A                  |
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [**MF \_ Ativar \_ MFT \_ bloqueado**](mf-activate-mft-locked-attribute.md)                                         | Especifica se o carregador de topologia irá alterar os tipos de mídia em um MFT.                                                                                                                  | MFTs                        |
| [**\_Reconhecimento de \_ D3D \_ SA do MF**](mf-sa-d3d-aware-attribute.md)                                                       | Especifica se uma Media Foundation transformação (MFT) dá suporte à aceleração de vídeo do DirectX.                                                                                                     | MFTs                        |
| [transformação do MF em \_ \_ Async](mf-transform-async.md)                                                                | Especifica se um MFT executa o processamento assíncrono.                                                                                                                                    | MFTs                        |
| [\_desbloqueio assíncrono de transformação MF \_ \_](mf-transform-async-unlock.md)                                                 | Habilita o uso de uma MFT assíncrona.                                                                                                                                                       | MFTs                        |
| [\_Atributo de \_ categoria de transformação MF \_](mf-transform-category-attribute.md)                                     | Especifica a categoria de um MFT.                                                                                                                                                            | Objetos de ativação de MFT      |
| [\_Atributo de \_ sinalizadores de transformação MF \_](mf-transform-flags-attribute.md)                                           | Contém sinalizadores para um objeto de ativação de MFT.                                                                                                                                                  | Objetos de ativação de MFT      |
| [\_Atributo de \_ mérito de codec de MFT \_](mft-codec-merit-attribute.md)                                                 | Contém o valor de mérito de um codec de hardware.                                                                                                                                                 | Objetos de ativação de MFT      |
| [\_atributo de \_ fluxo \_ conectado ao MFT](mft-connected-stream-attribute.md)                                       | Contém um ponteiro para os atributos de fluxo do fluxo conectado em um MFT baseado em hardware.                                                                                                  | MFTs                        |
| [MFT \_ conectado \_ ao \_ fluxo de HW \_](mft-connected-to-hw-stream.md)                                              | Especifica se um MFT baseado em hardware está conectado a outro MFT baseado em hardware.                                                                                                            | MFTs                        |
| [o \_ decodificador MFT \_ expõe os \_ \_ tipos \_ de saída na \_ \_ ordem nativa](mft-decoder-expose-output-types-in-native-order.md) | Especifica se um decodificador expõe os tipos de saída IYUV/I420 (adequados para transcodificação) antes de outros formatos.                                                                                   | MFTs                        |
| [\_dica de \_ \_ resolução de vídeo final do \_ decodificador MFT \_](mft-decoder-final-video-resolution-hint.md)                   | Especifica a resolução final de saída da imagem decodificada, após o processamento do vídeo.                                                                                                           | MFTs                        |
| [o \_ codificador MFT \_ dá suporte ao \_ \_ evento config](mft-encoder-supports-config-event.md)                                | Especifica que o codificador MFT dá suporte ao recebimento de eventos [MEEncodingParameter](meencodingparameters.md) durante o streaming.                                                                     | MFTs                        |
| [\_LUID de \_ adaptador de enumeração de MFT \_](mft-enum-adapter-luid.md)                                                         | Especifica um identificador exclusivo para um adaptador de vídeo. Use esse atributo ao chamar MFTEnum2 para enumerar MFTs associados a um adaptador específico.                                             | MFTs                        |
| [\_Atributo de \_ URL de hardware de enumeração de MFT \_ \_](mft-enum-hardware-url-attribute.md)                                    | Contém o link simbólico para um MFT baseado em hardware.                                                                                                                                          | Objetos de ativação MFTs/MFT |
| [\_Atributo de \_ ID de fornecedor de hardware de enumeração de \_ \_ MFT \_](mft-enum-hardware-vendor-id-attribute.md)                       | Especifica a ID do fornecedor para uma transformação de Media Foundation baseada em hardware                                                                                                                       | MFTs                        |
| [\_ \_ atributo somente de transcodificação de \_ MFT \_](mft-enum-transcode-only-attribute.md)                                | Especifica se um decodificador é otimizado para transcodificação em vez de para reprodução.                                                                                                            | MFTs                        |
| [\_Atributo de \_ desbloqueio de FIELDOFUSE MFT \_](mft-fieldofuse-unlock-attribute.md)                                     | Contém um ponteiro [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) , que pode ser usado para desbloquear o MFT.                                                                            | Objetos de ativação de MFT      |
| [\_Atributo de \_ nome \_ amigável de MFT](mft-friendly-name-attribute.md)                                             | Contém o nome de exibição para um MFT baseado em hardware.                                                                                                                                           | Objetos de ativação de MFT      |
| [\_Atributos de \_ tipos de entrada de MFT \_](mft-input-types-attributes.md)                                               | Contém os tipos de entrada registrados para um MFT.                                                                                                                                               | Objetos de ativação de MFT      |
| [\_Atributos de \_ tipos de saída de MFT \_](mft-output-types-attributes.md)                                             | Contém os tipos de saída registrados para um MFT.                                                                                                                                              | Objetos de ativação de MFT      |
| [\_perfil de \_ codificador de MFT preferencial \_](mft-preferred-encoder-profile.md)                                         | Contém propriedades de configuração para um codificador.                                                                                                                                             | Objetos de ativação de MFT      |
| [\_ \_ Atributo OutputType preferencial de \_ MFT](mft-preferred-outputtype-attribute.md)                               | Especifica o formato de saída preferencial para um codificador.                                                                                                                                         | Objetos de ativação de MFT      |
| [\_ \_ Atributo OutputType preferencial de \_ MFT](mft-preferred-outputtype-attribute.md)                               | Especifica o formato de saída preferencial para um codificador.                                                                                                                                         | Objetos de ativação de MFT      |
| [\_ \_ Atributo local do processo de MFT \_](mft-process-local-attribute.md)                                             | Especifica se um MFT é registrado apenas no processo do aplicativo.                                                                                                                     | Objetos de ativação de MFT      |
| [\_remux \_ de MFT \_ marca \_ I \_ imagem \_ como \_ ponto de limpeza](mft-remux-mark-i-picture-as-clean-point.md)                 | Especifica se o MFT do remux de vídeo H. 264 deve marcar I imagens como ponto de limpeza para melhor capacidade de busca. Isso tem o potencial de danos em buscas em arquivos MP4 finais em não conformidade. | Objetos de ativação de MFT      |
| [\_3DVIDEO de suporte de MFT \_](mft-support-3dvideo.md)                                                              | Especifica se uma Media Foundation transformação (MFT) dá suporte ao vídeo 3D estereoscópico.                                                                                                          | Objetos de ativação de MFT      |
| [**o MFT \_ dá suporte à \_ alteração de \_ formato dinâmico \_**](mft-support-dynamic-format-change-attribute.md)                  | Especifica se uma Media Foundation de transformação (MFT) dá suporte a alterações de formato dinâmico.                                                                                                         | MFTs                        |
| [\_ \_ Atributo CLSID de transformação de MFT \_](mft-transform-clsid-attribute.md)                                         | Contém o identificador de classe (CLSID) de um MFT.                                                                                                                                              | Objetos de ativação de MFT      |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
</dt> <dt>

[Atributos de Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[Transformações de Media Foundation](media-foundation-transforms.md)
</dt> </dl>

 

 



